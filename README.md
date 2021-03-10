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

## MobileNet--

