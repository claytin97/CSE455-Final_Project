## Dog Breed Identification Competition

**Group members:** Dingyu Zhang (dyzhang1), Yixiao Li (yixiaoli), Yifan Zhuo (zhouyf98), Katherine Cai (klc715)

### Problem we tackled

Create a classifier capable of determining a dog’s breed in an image. 

### Algorithms/Techniques we used

Convolutional Neural Network, Transfer Learning, Inception Neural Network, ResNeXt Neural Network

### Dataset 

Stanford Dogs Dataset

### Introduction

For our project, we created a classifier capable of determining a dog’s breed in an image. We used the Stanford Dogs Dataset, provided by a [Kaggle Competition](https://www.kaggle.com/c/dog-breed-identification), to train our classifier. We applied techniques taught in this class such as the convolutional neural network and feature extraction, and also explored more advanced ones like transfer learning to make our model even better. We hosted our model on a server and built a dog breed scanner web app so that internet users can upload pictures of a dog and learn its breed!

### Experiment reports with transfer learning:

[Inception v3](https://drive.google.com/file/d/1JxwztvF40rz28CJtgqwm3e70j2AsNFPk/view?usp=sharing)

[ResNeXt 50](https://drive.google.com/file/d/1HjYX76gJkZx6YWPcRGKdt_OHCVDaWEBA/view?usp=sharing)

### Architecture analysis report:

[ResNeXt 50 and Inception v3 Architecture Comparison](https://drive.google.com/file/d/1aJ6r_URVzbdJRwc8xiLvLNBAqQ-O6gJ6/view?usp=sharing)


# [Dog Breed Classification!](https://master.d3jonbje051vgo.amplifyapp.com/)

# Video

## Discussions:
### What problems did you encounter?
We have attempted to use large and sophisticated neural network models such as ResNeXt 50 and 101 to improve our classification task accuracy. However, due to the technical resource contraints (GPU memory is limited for Google colab and Kaggle notebook), we were not able to fine tune the pre-trained model.

In addition, the Kaggle Dog Breed Identification competition dataset was not well prepared for directly using dataloaders to load the data samples and labels for training. We needed to spend a significant amount of time figuring out how to access the data and transform the data in order to train our neural network models.

### Are there next steps you would take if you kept working on the project?

### How does your approach differ from others? Was that beneficial?
