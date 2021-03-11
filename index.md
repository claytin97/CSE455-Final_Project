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

For our project, we will be creating a classifier capable of determining a dog’s breed in an image. We will be using the Stanford Dogs Dataset, provided by a [Kaggle Competition](https://www.kaggle.com/c/dog-breed-identification), to train our classifier. We will apply techniques taught in this class such as the convolutional neural network and feature extraction, but we will also explore more advanced ones like transfer learning to make our model even better. At the end of the project, we hope to host our model on a server and build a dog breed scanner web app so that internet users can upload pictures of a dog and learn its breed!

### Experiment reports with transfer learning:

[Inception v3](https://drive.google.com/file/d/1JxwztvF40rz28CJtgqwm3e70j2AsNFPk/view?usp=sharing)

[ResNeXt 50](https://drive.google.com/file/d/1HjYX76gJkZx6YWPcRGKdt_OHCVDaWEBA/view?usp=sharing)


# Dog Breed Classification!
### Current best accuracy: 92%

### Upload your doggy image for classification!
<script>
var loadFile = function(event) {
	var image = document.getElementById('output');
	image.src = URL.createObjectURL(event.target.files[0]);
};
</script>

<input type="file"  accept="image/*" name="image" id="file"  onchange="loadFile(event)" style="display: none;">

<img id="output" width="299" />	
