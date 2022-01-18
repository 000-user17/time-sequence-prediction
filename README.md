# time-sequence-prediction
时间序列预测 ，利用mlp和lstm
有四个数据
train_all.csv 所有的111条训练数据，没有划分验证集出去

train.csv 划分了后30条数据给验证集dev.csv后的还有8条数据的训练数据

dev.csv 包含30条数据的验证集

test.csv 111条测试数据集

代码文件：
采用输入长度：56，112，679；损失函数：MSE，MAE；优化方法：SGD，Adam进行对比

mlp_base.ipynb：MLP模型框架，用于第一次跑通实验，然后以这为基础修改

mlp_with_dev.ipynb：利用train.csv 进行训练，然后球的数据在训练数据上的损失以及预测的值和
训练数据标签的sMAPE；除此之外还用训练后的模型来求在dev.csv上的sMAPE；
该文件包含相应的训练结果图片

mlp_without_dev.ipynb：使用train_all.csv 训练模型，然后计算在test.csv 上的sMAPE
该文件包含相应的训练结果图片

lsmt_base.ipynb：LSTM模型框架，用于第一次跑通实验，然后以这为基础修改

lstm_with_dev.ipynb：利用train.csv 进行训练，然后球的数据在训练数据上的损失以及预测的值和
训练数据标签的sMAPE；除此之外还用训练后的模型来求在dev.csv上的sMAPE
该文件包含相应的训练结果图片

lstm_prediction.ipynb：使用train_all.csv 训练模型，然后计算在test.csv 上的sMAPE
该文件包含相应的训练结果图片

如果要重复执行，只需要从上往下执行代码框即可得到新结果，如果有问题，就第一个代码狂让device='cpu'
都在cpu上执行。

