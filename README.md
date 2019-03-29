# Built-up-Areas-Mapping-v2.0
We uploaded the code based on artificial surface mapping v1.0. We renamed the artificial surface to built-up areas. This uploaded code can process batch images. 
## Corresponding Author  
Chang Liu, Kang Yang  
Changliu811@gmail.com, kangyang@nju.edu.cn   
Phone: (+86)17302560154  
School of Geography and Ocean Science, Nanjing University  
## Python Environment  
Arcpy(10.4), Anaconda(2.7, download in https://www.anaconda.com/download/).
## Python Pip  
Arcpy- os, math, shutil, sys.  
Anaconda- os, shutil, sys, numpy(1.15.1), skimage(0.14.0), gdal(2.2.2).  
## Attention  
1. This code has 9 steps. All the steps run with Arcpy environment except the 6th step. The 6th step runs with anaconda environment.  
2. Put the Landsat-8 imagery into the ‘predata’ file and click run step by step.  
3. In the 7th step, you need to get the classification thresholds by using the Arcmap (10.4). Change the classification intervals in the code manually. Set the nighttime data DN=0.4 or lower DN as the threshold to get the non-built-up areas training samples. Put all the batch thresholds in excel. Pay attention to the excel format. Excel example is below.   
![1](https://user-images.githubusercontent.com/46549560/55215175-d1e89080-5233-11e9-98d5-aec5d9828409.png)
![2](https://user-images.githubusercontent.com/46549560/55215174-d14ffa00-5233-11e9-8ca6-1ba6608621d0.jpg)
4. Before running the 9th step, you need to create the training features manually in Arcmap, they can not create in python automatically.
Add the ‘_nonbuilt_up_trainsample_dissolve.shp’ and ‘built_up_trainsample_dissolve.shp’ respectively into the training sample manager. Then save these feature classes as ‘merge_trainsample.shp’ in the ‘trainsamples’ file.  
![3](https://user-images.githubusercontent.com/46549560/55215172-d14ffa00-5233-11e9-93fd-39b21f1bb8a9.jpg)
![4](https://user-images.githubusercontent.com/46549560/55215169-d0b76380-5233-11e9-89fe-82cec7b3b671.jpg)
5. In the ‘image_result’ file, you will get the final mapping result of built-up areas. ‘result_bustack_TOA_LC08_L1TP_150038_20170605_20170616_01_T1’ .  
![5](https://user-images.githubusercontent.com/46549560/55215168-d01ecd00-5233-11e9-951e-c606ff9aa19d.jpg)
