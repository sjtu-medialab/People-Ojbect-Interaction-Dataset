# People-Ojbect Interaction Dataset

![](https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset/blob/main/frames.png)

## Introduction

The people-object interaction dataset comprises 38 series of 30-view multi-person or single-person RGB-D video sequences, complemented by corresponding camera parameters, foreground masks, SMPL models and some point clouds, mesh files.
Each video sequence boasts a 4K resolution, 25 FPS, and a duration of 1~19 seconds.
All 30 views are captured using Kinect Azure devices in a uniformly surrounding scene.

## Video Sequences Collection and Post Processing

We designed the collecting environment and system as shown below. 

![](https://github.com/sjtu-medialab/People-Ojbect-Interaction-Dataset/blob/main/system.png)

Details of collected video sequences are show below.

| Category                  | Amount | Duration (s) | Contents                                                                                           |
|---------------------------|--------|--------------|----------------------------------------------------------------------------------------------------|
| Empty Scene               | 1      | 1            | The empty scene that has nobody on the stage.                                                      |
| Camera Calibration        | 1      | 8            | Camera calibration sequences.                                                                      |
| One Person with Objects   | 23     | 2~19         | Flipping through a book, circling around a chair before sitting down, opening and closing an umbrella, pushing a suitcase, typing on a laptop, holding a chess board, body building, kongfu, flipping through a book and walking around, picking up the laptop, playing telephone while doing exercises, sitting on a chair, lying on a chair, wearing a helmet, playing with stuffed toys, carrying a backpack, holding a backpack, circling with a chess board, circling with a suitcase, reading books on a chair, working on a chair, playing the electronic keyboard, playing the electronic keyboard on a table. |
| Two People with Objects   | 11     | 2~14         | Two people working together to move a table; two people collaborating to sweep the floor; two people hurrying along, one carrying a backpack and the other pulling a suitcase; two people holding a chessboard; two people shaking hands; two people walking together; two people sitting on chairs talking to each other; two people working on a table; two people talking together; two people talking before a laptop; two people taking photos. |
| Three People with Objects | 2      | 2~5          | Three people taking a group photo together, three people taking pictures of each other,              |


For the post processing, we use [BackgroundMattingV2](https://github.com/PeterL1n/BackgroundMattingV2) to extract foreground masks, methods of [Zhou et al.](https://ieeexplore.ieee.org/abstract/document/10008839/) and [Zhou et al.](https://www.ibc.org/download?ac=18719) to extract point clouds and mesh files, [MMHuman3D](https://github.com/open-mmlab/mmhuman3d) to extract SMPL models.

## Dataset Download

At this time, you can access our [BaiduNetdisk](https://pan.baidu.com/s/11T6I3Mw7axq0qwiPNz43Zw?pwd=sjtu )(百度网盘) with verify code of 'sjtu', or [Medialab](https://medialab.sjtu.edu.cn/post/people-ojbect-interaction-dataset/).
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
