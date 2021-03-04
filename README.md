## Realtime object detector with Deep Learning

The installation of the Darknet network is usually complex and entails several excesses if it is not carried out in the correct way in a complex or well structured development environment it will not work correctly (or will not even work). Initially it was developed for Linux, therefore its adaptation may vary with respect to the distribution of the operating system.

Below I present several learning paths which I suggest be evaluated. Personally, I carried out the tests with all of them, but the most successful is the first option, as it is native in Windows, as well as the fact that its frameworks are also of "original" distribution. It is essential to follow the order in which each step is carried out.

Compiling with:
openCv 3.3.
Python 3.6
Anaconda 3

### Some Tutoriales to install
- https://medium.com/@acg.95.mx/yolo-compilar-darknet-desde-windows-subsystem-for-linux-563e72d34974 
- https://kezunlin.me/post/a5c428f1/
- https://medium.com/analytics-vidhya/installing-darknet-on-windows-462d84840e5a 
- https://medium.com/@oxanderv/instalando-y-entrenando-yolo-en-windows10-con-darkflow-6181166ee2ab 
- https://www.youtube.com/watch?v=7PX_H00V6RA&t=97s 
- https://medium.com/@oxanderv/instalando-y-entrenando-yolo-en-windows10-con-darkflow-6181166ee2ab 
- https://mc.ai/installing-darknet-on-windows/ 


## Necessary dependencies

- Python 3.6

- CMake >= 3.8 for modern CUDA support: https://cmake.org/download/

- CUDA 10.0: https://developer.nvidia.com/cuda-toolkit-archive

- CuDNN: https://developer.nvidia.com/rdp/cudnn-download 

  - Cuenta: aaandrades
  
  - Password: (You know)
  
- Git project of Darknet: https://github.com/AlexeyAB/darknet

- Opencv 3.4.4: Seguirlo completamente, es elaborado por el CEO de OpenCV: https://www.learnopencv.com/install-opencv-3-4-4-on-windows/
  - Scripts del Tutorial: https://github.com/spmallick/learnopencv/tree/master/InstallScripts/Windows-3

## Train
Para el entrenamiento del modelo se puede seguir el siguiente tutorial: http://emaraic.com/blog/yolov3-custom-object-detector, realmente es el mismo proceso en todos los tutoriales encontrados, cambia es el programa de etiquetado de las imágenes.

## Issues
- If there's problem with Dlib use:

  ```
    pip install https://pypi.python.org/packages/da/06/bd3e241c4eb0a662914b3b4875fc52dd176a9db0d4a2c915ac2ad8800e9e/dlib-19.7.0-cp36-cp36m-win_amd64.whl#md5=b7330a5b2d46420343fbed5df69e6a3f
  ```

- If error: (-215:Assertion failed) separator_index < line.size() in function 'ReadDarknetFromCfgStream' 
comment the lines 5, 6 y 7 and run the script.

## Steps to training
 - You have to take the dataset and label it with LabelIMG: It can be obtained from here: https://github.com/tzutalin/labelImg, modify the file inside of the folder Data/, and the .txt file with the class for labeling.
 - Then, you will save the data inside a folder called 'datasets'.
 - Create a folder called Custom with:
    1) Object.names: (The file with class created)
    2) test.txt y train.txt are created by the script to particionate the information between train and test.
    3) Trainer.data: include the information of classes, directory and backup.
    4) Config file (.cfg) modify just the line of the class [convolutional] before of [Yolo], it says filters=255 for (5+n)*3, where n it's the amount of classes, the same  n add in the line Classes before [yolo]
 - When you finish, just run the Red!.

### Demostration

https://youtu.be/3sgcgpfd4e4 (I'm the boy of the Helmet)

If you want to contribute to improve the app, please create your PR and write me :alien: . After it, sit down and take a beer, you deserve it! :beers:
*This project is for academic purposes only, all right reserved. Andrés Andrade 2021 :copyright::registered:*

