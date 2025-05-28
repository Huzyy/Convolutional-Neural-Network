# Convolutional-Neural-Network
Developing Conventional Neural Networks (CNN) capable of classifying clothing items into 3 categories: Casual, Formal and Smart Casual. 

# Balancing the dataset
Data preprocessing included ensuring the images were correctly labelled based on the information within the dataset, split into 3 sets: training, validation and testing using a 70%, 15%, 15% split.
The row counts and ratios for each category are as follows:
Casual: 34,414 rows (93.4%).
Formal: 2,359 rows (6.4%).
Smart Casual: 67 rows (0.2%).
The datasets are heavily imbalanced with the Casual images overwhelmingly dominating the underrepresented Formal and Smart Casual images, resulting in the simple CNN being prone to overfitting.

Data augmentation is used to improve the number of images from the underrepresented classes. The techniques used in data augmentation include rotating the image, shearing to distort the image, flipping the image horizontally and filling the generated pixels during transformation.
![image](https://github.com/user-attachments/assets/37f11c10-07c6-47ee-9b32-089efe915ae0)

Balancing the dataset resulted in equal numbers from each class which prevents the model from specifically training on casual clothing and failing to classify underrepresented clothing types.

# Visualisation
GRAD-CAM produces a heatmap to highlight different regions of the image that the model identifies as important for image classification. 
![image](https://github.com/user-attachments/assets/711c2401-c0f8-4578-b01a-daf164352d1e)


Dataset Source
Param Aggarwal. (2019). Fashion Product Images Dataset. Kaggle. https://doi.org/10.34740/KAGGLE/DS/139630
