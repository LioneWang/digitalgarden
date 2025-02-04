---
{"tags":["deep_learning","rnn","course"],"dg-publish":true,"permalink":"/Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/54 循环神经网络 RNN/","dgPassFrontmatter":true}
---

- 潜变量模型 
    - RNN
    ![tmp-193.png](/img/user/Assets/attachments/tmp/tmp-193.png)
- 困惑度
    - 实际就是交叉熵函数，只不过除以了n（n指的是时间步，因为对于序列模型不是只有一个输出，而是根据上一次的结果不停推断下一个词）
![tmp-195.png](/img/user/Assets/attachments/tmp/tmp-195.png)
- 梯度裁剪
    - 目的：防止梯度爆炸，相当于用L2正则化处理权重，对权重正则化
![tmp-196.png](/img/user/Assets/attachments/tmp/tmp-196.png)
- RNN的应用
    - 文本生成： [[Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/55 循环神经网络 RNN 的实现\|55 循环神经网络 RNN 的实现]]
    - 文本分类：
    - 机器翻译：[[Inbox/study/人工智能/机器学习/深度学习/李沐学深度学习/62 序列到序列学习（seq2seq）\|62 序列到序列学习（seq2seq）]]
![tmp-194.png](/img/user/Assets/attachments/tmp/tmp-194.png)
