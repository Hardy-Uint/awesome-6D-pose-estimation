# awesome-6D-pose-estimation

> 作者：Tom Hardy
>
> 来源：[3D视觉工坊](https://mp.weixin.qq.com/s?__biz=MzU1MjY4MTA1MQ==&mid=2247484684&idx=1&sn=e812540aee03a4fc54e44d5555ccb843&chksm=fbff2e38cc88a72e180f0f6b0f7b906dd616e7d71fffb9205d529f1238e8ef0f0c5554c27dd7&token=691734513&lang=zh_CN#rd)
>
> 主要基于RGB、RGB-D以及点云数据，估计物体和相机/基准坐标系的关系。
>
> 主要有整体方式、霍夫投票方式、Keypoint-based方式、Dense Correspondence方式等。

## 实现方式不同

### 整体方式

> 整体方法直接估计给定图像中物体的三维位置和方向。经典的基于模板的方法构造刚性模板并扫描图像以计算最佳匹配姿态。这种手工制作的模板对集群场景不太可靠。最近，人们提出了一些基于深度神经网络的方法来直接回归相机或物体的6D姿态。然而，旋转空间的非线性使得数据驱动的DNN难以学习和推广。

1. Discriminative mixture-of-templates for viewpoint classification
2. Gradient response maps for realtime detection of textureless objects.
3. Comparing images using the hausdorff distance
4. Implicit 3d orientation learning for 6d object detection from rgb images.
5. Instance- and Category-level 6D Object Pose Estimation

### 基于模型

1. Matching RGB Images to CAD Models for Object Pose Estimation - Georgios  Georgakis, Srikrishna Karanam, Ziyan Wu, and Jana Kosecka. [[Paper\]](https://arxiv.org/pdf/1811.07249.pdf)
2. Deep model-based 6d pose refinement in rgb

### Keypoint-based方式

> 目前基于关键点的方法首先检测图像中物体的二维关键点，然后利用PnP算法估计6D姿态

1. Surf: Speeded up robust features.
2. Object recognition from local scaleinvariant features
3. 3d object modeling and recognition using local affine-invariant image descriptors and multi-view spatial constraints.
4. DeepIM: Deep Iterative Matching for 6D Pose Estimation - Yi Li, Gu Wang, Xiangyang Ji, Yu Xiang, Dieter Fox. [[Paper\]](https://arxiv.org/pdf/1804.00175.pdf)
5. Stacked hourglass networks for human pose estimation
6. Making deep heatmaps robust to partial occlusions for 3d object pose estimation.
7. Bb8: A scalable, accurate, robust to partial occlusion method for  predicting the 3d poses of challenging objects without using depth
8. Real-time seamless single shot 6d object pose prediction.
9. Discovery of latent 3d keypoints via end-toend geometric reasoning.
10. Pvnet: Pixel-wise voting network for 6dof pose estimation.
11. Single-Stage 6D Object Pose Estimation - Yinlin Hu,Pascal Fua,Wei Wang,Mathieu Salzmann. [[Paper\]](https://arxiv.org/pdf/1911.08324.pdf)
12. Estimating 6D Pose From Localizing Designated Surface Keypoints - Zelin  Zhao, Gao Peng, Haoyu Wang, Hao-Shu Fang, Chengkun Li, Cewu Lu. [[Paper\]](https://arxiv.org/pdf/1812.01387v1.pdf)
13. Learning 6D Object Pose Estimation Using 3D Object Coordinates - Eric  Brachmann, Alexander Krull, Frank Michel, Stefan Gumhold, Jamie Shotton, Carsten Rother. [[Paper\]](https://link.springer.com/content/pdf/10.1007%2F978-3-319-10605-2_35.pdf)

### Dense Correspondence/霍夫投票方式

1. Independent object class detection using 3d feature maps.
2. Depth encoded hough voting for joint object detection and shape recovery.
3. aware object detection and pose estimation.
4. Learning 6d object pose estimation using 3d object coordinates.
5. Global hypothesis generation for 6d object pose estimation.
6. Deep learning of local rgb-d patches for 3d object detection and 6d pose estimation.
7. Cdpn: Coordinates-based disentangled pose network for real-time rgb-based 6-dof object pose estimation.
8. Pix2pose: Pixel-wise coordinate regression of objects for 6d pose estimation.
9. Normalized object coordinate space for categorylevel 6d object pose and size estimation.
10. Recovering 6d object pose and predicting next-bestview in the crowd.
11. PVNet: Pixel-wise Voting Network for 6DoF Pose Estimation -  Sida Peng, Yuan Liu, Qixing Huang, Xiaowei Zhou, Hujun Bao. [[Paper\]](https://arxiv.org/pdf/1812.11788.pdf)

### 基于分割

1. Segmentation-driven 6D Object Pose Estimation - Yinlin Hu, Joachim Hugonot, Pascal Fua, Mathieu Salzmann. [[Paper\]](https://arxiv.org/pdf/1812.02541.pdf)
2. Deep Object Pose Estimation for Semantic Robotic Grasping of Household  Objects - Jonathan Tremblay, Thang To, Balakumar Sundaralingam, Yu  Xiang, Dieter Fox, Stan Birchfield. [[Paper\]](https://arxiv.org/pdf/1809.10790.pdf)

### 深度学习方式

1. PoseCNN: A convolutional neural network for 6d object pose estimation in cluttered scenes.
2. Render for cnn: Viewpoint estimation in images using cnns trained with rendered 3d model views.
3. Segmentation-driven 6D Object Pose Estimation - Yinlin Hu, Joachim Hugonot, Pascal Fua, Mathieu Salzmann.[[Paper\]](http://openaccess.thecvf.com/content_CVPR_2019/papers/Hu_Segmentation-Driven_6D_Object_Pose_Estimation_CVPR_2019_paper.pdf)
4. Single-Stage 6D Object Pose Estimation - Yinlin Hu,Pascal Fua,Wei Wang,Mathieu Salzmann. [[Paper\]](https://arxiv.org/pdf/1911.08324.pdf)
5. Normalized Object Coordinate Space for Category-Level 6D Object Pose and Size Estimation -  He Wang, Srinath Sridhar, Jingwei Huang, Julien  Valentin, Shuran Song, Leonidas J. Guibas. [[Paper\]](https://arxiv.org/pdf/1901.02970v1.pdf)
6. Robust 6D Object Pose Estimation in Cluttered Scenesusing Semantic  Segmentation and Pose Regression Networks - Arul Selvam Periyasamy, Max  Schwarz, and Sven Behnke. [[Paper\]
7. [Implicit 3D Orientation Learning for 6D Object Detection from RGB Images](https://www.ais.uni-bonn.de/papers/IROS_2018_Periyasamy.pdf)
8. DenseFusion: 6D Object Pose Estimation by Iterative Dense Fusion - Chen  Wang, Danfei Xu, Yuke Zhu, Roberto Martín-Martín, Cewu Lu, Li Fei-Fei,  Silvio Savarese. [[Paper\]](https://arxiv.org/pdf/1901.04780.pdf)
9. Real-Time Object Pose Estimation with Pose Interpreter Networks- Jimmy  Wu, Bolei Zhou, Rebecca Russell, Vincent Kee, Syler Wagner, Mitchell  Hebert, Antonio Torralba, David M.S. Johnson. [[Paper\]](https://arxiv.org/pdf/1808.01099.pdf)
10. BB8: A Scalable, Accurate, Robust to Partial Occlusion Method for  Predicting the 3D Poses of Challenging Objects without Using Depth -  Mahdi Rad, Vincent Lepetit. [[Paper\]](https://arxiv.org/abs/1703.10896)
11. Real-Time Seamless Single Shot 6D Object Pose Prediction - Bugra Tekin, Sudipta N. Sinha, Pascal Fua. [[Paper\]](https://arxiv.org/pdf/1711.08848.pdf)
12. SSD-6D: Making RGB-based 3D detection and 6D pose estimation great again - Wadim Kehl, Fabian Manhardt, Federico Tombari, Slobodan Ilic, Nassir  Navab. [[Paper\]](https://arxiv.org/pdf/1711.10006.pdf)
13. Deep Learning of Local RGB-D Patches for 3D Object Detection and 6D Pose Estimation - Wadim Kehl, Fausto Milletari, Federico Tombari, Slobodan  Ilic, Nassir Navab. [[Paper\]](https://arxiv.org/pdf/1607.06038.pdf)
14. [Deep-6DPose: Recovering 6D Object Pose from a Single RGB Image - Thanh-Toan Do, Ming Cai, Trung Pham, Ian Reid.](https://arxiv.org/pdf/1802.10367.pdf)

## 数据格式不同

### 基于点云方式

1. PointFusion
2. Frustum PointNets
3. VoteNet

### 基于RGB方式

1. SilhoNet: An RGB Method for 6D Object Pose Estimation - Gideon Billings, Matthew Johnson-Roberson. [[Paper\]](https://arxiv.org/pdf/1809.06893.pdf)
2. PVNet: Pixel-wise Voting Network for 6DoF Pose Estimation -  Sida Peng, Yuan Liu, Qixing Huang, Xiaowei Zhou, Hujun Bao. [[Paper\]](https://arxiv.org/pdf/1812.11788.pdf)
3. DPOD: 6D Pose Object Detector and Refiner - Sergey Zakharov, Ivan Shugurov, Slobodan Ilic. [[Paper\]](https://arxiv.org/pdf/1902.11020v2.pdf)
4. Deep model-based 6d pose refinement in rgb
5. Implicit 3D Orientation Learning for 6D Object Detection from RGB Images - Martin Sundermeyer, Zoltan-Csaba Marton, Maxmilian Durner, Manuel  Brucker and Rudolph Triebel. [[Paper\]](https://arxiv.org/pdf/1902.01275v1.pdf)
6. BB8: A Scalable, Accurate, Robust to Partial Occlusion Method for  Predicting the 3D Poses of Challenging Objects without Using Depth -  Mahdi Rad, Vincent Lepetit. [[Paper\]](https://arxiv.org/abs/1703.10896)
7. Real-Time Seamless Single Shot 6D Object Pose Prediction - Bugra Tekin, Sudipta N. Sinha, Pascal Fua. [[Paper\]](https://arxiv.org/pdf/1711.08848.pdf)
8. SSD-6D: Making RGB-based 3D detection and 6D pose estimation great again - Wadim Kehl, Fabian Manhardt, Federico Tombari, Slobodan Ilic, Nassir  Navab. [[Paper\]](https://arxiv.org/pdf/1711.10006.pdf)
9. [Deep-6DPose: Recovering 6D Object Pose from a Single RGB Image - Thanh-Toan Do, Ming Cai, Trung Pham, Ian Reid.](https://arxiv.org/pdf/1802.10367.pdf)

### 基于RGB-D方式

1. Category-level 6D Object Pose Recovery in Depth Images - Caner Sahin and Tae-Kyun Kim. [[Paper\]](http://openaccess.thecvf.com/content_ECCVW_2018/papers/11129/Sahin_Category-level_6D_Object_Pose_Recovery_in_Depth_Images_ECCVW_2018_paper.pdf)
2. Holistic and local patch framework for 6D object pose estimation in RGB-D images - Haoruo Zhang, Qixin Cao. [[Paper\]](https://www.sciencedirect.com/science/article/pii/S1077314219300050)
3. Multi-view 6D Object Pose Estimation and Camera Motion Planning Using  RGBD Images - Juil Sock, S. Hamidreza Kasaei, Luís Seabra Lopes,  Tae-Kyun Kim. [[Paper\]](https://ieeexplore.ieee.org/document/8265470)
4. Deep Learning of Local RGB-D Patches for 3D Object Detection and 6D Pose Estimation - Wadim Kehl, Fausto Milletari, Federico Tombari, Slobodan  Ilic, Nassir Navab. [[Paper\]](https://arxiv.org/pdf/1607.06038.pdf)

## 相关源码

- [HybridPose](https://github.com/chensong1995/HybridPose)
- [PoseCNN](https://github.com/yuxng/PoseCNN)
- [Single Shot Pose Estimation](https://github.com/Microsoft/singleshotpose)
- [SSD-6D](https://github.com/wadimkehl/ssd-6d)
- [Dope Object Pose Estimation](https://github.com/NVlabs/Deep_Object_Pose)
- [Pose Interpreter Networks](https://github.com/jimmyyhwu/pose-interpreter-networks)
- [Tools for Evaluation of 6D Object Pose Estimation](https://github.com/thodan/obj_pose_eval)
- [Augmented Autoencoder](https://github.com/DLR-RM/AugmentedAutoencoder)
- [DeepIM](https://github.com/liyi14/mx-DeepIM)
- [DenseFusion](https://github.com/j96w/DenseFusion)
- [BetaPose](https://github.com/sjtuytc/betapose)
- [PVNet](https://github.com/zju3dv/pvnet)
