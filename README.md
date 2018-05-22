# SLAM_Interview
This is a private repository for SLAM job interview. The page is maintained by [Youjie Xia](https://github.com/YoujieXia), [Chi Liu](https://github.com/AmosLewis), [jiangshan Tian](https://github.com/tianjiangshan),[Zhengyu Zhou](https://github.com/z78406) and [Jimuyang Zhang](https://github.com/Jimuyangz). And this repo would keep constantly updated. 

Feel free to contact me chil1@alumni.cmu.edu

[chi] 前四类问题为主要专业知识 SLAM/CV/DL/C++，Question 多用中文描述，方便快速查找。后面的还可以补充点其他乱七八糟的问题。

[chi] answer关键词都用英文，方便背诵，解释中英结合方便快速理解，必要的话直接插图。主要给[keypoint]和 (口语化解释)。若有详细解释的link也可给出，答案可以只给出自己现在的理解，发现错了再改。相关理解性的东西用中文便于快速理解。

[chi] c++ 的话有code可以直接贴code 到另外一个C++文件夹下，然后给个link。

[chi] Book 里面我加了些C++的资料，我看着还蛮简明的， 查阅起来也蛮方便。不用全看，我给了使用方法了。

[chi] 这一页主要放我们被面过的问题，另外4个分开的readme 则具体整理复习时候具体的问题，还有以上面QA的格式给出，一个人给出答案，其他人看着有问题就修改，也可以在那个问题答案后面加上名字和comment。

# [1]. SLAM
##### Q1_(Calibration步骤)
[A1_(Calibration步骤).md](slam/A1_(Calibration步骤).md)


# [2]. Computer Vision
##### Q1_(SURF_SIFT_ORB比较优劣)
###### Q1_(Answer)
# [3]. Deep Learning
##### Q1_(YOLO1_2_3不同)
###### Q1_(Answer)
##### Q2 (RCNN_FastRCNN_FasterRCNN不同)
###### Q2_(Answer)
##### Q3 (BCE loss  公式)
###### Q3_(Answer)
##### Q4_(Activation_function的功能)
###### Q4_(Answer)
##### Q5_(Sigmoid_&_LeakRLU区别)
###### Q4_(Answer)
# [4]. C++
##### Q1_(static_cast和dynamic_cast区别)
###### [A1_static_cast和dynamic_cast 区别.md](cpp/A1_static_cast和dynamic_cast区别.md)


##### Q2_(deep_copy和shallow_copy区别)
###### Q2_(Answer)
##### Q3_(visual_function的作用)
base 有些功能对不同的derived实现是不同的，所以base自己先用vitual function定个接口的规范，derived去实现不同的function，然后base类型的object 还可以调用derive的 vitual function。 只要有 vitual function,那么derived -> base 转换的时候就用dynamic_cast.
# [5]. 其他乱七八糟的问题和坑
# [4]. 个人project的特定问题
##### Q1 (Question)(WHO)
###### Q1 (Answer)
