---
{"dg-publish":true,"tags":["deep_learning","course"],"permalink":"/Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/23 经典卷积神经网络 LeNet/","dgPassFrontmatter":true}
---



# 23 经典卷积神经网络 LeNet
- Lenet是早期运用[[Inbox/wiki/CNN\|CNN]]的成功的神经网络，发明者是YanLeCun
- 先使用卷积层来学习空间信息
- 最后使用全连接层来转换到类别空间
![tmp-110.png](/img/user/Assets/attachments/tmp/tmp-110.png)
- 每个卷积层和线性层后面有个sigmoid函数，作用是非线性化
![tmp-111.png](/img/user/Assets/attachments/tmp/tmp-111.png)
## 网络架构图

| Layer                    | Description                                       | Input Size | Output Size | Weight      | Flop             |
| ------------------------ | ------------------------------------------------- | ---------- | ----------- | ----------- | ---------------- |
| Input                    | 32×32 grayscale image                             | 1×1×32×32  | 1×1×32×32   | 0           | 0                |
| C1：Conv                  | Conv layer with 6filters of size 5×5，stride 1     | 1×1×32×32  | 1×6×28×28   | 1×6×5×5+6   | 1×5×5×outputsize |
| S2：Pooling               | Pooling layer with 2×2 average pooling，stride 2   | 1×6×28×28  | 1×6×14×14   | 0           | 0                |
| C3：Conv                  | Conv layer with 16 filters of sizen 5×5，stride1   | 1×6×14×14  | 1×16×10×10  | 6×16×5×5+16 | 6×5×5×outputsize |
| S4:Conv                  | Conv layer with 2×2 average pooling，stride 2      | 1×16×10×10 | 1×16×5×5    | 0           | 0                |
| F5:Fully connected layer | Fully connected layer with 400 inputs,120 outputs | 400        | 120         | 400×120+120 | 400×120          |
| F6：Fully connected layer | Fully connected layer with 120 inputs，84 outputs  | 120        | 84          | 120×84+84   | 120×84           |
| output                   | output layer with 84 inputs，10 outputs（10-class）  | 84         | 10          | 84×10+10    | 84×10            |
## 数据集
- MNIST
##  超参数
- kernel大小，卷积层输出通道数，padding，stride，隐藏层个数
## 权重
- kernel的数值，最后的全连接层的参数，偏置项
## 复杂度
- 可学习权重：61686 （决定内存大小）
- 总[[Inbox/tools/flop\|flop]]s：416520 （决定gpu能力）
## 损失函数
- 交叉熵函数
## 评估指标
- accuracy

QA
![tmp-112.png](/img/user/Assets/attachments/tmp/tmp-112.png)
- 一般情况下，输出通道减少一半，输出通道会变成两倍

![tmp-113.png](/img/user/Assets/attachments/tmp/tmp-113.png)
- Lua，pytorch的torch就是起源于lua语言

---
# References
[23 经典卷积神经网络 LeNet【动手学深度学习v2】_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1t44y1r7ct/?spm_id_from=333.1387.collection.video_card.click&vd_source=73a67190a2e14f51c71c0fa447f094aa)