# Age_detection_with_Keras
## Computer Vision project from Practicum by Yandex
The goal of this project was to develop a neural network model that predicts age of a person from a photograph. The project metric is MAE and it should be no more than 8.

This project's repo includes the project's jupyter notebook (Age_detection_with_Keras.ipynb);

There are more than 7.5k photos in this dataset. The age is slightly positively skewed, close to normal distribution. Most people in these photos are in their 30-s. Based on that we can assume that a neural network model might overestimate the age of younger people and underestimate the age of elder people.

We have applied several data augmentation techniques to help the model train better:

* horizontal_flip;
* height_shift_range;
* width_shift_range.
  
The final model is based on the ResNet-50 - a convolutional neural network that is 50 layers deep. We have adde the GlobalAveragePooling2D layer and 3 fully connected layers after that.

The model showed the desired quality - after 14 epochs the validation MAE is 5.93, which means that, on average, our model's predicted age diverges from the real age by slightly less than 6 years.
