# IDCBreastCancer_histopathologyImages_deepResidualLearning
IDC prediction in breast cancer histopathology images using deep residual learning with an accuracy of 99.37% in a subset of images containing a total of 7,500 microscopic images.
# Dataset
The dataset was obtained form kaggle link https://www.kaggle.com/paultimothymooney/predict-idc-in-breast-cancer-histology-images/notebook
The dataset actually contained a total of 277,542 images(198.738 IDC negative and 78,786 IDc positive). Out of the total no of images we used a subset of 7,500 images(3,000 IDc positive and 4,500 IDC negative) to avoid generating memory error.
# Preprocessing  
The image were originally acanned at 40x and hence they had a very low resolutino and for using deep learning algorithms I had to resize the images to an uniform resolutino of(50 X 50) due to very low resolution in the original images. The preprocessinmg was done using openCV resize method without mentaining the aspect ratio.
# Channel selection
The images were microscopic images hence to improve the feature extractino by deep learning algorithms we used 4 extra channels such as(l* and a* channel of LAB color space and hue and saturation channel of the HSV color space). The channel selection part is present in the 2nd cell of the ipynb file of the model.
# Model development 
The model is based on deep residual learning algorithm to perform extensive feature extraction for aiding to the classification task. The model consists of 4 residual blocks each with a shortcut path to allow residual learning containing convolutional layers with ELU activation. The model can be viewed at 'model.png'.
# Training 
The model can be trained by running the model.ipynb file after the setting the training parameters resent in the 1st cell under the specifyig parameters section according to your own requirements.
# Visualization
Grad-CAMs visualization has been performed to validate the model's performance along with training and loss curves of the model.
# Requirements
