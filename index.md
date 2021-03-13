## Dog Breed Identification Competition

**Group members:** Dingyu Zhang (dyzhang1), Yixiao Li (yixiaoli), Yifan Zhuo (zhouyf98), Katherine Cai (klc715)

### Problem we tackled:

Create a classifier capable of determining a dog’s breed in an image. 

### Algorithms/Techniques we used:

Convolutional Neural Network, Transfer Learning, Inception Neural Network, ResNeXt Neural Network

### Dataset:

[Stanford Dogs Dataset](http://vision.stanford.edu/aditya86/ImageNetDogs/)

### Introduction:

For our project, we created a classifier capable of determining a dog’s breed in an image. We used the Stanford Dogs Dataset, provided by a [Kaggle Competition](https://www.kaggle.com/c/dog-breed-identification), to train our classifier. We applied techniques taught in this class such as the convolutional neural network and feature extraction, and also explored more advanced ones like transfer learning to make our model even better. In particular, we experimented with ResNeXt and Inception neural networks. We hosted our model on a server and built a dog breed scanner web app so that internet users can upload pictures of a dog and learn its breed!

### Experiment reports with transfer learning:

[Inception v3](https://drive.google.com/file/d/1JxwztvF40rz28CJtgqwm3e70j2AsNFPk/view?usp=sharing)

[ResNeXt 50](https://drive.google.com/file/d/1HjYX76gJkZx6YWPcRGKdt_OHCVDaWEBA/view?usp=sharing)

### Architecture analysis report:

[ResNeXt 50 and Inception v3 Architecture Comparison](https://drive.google.com/file/d/1aJ6r_URVzbdJRwc8xiLvLNBAqQ-O6gJ6/view?usp=sharing)

### Our Approach:

From our experiments applying transfer learning to pretrained neural network models, we have tuned a good set of hyperparameters such as the learning rate and weight decay. The set of best hyperparameters allows our model to attain the highest classification accuracy on the validation dataset. By applying data augmentation, we are able to make our model generalize better to unseen data samples. We also utilized the step learning rate scheduler to further minimize the model's loss. Through using the pretrained neural network models as feature extractors, we were able to keep the pretrained information in the model and utilize such information to regularize our model. By creating the online dog breed classification application, we are able to further examine our model's performance by using it to classify any image found on the internet.


# [Dog Breed Classification App!](https://master.d3jonbje051vgo.amplifyapp.com/)

## [Project Presentation Video](https://www.youtube.com/watch?v=s99BOFDfnV0)

## Discussion:
### What problems did you encounter?
We have attempted to use large and sophisticated neural network models such as ResNeXt 50 and 101 to improve our classification task accuracy. However, due to the technical resource contraints (GPU memory is limited for Google colab and Kaggle notebook), we were not able to fine tune the pre-trained model.

In addition, the Kaggle Dog Breed Identification competition dataset was not well prepared for directly using dataloaders to load the data samples and labels for training. We needed to spend a significant amount of time figuring out how to organized the data images and transform the dataset in order to train our neural network models.

### Are there next steps you would take if you kept working on the project?
We would like to look into more sophisticated data augmentation techniques to make our model perform better on unseen data. We would also like to experiment with neural network ensemble to examine the effects of such technique on improving our classification accuracy.

### How does your approach differ from others? Was that beneficial?
By creating an application to classify any images found on the internet, we are able to directly examine what type of images our model have trouble making correct predictions. This way, we can look into more specific data augmentation techniques to try. In other words, we have created a method to directly examine the "deficiencies" of our model through using it for production, just like testing a piece of software. We think this method is beneficial in a sense that it helps with detacting what information is lost (such as why a Samoyed is being incorrectly classified as an Eskimo dog) during training and how to preserve that information to improve our model's accuracy.
