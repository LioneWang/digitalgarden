---
{"dg-publish":true,"tags":["deep_learning","course"],"permalink":"/Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/16 PyTorch 神经网络基础/","dgPassFrontmatter":true}
---



# 16 PyTorch 神经网络基础
- 层和块
	![tmp-90.png](/img/user/Assets/attachments/tmp/tmp-90.png)
	- 自定义块
	![tmp-91.png](/img/user/Assets/attachments/tmp/tmp-91.png)
	- 顺序块
	![tmp-92.png](/img/user/Assets/attachments/tmp/tmp-92.png)
	- 混合搭配各种组合块
	![tmp-93.png](/img/user/Assets/attachments/tmp/tmp-93.png)
	- 构造因素
		- init：给出所有的层
		- forward：给出前向计算的公式
- 参数管理
	- net[]：像数组一样访问每个层
	- print（net）：查看网络内部结构
	- 内置初始化：
	![tmp-94.png](/img/user/Assets/attachments/tmp/tmp-94.png)
	- 参数绑定——两个层共享权重
	![tmp-95.png](/img/user/Assets/attachments/tmp/tmp-95.png)
- 读写文件 
![tmp-96.png](/img/user/Assets/attachments/tmp/tmp-96.png)
- 保存模型参数
![tmp-97.png](/img/user/Assets/attachments/tmp/tmp-97.png)
- 读取模型及参数
![tmp-98.png](/img/user/Assets/attachments/tmp/tmp-98.png)

---
# References
[参数管理_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1AK4y1P7vs?spm_id_from=333.788.videopod.episodes&vd_source=73a67190a2e14f51c71c0fa447f094aa&p=2)