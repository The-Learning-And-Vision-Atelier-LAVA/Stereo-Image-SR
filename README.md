# NTIRE 2022: Stereo Image Super-Resolution Challenge <br>

Stereo image super-resolution (SR) challenge is held as a part of the [NTIRE workshop]() in conjunction with CVPR 2022. The goal of this challenge is to develop methods to accurately recover high-resolution (HR) stereo image pairs. <br>


## Introduction
Stereo image pairs can encode 3D scene cues into stereo correspondences between the left and right images. With the popularity of dual cameras in mobile phones, autonomous vehicles and robots, stereo vision has attracted increasingly attention in both academia and industry. In many applications like AR/VR and robot navigation, increasing the resolution of stereo images is highly demanded to achieve higher perceptual quality and help to parse the real world.

In recent years, remarkable progress of image super-resolution (SR) have been witnessed with deep learning techniques. However, most approaches focus on super-resolving single images and cannot be directly extended to the task of stereo image SR. For stereo images, how to effectively incorporate additional information from a second viewpoint at varying disparities remains challenging. 

In this challenge, we aim at establishing a benchmark for stereo image SR, and aspire to highlight the specific challenges and research problems faced by stereo image SR. This challenge provides an opportunity for researchers to work together to share their knowledge and insights, advance the algorithm performance, and promote the development of stereo image SR.

## Description of the Challenge
The objective of this challenge is to reconstruct high-resolution (HR) stereo images from their low-resolution (LR) counterparts. 

During the model development phase, the training set and the validation set will be released. Both HR stereo images and their LR counterparts in the training and validation sets are available. The participants can train their models on the training set and can evaluate their models with the validation set. 

During the test phase, the test set will be released, which includes LR images only. Challenge participants should apply their trained models to the LR test images to generate super-resolved test images.  These  super-resolved images will then be submitted by the participants and evaluated by the organizers with a set of objective quantitative metrics.

## Datasets
### Training Set:
The 800 stereo images in training set of the [Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/) are used as the training set of this challenge. Both HR  images and their LR versions (produced by bicubic downsampling) will be released. The participants can use these HR images as groundtruths to train their models. 
### Validation Set:
The 112 stereo images in the validation set of the [Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/) are used as the validation set of this challenge. Similar to the training set, both HR and LR images in the validation set are provided. The participants can download the validation set to evaluate the performance of their developed models by comparing their super-resolved images with the HR groundtruth images. **Note that, the validation set should be used for validation purpose only but cannot be used as additional training data.** The participants are encouraged to write papers to describe their methods and use the released validation set for performance evaluation.
### Test Set:
To rank the submitted models, a test set consisting of 100 stereo images will be provided. Different from the training and validation sets, only LR images will be released. The participants are required to apply their models to the released LR stereo images and submit their super-resolved images to the server. It should be noted that the images in the test set (even the LR versions) cannot be used for training.

## Evaluation Metrics
Peak signal-to-noise ratio (PSNR) and structural similarity (SSIM) will be used as metrics for performance evaluation.  Besides, we will use the warping error to measure the stereo consistency between the SR results. The warping error is defined as the mean square error between SR left and warped SR right images. **Note that, only PSNR is used for ranking.** PSNR and SSIM implementations can be found in most of the image processing toolboxes, for example, `scikit-image` and `tensorflow.image`. We report the average results of left and right views over all of the test scenes. Boundary cropping is not performed. 
To calculate warping error, we adopt a state-of-the-art stereo matching method to estimate dense disparities between HR images.

```
import imageio
from skimage.metrics import peak_signal_noise_ratio, structural_similarity
ref_img = imageio.imread('ref_img_name.png')
res_img = imageio.imread('res_img_name.png')
psnr = peak_signal_noise_ratio(ref_img, res_img)
ssim = structural_similarity(ref_img, res_img, multichannel=True, %gaussian_weights=True, use_sample_covariance=False)
```

## Baseline Model
Over the last few years, several milestone methods have been developed for stereo image SR, including [StereoSR](), [PASSRnet](https://github.com/The-Learning-And-Vision-Atelier-LAVA/PASSRnet), SPAMnet, DASSR, [iPASSR](https://github.com/YingqianWang/iPASSR) (see [YingqianWang/Stereo-Image-SR](https://github.com/YingqianWang/Stereo-Image-SR) for details). In this challenge, PASSRnet is used as a baseline model and the submitted results should be at least on par with PASSRnet. The solutions with PSNR values lower than PASSRnet will not be ranked in the leaderboard.

## Important Dates
* TBD: Release of training data, validation data, and test data;
* TBD: Validation server online;
* TBD: Testing server online;
* TBD: Test result submission deadline;
* TBD: Fact sheet / code / model submission deadline;
* TBD: Test preliminary score release to the participants;
* TBD: Challenge paper submission;
* TBD: Camera-ready;
* TBD: Workshop day;

## Issues and Questions:
The Stereo Image SR Challenge Forum: Please scan the code to join our WeChat group or raise issues to this repo:

## Organizers:
* [**Yulan Guo**](http://yulanguo.me/) ([yulan.guo@nudt.edu.cn](yulan.guo@nudt.edu.cn))
* [**Longguang Wang**](https://longguangwang.github.io/) ([wanglongguang15@nudt.edu.cn](wanglongguang15@nudt.edu.cn))
* [**Yingqian Wang**](https://yingqianwang.github.io/) ([wangyingqian16@nudt.edu.cn](wangyingqian16@nudt.edu.cn))
* [**Juncheng Li**](https://junchenglee.com/) ([junchengli@math.cuhk.edu.hk](junchengli@math.cuhk.edu.hk))
* [**Shuhang Gu**](https://sites.google.com/site/shuhanggu/) ([shuhanggu@gmail.com](shuhanggu@gmail.com))
* [**Radu Timofte**](https://people.ee.ethz.ch/~timofter/) ([Radu.Timofte@vision.ee.ethz.ch](Radu.Timofte@vision.ee.ethz.ch))

## Acknowledgement:
We would like to thank **<a href="https://www.flickr.com/photos/stereotron/" target="_blank">Sascha Becher</a>**
 and **<a href="https://www.flickr.com/photos/tombentz" target="_blank">Tom Bentz</a>** for the approval of using their cross-eye stereo photographs. <br>

## NTIRE 2022 Terms and Conditions:
The terms and conditions for participating in the challenge are provided [here]().

