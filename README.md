# yolov8-jetson-object-detect
# 实验一：目标检测与识别
> 桌面两类物体检测：bottle瓶子、mouse鼠标
部署平台：PC + Jetson
框架：YOLOv8 + ROS2 Humble

## 项目说明
1. 数据集：自采集桌面物体 + Roboflow公开鼠标数据集，分为训练集/验证集8:2
2. 模型：YOLOv8-s，best.pt训练权重
3. 功能
- PC端摄像头实时检测，显示检测框、类别、置信度
- Jetson ROS2节点运行，通过`/yolo_detections`话题JSON发布识别结果
- 输出保存测试样例与错误案例
4. 验收指标
- 识别2类物体；测试20物体识别率≥80%
- Jetson运行速度 ≥5FPS

## 环境依赖
```bash
pip install -r requirements.txt
### Experiment 1: Object Detection and Recognition

> 
> Two‑class desktop object detection: bottle, mouse
> Deployment Platform: PC + Jetson
> Framework: YOLOv8 + ROS2 Humble

### Project Description

1. Dataset: Self‑collected desktop objects combined with public mouse dataset from Roboflow. Split into training set / validation set at a ratio of 8:2.
2. Model: YOLOv8‑s, trained weight file `best.pt` (Download link: xxx)
3. Functions

- Real‑time camera‑based detection on PC; draw bounding boxes, object classes and confidence scores on frames.
- ROS2 node running on Jetson; publish detection results in JSON format via ROS2 topic `/yolo_detections`.
- Save normal test outputs and typical error cases.

4. Acceptance Criteria

- Support simultaneous recognition of two object classes; recognition accuracy ≥80% for 20 test objects.
- Real‑time inference FPS on Jetson ≥5 FPS.

## Dependencies

```
pip install -r requirements.txt
```
