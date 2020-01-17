# TUTORIAL PARA INSTALACIÓN DARKNET - FRAMEWORK DE RED NEURONAL PARA EJECTURAR YOLO V3. (WINDOWS 10) 
### Andrés Alexander Andrade - Machine Learning Engineer, Cadastral and Geomatic Engineer and Master in Geographic Information Systems with formation in data science and processing and analising spatial data. (Bog, Colombia).

La instalación de la red Darknet usualmente es compleja y conlleva varios desmanes si no es realizada de la forma correcta en un ambiente de desarrollo complejo o bien estructurado no funcionará correctamente (o ni siquiera funcionará). Inicialmente fue desarrollada para Linux, por lo tanto su adaptación puede variar respecto a la distribución del sistema operativo.

Existe una red adaptada para Windows que se puede acceder directamente desde acá: https://github.com/AlexeyAB/darknet

A continuación presento varias rutas de aprendizaje las cuales sugiero sean evaluadas. Personalmente realicé los test con todas pero las más acertiva es la primera opción, por ser de tipo nativo en Windows además de que sus frameworks son también de distribución "original". Indispensable seguir el orden de la realización de cada paso.

Compiling with:
openCv 3.3.
Python 3.6
Anaconda 3

### Ruta 1
https://medium.com/@acg.95.mx/yolo-compilar-darknet-desde-windows-subsystem-for-linux-563e72d34974 - Instalar en windows a traves de un Gestor de Ubuntu 18.04 LTS. (Nivel de dificultad: Bajo).

### Ruta 2
https://kezunlin.me/post/a5c428f1/ - Instalar en Windows (Nivel de dificultad: Alto).

### Ruta 3
https://medium.com/analytics-vidhya/installing-darknet-on-windows-462d84840e5a - Instalar Windows con una muy buena explicación. (Nivel de dificultad: Alto).

### Ruta 4
https://medium.com/@oxanderv/instalando-y-entrenando-yolo-en-windows10-con-darkflow-6181166ee2ab - Instalación más sencilla. (Nivel de dificultad: Medio).

### Ruta 5
https://www.youtube.com/watch?v=7PX_H00V6RA&t=97s - Instalación a traves de paquetes externos que simulan comandos Linux. (Nivel de dificultad: Bajo).

### Ruta 6
https://medium.com/@oxanderv/instalando-y-entrenando-yolo-en-windows10-con-darkflow-6181166ee2ab - Tutorial bastante completo. (Nivel de dificultad: Alto).

### Ruta 7
https://mc.ai/installing-darknet-on-windows/ - Tutorial bastante complejo pero muy completo y directo al punto. (Nivel de dificultad: Alto).



## Instalaciones Necesarias

Deben ser llevadas a cabo en este orden específco

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
- Si hay problema con Dlib ejecutar el siguiente comando:

  ```
    pip install https://pypi.python.org/packages/da/06/bd3e241c4eb0a662914b3b4875fc52dd176a9db0d4a2c915ac2ad8800e9e/dlib-19.7.0-cp36-cp36m-win_amd64.whl#md5=b7330a5b2d46420343fbed5df69e6a3f
  ```

- Si aparece error: (-215:Assertion failed) separator_index < line.size() in function 'ReadDarknetFromCfgStream' 
comentar las lineas 5, 6 y 7 y recompilar el script.

- Si el modelo falla en la lectura de los labels, copiar los labels en la misma carpeta que las imágenes: en la carpeta data/images.


