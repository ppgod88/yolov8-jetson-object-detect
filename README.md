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
