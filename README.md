# People-Ojbect-Interaction-Dataset

![](https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset/blob/main/frames.png)

## Dataset Download

At this time, you can access our [BaiduNetdisk](https://pan.baidu.com/s/11T6I3Mw7axq0qwiPNz43Zw?pwd=sjtu )(百度网盘) with verify code of 'sjtu'.
More access to our dataset will be released soon.

The name of subfolders in `Meshes and Point Clouds` and `SMPLs` are defined by:
```
4D_seriesname_frameindex,
```
where the `seriesname` corresponds to the name of subfolders in `RGB-D-Mask Sequences`, the `frameindex` are the frame index the meshes, point clouds, and SMPLs are constructed for.

## Camera Parameters

Camera parameters are provided in the `intrinsic.txt` and `extrinsic.txt`.
Extrinsics of our cameras are in the format of camera coordinate system to world coordinate system.
