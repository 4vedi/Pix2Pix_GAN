
# Develop a Pix2Pix GAN for Image-to-Image Translation </br>
(This project is a part of my Summer Internship 2020 from OSI with IIPC/TBI/Innovation Centre, KIET) </br>

The Pix2Pix Generative Adversarial Network, or GAN, is an approach to training a deep convolutional neural network for image-to-image translation tasks.
The careful configuration of architecture as a type of image-conditional GAN allows for both the generation of large images compared to prior GAN models (e.g. such as 256×256 pixels) and the capability of performing well on a variety of different image-to- image translation tasks.
</br></br></brr>

<h4>What Is the Pix2Pix GAN? </h4></br></br>
Pix2Pix is a Generative Adversarial Network, or GAN, model designed for general purpose image-to-image translation. </br>
The approach was presented by Phillip Isola, et al. in their 2016 paper titled “Image-to- Image Translation with Conditional Adversarial Networks” and presented at CVPR in 2017.</br>
https://phillipi.github.io/pix2pix/ </br></br>
The GAN architecture is comprised of a generator model for outputting new plausible synthetic images, and a discriminator model that classifies images as real (from the dataset) or fake (generated). The discriminator model is updated directly, whereas the generator model is updated via the discriminator model. As such, the two models are trained simultaneously in an adversarial process where the generator seeks to better fool the discriminator and the discriminator seeks to better identify the counterfeit images. </br>
The Pix2Pix model is a type of conditional GAN, or cGAN, where the generation of the output image is conditional on an input, in this case, a source image. The discriminator is provided both with a source image and the target image and must determine whether the target is a plausible transformation of the source image. </br>
The generator is trained via adversarial loss, which encourages the generator to generate plausible images in the target domain. The generator is also updated via L1 loss measured between the generated image and the expected output image. This additional loss encourages the generator model to create plausible translations of the source image. </br>
The Pix2Pix GAN has been demonstrated on a range of image-to-image translation tasks such as converting maps to satellite photographs, black and white photographs to color, and sketches of products to product photographs. </br>
     
Now that we are familiar with the Pix2Pix GAN, let’s prepare a dataset that we can use with image-to-image translation.</br>

![Plot of Three Image Pairs Showing Satellite and Google maps Images](https://github.com/4vedi/Pix2Pix_GAN/blob/master/Plot1.png)
