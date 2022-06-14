# autoencoder_for_background_extraction using Tensorflow and Keras
Background extraction is an import step for background subtraction. This small project shows how to model background using convolutional autoencoder. The principle is that we treat the foreground of images as noises and use autoencoder to rebuild the missing informations.  


## Autoencoder in Keras

Create some folders at the same level as the file "Autoencoder.py" before running it  
--- train_image: this folder for the training images. Here 200 images were used for training autoencoder. The dataset can be found in changedetection.net [4].  
--- test_image: this folder for the testing images   
--- save_img: save the predicted backgrounds  
--- model_save: save the model of autoencoder  
  

## Autoencoder in Tensorflow
  
The codes base on the project[1] which provides pure tensorflow code to build a convolutional autoencoder. Here the ssim index [2] is used as the loss function. The tensorflow code of ssim can be found in [3]. 

At first you should creat some folders at the same level as the file "convolutional_autoencoder.py":  
--- train_image: this folder for the training images. Here 200 images were used for training autoencoder. The dataset can be found in changedetection.net [4].  
--- test_image: this folder for the testing images    
--- test_gray: save the gray-scale images of testing image  
--- saver: save the model of autoencoder  
--- background: save the predicted backgrounds  

The following images show the result of AE in Tensorflow. The first image is the input image.   
![Original_Image](https://github.com/klickmal/autoencoder_for_background_extraction/blob/master/result/original.jpg)   
The second image is the predicted background.  
![Background_Image](https://github.com/klickmal/autoencoder_for_background_extraction/blob/master/result/bg.jpg)    
Reference:  
[1] https://github.com/Seratna/TensorFlow-Convolutional-AutoEncoder  
[2] Zhou Wang et al. Image Quality Assessment: From Error Visibility to Structural Similarity, IEEE, Transacctions on Image Processing, 2014  
[3] https://stackoverflow.com/questions/39051451/ssim-ms-ssim-for-tensorflow  
[4] http://changedetection.net/
