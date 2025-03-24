# MVImgNet2.0: A Larger-scale Dataset of Multi-view Images

## [Project Page](https://luyues.github.io/mvimgnet2/) | [Paper (Arxiv)](https://arxiv.org/abs/2412.01430) 

<img src="./assets/teaser.png" width="900"/>

by [Xiaoguang Han*#](https://gaplab.cuhk.edu.cn/), [Yushuang Wu*](https://yushuang-wu.github.io/), [Luyue Shi*](https://luyues.github.io/), [Haolin Liu*](https://haolinliu97.github.io/), Hongjie Liao, Lingteng Qiu, Weihao Yuan, Xiaodong Gu, Zilong Dong, Shuguang Cui from [GAP-Lab](https://gaplab.cuhk.edu.cn/).

## Introduction

MVImgNet2.0 contains ∼300k real-world objects in 340+ classes, expands [MVImgNet](https://github.com/GAP-LAB-CUHK-SZ/MVImgNet) to a total of ~520k real-life objects and 515 categories. The annotation comprehensively covers object masks, camera parameters, and point clouds.

Please fill out this [form](https://forms.office.com/Pages/ResponsePage.aspx?id=eouJ5YecS0qyKi3z81XgHtu64XHwYCVMlIWpSlrs63lUNzNHV1pYR0lBUEtET1JGWTEzVTdVVUoyVy4u) to get the download link and password.

### Updates

- We have uploaded the script for downloading MVImgNet2.0.
- We have released the first part of MVImgNet2.0, which contains ~180k videos. Please fill out the above form to get the download links. We will release the remaining videos recently.

### Folder structure
```
|-- ROOT
    |-- class_label
        |-- instance_id
            |-- images
            |-- masks
            |-- sparse/0 # camera parameters and sparse point clouds in colmap format
                |-- cameras.bin   
                |-- images.bin    
                |-- points3D.bin   
```

The mapping between `class_label` and class name can be found in `mvimgnet2_category.json` (The json file contains all the categories of MVImgNet and MVImgNet2.0, to use the data of MVImgNet, please refer to [MVImgNet](https://github.com/GAP-LAB-CUHK-SZ/MVImgNet) for dataset download).

The `images` folder contains the multi-view images, the `masks` folder contains the corresponding object masks, and the `sparse` folder contains the reconstructed camera parameters in COLMAP format. It is recommended to use the functions provided by [COLMAP](https://github.com/colmap/colmap/blob/dev/scripts/python/read_write_model.py) to read the binary files under `sparse` folder.

## License

The data is released under the MVImgNet2.0 Terms of Use, and the code is released under the Attribution-NonCommercial 4.0 International License.

Copyright (c) 2024