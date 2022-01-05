# NTIRE 2022 Stereo Image Super-Resolution Challenge

## Challenge Overview
Stereo image pairs can encode 3D scene cues into stereo correspondences between the left and right images. 
With the popularity of dual cameras in mobile phones, autonomous vehicles and robots, stereo vision has attracted increasingly attention in both academia and industry. 
In many applications like AR/VR,  and robot navigation, increasing the resolution of stereo images is highly demanded to achieve higher perceptual quality and help to parse the real world.

In recent years, remarkable progress of image super-resolution (SR) have been witnessed with deep learning techniques. However, most approaches focus on super-resolving single images and cannot be directly extended to the task of stereo image SR. For stereo images, how to effectively incorporate additional information from a second viewpoint at varying disparities remains challenging. 

In this challenge, we aim at establishing a benchmark for stereo image SR. 
We aspire to highlight the specific challenges and research problems faced by stereo image SR. 
We hope that this challenge could inspire the community to explore the cross area of low-level vision and 3D vision, and ultimately drive technological advancement in emerging applications such as AR/VR and autonomous vehicles.

## Description of the Challenge
The objective of this challenge is to reconstruct high-resolution (HR) stereo images from their low-resolution (LR) counterparts. 

During the model development phase, the training set and the validation set will be released. Both HR stereo images and their LR counterparts in the training and validation sets are available. The participants can train their models on the training set and can evaluate their models with the validation set. 

During the test phase, the test set will be released, which includes LR images only. Challenge participants should apply their trained models to the LR test images to generate super-resolved test images.  These  super-resolved images will then be submitted by the participants and evaluated by the organizers with a set of objective quantitative metrics.

## Datasets
1. **Training Set:** The training set of the Flickr1024 dataset \cite{Wang2019Flickr1024} (with 800 images) is used as the training set of this challenge.} Both original HR images and their LR versions (which are produced by bicubic downsampling) will be released. The participants can use these HR images as groundtruths to train their models. 
2. **Validation Set:** The validation set of the Flickr1024 dataset (with 112 images) is used as the validation set of this challenge. Similar to the training set, both HR and LR images in the validation set are provided. The participants can download the validation set to evaluate the performance of their developed models by comparing their super-resolved images with the HR groundtruth images. Note that, the validation set should be used for validation purpose only but cannot be used as additional training data. The participants are encouraged to write papers to describe their methods and use the released validation set for performance evaluation.
3. **Test Set:** To rank the submitted models, a test set consisting of 100 stereo images are provided. Different from the training and validation sets, only LR images will be released for the test set. The participants are required to apply their models to the released LR stereo images and submit their super-resolved images to the server. It should be noted that the images in the test set (even the LR versions) cannot be used for training. %For example, the zero-shot SR scheme is forbidden in this challenge.

## Evaluation Metrics
Peak signal-to-noise ratio (PSNR) and structural similarity (SSIM) will be used as metrics for performance evaluation.  Following \cite{Song2020Stereoscopic}, we will use the warping error to measure the stereo consistency between the SR results. The warping error is defined as the mean square error between SR left and warped SR right images. **Note that, only PSNR is used for ranking.** PSNR and SSIM implementations can be found in most of the image processing toolboxes, for example, `scikit-image` and `tensorflow.image`. We report the average results of left and right views over all of the test scenes. Boundary cropping is not performed. 
To calculate warping error, we adopt a state-of-the-art stereo matching method \cite{Zhang2020Domain} to estimate dense disparities between HR images.

```
import imageio
from skimage.metrics import peak_signal_noise_ratio, structural_similarity
ref_img = imageio.imread('ref_img_name.png')
res_img = imageio.imread('res_img_name.png')
psnr = peak_signal_noise_ratio(ref_img, res_img)
ssim = structural_similarity(ref_img, res_img, multichannel=True, %gaussian_weights=True, use_sample_covariance=False)
```

## Baseline Model
Over the last few years, several milestone methods have been developed for stereo image SR, including PASSRnet, SPAMnet, DASSR, iPASSR. In this challenge, PASSRnet is used as a baseline model and the submitted results should be at least on par with PASSRnet. The solutions with PSNR values lower than PASSRnet will not be ranked in the leaderboard.













