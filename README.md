
# Title of the Project: Underwater Sea-grass Classification Using Deep Learning Techniques

## Prerequisties:
Install the following python libraries
- Python 3.10
- Numpy
- Pandas
- matplotlib
- Tensorflow 2
> You can use google colab also to avoid dependency issues

## Description: 

- Identification of seagrass with bare eyes is really difficult, hence, this work proposed a deep learning
model which incorporates transfer learning method- Inception V3.
- **Methodology**
 ![image](https://user-images.githubusercontent.com/72349386/207402795-8f65cc9a-b5e9-452d-96e6-ba8bc9e2b9ad.png)
 
Here, we use a pretrained CNN classifier – Inception V3.
Step by step process involved in this implementation:
1. Dataset Preperation- Extract images frame by frame, image resizing, define train & test data.
2. Data Preprocessing- image rescaling to (0, 1), no changes of image properties.
3. Model building- Initialize inception v3, Total – 42 layers, Activation function- softmax, Cost
function- categorical entropy .
4. Image Augmentation- Image data generator- change in image properties.
5. Model tuning - freeze top 28 layers, optimizer- stochastic gradiant descent & retrain agian.
6. Evaluation – Train & test data accuracy.

– The 4 classes dataset is collected from CSIRO, Australia database which consists of training data: 80% - 42848
images and test data: 20% - 8566 images. 
![image](https://user-images.githubusercontent.com/72349386/207402394-ddf442c2-13c3-4f2c-8c7a-ee0b016bfd78.png)

- Firstly, implemented Inception V3 model which has 42 layers.
![image](https://user-images.githubusercontent.com/72349386/207403488-a65a5e97-337d-4eba-9d3c-3fc9d31862b0.png)
![image](https://user-images.githubusercontent.com/72349386/207403929-9ed583ef-20f9-4433-9dc7-20f9f578734e.png)


 

– Respectively, before augmentation and after augmentation – the inception V3 model gives 98.2% ac-
curacy and 97.4% accuracy.
![image](https://user-images.githubusercontent.com/72349386/207403670-01c0591c-2720-431e-a676-1f404dedfd5b.png)
![image](https://user-images.githubusercontent.com/72349386/207403842-503661bc-63ca-4d93-ae09-cc2baf629604.png)
![image](https://user-images.githubusercontent.com/72349386/207404020-4557cfcf-e707-4351-ae46-703a95ebe607.png)
![image](https://user-images.githubusercontent.com/72349386/207404085-025a1c4a-6de2-4814-afa7-3e6d04069c75.png)

- Classification Report
![image](https://user-images.githubusercontent.com/72349386/207406400-073dee10-1448-432a-bc59-75c50e091b3b.png)

- Secondly, implemented efficientnet B7 which has 813 layers (accuracy increases by increasing the no.
of epochs).
- Finally, implemented convnet 5 layers and at final layer added ’l2’ regularizer. Activation
function: ’softmax’ for all 3 models.
- the efficientnet B7 model gives 36% accuracy and 45% accuarcy
-  And the covnet gives 92.7% accuracy and 80% accuracy



## Conclusion: 
This project has implemented a deep learning method for automated detection and clas-
sification of seagrass species. The approach focused on classification of seagrass into three major
morphological super-classes plus background and presented a novel method of training a multi-species
seagrass classifier using a dataset of single species images. The four-class approach achieved an overall
accuracy of 96.2 percent, which was then improved to 98.4 percent by tuning the model and retraining
the model using augmented images. The approach could be extended by separating morphological
super-classes into the individual seagrass species and would benefit from increased training data and
robust testing in the field. Furthermore, the approach presented could be used as a basis for estima-
tions of species-specific percentage cover and density.

## Reference:
- Raine, S., Marchant, R., Moghadam, P., Maire, F., Kettle, B. and Kusy, B., 2020, November. Multi-species seagrass detection and classification from underwater images. In 2020 Digital Image Computing: Techniques and Applications (DICTA) (pp. 1-8). IEEE.


