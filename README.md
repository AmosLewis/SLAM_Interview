# SLAM_Interview
This is a private repository for SLAM job interview. The page is maintained by [Youjie Xia](https://github.com/YoujieXia), [Chi Liu](https://github.com/AmosLewis), [jiangshan Tian](https://github.com/tianjiangshan),[Zhengyu Zhou](https://github.com/z78406) and [Jimuyang Zhang](https://github.com/Jimuyangz). And this repo would keep constantly updated. 

Feel free to contact me chil1@alumni.cmu.edu

[chi] 前四类问题为主要专业知识 SLAM/CV/DL/C++，Question 多用中文描述，方便快速查找。后面的还可以补充点其他乱七八糟的问题。

[chi] answer关键词都用英文，方便背诵，解释中英结合方便快速理解，必要的话直接插图。主要给[keypoint]和 (口语化解释)。若有详细解释的link也可给出，答案可以只给出自己现在的理解，发现错了再改。相关理解性的东西用中文便于快速理解。

[chi] c++ 的话有code可以直接贴code 到另外一个C++文件夹下，然后给个link。

[chi] Book 里面我加了些C++的资料，我看着还蛮简明的， 查阅起来也蛮方便。不用全看，我给了使用方法了。

[chi] 这一页主要放我们被面过的问题，另外4个分开的readme 则具体整理复习时候具体的问题，还有以上面QA的格式给出，一个人给出答案，其他人看着有问题就修改，也可以在那个问题答案后面加上名字和comment。

# [1]. SLAM
##### Q1 (Calibration 步骤)
[Matlab TOOLBOX Calibration step](https://www.mathworks.com/help/vision/ug/single-camera-calibrator-app.html?w.mathworks.com)

- [MATLAB Toolstrip] On the Apps tab, in the Image Processing and Computer Vision section, click the Camera Calibrator icon.]

    - [Prepare checkboard]

        - [Print the Checkerboard Pattern] 打印标定板，不能用正方形
        
        - [Attach the checkerboard printout to a Flat Surface]
        
        - [Measure one side of the checkerboard square.]
    - [Prepare Camrea]
    
         - [Focus] Keep the pattern in focus 不能用自动对焦
    - [Capture Image]
    
         - [10-20 images]

         - [Different Orientation]
        
         - [Less than 45 degree]  checkboard的
        
         - [20%] checkboard至少占图片的20%
    
    - [Add Images]
    
         - [Add Images from File] On the Calibration tab, in the File section, click Add images, and then select From file. ，也可以 Acquire Live Images
     
    - [Analyze images]
    
         - [Specify size of the checkerboard square]
        
    - [View images & Detect point]
    
         - matlab 可以显示图片，自动检测出角点并现实绿色圆圈， 黄色方框是远点，还有x y轴坐标，角点检测不满意还可以用 zoom control调整到满意为止。
        
    - [Calibrate]

         - 满意了就点Calibrate button, 同时算出intrinsic parameters, the extrinsic parameters, and the distortion coefficients. 默认用  nonlinear least-squares minimization (Levenberg–Marquardt algorithm). 

# [2]. Computer Vision
##### Q1 (SURF,SIFT，ORB 比较优劣)
###### Q1 (Answer)
# [3]. Deep Learning
##### Q1 (YOLO123 不同)
###### Q1 (Answer)
##### Q2 (RCNN FastRCNN FasterRCNN 不同)
###### Q2 (Answer)
##### Q3 (BCE loss  公式)
###### Q3 (Answer)
##### Q4 (Activation function 的功能)
###### Q4 (Answer)
##### Q5 (Sigmoid and LeakRLU 区别)
###### Q4 (Answer)
# [4]. C++
##### Q1 (static_cast 和 dynamic_cast 区别)
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

		- [3] [***Polymorphic Argument Type***] (多态 polymorphic means base 必须有 vitual function，这才是判断要不要用dynamic_cast的核心原因就看 base中有没有 vitual function, 参见Q3 )

		- [4] [***Only Reference & Pointer***] (只能被用于 class 的reference and pointer)

##### Q2 (deep copy 和 shallow copy 区别)
###### Q2 (Answer)
##### Q3 (visual function 的作用)
base 有些功能对不同的derived实现是不同的，所以base自己先用vitual function定个接口的规范，derived去实现不同的function，然后base类型的object 还可以调用derive的 vitual function。derived -> base 的时候就用dynamic_cast.
# [5]. 其他乱七八糟的问题和坑
# [4]. 个人project的特定问题
##### Q1 (Question)(WHO)
###### Q1 (Answer)
