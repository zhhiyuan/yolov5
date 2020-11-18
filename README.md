## 基于YOLOv5实现安全帽检测

训练时map0.91

### 数据集来源
[安全帽佩戴检测赛](https://static.leiphone.com/Safety_helmet.zip)

数据集放在`.data/`下

### 运行

#### 数据准备

进入`./weights`目录运行sh文件下载权重。


进入`.data/`文件夹下。

1. 运行`1.split_data.py`划分数据集

2. 运行`2.xml2txt.py`代码将xml标签转为txt格式，修改文件中第30,32,71行中的valid为train。将原来的train，valid文件夹删除并将txt_train，txt_valid文件夹重命名看那个为train，valid。

3. 运行`3.creattxt.py`代码，生成train/valid.txt

#### 训练

本人使用的是yolov5m，直接运行`trian.py`即可，未测试过其他模型，使用其他模型参考[链接1](https://github.com/ultralytics/yolov5)和[链接2](https://github.com/ultralytics/yolov5/wiki/Train-Custom-Data)

#### 测试

运行`detect.py`