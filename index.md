# CSE 455 Final Project

## Dog Breed Identification Competition

**Group members:** Dingyu Zhang (dyzhang1), Yixiao Li (yixiaoli), Yifan Zhuo (zhouyf98), Katherine Cai (klc715)

### Problem

Create a classifier capable of determining a dog’s breed in an image. 

### Algorithms/Techniques

Convolutional Neural Network, Transfer Learning, Inception Neural Network

### Dataset 

Stanford Dogs Dataset

### Introduction

For our project, we created a classifier capable of determining a dog’s breed in an image. We used the Stanford Dogs Dataset, provided by a [Kaggle Competition](https://www.kaggle.com/c/dog-breed-identification), to train our classifier. We applied techniques taught in this class such as the convolutional neural network and feature extraction, and also explored more advanced ones like transfer learning to make our model even better. We hosted our model on a server and built a dog breed scanner web app so that internet users can upload pictures of a dog and learn its breed!

### Experiment reports with transfer learning:

[Inception v3](https://drive.google.com/file/d/1JxwztvF40rz28CJtgqwm3e70j2AsNFPk/view?usp=sharing)

[ResNeXt 50](https://drive.google.com/file/d/1HjYX76gJkZx6YWPcRGKdt_OHCVDaWEBA/view?usp=sharing)

### Architecture analysis report:

[ResNeXt 50 and Inception v3 Architecture Comparison](https://drive.google.com/file/d/1aJ6r_URVzbdJRwc8xiLvLNBAqQ-O6gJ6/view?usp=sharing)


# Dog Breed Classification!
### Current best accuracy: 92%

### Upload your doggy image for classification!
<form action="/action_page.php">
  <input type="file"  accept="image/gif, image/jpeg, image/png" name="image" id="file" style="display: none;">
  <input type="submit">
</form>

<img id="output" width="299" />	
