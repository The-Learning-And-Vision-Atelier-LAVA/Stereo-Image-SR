### <img src="https://raw.github.com/YingqianWang/Awesome-Stereo-Image-SR/master/Fig/Thumbnail.jpg" width="1000">
#### With recent advances in stereo vision, dual cameras are commonly adopted in mobile phones and autonomous vehicles. Using the complementary information provided by binocular systems, the resolution of image pairs can be enhanced by stereo image super-resolution (SR) algorithms. In this repository, we present a collection of papers and datasets on stereo image SR, together with their codes and repos. 
#### Note: This repository will be updated on a regular basis, so stay tuned~~🎉🎉🎉

## Datasets

|     Name     |   links |  Comments |
| :----------: |  :-----: | :-------: |
|     **Flickr1024**     | [**website**](https://yingqianwang.github.io/Flickr1024/) & [**paper**](http://openaccess.thecvf.com/content_ICCVW_2019/papers/LCI/Wang_Flickr1024_A_Large-Scale_Dataset_for_Stereo_Image_Super-Resolution_ICCVW_2019_paper.pdf) | **large-scale; high-quality images; diverse senarios** |
|     **Middlebury**     | [**website**](http://vision.middlebury.edu/stereo/data/) & [**paper**](https://elib.dlr.de/90624/1/ScharsteinEtal2014.pdf) | **indoor scenarios; groundtruth disparity** |
|     **KITTI2012**     | [**website**](http://www.cvlibs.net/datasets/kitti/index.php) & [**paper**](http://ww.cvlibs.net/publications/Geiger2012CVPR.pdf) | **driving perspectives; multi-role; groundtruth disparity** |
|     **KITTI2015**     | [**website**](http://www.cvlibs.net/datasets/kitti/index.php) & [**paper**](http://openaccess.thecvf.com/content_cvpr_2015/papers/Menze_Object_Scene_Flow_2015_CVPR_paper.pdf) | **driving perspectives; multi-role; groundtruth disparity** |
|     **Holopix50k**     | [**website**](http://github.com/leiainc/holopix50k) & [**paper**](https://arxiv.org/pdf/2003.11172.pdf) | **large-scale; 50K images; diverse senarios** |


## Methods
|     Model     |   Published |  Codes | Keywords | Better Performance than|
| :----------: |  :-----: | :-------: | :-------: | :-------: |
| **StereoSR** | **-CVPR2018-**<br> [**paper**](http://openaccess.thecvf.com/content_cvpr_2018/papers/Jeon_Enhancing_the_Spatial_CVPR_2018_paper.pdf) & [**supp**](http://openaccess.thecvf.com/content_cvpr_2018/Supplemental/0493-supp.pdf) | [**TensorFlow**](https://github.com/PeterZhouSZ/stereosr)* | **pioneering work** | *SRCNN, VDSR*
| **PASSRnet** | **-CVPR2019-**<br> [**paper**](http://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_Learning_Parallax_Attention_for_Stereo_Image_Super-Resolution_CVPR_2019_paper.pdf) & [**supp**](http://openaccess.thecvf.com/content_CVPR_2019/supplemental/Wang_Learning_Parallax_Attention_CVPR_2019_supplemental.pdf) | [**PyTorch**](https://github.com/LongguangWang/PASSRnet) | **parallax attention** | **StereoSR**, *SRCNN, VDSR, DRCN, DRRN, LapSRN*
| **SAM** | **-SPL2020-**<br> [**paper**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8998204) | [**PyTorch**](https://github.com/XinyiYing/SAM) | **stereo attention, equipped with SISR networks for stereo image SR** | *SRResNet* < **PASSRnet** < *SRResNet+SAM* |
| **SPAMnet** | **-AAAI2020-**<br> [**paper**](https://www.aaai.org/Papers/AAAI/2020GB/AAAI-SongW.10348.pdf) | -- | **stereo consistency, self-and-parallax attention** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN, LapSRN* |
| **DCSSRnet** | **-ICLRW2020-**<br> [**paper**](https://arxiv.org/pdf/2003.08539.pdf) | -- | **endoscopic image, disparity-constrained parallax attention** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN* |
| **NNRANet** | **-ICASSP2020-**<br> [**paper**](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9054687) | -- | **non-local, nested residual group** | **StereoSR, PASSRnet**, *SRCNN, VDSR, DRRN, LapSRN* |

#### Notes: * denotes unofficial implementation.

## Other Recources
* [**YapengTian/Single-Image-Super-Resolution**](https://github.com/YapengTian/Single-Image-Super-Resolution)
* [**LoSealL/VideoSuperResolution**](https://github.com/LoSealL/VideoSuperResolution)
* [**ChaofWang/Awesome-Super-Resolution**](https://github.com/ChaofWang/Awesome-Super-Resolution)
* [**ptkin/Awesome-Super-Resolution**](https://github.com/ptkin/Awesome-Super-Resolution)

