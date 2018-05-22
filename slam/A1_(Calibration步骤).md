##### A1 (Calibration 步骤)
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
