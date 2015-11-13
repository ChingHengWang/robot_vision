# usb_camera


## Device

* internal camera - /dev/video0
* external camera - /dev/video1

## Package - rbx1_vision
* github : https://github.com/pirobot/rbx1
* according to this package , use lauch in this

## Command Step
* step1. roscore
* step2. roslaunch rbx1_vision uvc_cam.launch device:=/dev/video1
  * after this cmd, you can see the image raw data is on the topic!
  * choose the correct device name!
  * remember use root !
  * change topic name

		***node name="uvc_cam_node" pkg="uvc_camera" type="uvc_camera_node" output="screen"***

  * change device name

		***arg name="device" default="/dev/video0" /***

* step3. rosrun image_view image_view image:=/camera/rgb/image_color
  * create a window to display image!

