# NTIRE 2024: Stereo Image Super-Resolution Challenge <br> 
<p align="center">  <img src="https://raw.github.com/YingqianWang/Stereo-Image-SR/NTIRE2024/Fig/logo.png" width="50%"> </p>

**Stereo image super-resolution (SR) challenge is held as a part of the [NTIRE workshop](https://cvlai.net/ntire/2024/) in conjunction with CVPR 2024. The goal of this challenge is to develop methods to recover high-resolution (HR) stereo image pairs.** <br>

## News and Updates:
* **2024-01-29**: CodaLab servers for [Track1](https://codalab.lisn.upsaclay.fr/competitions/17245) and [Track2](https://codalab.lisn.upsaclay.fr/competitions/17246) are online. Training and validation data has been released.

## Introduction
Stereo image pairs can encode 3D scene cues into stereo correspondences between the left and right images. 
With the popularity of dual cameras in mobile phones, autonomous vehicles and robots, stereo vision has attracted increasing attention in both academia and industry. 
In many applications like AR/VR and robot navigation, increasing the resolution of stereo images is highly demanded to achieve higher perceptual quality and help to parse the real world.

In recent years, remarkable progress in image super-resolution (SR) has been witnessed with deep learning techniques. However, most approaches focus on super-resolving single images and cannot be directly extended to the task of stereo image SR. For stereo images, effectively incorporating additional information from a second viewpoint at varying disparities remains challenging. 

In this challenge, we aim at establishing a benchmark for stereo image SR. We aspire to highlight the specific challenges and research problems faced by stereo image SR. 
We hope that this challenge could inspire the community to explore the cross area of low-level vision and 3D vision, and ultimately drive technological advancement in emerging applications such as AR/VR and autonomous vehicles.

## Description of the Challenge
The objective of this challenge is to reconstruct high-resolution (HR) stereo images from their low-resolution (LR) counterparts. 

During the model development phase, the training set and the validation set will be released. Both HR stereo images and their LR counterparts in the training and validation sets are available. The participants can train their models on the training set and evaluate them with the validation set. 

During the test phase, the test set will be released, which includes LR images only. Challenge participants should apply their trained models to the LR test images to generate super-resolved test images. These super-resolved images will then be submitted by the participants and evaluated by the organizers with a set of objective quantitative metrics.

## Datasets
### Training Set: *[[JianguoYun](https://www.jianguoyun.com/p/Da4VFtMQstPqChjpkrsFIAA)][[Google Drive](https://drive.google.com/drive/folders/136h3xlftEIc2NzKmDaw-8DlRoiO1ioOO)]*
The 800 stereo images in training set of the [Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/) are used as the training set of this challenge. Both HR images and their LR versions (produced by bicubic downsampling) will be released. The participants can use these HR images as groundtruths to train their models. **Note that, external dataset (e.g., the Middlebury or KITTI datasets, validation/test sets of the Flickr1024 dataset) is NOT allowed in this challenge. Besides, models pretrained on other datasets (e.g., RCAN/SwinIR developed on DIV2K datasets) are NOT allowed in this challenge.**

### Validation Set: *[[JianguoYun](https://www.jianguoyun.com/p/Da4VFtMQstPqChjpkrsFIAA)][[Google Drive](https://drive.google.com/drive/folders/136h3xlftEIc2NzKmDaw-8DlRoiO1ioOO)]*
The 112 stereo images in the validation set of the [Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/) are used as the validation set of this challenge. Similar to the training set, both HR and LR images in the validation set are provided. The participants can download the validation set to evaluate the performance of their developed models by comparing their super-resolved images with the HR groundtruth images. **Note that, the validation set should be used for validation purpose only but cannot be used as additional training data.** The participants are encouraged to write papers to describe their methods and use the released validation set for performance evaluation.

### Test Set:
To rank the submitted models, a test set consisting of 100 stereo images are provided. Different from the training and validation sets, only LR images will be released. The participants are required to apply their models to the released LR stereo images and submit their super-resolved images to the server. It should be noted that the images in the test set (even the LR versions) cannot be used for training.

## Tracks (NEW!)
### Track 1: [Constrained SR & Bicubic Degradation](https://codalab.lisn.upsaclay.fr/competitions/17245)
#### Degradation Model:
In this track, bicubic degradation is used to generate LR images: 
$$I^{LR}=I^{HR}\downarrow_s,$$
where $I^{LR}$ and $I^{HR}$ are LR and HR images, $\downarrow_s$ represents bicubic downsampling with scale factor $s$. 

#### Evaluation Metrics:
Peak signal-to-noise ratio (PSNR) and structural similarity (SSIM) are used as metrics for performance evaluation. The average results of left and right views over all of the test scenes are reported. Note that, only PSNR is used for ranking. 

### Track 2: [Constrained SR & Realistic Degradation](https://codalab.lisn.upsaclay.fr/competitions/17246)
#### Degradation Model:
In this track, a realistic degradation model consisting of blur, downsampling, noise, and compression is adopted to synthesize LR images:

$$I^{LR}=\mathcal{C}\left(\left(I^{HR}\otimes{k}\right)\downarrow_s+n\right),$$

where $k$ is the blur kernel, $n$ is additive Gaussian noise, and $\mathcal{C}$ represents JPEG compression. 

#### Evaluation Metrics:
PSNR and SSIM are used as metrics for performance evaluation. The average results of left and right views over all of the test scenes are reported. Note that, only PSNR is used for ranking. 


## Submission
We use [CodaLab](https://codalab.lisn.upsaclay.fr/competitions/17245) for online submission in the development phase. **Here, we provide an example ([Jianguoyun Drive](https://www.jianguoyun.com/p/DXWimH4QwOebChipxasE) or [Google Drive](https://drive.google.com/file/d/1gyaan54AwbAYLIIA1rly_wrLzdyQ7VAh/view?usp=sharing) to help participants to format their submissions.** In the test phase, the final results and the source codes (both training and test) need to be submitted via emails (ntire.stereosr@outlook.com). Please refer to our [online website](https://codalab.lisn.upsaclay.fr/competitions/17245) for details of the submission rules.

## Important Dates
* 2024-01-14: Release of training data, validation data, and test data;
* 2024-01-30: Validation server online;
* 2024-03-15: Testing server online;
* 2024-03-21: Test result submission deadline;
* 2024-03-22: Fact sheet / code / model submission deadline;
* 2024-03-24: Test preliminary score release to the participants;
* 2024-04-05: Challenge paper submission;
* 2024-04-13: Camera-ready;
* 2024-06-18 (TBU): Workshop day
<br><br>

## Group number policy
Each group cannot have more than six group members (i.e., 1 to 6 group members is OK), and each paricipant can only join one group. Each group can only submit one algorithm for final ranking.


## Issues and Questions:
For any question regarding this challenge, raise an issue under this repository. <br>
You can also join our WeChat group by scanning the code below:

<p align="center"> <img src="https://raw.github.com/The-Learning-And-Vision-Atelier-LAVA/Stereo-Image-SR/NTIRE2024/Fig/WeChat.jpg" width="40%"> </p>

## Organizers:
* [**Longguang Wang**](https://longguangwang.github.io/) ([wanglongguang15@nudt.edu.cn](wanglongguang15@nudt.edu.cn))
* [**Yulan Guo**](http://yulanguo.me/) ([yulan.guo@nudt.edu.cn](yulan.guo@nudt.edu.cn))
* [**Yingqian Wang**](https://yingqianwang.github.io/) ([wangyingqian16@nudt.edu.cn](wangyingqian16@nudt.edu.cn))
* [**Juncheng Li**](https://junchenglee.com/) ([junchengli@math.cuhk.edu.hk](junchengli@math.cuhk.edu.hk))
* [**Zhi Jin**](https://scholar.google.com/citations?user=v70dNBoAAAAJ&hl=zh-CN&oi=ao) ([jinzh26@mail.sysu.edu.cn](jinzh26@mail.sysu.edu.cn))
* [**Shuhang Gu**](https://shuhanggu.github.io/) ([shuhanggu@gmail.com](shuhanggu@gmail.com))
* [**Radu Timofte**](https://people.ee.ethz.ch/~timofter/) ([Radu.Timofte@vision.ee.ethz.ch](Radu.Timofte@vision.ee.ethz.ch))

## Acknowledgement:
We would like to thank **<a href="https://www.flickr.com/photos/stereotron/" target="_blank">Sascha Becher</a>**
 and **<a href="https://www.flickr.com/photos/tombentz" target="_blank">Tom Bentz</a>** for the approval of using their cross-eye stereo photographs. <br>

## NTIRE 2024 Terms and Conditions:
The terms and conditions of this challenge can be viewed [here](https://codalab.lisn.upsaclay.fr/competitions/17245#learn_the_details-terms_and_conditions).

