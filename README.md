# Image-Classification-using-Transfer-learning
Image classification on a very small dateset while maintaining accuracy more than 80% using Transfer Learning.

Used CIFAR-100 image dataset for training my model.
CIFAR-100 has 102 classes in it.
Took only 20 classes for training purpose.

Splitted the data in two Train and Test part using Split-Folder python script.
Split-Folder.ipynb uses (os) module to read all the images and split it in two different folder
Namely :- Train and Test

After that since we have a very small dataset
We will perform Augmentation on the dataset using (ImageDataGenerator).

ImageDataGenerator transforms and rotates our images to forms new images from
Pre-existing images.
This will increase our dataset.

We will use the Resnet pre-trained model to perform transfer training on our model.
Then we will build our model using Resnet pre-trained model.

Then we will set Loss function as Categorical Crossentropy.
And Optimizers as Adam.

Then we will compile our model.

After compiling, we use ReduceLROnPlateau, which will reduce learning rate whenever our
model stops improving any more.
Reducing learning rate helps our model to even learn more from our data.

Finally, we will train our model on already split training and validation data.

After getting our model trained, we will plot our results.
Training Accuracy vs Validation Accuracy
Training Loss vs Validation Loss

After training <br />
We reached :- <br />
Training accuracy = 97.51%    <br />
Validation accuracy = 86.98%
