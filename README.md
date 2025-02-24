# Arabic-Sing-Language

Arabic Sign Language (ArSL) recognition using state-of-the-art artificial intelligence techniques. automatic sign language recognition is required to facilitate and better understand interactions with such people. However, one of the main challenges in this field is the real-time sign recognition. That is why, deep learning-based object detection models can be used to improve recognition performance (in terms of time and accuracy). We constructed an image dataset of 32 Arabic signs alphabets 10 numbers and 19 words with different sizes of hands, lighting conditions, backgrounds, and with/without accessories. We then trained and tested different variants of YOLOv8 on the constructed dataset. The conducted experiments on our ArSL real-time recognition system show that the adapted YOLOv8 is the most effective. The primary objective is to develop a robust system that can effectively detect and translate ArSL alphabets, numbers, and words in real time. To achieve this goal.

# Alphabet Dataset (Arabic Sign Language Dataset 2022)

The alphabet dataset primarily draws from the "Arabic Sign Language Dataset 2022" available on Kaggle (ArSL alphabet signs 2022)  This dataset provides a foundation of ArSL alphabet signs captured under different environmental conditions and by multiple signers. The dataset's contributors took care to ensure that images represented a variety of lighting conditions, signers, and sign variations.

# Numbers Dataset

For the number dataset, 1135 images were collected in diverse environments by the four dedicated volunteers. These images represent Arabic sign language numbers from 0 to 9, ensuring a wide range of conditions and sign variations. To augment this dataset, the Rotoflow platform (https://roboflow.com/) was employed for preprocessing and data augmentation.

# Words Dataset

The words dataset comprises 1345 images captured in different locations and lighting conditions by the same four volunteers. These images depict a specific set of ArSL words, including "identity conformity," "fixed," "ready," "certificate," "plate," "true," "aim at," "necessary," "injury," "accident," "government," "bandage," "student," "emergency," "no," "negative outcome," "positive outcome," "slow," "support," and "reparent the emergence cases." These words were chosen to represent a broad range of concepts and scenarios commonly encountered in ArSL communication and after the Data Augmentation with Rotoflow the number of the images is 2116. 

# Dataset Annotation

Data annotation is an essential step in object detection tasks. Each image in the dataset was labeled with its corresponding sign of the Arabic alphabet and numbers and words. Bounding box annotation was also performed to define the location of the target object. So, the bounding box around the hand gesture can be determined by the coordinates of the upper left corner (x, y), and specified by its width and height. All the labels were saved in your files.

# Dataset Annotation

Data annotation is an essential step in object detection tasks. Each image in the dataset was labeled with its corresponding sign of the Arabic alphabet and numbers and words. Bounding box annotation was also performed to define the location of the target object. So, the bounding box around the hand gesture can be determined by the coordinates of the upper left corner (x, y), and specified by its width and height. All the labels were saved in the files.

# Data Sampling

Training and testing YOLOv8 involve image sampling. It randomly splinted the image dataset into training, validation, and test sets containing 80%,10%, and 10% of the sign data, respectively. It's selected. these partition values according to some conducted tests.

All the signs in the dataset were selected based on the Unified Arabic Sign Language Dictionary, ensuring conformity with standardized ArSL representations.

# Model Selection - YOLOv8

For object detection and recognition in the ArSL domain, the YOLOv8 (You Only Look Once version 8) algorithm has been chosen and it’s the latest, state-of-the-art, model in the YOLO series, up to this date. Currently, it has five versions, which all are models aimed at 640-pixel datasets. It was designed to boost performance and accuracy.
YOLOv8 (https://github.com/ultralytics/ultralytics)
The choice of YOLOv8 is based on its ability to simultaneously detect and classify multiple objects within a single frame. Adaptations will be made to the YOLOv8 model to accommodate the unique characteristics of ArSL gestures, such as their distinct shapes and movements., currently it has five versions, which all are models aimed at 640 pixels datasets. It was designed to boost performance and accuracy.
Each new version has a boosted performance (inference speed and mAP score) compared to its predecessor. The YOLO algorithm applies a single neural network to the input image. The latter is divided into SxS grids. Each grid cell detects the object defined by its center.The output of the algorithm is a vector computed for each grid cell (i.e. object), containing the predicted bounding box (width, height), the confidence score of having an object, and the number of classes.

![YoloV8](https://raw.githubusercontent.com/mustafa-raads/Arabic-Sign-Language/main/YoloV8.jpg)





