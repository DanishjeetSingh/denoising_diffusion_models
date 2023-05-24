# PyTorch Implementation of Denoising Diffusion Probabilistic Models

## Papers implemented

- [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239)
- [CLASSIFIER-FREE DIFFUSION GUIDANCE](https://arxiv.org/abs/2207.12598)


## Results

---
## Unconditional Diffusion Model

### Sample images

![](samples/ddpm_unconditional_0.png)
![](samples/ddpm_unconditional_1.png)
![](samples/ddpm_unconditional_2.png)

#### Here's a gif I made from the last 20 training epochs :)
![](samples/ddpm_unconditional.gif)

---
## Conditional Diffusion model

### Sample images
##### All of them are frogs 🐸(*it's one of the labels in the CIFAR10 dataset*), because why not :), although maybe a horse could have been a nice choice too.

### This time we have done things 4 ways, since we have CFG(Classifier free guidance) and EMA(Exponential Moving Average)

### 🚫EMA 🚫CFG

![](samples/ddpm_conditional_0.png)
![](samples/ddpm_conditional_1.png)

### 🚫EMA ✅CFG
![](samples/ddpm_conditional_cfg_0.png)
![](samples/ddpm_conditional_cfg_1.png)

### ✅EMA 🚫CFG
![](samples/ddpm_conditional_ema_0.png)
![](samples/ddpm_conditional_ema_1.png)

### ✅EMA ✅CFG
![](samples/ddpm_conditional_cfg_ema_0.png)
![](samples/ddpm_conditional_cfg_ema_1.png)

##### Note: In the CFG paper the authors mentioned heavy saturation when CFG levels were too high(i.e = 3), we are able to reproduce that same effect in the above picture. 

## Clearly the results with EMA are much better generally, however CFG helps with more stable looking images :)

---
## Dataset used
- [Landscapes dataset](https://www.kaggle.com/datasets/arnaud58/landscape-pictures) 
(for unconditional model)
- [CIFAR-10 Resized](https://www.kaggle.com/datasets/joaopauloschuler/cifar10-64x64-resized-via-cai-super-resolution)
  (for conditional model)
## Helpful resources

- https://github.com/lucidrains/denoising-diffusion-pytorch
- https://github.com/hojonathanho/diffusion
- https://www.youtube.com/watch?v=TBCRlnwJtZU
- https://theaisummer.com/unet-architectures/
