## Dog Breed Identification Competition

**Group members:** Dingyu Zhang (dyzhang1), Yixiao Li (yixiaoli), Yifan Zhuo (zhouyf98), Katherine Cai (klc715)

### Problem we tackled:

Create a classifier capable of determining a dog’s breed in an image. 

### Algorithms/Techniques we used:

Convolutional Neural Network, Transfer Learning, Inception Neural Network, ResNeXt Neural Network, Data Augmentation, Using Model For Production

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

1. From our experiments applying transfer learning to pretrained neural network models, we have tuned a good set of hyperparameters such as the learning rate, weight decay and the fully-connected layer. The set of best hyperparameters allows us to begin with a model that has a relatively good classification accuracy on the validation dataset.
2. Then, by applying data augmentation, we are able to examine good and bad techniques to make our model generalize better to unseen data samples. The attempted data augmentation techniques including RandomErasing and RandomResizedCrop provided meaningful insights such as what kind of training data samples would in fact reduce our model's classification accuracy.
3. Through using the pretrained neural network models as feature extractors, we were able to keep the pretrained information in the model and utilize such information to regularize our model to obtain better generalization performance (fine tuning the models turns out had much worse performance in terms of loss and classification accuracy on both training and validation datasets). 
4. By creating the online dog breed classification application, we are able to further examine our model's performance by using it to classify any image available on the internet.


# [Dog Breed Classification App!](https://master.d3jonbje051vgo.amplifyapp.com/)

## [Project Presentation Video](https://www.youtube.com/watch?v=s99BOFDfnV0)

## Discussion:
### What problems did you encounter?
1. We have attempted to use large and sophisticated neural network models such as ResNeXt 50 and 101 to improve our classification task accuracy. However, due to the technical resource contraints (GPU memory is limited for Google colab and Kaggle notebook), we were not able to fine tune the pre-trained models.
2. In addition, the Kaggle Dog Breed Identification competition dataset was not well prepared for directly using dataloaders to load the data samples and labels for training. We needed to spend a significant amount of time figuring out how to organized the data images and transform the dataset in order to train our neural network models.
3. Some neural network models such as the Inception v3 model are susceptible to having very poor performance with slight augmentation in training samples. The deficiencies in neural network architecture disallows many opportunities for applying data augmentation techniques.

### Are there next steps you would take if you kept working on the project?
We would like to look into more sophisticated data augmentation techniques to make our model perform better on unseen data. After we used the online app to examine our model's performance on dog images outside of the Stanford dogs dataset, we noticed that it is inevitable that some dogs are mix-breed and our model performs very bad on classifying mix-breed dog images. We think the most important step later would be to improve the model to be capable of having much more accurate predictions on mix-breed dog images. We would also like to experiment with neural network ensemble to examine the possibility of such technique on improving our model's performance on mix-breed dog images.

### How does your approach differ from others? Was that beneficial?
Our apprach differs from others for we have utilized interesting techniques to examine the "deficiencies" of neural network models. (This is something similar to Adversarial attacks but in a more constructive way.) By applying RandomErasing to our training data samples, the Inception v3 model was broken and was not able to successfully reduce loss and ended up with around 3% accuracy. This is a good indication for poor model performance on images that have slight scaling issues or outlier pixel values. This happens even when the scale parameter of RandomErasing was set to 0.01.  On the other hand, while RandomResizedCrop has been popularly used for training Inception models, it did not work well in our case and our Inception v3 model ended up having around 66% validation accuracy with using RandomResizedCrop. However, RandomCrop was in particular useful and it helped one of our examined ResNeXt models to reach 92.89% validation accuracy. Since tuning data augmentation techniques indeed further improves model performance, in our opinion this approach was quite beneficial.

By creating an application to classify any images found on the web, we are able to directly examine what type of images our model have trouble making correct predictions (such as mix-breed dog images). This way, we were able to look into more specific things that we could try. In other words, we have created a method to directly examine the "deficiencies" of our model through using it for production, just like testing a piece of software. We think this method was beneficial in a sense that it helped with detacting what information gets lost during training (such as why a Samoyed is being incorrectly classified as an Eskimo dog) and how to preserve that information in order for the model to make correct predictions.
