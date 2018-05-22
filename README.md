# SLAM_Interview
This is a private repository for SLAM job interview. The page is maintained by [Youjie Xia](https://github.com/YoujieXia), [Chi Liu](https://github.com/AmosLewis), [Jimuyang Zhang](https://github.com/Jimuyangz) and [Zhengyu Zhou](https://github.com/z78406). And this repo would keep constantly updated. 

[chi] 前四类问题为主要专业知识 SLAM/CV/DL/C++，Question 多用中文描述，方便快速查找。后面的还可以补充点其他乱七八糟的问题。

[chi] answer多用英文，方便背诵，中英结合，关键词都用英文，必要的话直接插图。主要给[keypoint]和 (口语化解释)。若有详细解释的link也可给出，答案可以只给出自己现在的理解，发现错了可以再改。相关理解性可以用中文便于快速理解。

[chi] c++ 的话有code可以直接贴code 到另外一个C++文件夹下，然后给个link。

[chi] Book 里面我加了些C++的资料，我看着还蛮简明的， 查阅起来也蛮方便。不用全看，我给了使用方法了。

[chi] 这一页主要放我们被面过的问题，另外4个分开的readme 则具体整理复习时候具体的问题，还有以上面QA的格式给出，一个人给出答案，其他人看着有问题就修改，也可以在那个问题答案后面加上名字和comment。

# [1]. SLAM
##### Q1 (Calibration 步骤)(宁面试的一家公司问的)
[Matlab TOOLBOX Calibration step](https://www.mathworks.com/help/vision/ug/single-camera-calibrator-app.html?w.mathworks.com)
# [2]. Computer Vision
##### Q1 (Question)(Company)
###### Q1 (Answer)
# [3]. Deep Learning
##### Q1 (Question)(Company)
###### Q1 (Answer)
# [4]. C++
##### Q1 (static_cast 和 dynamic_cast 区别)(杨面试的一家公司问的)
[Stackflow Link：regular-cast-vs-static-cast-vs-dynamic-cast](https://stackoverflow.com/questions/28002/regular-cast-vs-static-cast-vs-dynamic-cast) C++基础或者进阶的书里也有说明
- Same point: 

    - [1] [***Upcast***]("Up-cast" (derive->base class) is always valid )

    - [2] [***None Relevent Class***]( Report error during **compile** if cast two unrelevent class,如 char->int  在C里面就是可以的，C++里面就必须用, reinterpret_cast, 我们平时用的基本都是C风格的强制转换，就在变量前面加一个（要强转的类型）什么的。 )

- Different point: 

    - **static_cast** : 

        - [1] [***No runtime checks***] ( Used if you know that you refer to an object of a specific type, and thus a check would be unnecessary.)
  
        - [2] [***Downcast***]( Even cannot downcast, the static_cast won't give you error reprort during **compile**)
    
        - [3] [***No Polymorphic Argument Type***]( Class base don't need to have vitual function )
    
        - [4] [***Numerical Cast***]( Not only reference & pointer, but also numerical cast. )

    - **dynamic_cast** :

        - [1] [***Run Time Checks***] ( Used when you don't know what the dynamic type of the object. Returns a null pointer if cast fail.)

       - [2] [***No Downcast***]( Cannot be used base->derived class)

       - [3] [***Polymorphic Argument Type***]( 多态 polymorphic means base must have vitual function )

       - [4] [***Only Reference & Pointer***] ( 只能被用于 class 的reference and pointer )

##### Q2 (deep copy 和 shallow copy 区别)(夏面试的一家公司问的)
###### Q2 (Answer)
##### Q3 (visual function 的作用)(夏面试的一家公司问的)
###### Q3 (Answer)
# [5]. 其他乱七八糟的问题和坑
# [4]. 个人project的特定问题
##### Q1 (Question)(WHO)
###### Q1 (Answer)
