## ELEC5660 Introduction to Aerial Robotics: Project 2 Phase 1

In Project 2 Phase 1, you need to implement the algorithm on Lecture 7 to estimate camera’s poses with images.
This is an individual project, which means you must complete it by yourself.

### Project Requirements

- Calculating the camera’s pose corresponding to every image.

- Publishing camera pose information in the form of nav msgs/Odometry.

- Plotting these poses with rqt rviz.

- Comparing your result with the reference.

your code here:
```cpp
void process(const vector<int> &pts_id, const vector<cv::Point3f> &pts_3, const vector<cv::Point2f> &pts_2, const ros::Time& frame_time)
{
    // version 2, your work
    Matrix3d R;
    Vector3d T;
    R.setIdentity();
    T.setZero();
    ROS_INFO("write your code here!");
    //...
    //...
    //...
    Quaterniond Q_yourwork;
}
```


### Tutorial
You will be provided with a ROS package named `tag detector`, where a serial of points and their positions
will be calculated with images. You need to implement this project based on the point and position array. You can
follow the below procedures to prepare for your coding.


- put [`aruco-1.2.4`](https://github.com/HKUST-Aerial-Robotics/HKUST-ELEC5660-Introduction-to-Aerial-Robots/tree/master/L7-%20Multi-View%20Geometry%202D-2D%2C%203D-2D%2C%203D-3D/proj2phase1/aruco-1.2.4) and [`tag detector`](https://github.com/HKUST-Aerial-Robotics/HKUST-ELEC5660-Introduction-to-Aerial-Robots/tree/master/L7-%20Multi-View%20Geometry%202D-2D%2C%203D-2D%2C%203D-3D/proj2phase1/tag_detector) in your workspace `catkin_ws/src/`

- install aruco (following [`aruco-1.2.4/README`](https://github.com/HKUST-Aerial-Robotics/HKUST-ELEC5660-Introduction-to-Aerial-Robots/blob/master/L7-%20Multi-View%20Geometry%202D-2D%2C%203D-2D%2C%203D-3D/proj2phase1/aruco-1.2.4/README))

- Setup your ROS environment and compile the `tag_detector` package.

- Find `bag_tag.launch` in `tag_detector/launch`, and `images.bag` in `tag_detector/bag`.

- Use `bag_tag.launch` and `images.bag` to run this package (`roslaunch bag tag.launch`).

- Read the comments in `tag_detector/src/tag detector node.cpp` carefully.

- Add your code into tag `detector/src/tag_detector_node.cpp`.

- Note that the pose you calculated is (<img src="https://latex.codecogs.com/gif.latex?t_{cw}" title="t_{cw}" /> , <img src="https://latex.codecogs.com/gif.latex?R_{cw}" title="R_{cw}" /> ), which represents the pose of world frame respecting to the camera frame.

### Dataset

The dataset is uploaded to the cloud drive:

Dataset 1: ekf_A3.bag  
Download link: [`Google Drive`](https://drive.google.com/file/d/1lOyvXUbvCaAWDh5bh6ZYCT9Vha7crga5/view?usp=sharing "Google Drive")   [`百度网盘`](https://pan.baidu.com/s/1d7rWE6 "百度网盘")

Dataset 2: ekf_A3_2.bag  
Download link:[`Google Drive`](https://drive.google.com/file/d/1WNfVuK27iz5JPcYyZIHZU6bHl_8lZSJT/view?usp=sharing "Google Drive") [`百度网盘`](https://pan.baidu.com/s/1c3oWZzM "百度网盘")




