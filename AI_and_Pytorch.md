# 人工智能与pytorch知识梳理

## 卷积神经网络(cnn)的应用

1.目标检测
2.图像分类
3.图像语义分割
4.人脸识别

## 知识点

目标检测算法: YOLO
数据集: CIFAR-10
激活函数: softmax sigmoid relu
神经网络4层:输入层->卷积层->全连接层->输出层
pytorch模型库: Torchvision 里有许多模型
损失函数：如,MSE
优化方法:如,SGD
pytorch可视化工具:TensorboardX

## 构建网络几个重要的点

1. 继承 nn.Module 类
(Torchvision里面的模型也是继承 nn.Module)
2. 重写 __init__() 方法, 使用了nn.Parameter()，作为可训练的参数
3. forward() 是必须重写的方法

pytorch保存模型: torch.save(model,'./linear_model_with_arc.pth')

pytorch加载模型
linear_model_2 = torch.load('./linear_model_with_arc.pth')

## 经典的神经网络: VGG GoogLeNet ResNet

## 模型评估:业界标杆ImageNet

## 语义分割领域的一些新网络

1. Gan网络
2. Wide ResNet
3. ResNeXT
4. DenseNet

## NLP领域 transformer,bert
