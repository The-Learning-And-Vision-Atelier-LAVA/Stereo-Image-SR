### <img src="https://raw.github.com/YingqianWang/Awesome-Stereo-Image-SR/master/Fig/Thumbnail.jpg" width="1000">
#### With recent advances in stereo vision, dual cameras are commonly adopted in mobile phones and autonomous vehicles. Using the complementary information provided by binocular systems, the resolution of image pairs can be enhanced by stereo image super-resolution (SR) algorithms. In this repository, we present a collection of papers and datasets on stereo image SR, together with their codes and repos. 
#### Note: This repository will be updated on a regular basis, so stay tuned~~🎉🎉🎉

## Datasets

|     Name     |   links |  Comments |
| :----------: |  :-----: | :-------: |
|     **Flickr1024**     | [**website**](https://yingqianwang.github.io/Flickr1024/) & [**paper**](http://openaccess.thecvf.com/content_ICCVW_2019/papers/LCI/Wang_Flickr1024_A_Large-Scale_Dataset_for_Stereo_Image_Super-Resolution_ICCVW_2019_paper.pdf) | **large-scale; high-quality images; diverse senarios** |
|     **Middlebury**     | [**website**](http://vision.middlebury.edu/stereo/data/) & [**paper**](https://elib.dlr.de/90624/1/ScharsteinEtal2014.pdf) | **indoor scenarios; groundtruth disparity** |
|     **KITTI2012**     | [**website**](http://www.cvlibs.net/datasets/kitti/eval_stereo_flow.php?benchmark=stereo) & [**paper**](http://ww.cvlibs.net/publications/Geiger2012CVPR.pdf) | **driving perspectives; groundtruth disparity** |
|     **KITTI2015**     | [**website**](http://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=stereo) & [**paper**](http://openaccess.thecvf.com/content_cvpr_2015/papers/Menze_Object_Scene_Flow_2015_CVPR_paper.pdf) | **driving perspectives; groundtruth disparity** |


## Methods
|     Method    |  Paper  | Demonstrated Superior to |
| :----------: |  :----------------------------------------------------------------: | :----------: |
| [**StereoSR**](https://github.com/PeterZhouSZ/stereosr) | [**Enhancing the Spatial Resolution of Stereo Images using a Parallax Prior**](http://openaccess.thecvf.com/content_cvpr_2018/papers/Jeon_Enhancing_the_Spatial_CVPR_2018_paper.pdf), ***CVPR2018***. | *SRCNN, VDSR*
| [**PASSRnet**](https://github.com/LongguangWang/PASSRnet) | [**Learning Parallax Attention for Stereo Image Super-Resolution**](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Learning_Parallax_Attention_for_Stereo_Image_Super-Resolution_CVPR_2019_paper.pdf), ***CVPR2019 & TPAMI2020***. | **StereoSR**,<br> *SRCNN, VDSR, DRCN, DRRN, LapSRN*
| [**SAM**](https://github.com/XinyiYing/SAM) | [**A Stereo Attention Module for Stereo Image Super-Resolution**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8998204), ***SPL2020.*** | *SRResNet* < **PASSRnet** < *SRResNet+SAM* |
| **SPAMnet** | **Stereoscopic image super-resolution with stereo consistent feature**, ***AAAI2020.*** | **StereoSR, PASSRnet**,<br> *SRCNN, VDSR, DRRN, LapSRN* |
| **DASSR** | [**Disparity-Aware Domain Adaptation in Stereo Image Restoration**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yan_Disparity-Aware_Domain_Adaptation_in_Stereo_Image_Restoration_CVPR_2020_paper.pdf), ***CVPR2020.*** | **StereoSR, PASSRnet**,<br> *EDSR, SRNTT, DUF, SMPC* |
| **IMSSRnet** | **Deep Stereoscopic Image Super-Resolution via Interaction Module**, ***TCSVT2020.*** | **StereoSR, PASSRnet** |
| [**CPASSRnet**](https://github.com/canqChen/CPASSRnet) | **Cross Parallax Attention Network for Stereo Image Super-Resolution**, ***TMM2021.*** | **StereoSR, PASSRnet**, <br> *SRCNN, LapSRN，SRDense* |
| [**BSSRnet**](https://github.com/xuqingyu26/BSSRnet) | [**Deep Bilateral Learning for Stereo Image Super-Resolution**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9382858), ***SPL2021.*** | **StereoSR, PASSRnet, SRRes+SAM**, <br> *VDSR, LapSRN，DRRN* |
| [**iPASSR**](https://github.com/YingqianWang/iPASSR) | [**Symmetric Parallax Attention for Stereo Image Super-Resolution**](https://arxiv.org/pdf/2011.03802.pdf), ***CVPRW2021.*** | **StereoSR, PASSRnet, SRRes+SAM**,<br> *EDSR, RDN, RCAN* |

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
| BSSRnet    | 2×  | 1.91M | 31.03/0.9241 | 30.74/0.9344 | 34.74/0.9475 | 28.53/0.9090 |
| iPASSR     | 2×  | 1.37M | 31.11/0.9240 | 30.81/0.9340 | 34.51/0.9454 | 28.60/0.9097 |			
			
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

#### We provide some original super-resolved images and useful resources to facilitate researchers to reproduce the above results.
* **The 2x/4x models of EDSR/RDN/RCAN retrained on stereo image datasets. [Google Drive](https://drive.google.com/drive/folders/1ovN_O34qTToI6jiaL69T1_vlHv2jwu0f?usp=sharing), [Baidu Drive](https://pan.baidu.com/s/1GrKi8taYnEColKz_wa5f4w) (Key: NUDT).**
* **The 2x/4x results of StereoSR. [Google Drive](https://drive.google.com/file/d/1nt6uBhyze0Cx0VdI3O7PsxN51qZNqIKd/view?usp=sharing), [Baidu Drive](https://pan.baidu.com/s/1E_w0BHeaNzjQEyc22To5FQ) (Key: NUDT).**
* **The 4x results of SRRes+SAM. [Google Drive](https://drive.google.com/file/d/1uOM-LUDandK2lX9p2mknc_J1C81Zbn8e/view?usp=sharing), [Baidu Drive](https://pan.baidu.com/s/1KIr0v1XfBPPQR-MEMTUbwg) (Key: NUDT).**
* **The 2x/4x results of iPASSR. [Google Drive](https://drive.google.com/file/d/1LKe86Cet8LFRG-mgG9oYAJlyiJljDJb0/view?usp=sharing) and [Baidu Drive](https://pan.baidu.com/s/1w8RtQau2RoY89jsFvMCStw) (Key: NUDT).**
