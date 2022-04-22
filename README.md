### <img src="https://raw.github.com/YingqianWang/Stereo-Image-SR/master/Fig/Thumbnail.jpg" width="1000">
#### With recent advances in stereo vision, dual cameras are commonly adopted in mobile phones and autonomous vehicles. Using the complementary information provided by binocular systems, the resolution of image pairs can be enhanced by stereo image super-resolution (SR) algorithms. In this repository, we first present a collection of datasets and papers on stereo image SR, together with their codes or repos. Then, we develop a benchmark to comprehensively evaluate milestone and state-of-the-art methods. Welcome to raise issues regarding our survey and submit novel results (better together with original files and source codes) to our benchmark.

#### Note: This repository will be updated on a regular basis, so stay tuned~~🎉🎉🎉

### News:
* 2022-04-20: We add a new work [*Trans-SVSR*](https://github.com/H-deep/Trans-SVSR) that is accepted to CVPRW 2022.
* 2022-04-20: We add a new work [*NAFSSR*](https://github.com/megvii-research/NAFNet) to our repo, which is the Champion of the [*NTIRE 2022 Stereo Image Super-Resolution Challenge*](https://github.com/The-Learning-And-Vision-Atelier-LAVA/Stereo-Image-SR/tree/NTIRE2022).


## Challenges:
### [*NTIRE 2022 Stereo Image Super-Resolution Challenge*](https://github.com/YingqianWang/Stereo-Image-SR/tree/NTIRE2022)

## Datasets:
|     Dataset    |  Publication  |
| :----------: |  :----------------------------------------------------------------: |
| [**Flickr1024**](https://yingqianwang.github.io/Flickr1024/)  | Flickr1024: A Large-Scale Dataset for Stereo Image Super-Resolution, [ICCVW 2019](http://openaccess.thecvf.com/content_ICCVW_2019/papers/LCI/Wang_Flickr1024_A_Large-Scale_Dataset_for_Stereo_Image_Super-Resolution_ICCVW_2019_paper.pdf)  |
| [**Middlebury**](http://vision.middlebury.edu/stereo/data/)  | High-resolution stereo datasets with subpixel-accurate ground truth, [GCPR 2014](www.cs.middlebury.edu/~schar/papers/datasets-gcpr2014.pdf) | 
| [**KITTI 2012**](http://www.cvlibs.net/datasets/kitti/eval_stereo_flow.php?benchmark=stereo)   |  Are we ready for Autonomous Driving? The KITTI Vision Benchmark Suite, [CVPR 2012](https://projet.liris.cnrs.fr/imagine/pub/proceedings/CVPR2012/data/papers/424_O3C-04.pdf) |
| [**KITTI 2015**](http://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo) |  Object Scene Flow for Autonomous Vehicles, [CVPR 2015](http://openaccess.thecvf.com/content_cvpr_2015/papers/Menze_Object_Scene_Flow_2015_CVPR_paper.pdf) |


## Methods:
|     Method    |  Publication  | Official Repository |
| :----------: |  :----------------------------------------------------------------: | :----------: |
| **StereoSR**  | [Enhancing the Spatial Resolution of Stereo Images using a Parallax Prior](http://openaccess.thecvf.com/content_cvpr_2018/papers/Jeon_Enhancing_the_Spatial_CVPR_2018_paper.pdf), CVPR 2018  | [PeterZhouSZ/<br/>stereosr](https://github.com/PeterZhouSZ/stereosr)
| **PASSRnet**  | [Learning Parallax Attention for Stereo Image Super-Resolution](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Learning_Parallax_Attention_for_Stereo_Image_Super-Resolution_CVPR_2019_paper.pdf), CVPR 2019 | [LongguangWang/<br/>PASSRnet](https://github.com/LongguangWang/PASSRnet) | 
| **SAM**   |  [A Stereo Attention Module for Stereo Image Super-Resolution](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8998204), SPL 2020 | [XinyiYing/SAM](https://github.com/XinyiYing/SAM) |
| **SPAMnet** | [Stereoscopic image super-resolution with stereo consistent feature](https://ojs.aaai.org/index.php/AAAI/article/view/6880/6734), AAAI 2020.  | -- |
| **DASSR** | [Disparity-Aware Domain Adaptation in Stereo Image Restoration](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yan_Disparity-Aware_Domain_Adaptation_in_Stereo_Image_Restoration_CVPR_2020_paper.pdf), CVPR 2020. | -- |
| **IMSSRnet** | Deep Stereoscopic Image Super-Resolution via Interaction Module, TCSVT 2020. | -- |
| **CPASSRnet** | Cross Parallax Attention Network for Stereo Image Super-Resolution, TMM 2021. | [canqChen/<br/>CPASSRnet](https://github.com/canqChen/CPASSRnet) |
| **BSSRnet** | [Deep Bilateral Learning for Stereo Image Super-Resolution](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9382858), SPL 2021. | [xuqingyu26/<br/>BSSRnet](https://github.com/xuqingyu26/BSSRnet) |
| **iPASSR** | [Symmetric Parallax Attention for Stereo Image Super-Resolution](https://arxiv.org/pdf/2011.03802.pdf), CVPRW 2021. | [YingqianWang/<br/>iPASSR](https://github.com/YingqianWang/iPASSR) |
| **DFAM**  | A Disparity Feature Alignment Module for Stereo Image Super-Resolution, SPL 2021. | [JiawangDan/DFAM](https://github.com/JiawangDan/DFAM) |
| **CVCnet** | Cross View Capture for Stereo Image Super-Resolution, TMM 2021. | [xyzhu1/CVCnet](https://github.com/xyzhu1/CVCnet) |
| **SSRDE-FNet** | [Feedback Network for Mutually Boosted Stereo Image Super-Resolution and Disparity Estimation](https://arxiv.org/pdf/2106.00985.pdf), ACM MM 2021. | [MIVRC/SSRDEFNet-PyTorch](https://github.com/MIVRC/SSRDEFNet-PyTorch) |
| **SVSRNet** | Stereo video super-resolution via exploiting view-temporal correlations, ACM MM 2021. | -- |
| **PSSR** | Perception-Oriented Stereo Image Super-Resolution, ACM MM 2021. | -- |
| **NAFSSR** | [NAFSSR: Stereo Image Super-Resolution Using NAFNet, CVPRW 2022](https://arxiv.org/pdf/2204.08714.pdf). | [megvii-research/<br/>NAFNet](https://github.com/megvii-research/NAFNet) |
| **Trans-SVSR** | [A New Dataset and Transformer for Stereoscopic Video Super-Resolution, CVPRW 2022](https://arxiv.org/pdf/2204.10039.pdf). | [H-deep/<br/>Trans-SVSR](https://github.com/H-deep/Trans-SVSR) |

## Benchmark
**We benchmark several methods on the KITTI 2012, KITTI 2015, Middlebury and Flickr1024 datasets. The test sets used below can be downloaded from [Google Drive](https://drive.google.com/file/d/1LQDUclNtNZWTT41NndISLGvjvuBbxeUs/view?usp=sharing) and [Baidu Drive](https://pan.baidu.com/s/1SIYGcMBEDDZ0wYrkxL9bnQ) (Key: NUDT). Note that, All these methods have been retrained on the same training set (60 images from the Middlebury dataset and 800 images from the Flickr1024 dataset) for fair comparison.**

**PSNR and SSIM metrics are used for quantitative evaluation, which are first calculated on each view (without boundary cropping) independently, then averaged between left and right views to generate the score of a scene. Finally, the score of a dataset is obtained by averaging the scores of all its scenes.**


### PSNR and SSIM values achieved by different methods for 2xSR:
| Method | Scale | #Params.|  KITTI 2012  |  KITTI 2015  |  Middlebury  |  Flickr1024  |
|:--------------:|  :----: | :------: | :----------: | :----------: | :----------: | :----------: |
| Bicubic    | 2×  |   —   | 28.51/0.8842 | 28.61/0.8973 | 30.60/0.8990 | 24.94/0.8186 |
| VDSR       | 2×  | 0.66M | 30.30/0.9089 | 29.78/0.9150 | 32.77/0.9102 | 25.60/0.8534 |
| EDSR       | 2×  | 38.6M | 30.96/0.9228 | 30.73/0.9335 | 34.95/0.9492 | 28.66/0.9087 |
| RDN        | 2×  | 22.0M | 30.94/0.9227 | 30.70/0.9330 | 34.94/0.9491 | 28.64/0.9084 |
| RCAN       | 2×  | 15.3M | 31.02/0.9232 | 30.77/0.9336 | 34.90/0.9486 | 28.63/0.9082 |
| StereoSR   | 2×  | 1.08M | 29.51/0.9073 | 29.33/0.9168 | 33.23/0.9348 | 25.96/0.8599 |	 	
| PASSRnet   | 2×  | 1.37M | 30.81/0.9190 | 30.60/0.9300 | 34.23/0.9422 | 28.38/0.9038 |
| BSSRnet    | 2×  | 1.89M | 31.03/0.9241 | 30.74/0.9344 | 34.74/0.9475 | 28.53/0.9090 |
| iPASSR     | 2×  | 1.37M | 31.11/0.9240 | 30.81/0.9340 | 34.51/0.9454 | 28.60/0.9097 |
| SSRDE-FNet | 2×  | 2.10M | 31.23/0.9254 | 30.90/0.9352 | 35.09/0.9511 | 28.85/0.9132 |
| NAFSSR-T   | 2×  | 0.45M | 31.26/0.9254 | 30.99/0.9355 | 35.01/0.9495 | 28.94/0.9128 |
| NAFSSR-S   | 2×  | 1.54M | 31.38/0.9266 | 31.08/0.9367 | 35.30/0.9514 | 29.19/0.9160 |
| NAFSSR-B   | 2×  | 6.77M | 31.55/0.9283 | 31.22/0.9380 | 35.68/0.9544 | 29.54/0.9204 |
| NAFSSR-L   | 2×  | 23.8M | 31.60/0.9291 | 31.25/0.9386 | 35.88/0.9557 | 29.68/0.9221 |
			
### PSNR and SSIM values achieved by different methods for 4xSR:
| Method | Scale | #Params.|  KITTI 2012  |  KITTI 2015  |  Middlebury  |  Flickr1024  |
|:--------------:|  :----: | :------: | :----------: | :----------: | :----------: | :----------: |
| Bicubic    | 4×  |   —   | 24.58/0.7372 | 24.38/0.7340 | 26.40/0.7572 | 21.82/0.6293 |
| VDSR       | 4×  | 0.66M | 25.60/0.7722 | 25.32/0.7703 | 27.69/0.7941 | 22.46/0.6718 |
| EDSR       | 4×  | 38.9M | 26.35/0.8015 | 26.04/0.8039 | 29.23/0.8397 | 23.46/0.7285 |
| RDN        | 4×  | 22.0M | 26.32/0.8014 | 26.04/0.8043 | 29.27/0.8404 | 23.47/0.7295 |
| RCAN       | 4×  | 15.4M | 26.44/0.8029 | 26.22/0.8068 | 29.30/0.8397 | 23.48/0.7286 |
| StereoSR   | 4×  | 1.08M | 24.53/0.7555 | 24.21/0.7511 | 27.64/0.8022 | 21.70/0.6460 | 	
| PASSRnet   | 4×  | 1.42M | 26.34/0.7981 | 26.08/0.8002 | 28.72/0.8236 | 23.31/0.7195 |
| SRRes+SAM  | 4×  | 1.73M | 26.44/0.8018 | 26.22/0.8054 | 28.83/0.8290 | 23.27/0.7233 |
| BSSRnet    | 4×  | 1.91M | 26.47/0.8049 | 26.17/0.8075 | 29.08/0.8362 | 23.40/0.7289 |
| iPASSR     | 4×  | 1.42M | 26.56/0.8053 | 26.32/0.8084 | 29.16/0.8367 | 23.44/0.7287 |
| SSRDE-FNet | 4×  | 2.24M | 26.70/0.8082 | 26.43/0.8118 | 29.38/0.8411 | 23.59/0.7352 |
| NAFSSR-T   | 4×  | 0.46M | 26.79/0.8105 | 26.62/0.8159 | 29.32/0.8409 | 23.69/0.7384 |
| NAFSSR-S   | 4×  | 1.56M | 26.93/0.8145 | 26.76/0.8203 | 29.72/0.8490 | 23.88/0.7468 |
| NAFSSR-B   | 4×  | 6.80M | 27.08/0.8181 | 26.91/0.8245 | 30.04/0.8568 | 24.07/0.7551 |
| NAFSSR-L   | 4×  | 23.8M | 27.12/0.8194 | 26.96/0.8257 | 30.20/0.8605 | 24.17/0.7589 |

## Recources
#### We provide some original super-resolved images and useful resources to facilitate researchers to reproduce the above results.
* **The 2x/4x models of EDSR/RDN/RCAN retrained on stereo image datasets. [Google Drive](https://drive.google.com/drive/folders/1ovN_O34qTToI6jiaL69T1_vlHv2jwu0f?usp=sharing), [Baidu Drive](https://pan.baidu.com/s/1GrKi8taYnEColKz_wa5f4w) (Key: NUDT).**
* **The 2x/4x results of StereoSR. [Google Drive](https://drive.google.com/file/d/1nt6uBhyze0Cx0VdI3O7PsxN51qZNqIKd/view?usp=sharing), [Baidu Drive](https://pan.baidu.com/s/1E_w0BHeaNzjQEyc22To5FQ) (Key: NUDT).**
* **The 4x results of SRRes+SAM. [Google Drive](https://drive.google.com/file/d/1uOM-LUDandK2lX9p2mknc_J1C81Zbn8e/view?usp=sharing), [Baidu Drive](https://pan.baidu.com/s/1KIr0v1XfBPPQR-MEMTUbwg) (Key: NUDT).**
* **The 2x/4x results of iPASSR. [Google Drive](https://drive.google.com/file/d/1LKe86Cet8LFRG-mgG9oYAJlyiJljDJb0/view?usp=sharing) and [Baidu Drive](https://pan.baidu.com/s/1w8RtQau2RoY89jsFvMCStw) (Key: NUDT).**
* **The 2x/4x results of BSSRnet. [Google Drive](https://drive.google.com/file/d/1MxYcpZMap9Vfc4jJp6QHBFqBj9gqb1-K/view?usp=sharing) and [Baidu Drive](https://pan.baidu.com/s/1V9rgQLw3VbtQk9Nk_rVvFQ) (Key: NUDT).**


