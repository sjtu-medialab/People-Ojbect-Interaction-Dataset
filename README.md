# People-Ojbect-Interaction-Dataset

![](https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset/blob/main/frames.png)

## Introduction

The people-object interaction dataset comprises 38 series of 30-view multi-person or single-person RGB-D video sequences, complemented by corresponding camera parameters, foreground masks, SMPL models and some point clouds, mesh files.
Each video sequence boasts a 4K resolution, 25 FPS, and a duration of 1~19 seconds.
All 30 views are captured using Kinect Azure devices in a uniformly surrounding scene.

## Video Sequences Collection and Post Processing

We designed the collecting environment and system as shown below. 

![](https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset/blob/main/system.png)

Details of collected video sequences are show below.

![](https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset/blob/main/contents.png)

For the post processing, we use [BackgroundMattingV2](https://github.com/PeterL1n/BackgroundMattingV2) to extract foreground masks, methods of [Zhou et al.](https://ieeexplore.ieee.org/abstract/document/10008839/) and [Zhou et al.](https://www.ibc.org/download?ac=18719) to extract point clouds and mesh files, [MMHuman3D](https://github.com/open-mmlab/mmhuman3d) to extract SMPL models.

## Dataset Download

At this time, you can access our [BaiduNetdisk](https://pan.baidu.com/s/11T6I3Mw7axq0qwiPNz43Zw?pwd=sjtu )(百度网盘) with verify code of 'sjtu'.
More access to our dataset will be released soon.

The name of subfolders in `Meshes and Point Clouds` are defined by:
```
4D_seriesname_frameindex,
```
where the `seriesname` corresponds to the name of subfolders in `RGB-D-Mask Sequences`, the `frameindex` are the frame index the meshes, and point clouds are constructed for.

## Camera Parameters

Camera parameters are provided in the `intrinsic.txt` and `extrinsic.txt`.
Extrinsics of our cameras are in the format of camera coordinate system to world coordinate system.

## Citation

Our paper if now under review of ICIP-2024.
If you find our dataset useful in your research, by now, please consider cite:

```
@misc{POID,
    title={People-Ojbect-Interaction-Dataset},
    author={People-Ojbect-Interaction-Dataset Contributors},
    howpublished = {\url{https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset}},
    year={2024}
}
```
