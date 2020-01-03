# Deep learning method for Single Image Super Resolution
Capstone project for a [course on machine learning and deep learning](http://www.ai.iitkgp.ac.in/outreach)

- This is an implementation of [Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network](https://arxiv.org/abs/1609.04802).Used [left-thomas's implementation of SRGAN](https://github.com/leftthomas/SRGAN).

- Trained a modified SRGAN model using google colab, with the VOC2012 dataset(approx 1000 images) for different upscale values. 

- Tried to modify the network to be able to take in any upscale value (not fractional), instead having only exponentials of 2 as is in the paper, upon doign so, noticed that the modification resulted in more number of parameters than the original model, for upscale values like 4,6,8 etc.

- This is why I think it resulted in more number of parameters:
![explanation](RESULTS/explanation.png)

tl;dr

Original model uses lesser number of "channels" to upscale the image when compared to the modified model. [Read this to understand more](https://www.inference.vc/holiday-special-deriving-the-subpixel-cnn-from-first-principles/)


- Some results from the trained model

modified SRGAN model, trained for 930 epochs:

input : 
![input_flower](RESULTS/input_SRGAN_flower.jpg)

output: 
![output_flower](RESULTS/ouput_SRGAN_flower_930epochs_psnr27.07.jpg) PSNR:27.07

----------

input : 
![input_dog](RESULTS/input_SRGAN_dog.jpg)

output: 
![output_dog](RESULTS/output_SRGAN_100epoch_psnr-20.50.jpg) PSNR:20.50

----------

input : 
![input_house](RESULTS/input_SRGAN_house.jpg)

output: 
![output_house](RESULTS/output_SRGAN_house_psnr28.57_930epochs.jpg) PSNR:28.57

----------

Pre-trained ESRGAN:

input : 
![input_ESRGAN](RESULTS/input_ESRGAN.png)

output: 
![output_ESRGAN](RESULTS/output_ESRGAN.png)

