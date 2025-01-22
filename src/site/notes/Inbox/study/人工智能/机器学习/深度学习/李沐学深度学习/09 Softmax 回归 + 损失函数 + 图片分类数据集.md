---
{"dg-publish":true,"tags":["deep_learning","course"],"permalink":"/Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/09 Softmax 回归 + 损失函数 + 图片分类数据集/","dgPassFrontmatter":true}
---



# 09 Softmax 回归 + 损失函数 + 实战图片分类数据集
- 回归问题和分类问题
	![tmp-74.png](/img/user/Assets/attachments/tmp/tmp-74.png)
- 分类问题
	- 损失函数：
		- 差值（ylabel-yi）
		- 交叉熵（y的概率-yi的概率）
			- 我们其实不关系Oi的值，只是关心预测的label和其他label之间的差别要大，所以用softmax把Oi变成一个0-1之间的概率
			![tmp-75.png](/img/user/Assets/attachments/tmp/tmp-75.png)
			- 损失函数
				- 公式：![tmp-76.png](/img/user/Assets/attachments/tmp/tmp-76.png)
				- 求导运算：![tmp-77.png](/img/user/Assets/attachments/tmp/tmp-77.png)
					- 公式推导：
						![tmp-78.png](/img/user/Assets/attachments/tmp/tmp-78.png)
- 对于图片分类数据集的softmax回归完整实现
	- 环境
		- 虚拟环境名字：regression
		- python版本：3.9
		- cuda版本：11.6
	- 数据获取：用torchvision下载数据集
	- 数据清洗：图片不需要清洗
	- 特征工程：图片归一化——PIL图片（灰度图，0-255）转化成tensor（单通道，0-1），每个像素是一个输入值
	- 选择模型，损失函数和优化器，超参数进行训练：
		- 模型：线性模型[3.3 线性模型](3.3%20线性模型.md)
		- 损失函数：
			- net的最后一层输出层Oi经过softmax处理
			- 经过softmax处理后的值和标签的交叉熵作为损失函数
		- 优化器：
			- 小批量SGD（和dataloader一起使用，batchsize相同，在dataloader中随机选取batchsize个样本处理）
				- 实现细节：每个批量中的所有样本计算损失函数，然后再求平均，更新相应权重和偏移（区分均方误差，两者的区别在于回归问题MSE已经平均过了，而回归问题的sgd需要根据批量大小进行平均）
		- 超参数：epochs,batch_size,learning rate
		- 评估指标：
			- 分类问题：accuracy（预测正确的样本/预测错误的样本）

---
# References
🔗[09 Softmax 回归 + 损失函数 + 图片分类数据集【动手学深度学习v2】_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV1K64y1Q7wu?spm_id_from=333.788.videopod.episodes&vd_source=73a67190a2e14f51c71c0fa447f094aa)