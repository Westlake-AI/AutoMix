# Installation

We provide installation instructions for image classification experiments here.

## Dependency Setup
Create an new conda virtual environment
```
conda create -n automix python=3.8 -y
conda activate automix
```

Install [Pytorch](https://pytorch.org/)>=1.8.0, [torchvision](https://pytorch.org/vision/stable/index.html)>=0.9.0 following official instructions. For example:
```
pip install torch==1.10.0+cu111 torchvision==0.11.0+cu111 torchaudio==0.10.0 -f https://download.pytorch.org/whl/torch_stable.html
```

Clone this repo and install required packages. You can install [apex-amp](https://github.com/NVIDIA/apex) if you want to use fp16 with Pytorch<=1.6.0.
```
git clone git@github.com:Lupin1998/AutoMix.git
pip install timm
```

## Dataset Preparation

We suggest placing all datasets in a folder (e.g., `./data`). You can link each dataset to the folder with soft link.

### CIFAR-10/100

You can download [CIFAR-10/100](http://www.cs.toronto.edu/~kriz/learning-features-2009-TR.pdf) classification datasets with a line of code or from the [official website](https://www.cs.toronto.edu/~kriz/cifar.html).

```bash
python -c "import torchvision; torchvision.datasets.CIFAR100(download=True, root='data/cifar100');"
```

### Tiny-ImageNet

Download the [Tiny-ImageNet](https://arxiv.org/abs/1707.08819) classification dataset from the [official website](http://image-net.org/download-images) and structure the data as follows.
```
│tiny_imagenet/
├──train/
│  ├── n01443537
│  │   ├── n01443537_0.JPEG
│  │   ├── n01443537_1.JPEG
│  │   ├── ......
│  ├── ......
├──val/
│  ├── n03444034
│  │   ├── val_0.JPEG
│  │   ├── val_284.JPEG
│  │   ├── ......
│  ├── ......
```

### ImageNet-1K

Download the [ImageNet-1K](http://image-net.org/) classification dataset ([train](https://image-net.org/data/ILSVRC/2012/ILSVRC2012_img_train.tar) and [val](https://image-net.org/data/ILSVRC/2012/ILSVRC2012_img_val.tar)) and structure the data as follows. You can extract ImageNet with this [script](https://gist.github.com/BIGBALLON/8a71d225eff18d88e469e6ea9b39cef4).
```
│imagenet/
├──train/
│  ├── n01440764
│  │   ├── n01440764_10026.JPEG
│  │   ├── n01440764_10027.JPEG
│  │   ├── ......
│  ├── ......
├──val/
│  ├── n01440764
│  │   ├── ILSVRC2012_val_00000293.JPEG
│  │   ├── ILSVRC2012_val_00002138.JPEG
│  │   ├── ......
│  ├── ......
```
