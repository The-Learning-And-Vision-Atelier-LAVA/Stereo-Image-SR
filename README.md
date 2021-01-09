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
|     Model     |   Published |  Codes | Keywords | Better Performance than|
| :----------: |  :-----: | :-------: | :-------: | :-------: |
| **StereoSR** | **--CVPR2018--**<br> [**paper**](http://openaccess.thecvf.com/content_cvpr_2018/papers/Jeon_Enhancing_the_Spatial_CVPR_2018_paper.pdf) & [**supp**](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/0493-supp.pdf) | [**TensorFlow**](https://github.com/PeterZhouSZ/stereosr)* | **pioneering work** | *SRCNN, VDSR*
| **PASSRnet** | **--CVPR2019--**<br> [**paper**](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Learning_Parallax_Attention_for_Stereo_Image_Super-Resolution_CVPR_2019_paper.pdf) & [**supp**](http://openaccess.thecvf.com/content_CVPR_2019/supplemental/Wang_Learning_Parallax_Attention_CVPR_2019_supplemental.pdf)<br>**--TPAMI2020--**<br> [**paper**](https://arxiv.org/pdf/2009.08250.pdf) | [**PyTorch**](https://github.com/LongguangWang/PASSRnet) | **parallax attention** | **StereoSR**, *SRCNN, VDSR, DRCN, DRRN, LapSRN*
| **SAM** | **--SPL2020--**<br> [**paper**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8998204) | [**PyTorch**](https://github.com/XinyiYing/SAM) | **stereo attention, equipped with SISR networks for stereo image SR** | *SRResNet* < **PASSRnet** < *SRResNet+SAM* |
| **SPAMnet** | **--AAAI2020--**<br> [**paper**](https://aaai.org/ojs/index.php/AAAI/article/view/6880/6734) | -- | **stereo consistency, self-and-parallax attention** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN, LapSRN* |
| **DCSSRnet** | **--ICLRW2020--**<br> [**paper**](https://arxiv.org/pdf/2003.08539.pdf) | -- | **endoscopic image, disparity-constrained parallax attention** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN* |
| **NNRANet** | **--ICASSP2020--**<br> [**paper**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9054687) | -- | **non-local, nested residual group** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN, LapSRN* |
| **DASSR** | **--CVPR2020--**<br> [**paper**](http://openaccess.thecvf.com/content_CVPR_2020/papers/Yan_Disparity-Aware_Domain_Adaptation_in_Stereo_Image_Restoration_CVPR_2020_paper.pdf) | -- | **domain adaptive, stereo image restoration** | **StereoSR, PASSRnet**, *EDSR, SRNTT, DUF, SMPC* | 
| **IMSSRnet** | **--TCSVT2020--**<br> [**paper**](https://ieeexplore.ieee.org/document/9253563/) | -- | **interaction module** | **StereoSR, PASSRnet** |
| **iPASSR** | **--arXiv2020--**<br> [**paper**](https://arxiv.org/pdf/2011.03802.pdf) | [**PyTorch**](https://github.com/YingqianWang/iPASSR) | **bi-directional parallax attention, inline occlusion handling, illuminance-robust losses** | **StereoSR, PASSRnet, SRRes+SAM**, comparable or even better than *EDSR, RDN, RCAN* |
| **CPASSRnet** | **--TMM2021--**<br> [**paper**](https://ieeexplore.ieee.org/document/9318556) | [**Tensorflow**](https://github.com/canqChen/CPASSRnet) | **cross parallax attention module** | **StereoSR, PASSRnet**, *SRCNN, LapSRN，SRDense* |


#### Notes: * denotes unofficial implementation.

