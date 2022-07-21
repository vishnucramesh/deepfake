# Image Classification with Shannon Information

Run the notebook file with Google Colab or notebook.
In this project a new approach on image classification has been applied from scratch. The main purpose is to try to increase the classification accuracy with a method that has never been applied, i.e. leveraging the usage of pixel’s values Shannon informations (SI) in two different ways. Besides applying these approaches with a
simple Convolutional Neural Network (CNN), in case of over fitting regular dropout and Monte Carlo(MC) dropout has been applied. In the end, a comparison between all the implemented models results has been performed.

## The Dataset

CIFAR-100 dataset (Canadian Institute for Advanced Research, 100 classes) has been used. CIFAR-100 dataset is a subset of the Tiny Images dataset and consists of 60000 32x32x3 color images. The 100 classes in the CIFAR-100 are grouped into 20 superclasses. There are 600 images per class. Each image comes with a ”fine” label (the class to which it belongs) and a ”coarse” label (the superclass to which it belongs) which the project classified images w.r.t. the superclass. There are 500 training images and 100 testing images per class, in total 50,000 training and 10,000 test images.


## The model

Since we are just focusing on the relevance of the Shannon information on improving accuracy, a simple CNN will be used. It contains 5 convolutional blocks (each containing a Convolutional layer, a MaxPooling layer with kernel of size (2, 2) and a ReLu activation layer) each of them containing respectively 128, 512, 512, 512
and 512 filters. A dense layer with 20 neurons is then appended at the end as classifier. As loss function, Categorical Crossentropy has been used.


## 1° approach: appending Shannon informations to images

In this first approach, each image is transformed from a tensor of size (32, 32, 3) into a tensor of size (32, 32, 6), i.e. for each pixel in the RGB layers the image will be augmented to store its Shannon information value in the corresponding Shannon information layer.

## 2° approach: a Shannon information regularization term

In this second approach, original images of size (32, 32, 3) are fed into the CNN. The Shannon information content is instead exploited by the addition of a regularization therm R.T.(·) to the Categorical Crossentropy loss. 

To reproduce and get deep intuition simply run the notebook file with Google Colab or same!


## License
[MIT](https://choosealicense.com/licenses/mit/)
[MIT](https://choosealicense.com/licenses/mit/)
