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
|     Model     |  Paper  | Better Performance than |
| :----------: |  :----------------------------------------------------------------: | :----------: |
| [**StereoSR**](https://github.com/PeterZhouSZ/stereosr) | [**Enhancing the Spatial Resolution of Stereo Images using a Parallax Prior**](http://openaccess.thecvf.com/content_cvpr_2018/papers/Jeon_Enhancing_the_Spatial_CVPR_2018_paper.pdf), ***CVPR2018***. | *SRCNN, VDSR*
| [**PASSRnet**](https://github.com/LongguangWang/PASSRnet) | [**Learning Parallax Attention for Stereo Image Super-Resolution**](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Learning_Parallax_Attention_for_Stereo_Image_Super-Resolution_CVPR_2019_paper.pdf), ***CVPR2019 & TPAMI2020***. | **StereoSR**,<br> *SRCNN, VDSR, DRCN, DRRN, LapSRN*
| [**SAM**](https://github.com/XinyiYing/SAM) | [**A Stereo Attention Module for Stereo Image Super-Resolution**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8998204), ***SPL2020.*** | *SRResNet* < **PASSRnet** < *SRResNet+SAM* |
| **SPAMnet** | **Stereoscopic image super-resolution with stereo consistent feature**, ***AAAI2020.*** | **StereoSR, PASSRnet**,<br> *SRCNN, VDSR, DRRN, LapSRN* |
| **DASSR** | [**Disparity-Aware Domain Adaptation in Stereo Image Restoration**](https://openaccess.thecvf.com/content_CVPR_2020/papers/Yan_Disparity-Aware_Domain_Adaptation_in_Stereo_Image_Restoration_CVPR_2020_paper.pdf), ***CVPR2020.*** | **StereoSR, PASSRnet**,<br> *EDSR, SRNTT, DUF, SMPC* |
| **IMSSRnet** | **Deep Stereoscopic Image Super-Resolution via Interaction Module**, ***TCSVT2020.*** | **StereoSR, PASSRnet** |
| [**iPASSR**](https://github.com/YingqianWang/iPASSR) | [**Symmetric Parallax Attention for Stereo Image Super-Resolution**](https://arxiv.org/pdf/2011.03802.pdf), ***arXiv2020.*** | **StereoSR, PASSRnet, SRRes+SAM**,<br> *EDSR, RDN, RCAN* |
| [**CPASSRnet**](https://github.com/canqChen/CPASSRnet) | **Cross Parallax Attention Network for Stereo Image Super-Resolution**, ***TMM2021.*** | **StereoSR, PASSRnet**, <br> *SRCNN, LapSRN，SRDense* |


<!--
| **DCSSRnet** | **--ICLRW2020--**<br> [**paper**](https://arxiv.org/pdf/2003.08539.pdf) | -- | **endoscopic image, disparity-constrained parallax attention** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN* |
| **NNRANet** | **--ICASSP2020--**<br> [**paper**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9054687) | -- | **non-local, nested residual group** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN, LapSRN* |
-->
