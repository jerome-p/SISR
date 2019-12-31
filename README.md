# SISR using deep learning

- This is an implementation of [Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network](https://arxiv.org/abs/1609.04802).

- The code is taken from [left-thomas's implementation of SRGAN](https://github.com/leftthomas/SRGAN).

- I explore different image super resolution techniques and try to compare them. (Only ESRGAN ans SRGAN's results are uploaded to github).

- Trained SRGAN using google colab. Hence could not use a lot of images for training.

- Tried to modify the network to be able to take in any upscale value (not fractional), intead having only exponentials of 2 as is in the paper.
Noticed that the modifictaion resulted in more number of parameters than the original model, for upscale values like 4,6,8 etc.

- This is my understanding of why it happened:
![explanation](RESULTS/explanation.png)

- Some results from the trained model

modified SRGAN model, trained for 930 epochs:

input : ![input_flower](RESULTS/input_SRGAN_flower.jpg)

output: ![output_flower](RESULTS/ouput_SRGAN_flower_930epochs_psnr27.07.jpg) PSNR:27.07

----------

input : ![input_dog](RESULTS/input_SRGAN_dog.jpg)

output: ![output_dog](RESULTS/output_SRGAN_100epoch_psnr-20.50.jpg) PSNR:20.50

----------

input : ![input_house](RESULTS/input_SRGAN_house.jpg)

output: ![output_house](RESULTS/output_SRGAN_house_psnr28.57_930epochs.jpg) PSNR:28.57

----------

Pre-trained ESRGAN:

input : ![input_ESRGAN](RESULTS/input_ESRGAN.png)

output: ![output_ESRGAN](RESULTS/output_ESRGAN.png)

