# DCGAN_Tensorflow
## SUMMARY
 •	DCGAN
### *Deep Convolutional Generative Adversarial Networks*
#### Introduction	
One way to build good natural images is by training Generative Adversarial Networks (GANS). ,and we can later even reuse parts of the generator and discriminator networks as feature extractors for supervised tasks .DCGANs is actually one of the class of GANs using CNNs architecture for both of its components i.e.  a generator and a discriminator.
#### Model Architecture	
In general, GANs consist of a generator and a discriminator. These two are separately a CNN architecture and are trained together.

  
##### GENERATOR :
A ANN model which is aimed for the generation of new images. They took in input a random noise z and various convolution transpose layers are applied and it generates a image i.e. a matrices of pixel values (G(z)) .Generator never get to see the real world actual images or the training dataset of images.
##### DISCRIMINATOR:
A CNN classification model used to classify whether an image passed to it is real or fake (generated by the generator).It take image from training examples x and from those generated by generator (G (z)) and predicts the probability of the image to be real (D(x)) or fake (D (G (z))).

Now, while training the model, generator tries to increase the discriminator error as it tries to fool discriminator by improving its generated image so that they resemble real images while discriminator tries to decrease it’s error by trying to judge correctly the real and the fake images. For weights of the model normally initiated ,we first train generator say for y no. of images keeping the discriminator’s weights constant .Then, as generator’s weight are updated ,we train discriminator keeping generator’s weights to be constant for y fake and y real images and this process is then repeated for several epochs using cross entropy loss function.

![alt text](https://git
  



