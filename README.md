# Convolutional Neural Networks for Image Classification
Developing Conventional Neural Networks (CNN) capable of classifying clothing items. 

# Balancing the dataset
The dataset of 40,000 images is split into 3 sets: training, validation and testing using a 70%, 15%, 15% split.
The image counts and % for each category are as follows:
Casual: 34,414 rows (93.4%).
Formal: 2,359 rows (6.4%).
Smart Casual: 67 rows (0.2%).
This dataset is heavily imbalanced with the Casual images overwhelmingly dominating the underrepresented Formal and Smart Casual images, resulting in the simple CNN being prone to overfitting.

Data augmentation is used to solve this by increasing the number of images from the underrepresented classes. The techniques used in data augmentation include rotating the image, shearing to distort the image, flipping the image horizontally and filling the generated pixels during transformation.

![image](https://github.com/user-attachments/assets/37f11c10-07c6-47ee-9b32-089efe915ae0)

Balancing the dataset resulted in equal numbers from each class which prevents the model from exclusively training on casual clothing and failing to classify underrepresented clothing types.

# Architecture
First model:
CNN with 2 Conv2D layers and ReLU activation followed by MaxPooling2d. A Flatten layer followed, feeding into 2 Dense layers and used softmax for the final activation. This model achieved modest accuracy but struggled with balancing the dataset as the Formal and Smart Casual images were heavily underrepresented.

Improved model:
Implemented Transfer Learning into the model and added custom dense layers which helps the model to avoid underfitting. ResNet50 from Microsoft is used for Transfer Learning, which is highly efficient in image classification. Data augmentation techniques were used to balance the dataset.

# Visualisation
GRAD-CAM produces a heatmap to highlight what the model identifies as important features, which visualises the features identified by the models and helps with optimising the model’s parameters to improve accuracy. 
![image](https://github.com/user-attachments/assets/711c2401-c0f8-4578-b01a-daf164352d1e)

Dataset Source
Param Aggarwal. (2019). Fashion Product Images Dataset. Kaggle. https://doi.org/10.34740/KAGGLE/DS/139630
