# costmap_generation_from_realsense
This repo introduce how to generate costmap using realsen camera(d455).
refer to [this](https://github.com/ros2/demos/blob/foxy/composition/launch/composition_demo.launch.py) for using components in launch file.
i use [image_pipeline](https://github.com/ros-perception/image_pipeline/tree/foxy) to convert depth image to pointcloud.

'''
sudo apt install ros-foxy-camera-info-manager
git clone https://github.com/ros-perception/image_pipeline.git -b foxy
cd ..
colcon build
'''

test

'''
ros2 component types
'''
part of terminal output
'''
depth_image_proc
  depth_image_proc::ConvertMetricNode
  depth_image_proc::CropForemostNode
  depth_image_proc::DisparityNode
  depth_image_proc::PointCloudXyzNode
  depth_image_proc::PointCloudXyzRadialNode
  depth_image_proc::PointCloudXyziNode
  depth_image_proc::PointCloudXyziRadialNode
  depth_image_proc::PointCloudXyzrgbNode
  depth_image_proc::PointCloudXyzrgbRadialNode
  depth_image_proc::RegisterNode
'''

from this [wiki](http://wiki.ros.org/depth_image_proc?distro=noetic), i guess i should use compenent depth_image_proc::PointCloudXyzNode.(or maybe depth_image_proc::PointCloudXyzrgbNode)

refer to [this launch file](https://github.com/ros2/demos/blob/foxy/composition/launch/composition_demo.launch.py), i test the compenent depth_image_proc::PointCloudXyzNode.
