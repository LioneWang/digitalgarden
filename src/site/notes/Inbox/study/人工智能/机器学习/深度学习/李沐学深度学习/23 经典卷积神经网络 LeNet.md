---
{"dg-publish":true,"tags":["deep_learning","course"],"permalink":"/Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/23 经典卷积神经网络 LeNet/","dgPassFrontmatter":true}
---



# 23 经典卷积神经网络 LeNet
- Lenet是早期运用CNN的成功的神经网络，发明者是YanLeCun
- 先使用卷积层来学习空间信息
- 最后使用全连接层来转换到类别空间
![tmp-110.png](/img/user/Assets/attachments/tmp/tmp-110.png)
- 每个卷积层和线性层后面有个sigmoid函数，作用是非线性化
![tmp-111.png](/img/user/Assets/attachments/tmp/tmp-111.png)

QA
![tmp-112.png](/img/user/Assets/attachments/tmp/tmp-112.png)
- 一般情况下，输出通道减少一半，输出通道会变成两倍

![tmp-113.png](/img/user/Assets/attachments/tmp/tmp-113.png)
- Lua，pytorch的torch就是起源于lua语言

---
# References
[23 经典卷积神经网络 LeNet【动手学深度学习v2】_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1t44y1r7ct/?spm_id_from=333.1387.collection.video_card.click&vd_source=73a67190a2e14f51c71c0fa447f094aa)