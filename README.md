# S-Aware-network (AAAI'2023)

## Introduction
This is an implementation of the following paper.
> [Estimating Reflectance Layer from A Single Image: Integrating Reflectance Guidance and Shadow/Specular Aware Learning.](https://arxiv.org/abs/2211.14751)
> AAAI Conference on Artificial Intelligence, (AAAI'2023)

[Yeying Jin](https://jinyeying.github.io/), [Ruoteng Li](https://liruoteng.github.io/), [Wenhan Yang](https://flyywh.github.io/) and [Robby T. Tan](https://tanrobby.github.io/pub.html)

[[Paper]](https://arxiv.org/pdf/2211.14751.pdf)
[[Poster]](https://www.dropbox.com/s/epc69nk2aqsdi7v/SAware_poster.pdf?dl=0) 
[[Slides]](https://www.dropbox.com/s/7f3j2d5ugifpftv/SAware_ppt.pdf?dl=0) 

### Abstract
Estimating reflectance layer from a single image is a challenging task. 
It becomes more challenging when the input image contains shadows or specular highlights, which often render an inaccurate estimate of the reflectance layer. Therefore, we propose a two-stage learning method, including reflectance guidance and a Shadow/Specular-Aware (S-Aware) network to tackle the problem. In the first stage, an initial reflectance layer free from shadows and specularities is obtained with the constraint of novel losses that are guided by prior-based shadow-free and specular-free images. To further enforce the reflectance layer to be independent from shadows and specularities in the second-stage refinement, we introduce an S-Aware network that distinguishes the reflectance image from the input image. Our network employs a classifier to categorize shadow/shadow-free, specular/specular-free classes, enabling the activation features to function as attention maps that focus on shadow/specular regions. Our quantitative and qualitative evaluations show that our method outperforms the state-of-the-art methods in the reflectance layer estimation that is free from shadows and specularities.

## Datasets
### Intrinsic Image Decomposition

1.[IIW](<https://labelmaterial.s3.amazonaws.com/release/iiw-dataset-release-0.zip>) OR [IIW](http://opensurfaces.cs.cornell.edu/publications/intrinsic/)

2.[MIT](https://github.com/davidstutz/grosse2009-intrinsic-images) OR [MIT](http://www.cs.toronto.edu/~rgrosse/intrinsic/downloads.html)

3.[MPI-Sintel](https://www.dropbox.com/s/4p6hlwsv2bv9vgp/MPI_300.zip?dl=0)

4.[ShapeNet](https://www.dropbox.com/s/vzi9cak5kr2obeq/ShapeNet-intrinsic-car-modified.zip?dl=0)
(https://github.com/JannerM/intrinsics-network)


### Shadow Removal

1.SRD ([train](https://drive.google.com/file/d/1W8vBRJYDG9imMgr9I2XaA13tlFIEHOjS/view) [BaiduNetdisk](https://pan.baidu.com/s/1mj3BoRQ) and [test](http://www.shengfenghe.com/publications/)).

2.[AISTD](https://www3.cs.stonybrook.edu/~cvl/projects/SID/index.html) 

### Specularity/highlight Removal
1.[Specularity separation](https://www.dropbox.com/s/awk9fa00xvfeqmf/specular%2Bdataset.zip?dl=0)

2.[ShapeNet]

Renjiao Yi, Ping Tan and Stephen Lin, "Leveraging Multi-view Image Sets for Unsupervised Intrinsic Image Decomposition and Highlight Separation", AAAI 2020.

## Specular-Free Loss
Get the following Figure 6 in the main paper,
<p align="left">
  <img width=550" src="teaser/specular-free.png">
</p>

```
demo_spfree_release.m
```

### Citation
If this work is useful for your research, please cite our paper. 
```
@article{jin2022estimating,
  title={Estimating Reflectance Layer from A Single Image: Integrating Reflectance Guidance and Shadow/Specular Aware Learning},
  author={Jin, Yeying and Li, Ruoteng and Yang, Wenhan and Tan, Robby T},
  journal={arXiv preprint arXiv:2211.14751},
  year={2022}
}
```
