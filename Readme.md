# 操作步骤
1. 从github下载代码和图片数据集，代码有3个文件，charNeuralNet.py用来训练和测试字符识别模型，plateNeuralNet.py用来训练和测试车牌检测模型，carPlateIdentity.py是最终的测试程序，会调用前面2个训练好的模型识别图片中的车牌字符。数据集包括cnn_char_train(字符数据集)、cnn_plate_train(车牌数据集)、pictures(最终测试图片，仅供参考)、opencv_output(这是我测试的结果)，字符数据集和车牌数据集没有划分训练集和测试集，自行按比例切分；
2. 将charNeuralNet.py在main函数的train_flag改成1，在当前工程目录下创建carIdentityData/cnn_char_train和carIdentityData/model/char_recongnize目录，取字符训练集放在carIdentityData/cnn_char_train路径下，执行该程序训练字符识别模型，模型保存在carIdentityData/model/char_recongnize路径下；
3. 将charNeuralNet.py在main函数的train_flag改成0，在当前工程目录下创建carIdentityData/cnn_char_test目录，取字符测试集放在此路径下，将model_path修改成自己模型的路径，执行程序测试字符识别准确率;
4. plateNeuralNet.py的操作步骤同2、3步骤相似，用来获取车牌检测模型；
5. 将carPlateIdentity.py程序的plate_model_path、char_model_path修改成自己训练好的模型路径，下面测试图片的img路径也修改成自己图片的路径，执行该程序进行车牌字符检测。

# 操作环境
Python3.6、Tensorflow==1.12./*、opencv-python==3.4.4./*

# 源项目Fork by
https://github.com/simple2048/CarPlateIdentity

# 后续计划更新
1. tf1的部分组件优化至tf2版本
2. cnn网络优化
