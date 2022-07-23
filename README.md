# IBM-AI-Applied-Deep-Learning-project
In this project, the aim will be to predict the classification of images of cracked concrete blocks using deep learning model that uses ResNet50.
Some of the key processes carried out are as follows:
1. Loading the data
2. Preparing the data 
3. Pre-trained models
-------------------------------------------------------------------------------------------------------------------------

**Introduction**

Crack detection has vital importance for structural health monitoring and inspection. In this series of labs, you learn everything you need to efficiently build a classifier using a pre-trained model that would detect cracks in images of concrete. For problem formulation, we will denote images of cracked concrete as the positive class and images of concrete with no cracks as the negative class.

-------------------------------------------------------------------------------------------------------------------------

**1. Loading the data** [click here](https://github.com/nbjeelan/IBM-AI-Applied-Deep-Learning-project/blob/master/Module_1%20_%20Data%20Collection/1.1%20DL0321EN-1-1-Loading-Data-py-v1.0.ipynb)
- Data collection using the url [here](https://s3-api.us-geo.objectstorage.softlayer.net/cf-courses-data/CognitiveClass/DL0321EN/data/images/concrete_crack_images_for_classification.zip)
  
  Libraries used: os, matplotlib, numpy, PIL
  - The data was collected and unzipped using wget command on google colab
  - Used the os library to correctly identify the directory that contained the images
  - Visualized the positive and negative class of images using the matplotlib library
  
-------------------------------------------------------------------------------------------------------------------------

**2. Data preparation** [click here](https://github.com/nbjeelan/IBM-AI-Applied-Deep-Learning-project/blob/master/Module_2%20_%20Data%20preparation/1.2%20DL0321EN-2-1-Data-Preparation-py-v1.0.ipynb)
- Image data generation
  
  Libraries used: os, numpy, matplotlib, keras
  - Used Imagedatagenerator of keras library to create an instance
  - Created the standard and custome imagedatagenerator
  - Visualized the batches of images generated using the matplotlib library
  
-------------------------------------------------------------------------------------------------------------------------

**3. Pre-trained models** [click here](https://github.com/nbjeelan/IBM-AI-Applied-Deep-Learning-project/blob/master/Module_3%20_%20Pretrained%20Models/1.3%20DL0321EN-3-1-Pretrained-Models-py-v1.0.ipynb)
- Building and comparing models like ResNet50
  
  Libraries used: tensorflow, keras, sequential, dense, resnet50
  - Built a model using tensorflow library and used augmented pretrained resnet50
  - Classfication of 40000 images was carried out for training, validation and test data
  - Unlike a conventional deep learning training were data is not streamed from a directory, with an ImageDataGenerator where data is augmented in batches, we use the fit_generator method.
  - Compiled the data using adam optimizer that gives metrics of accuracy and loss
  
-------------------------------------------------------------------------------------------------------------------------
**Conclusion**

The accuracy scores and loss values obtained are as follow
  
  1. Test_Accuracy : 98.70 | Validation Accuracy : 99.86
  2.Loss : 0.0056 | Validation loss : 0.0046
