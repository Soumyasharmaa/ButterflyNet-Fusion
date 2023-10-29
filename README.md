# ButterflyNet-Fusion
## Butterfly Image Classification Dataset

- **Source**: The dataset is sourced from Kaggle and is titled "Butterfly Image Classification."

- **Objective**: The primary goal is to identify the class to which each butterfly image belongs.

- **Dataset Features**:
  - The dataset includes 75 different classes of butterflies.
  - It contains over 1000 labeled images, including validation images.
  - Each image belongs to one and only one butterfly category.

- **Label Information**: The labels for each image are provided in the "Training_set.csv" file.

- **Dataset Link**: You can access the dataset on Kaggle through this link: [Butterfly Image Classification Dataset](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification/data)
- ## Ensemble Model Component Summaries
- ### Component Model 1
```plaintext
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_4 (Conv2D)           (None, 26, 26, 32)        320       
 max_pooling2d_3 (MaxPooling2D) (None, 13, 13, 32)        0         
 dropout_3 (Dropout)         (None, 13, 13, 32)        0         
 conv2d_5 (Conv2D)           (None, 11, 11, 64)        18496     
 max_pooling2d_4 (MaxPooling2D) (None, 5, 5, 64)          0         
 dropout_4 (Dropout)         (None, 5, 5, 64)          0         
 conv2d_6 (Conv2D)           (None, 3, 3, 128)         73856     
 max_pooling2d_5 (MaxPooling2D) (None, 1, 1, 128)         0         
 dropout_5 (Dropout)         (None, 1, 1, 128)         0         
 flatten_1 (Flatten)         (None, 128)               0         
 dense_2 (Dense)             (None, 128)               16512     
 dense_3 (Dense)             (None, 75)                9675      
=================================================================
Total params: 118,859 (464.29 KB)
Trainable params: 118,859 (464.29 KB)
Non-trainable params: 0 (0.00 Byte)
```
### Component Model 2
```plaintext
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_7 (Conv2D)           (None, 26, 26, 32)        320       
 conv2d_8 (Conv2D)           (None, 24, 24, 32)        9248      
 max_pooling2d_6 (MaxPooling2D) (None, 12, 12, 32)        0         
 conv2d_9 (Conv2D)           (None, 10, 10, 64)        18496     
 conv2d_10 (Conv2D)          (None, 8, 8, 64)          36928     
 conv2d_11 (Conv2D)          (None, 6, 6, 64)          36928     
 max_pooling2d_7 (MaxPooling2D) (None, 3, 3, 64)          0         
 conv2d_12 (Conv2D)          (None, 1, 1, 128)         73856     
 conv2d_13 (Conv2D)          (None, 1, 1, 25)          3225      
 flatten_2 (Flatten)         (None, 25)                0         
 dense_4 (Dense)             (None, 75)                1950      
=================================================================
Total params: 180,951 (706.84 KB)
Trainable params: 180,951 (706.84 KB)
Non-trainable params: 0 (0.00 Byte)
```
### Component Model 3
```plaintext
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_18 (Conv2D)          (None, 26, 26, 32)        320       
 max_pooling2d_12 (MaxPooling2D) (None, 13, 13, 32)        0         
 dropout_10 (Dropout)        (None, 13, 13, 32)        0         
 conv2d_19 (Conv2D)          (None, 11, 11, 64)        18496     
 max_pooling2d_13 (MaxPooling2D) (None, 5, 5, 64)          0         
 dropout_11 (Dropout)        (None, 5, 5, 64)          0         
 flatten_5 (Flatten)         (None, 1600)              0         
 dense_7 (Dense)             (None, 75)                120,075    
=================================================================
Total params: 138,891 (542.54 KB)
Trainable params: 138,891 (542.54 KB)
Non-trainable params: 0 (0.00 Byte)
```
The ensemble model is constructed by summing the outputs or predictions of the individual component models, resulting in a combined prediction.


### Model Accuracies

| Model                   | Accuracy Score |
|-------------------------|-----------------|
| Model 1                 | 0.24154         |
| Model 2                 | 0.31077         |
| Model 3                 | 0.32462         |
| Average Ensemble        | 0.35769         |



