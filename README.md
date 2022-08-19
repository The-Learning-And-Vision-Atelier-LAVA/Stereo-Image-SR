# NTIRE 2022: Stereo Image Super-Resolution Challenge <br> 
<p align="center">  <img src="https://raw.github.com/YingqianWang/Stereo-Image-SR/NTIRE2022/Fig/logo.png" width="50%"> </p>

**Stereo image super-resolution (SR) challenge is held as a part of the [NTIRE workshop](https://data.vision.ee.ethz.ch/cvl/ntire22/) in conjunction with CVPR 2022. The goal of this challenge is to develop methods to accurately recover high-resolution (HR) stereo image pairs.** <br>

## News and Updates:
* **2021-03-24**: Test data ([Jianguoyun](https://www.jianguoyun.com/p/DWQY4hYQwOebChjh37QE) or [Google Drive](https://drive.google.com/file/d/1moEgPa0S9kaV9WHaY_cmFkQZ6YwwhXk0/view?usp=sharing)) has been released. Paticipants can apply their developed models to the released test data, and submit their SR results to the [test server](https://codalab.lisn.upsaclay.fr/competitions/1598#learn_the_details). 
* **2021-03-04**: The timeline of the challenge has been extended.
* **2021-02-07**: Update readme and address the policy of external data usage of this challenge. **That is, external dataset (e.g., the Middlebury or KITTI datasets, validation/test sets of the Flickr1024 dataset) is NOT allowed in this challenge. Besides, models pretrained on other datasets (e.g., RCAN/SwinIR developed on DIV2K datasets) are NOT allowed in this challenge.**
* **2021-01-28**: Validation server is online. Participants can sign up for the challenge and submit their results [here](https://codalab.lisn.upsaclay.fr/competitions/1598).
* **2021-01-21**: Training ([Jianguoyun Drive](https://www.jianguoyun.com/p/DR03yFcQwOebChjC1KoE) or [Google Drive](https://drive.google.com/file/d/1CjfnSpdpmLssYvHU2EgQoRqKbnzYItcC/view?usp=sharing))  and validation ([Jianguoyun Drive](https://www.jianguoyun.com/p/DeGlXW0QwOebChjE1KoE) or [Google Drive](https://drive.google.com/file/d/1D-el9JGt0RVYCl8nZ4_LSg6fyVfgcKHV/view?usp=sharing)） data has been released. Paticipants can use the released data to develop their algorithms (only 4xSR is considered in this challenge). We are still waiting for further notes from the NTIRE organizers.


## Introduction
Stereo image pairs can encode 3D scene cues into stereo correspondences between the left and right images. With the popularity of dual cameras in mobile phones, autonomous vehicles and robots, stereo vision has attracted increasingly attention in both academia and industry. In many applications like AR/VR and robot navigation, increasing the resolution of stereo images is highly demanded to achieve higher perceptual quality and help to parse the real world.

In recent years, remarkable progress of image super-resolution (SR) have been witnessed with deep learning techniques. However, most approaches focus on super-resolving single images and cannot be directly extended to the task of stereo image SR. For stereo images, how to effectively incorporate additional information from a second viewpoint at varying disparities remains challenging. 

In this challenge, we aim at establishing a benchmark for stereo image SR, and aspire to highlight the specific challenges and research problems faced by stereo image SR. This challenge provides an opportunity for researchers to work together to share their knowledge and insights, advance the algorithm performance, and promote the development of stereo image SR.

## Description of the Challenge
The objective of this challenge is to reconstruct high-resolution (HR) stereo images from their low-resolution (LR) counterparts. 

During the model development phase, the training set and the validation set will be released. Both HR stereo images and their LR counterparts in the training and validation sets are available. The participants can train their models on the training set and can evaluate their models with the validation set. 

During the test phase, the test set will be released, which includes LR images only. Challenge participants should apply their trained models to the LR test images to generate super-resolved test images.  These super-resolved images will then be submitted by the participants and evaluated by the organizers with a set of objective quantitative metrics.

## Datasets
### Training Set: *[[download HR-LR training data](https://www.jianguoyun.com/p/DR03yFcQwOebChjC1KoE)]*
The 800 stereo images in training set of the [Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/) are used as the training set of this challenge. Both HR images and their LR versions (produced by bicubic downsampling) will be released. The participants can use these HR images as groundtruths to train their models. **Note that, external dataset (e.g., the Middlebury or KITTI datasets, validation/test sets of the Flickr1024 dataset) is NOT allowed in this challenge. Besides, models pretrained on other datasets (e.g., RCAN/SwinIR developed on DIV2K datasets) are NOT allowed in this challenge.**

### Validation Set: *[[download HR-LR validation data](https://www.jianguoyun.com/p/DeGlXW0QwOebChjE1KoE)]*
The 112 stereo images in the validation set of the [Flickr1024 dataset](https://yingqianwang.github.io/Flickr1024/) are used as the validation set of this challenge. Similar to the training set, both HR and LR images in the validation set are provided. The participants can download the validation set to evaluate the performance of their developed models by comparing their super-resolved images with the HR groundtruth images. **Note that, the validation set should be used for validation purpose only but cannot be used as additional training data.** The participants are encouraged to write papers to describe their methods and use the released validation set for performance evaluation.

### Test Set: *[[download LR test data](https://www.jianguoyun.com/p/DWQY4hYQwOebChjh37QE)]*
To rank the submitted models, a test set consisting of 100 stereo images are provided. Different from the training and validation sets, only LR images will be released. The participants are required to apply their models to the released LR stereo images and submit their super-resolved images to the server. It should be noted that the images in the test set (even the LR versions) cannot be used for training.

## Evaluation Metrics
We evaluate the submitted results by comparing them with the ground truth stereo image pairs. To measure the fidelity, we use the standard Peak Signal to Noise Ratio (PSNR) and, complementarily, the Structural Similarity (SSIM) index as they are often employed in the literature. PSNR and SSIM implementations can be found in most of the image processing toolboxes. We report the average results over all the processed stereo images (both left and right) in the evaluation dataset. **Note that, the final results are ranked by PSNR calculated in the RGB domain.**


## Baseline Model
Over the last few years, several milestone methods have been developed for stereo image SR, including [StereoSR](https://github.com/PeterZhouSZ/stereosr), [PASSRnet](https://github.com/The-Learning-And-Vision-Atelier-LAVA/PASSRnet), [iPASSR](https://github.com/YingqianWang/iPASSR) and [SSRDE-FNet](https://github.com/MIVRC/SSRDEFNet-PyTorch). In this challenge, [PASSRnet](https://github.com/The-Learning-And-Vision-Atelier-LAVA/PASSRnet) is used as a baseline model and the submitted results should be at least on par with PASSRnet. The solutions with PSNR values lower than PASSRnet will not be ranked in the leaderboard.

### PSNR and SSIM values achieved by baseline methods on the validation set for 4xSR:
| Method | PSNR (Y)  |  PSNR (RGB)  | SSIM (Y)  | SSIM (RGB)  |
|:------:|  :--------: | :--------: | :---------: | :-------: |
| Bicubic    | 23.3865 | 21.8358 | 0.6443 | 0.6287 |
| PASSRnet   | 24.6990 | 23.1211 | 0.7283 | 0.7095 |

## Submission
We use [CodaLab](https://codalab.lisn.upsaclay.fr/competitions/1598) for online submission in the development phase. **Here, we provide an example ([Jianguoyun Drive](https://www.jianguoyun.com/p/DXWimH4QwOebChipxasE) or [Google Drive](https://drive.google.com/file/d/1gyaan54AwbAYLIIA1rly_wrLzdyQ7VAh/view?usp=sharing)) to help participants to format their submissions.** In the test phase, the final results and the source codes (both training and test) need to be submitted via emails (ntire.stereosr@outlook.com). Please refer to our [online website](https://codalab.lisn.upsaclay.fr/competitions/1598) for details of the submission rules.

## Important Dates
* 2022-01-21: Release of training and validation data;
* 2022-01-31: Validation server online;
* 2022-03-23: Final test data release, validation server closed;
* 2022-03-30: Test result submission deadline;
* 2022-03-30: Fact sheet / code / model submission deadline;
* 2022-04-01: Test preliminary score release to the participants;
* 2022-04-01: Challenge paper submission deadline;

## Group number policy
Each group cannot have more than six group members (i.e., 1 to 6 group members is OK), and each paricipant can only join one group. Each group can only submit one algorithm for final ranking.


## Issues and Questions:
For any question regarding this challenge, raise an issue under this repository. <br>
You can also join our WeChat group by scanning the code below:

<p align="center"> <img src="https://raw.github.com/The-Learning-And-Vision-Atelier-LAVA/Stereo-Image-SR/NTIRE2022/Fig/WeChat.jpg" width="30%"> </p>

## Organizers:
* [**Yulan Guo**](http://yulanguo.me/) ([yulan.guo@nudt.edu.cn](yulan.guo@nudt.edu.cn))
* [**Longguang Wang**](https://longguangwang.github.io/) ([wanglongguang15@nudt.edu.cn](wanglongguang15@nudt.edu.cn))
* [**Yingqian Wang**](https://yingqianwang.github.io/) ([wangyingqian16@nudt.edu.cn](wangyingqian16@nudt.edu.cn))
* [**Juncheng Li**](https://junchenglee.com/) ([junchengli@math.cuhk.edu.hk](junchengli@math.cuhk.edu.hk))
* [**Shuhang Gu**](https://shuhanggu.github.io/) ([shuhanggu@gmail.com](shuhanggu@gmail.com))
* [**Radu Timofte**](https://people.ee.ethz.ch/~timofter/) ([Radu.Timofte@vision.ee.ethz.ch](Radu.Timofte@vision.ee.ethz.ch))

## Acknowledgement:
We would like to thank **<a href="https://www.flickr.com/photos/stereotron/" target="_blank">Sascha Becher</a>**
 and **<a href="https://www.flickr.com/photos/tombentz" target="_blank">Tom Bentz</a>** for the approval of using their cross-eye stereo photographs. <br>

## NTIRE 2022 Terms and Conditions:
The terms and conditions of this challenge can be viewed [here](https://codalab.lisn.upsaclay.fr/competitions/1598#learn_the_details-terms_and_conditions).

