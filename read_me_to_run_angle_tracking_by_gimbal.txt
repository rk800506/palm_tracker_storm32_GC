1. Run object detector node

roslaunch ros_deep_learning detectnet.ros1.launch \
input:="/dev/video0" \
output:="Display://0" \
model_path:=/home/nvidia/ros_ws/src/ros_deep_learning/mbv1ssd_pedes_detector/open_palm/open_palm_ssd-mobilenet.onnx \
class_labels_path:=/home/nvidia/ros_ws/src/ros_deep_learning/mbv1ssd_pedes_detector/open_palm/labels.txt \
input_blob:=input_0 \
output_cvg:=scores \
output_bbox:=boxes \
input_width:=640 \
input_height:=480 \
input_loop:=0 \
input_codec:=jpg \
threshold:=0.9


2. run storm32 controller node

roslaunch storm32_gimbal gimbal.launch

3. run angle publisher

rosrun storm32_gimbal angle_publisher.py

4. rosbag record /gimbal/control/camera_orientation /gimbal/control/target_orientation /gimbal/control/controller_orientation