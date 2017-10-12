## This code is heavily built on these repo:   
- [CoGAN](https://github.com/carpedm20/DCGAN-tensorflow) from @andrewliao11
- [WGAN](https://github.com/mingyuliutw/CoGAN) from @Zardinality
```
Thanks to the the contribution of @andrewliao11, @Zardinality.
```
## Requirement

- Python 2.7
- Tensorflow.1.3.0

## Kick off
First you have to clone this repo:
```
$ git clone https://github.com/liulirong/cogan-wgan.git
```
Download the data:
This step will automatically download the data under the current folder.
```
$ python download.py mnist
```
Preprocess(invert) the data:
```
$ python invert.py 
```
Train your CoGAN:
```
$ python main.py --is_train True
```
During the training process, you can see the average loss of the generators and the discriminators, which can hellp your debugging. After training, it will save some sample to the ```./samples/top and ./samples/bot```, respectively. 

## Notices
- ***Note: To avoid the fast convergence of D (discriminator) network, G (generator) network is updated twice for each D network update, which differs from original paper.***
- ***Note: The changes I've made: 1. set lam 1.  2. Don't use batch normalization in discriminator. 3. Don't use sigmoid on the output of discriminator .***


