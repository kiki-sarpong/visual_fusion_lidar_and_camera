# visual_fusion_lidar_and_camera

### This project is a visual fusion of a lidar and camera. The data is from the rectified KITTI dataset (category:City) 
http://www.cvlibs.net/datasets/kitti/raw_data.php
<br/>
#### Step 1 - Projecting a pointclound onto an image.
This is the first main step in the visual fusion project. I collect a rectified/synced dataset from the list of datasets from the
KITTI website along with the calibration files.<br/>
Next is organizing the calibration files I need to make it easier to call the right matrices for calculations.<br/>
I am able to read the images and associated pointclouds with the opencv and open3d libraries respectively.<br/><br/>

The equation for projecting the pointcloud from the Velodyne lidar into the image is given below and can be obtained from
http://www.cvlibs.net/publications/Geiger2013IJRR.pdf which is also available on the KITTI website.
![image](https://user-images.githubusercontent.com/17696533/125328237-15d30700-e312-11eb-938d-e28eff8a857b.png)
#
<br/>
The projected lidar points are displayed with a color gradients based on the depth of obstacles in the image.<br/>
A red, yellow, green color gradient is created using the matplotlib library.<br/>

![image](https://user-images.githubusercontent.com/17696533/125328285-271c1380-e312-11eb-8a9a-b9763829fdaa.png)
<br/>
# 
#### Lidar and Camera views<br/> 
![image](https://user-images.githubusercontent.com/17696533/125382793-552a4380-e364-11eb-8fa3-cee996c6e18b.png)
![image](https://user-images.githubusercontent.com/17696533/125382835-6bd09a80-e364-11eb-96da-811450afe0a8.png)

#
#### The final results for Step 1 are shown below:
![image](https://user-images.githubusercontent.com/17696533/125238594-6ec08200-e2b5-11eb-87c5-02bc49c4c1e8.png)

<br/> 
(This result is more refined and coloring the depth based on specific distance thresholds)<br/>

![image](https://user-images.githubusercontent.com/17696533/125337422-fab9c480-e31c-11eb-973c-75b44d7a2290.png)

<br/>

![image](https://user-images.githubusercontent.com/17696533/125238892-e5f61600-e2b5-11eb-910d-9c7c4e637391.png)

<br/>
Video 1: Lidar and Image projection <br/>
https://drive.google.com/file/d/11myuQPvnen_iR4LrzenMbU-ZeeXalk0X/view?usp=sharing
<br/>
Video 2:  Lidar projection <br/>
https://drive.google.com/file/d/1LYzQjWLdKmNc8ROX10att_2s3qv1VYv8/view?usp=sharing
<br/>

### Next Steps: Object segmentation/detection

