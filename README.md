cd ~/ros2_ws

colcon build

pip install opencv-python

pip install opencv-python cv-bridge


rosdep install --from-paths src --ignore-src -r -y

cd ros2_ws/src

ros2 pkg create usb_cam_example --build-type ament_python --dependencies rclpy sensor_msgs cv_bridge


เข้าไปที่ตำแหน่งโฟลเดอร์ไฟล์
python3 camera_publisher.py
python3 camera_subscriber.py

รันด้วยคำสั่งใน ROS2

ros2 run usb_cam_example camera_publisher

ros2 run usb_cam_example camera_subscriber
