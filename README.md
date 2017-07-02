# 任务板

### 基本环境安装

#### Prepare Software
* [Pycharm](https://www.jetbrains.com/pycharm/download/)

1. For Windows
* [python-3.6.1-amd64.exe](https://www.python.org/ftp/python/3.6.1/python-3.6.1-amd64.exe)

安装python，然后将python添加到系统环境变量
打开cmd
输入一下命令

```python
pip show pip
pip install -U pip
pip install numpy scikit sklearn
pip install python-opencv
```

2. For Linux
打开ternminal，运行如下命令

```python
apt-get update && apt-get upgrade
apt-get install python3-dev
apt-get install python-pip

pip install -U pip
pip install numpy scikit sklearn
pip install python-opencv
```

----------------------

## TODO LIST
### 图像预处理
1. 对于给定的图像进行如下操作  
  1.1 镜像，分别沿x方向中轴，沿y方向的中轴  
  1.2 旋转  
  1.3 在图像中添加随机噪声  
2. 编写对图像缩放函数，同时要保证对应的label区域的有效性  
3. 将图像中的label写成一个json文件  
```bash
sign_labels = dict()
sign_labels = {
  "label01":1,
  "label01":2,
}
```
4. 将图像信息和label信息组织成字典，存储在pkl中，具体的格式如下：  
```bash
image_sampples = dict()
image_sampples = {
  "image_file_path" : [
      {'class': class_int, 'box_coords': (x_min, y_min, x_max, y_max)}, 
      {'class': class_int, 'box_coords': (x_min, y_min, x_max, y_max)},
    ],
  "image_file_path" : [],
  "image_file_path" : []
}
```

