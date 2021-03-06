# Machine learning and deep learning code examples

* [jupyter notebook 在这里](https://nbviewer.jupyter.org/github/AutuanLiu/MDeepLearn/tree/master/Kaggle/)

Docker tag | status
--- | ---
CPU | [![Build Status][1]][2]
GPU | [![Build Status][1]][2]

* 这个库使用具体的例子来学习 [机器学习 + 深度学习]

* 使用尽可能详细的注释来写代码, 另外，相关的书面说明以及个人见解与总结会发布在 [website][3]

## Usage

1. 可以通过构建 Docker 容器的方式来进行学习(免去了环境配置的麻烦， 同时支持跨平台)  
```bash
# 通过提供的 Dockerfile 进行构建
$ docker build -t ml-example:latest -f Dockerfile .
``` 

2. 直接 pull image, 运行方式参见 [docker run][4]
```bash
# for CPU version
$ docker pull machine-learning-on-docker:cpu

# for GPU version
$ docker pull machine-learning-on-docker:gpu
```
    
4. git clone(需要自己配置环境)
```bash
$ git clone https://github.com/AutuanLiu/MDeepLearn.git
$ cd MDeepLearn
```

4. [download zip file][5]

## 主要涉及内容

[以下持续更新中......]
* [机器学习常见函数及其图像](function_images.md)
* [线性模型](./TensorFlow)
    * 最小二乘回归
    * Lasso 回归
    * Ridge 回归
    * 多项式回归
    * 核岭回归
    * 弹性网
    * 逻辑回归
    * LDA
    * QDA
* [分类](./sklearn)
    * SVM
    * RandomForest
    * Gradient Boost tree
    * XGBoost
    * AdaBoost
    * CatBoost
    * LightGBM
* [imbalance learn](./imbalanceLearn)
    * over-sampling
    * under-sampling
    * Combining over-sampling and under-sampling
    * Create ensemble balanced sets
* [聚类](./sklearn/unsupervised)
    * K-means
    * GMM
    * Affinity Propagation
    * SpectralClustering
    * DBSCAN
    * MeanShift
* [降维](./sklearn)
    * PCA
    * LDA
    * SVD
* [神经网络](./Pytorch)
    * CNN
    * RNN
    * LSTM
    * DNN
    * autoEncoder
* [env config](env_configure.sh)
    * ubuntu 一键环境配置
    * 云服务器同样可用
    * [Linux environment configurations](https://github.com/AutuanLiu/Alne)

------
#### 说明信息

以上内容(不完整)都会采用 TensorFlow, Pytorch, sklearn 进行实现(进度可能有点慢, 因为我也是在学习的阶段), PyTorch 模型实现之后会
独立成库(目前主攻 PyTorch)

* `TensorFlow` 和 `Pytorch` 主要是构建深度学习框架，神经网络的，这里使用它们建立线性回归等只是说明它们可以实现这样的模型
* 对于机器学习模型应该尽可能采用 `sklearn` 进行构造，毕竟**术业有专攻**

------
#### 敬告自己

* 同一个神经网络有多种实现方式, 选一种喜欢的就好
* keras 相关代码完全使用 Tensorflow 作为后端, 因为 tensorflow 已经封装了 keras 所以，可以完全不用 安装 keras 而使用
* Pytorch 和 keras 都是 面向对象 的神经网络编程
* keras 相对于 tensorlayer 封装的更为抽象, tensorlayer 在封装时仍然可以和底层的 tensorflow 代码进行交互，相对比较透明
* 纯 tensorflow 相对还是有难度的, 但是可以结合 Tensorlayer 等进行学习, 可能会比较容易(网络结构比较清晰)
* 不过要实现自己的网络结构的话, pytorch 可能是最合适的
* 尽可能全面转向 **面向对象和面向函数** 编程思维
* 优先使用 pytorch 实现
-----

### 参考文献

1.  [Tensorflow Machine Learning Cookbook](https://github.com/nfmcclure/tensorflow_cookbook)
2.  [scikit-learn](http://sklearn.apachecn.org/cn/0.19.0/documentation.html)
3.  [TensorFlow-Tutorials](https://github.com/golbin/TensorFlow-Tutorials)
4.  [Simple PyTorch Tutorials Zero to ALL](https://github.com/hunkim/PyTorchZeroToAll)
5.  [TensorFlow Basic Tutorial Labs](https://github.com/hunkim/DeepLearningZeroToAll)
6.  [A set of examples around pytorch](https://github.com/pytorch/examples)
7.  [pytorch中文网](https://ptorch.com/news/17.html)
8.  [PyTorch](http://pytorch.org/)
9.  [Getting Started With TensorFlow](https://www.tensorflow.org/get_started/get_started)
10. [tensorflow-zh](https://github.com/jikexueyuanwiki/tensorflow-zh)
11. [machine learning in Python](https://github.com/scikit-learn/scikit-learn)
12. [skorch](https://github.com/dnouri/skorch)
13. [Deep-Learning-Boot-Camp](https://github.com/QuantScientist/Deep-Learning-Boot-Camp)
14. [pytorch welcome_tutorials](https://github.com/mila-udem/welcome_tutorials)
15. [PyTorch-Mini-Tutorials](https://github.com/vinhkhuc/PyTorch-Mini-Tutorials)
16. [practical-pytorch](https://github.com/spro/practical-pytorch)
17. [the-incredible-pytorch](https://github.com/ritchieng/the-incredible-pytorch)
18. [pytorch-tutorial](https://github.com/yunjey/pytorch-tutorial)
19. [imbalanced-learn documentation](http://contrib.scikit-learn.org/imbalanced-learn/stable/install.html)
20. [How to handle Imbalanced Classification Problems in machine learning?](https://www.analyticsvidhya.com/blog/2017/03/imbalanced-classification-problem/)
21. [Understanding Neural Networks Through Deep Visualization](http://yosinski.com/deepvis)
22. [deep-visualization-toolbox: DeepVis Toolbox](https://github.com/yosinski/deep-visualization-toolbox)
23. [Simplified implementations of deep learning related works](https://github.com/exacity/simplified-deeplearning)
24. [Deep Learning Book Chinese Translation](https://github.com/exacity/deeplearningbook-chinese)
25. [Essential Cheat Sheets for deep learning and machine learning researchers](https://github.com/kailashahirwar/cheatsheets-ai)
26. [Practical Business Python](http://pbpython.com/)
27. [Distill — Latest articles about machine learning](https://distill.pub/)
28. 原理可视化: [Setosa data visualization and visual explanations](http://setosa.io/#/)
29. 神经网络总结: [Neural networks and deep learning](http://neuralnetworksanddeeplearning.com/)

### 学习链接
1. [PyTorch 官方实例](https://github.com/pytorch/examples)
2. 斯坦福大学 CS231 课程[Stanford University CS231n: Convolutional Neural Networks for Visual Recognition](http://vision.stanford.edu/teaching/cs231n/)
3. 博客 [Sasank's Blog](http://chsasank.github.io/)
4. 在线书籍[《Python进阶》](http://docs.pythontab.com/interpy/)
5. Fast.ai 在线学习网站(推荐)[fast.ai · Making neural nets uncool again](http://www.fast.ai/)
6. [Python魔法方法指南](http://pyzh.readthedocs.io/en/latest/python-magic-methods-guide.html)
7. [Object serialization in Python](https://medium.com/the-python-corner/object-serialization-in-python-1d49c6ad071)

### 参考书籍

1.  《TensorFlow 机器学习实战指南》
2.  《深度学习》(花书)
3.  《机器学习 周志华》(西瓜书)
4.  《The Element of Statistical Learning》
5.  《Hands On Machine Learning with Scikit Learn and TensorFlow》
6.  《机器学习实战》
7.  《Tensorflow 实战Google深度学习框架》
8.  《A guide to convolution arithmetic for deep》论文
9.  《An Introduction to Statistical Learning》
10. 《Convex Optimization》
11. 《Statistical Analysis with Missing Data-Wiley-Interscience (2002)》
12. 《TensorFlow 官方文档中文版 - v1.2》极客学院
13. 《TensorFlow技术解析与实战.李嘉璇.2017》
14. 《Reinforcement Learning: An Introduction》
15. 《Pattern Recognition And Machine Learning》经典
16. 《统计学习方法 李航》
17. 《Machine Learning  Kevin P·Murph》
18. 《Bayesian Reasoning and Machine Learning David Barber 》
19. 《深度学习：一起玩转TensorLayer》


P.S. 这也是逼迫自己写代码，实战的一种手段吧！

* 如果你觉得这个 repository 有用，并且希望丰富这个repository的内容，欢迎 PR

## 目录结构
* 参见(待更新) [dir_tree.txt](dir_tree.txt)

```bash
$ tree -h -I 'Mnist|fashionMnist|__pycache__' > dir_tree.txt
```



[1]:https://travis-ci.org/AutuanLiu/MDeepLearn.svg?branch=master
[2]:https://travis-ci.org/AutuanLiu/MDeepLearn
[3]:https://autuanliu.github.io/
[4]:https://github.com/AutuanLiu/ML-Docker-Env
[5]:https://github.com/AutuanLiu/Machine-Learning-on-docker/archive/master.zip
