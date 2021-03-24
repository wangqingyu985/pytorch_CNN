# **几种类型的BackBone**

## LeNet--1998年

![image-20210309084647702](C:\Users\HUWEI\AppData\Roaming\Typora\typora-user-images\image-20210309084647702.png)

## AlexNet--2010年

<img src="C:\Users\HUWEI\AppData\Roaming\Typora\typora-user-images\image-20210308214421695.png" alt="image-20210308214421695" style="zoom:50%;" />

![image-20210308215629691](C:\Users\HUWEI\AppData\Roaming\Typora\typora-user-images\image-20210308215629691.png)

## VGG--2014年

使用三个3×3的卷积核替代一个7×7的卷积核，以减少网络的参数

## GoogleNet--2014年

1.引入了Inception结构（可以融合不同尺度的信息）

2.使用了1×1的卷积核进行降维处理

3.在训练网络的时候添加了两个辅助分类器（loss=loss0+loss1×0.3+loss2×0.3），测试的时候只有一个主输出

4.丢弃全连接层，使用平均池化以减少网络参数

<img src="C:\Users\HUWEI\AppData\Roaming\Typora\typora-user-images\image-20210308215512251.png" alt="image-20210308215512251" style="zoom:80%;" />

## ResNet--2017年

1.突破1000层的网络结构

2.提出残差（residual）模块，解决精度随网络层数加深而下降的“退化”问题

3.使用Batch Normalization加速训练过程，同时解决梯度消失和梯度爆炸的问题，丢弃dropout层

## MobileNet v1--2017年

正常的卷积：

![微信图片_20210323092007](D:\Users\HUWEI\Desktop\微信图片_20210323092007.png)

![微信图片_20210323092013](D:\Users\HUWEI\Desktop\微信图片_20210323092013.png)

问题：之前的普通convolution构成的backbone参数过多，不利于移动端设备开发。

1.通过Depthwise Convolution（卷积核的channel恒定为1）和Pointwise Convolution（卷积核的大小恒定为1，其余特征和普通卷积相同）减少参数量

DW+PW组成的卷积效果和普通卷积是相同的，但是大大减少了参数的量。

2.增加超参数α：控制卷积核个数、β：控制图像输入大小。

## MobileNet v2--2018年

1.倒残差结构（先升维后降维，且采用ReLu6激活函数）

2.linear bottlenecks

## ShuffleNet--2017年

1.

2.

## EfficientNet--2019年



