<div align="center">
<h2><a href="https://arxiv.org/abs/2103.13027">AutoMix: Unveiling the Power of Mixup for Stronger Classifiers</a> (ECCV 2022 Oral)</h2>

[Zicheng Liu](https://pone7.github.io/)<sup>\*,1,2</sup>, [Siyuan Li](https://lupin1998.github.io/)<sup>\*,1,2</sup>, [Di Wu](https://scholar.google.com/citations?user=egz8bGQAAAAJ&hl=zh-CN)<sup>1,2</sup>, [Zhiyuan Chen](https://zyc.ai/)<sup>1</sup>, [Lirong Wu](https://lirongwu.github.io/)<sup>1,2</sup>, [Stan Z. Li](https://scholar.google.com/citations?user=Y-nyLGIAAAAJ&hl=zh-CN)<sup>†,1</sup>

<sup>1</sup>[Westlake University](https://westlake.edu.cn/), <sup>2</sup>[Zhejiang University](https://www.zju.edu.cn/english/)
</div>

<p align="center">
<a href="https://arxiv.org/abs/2103.13027" alt="arXiv">
    <img src="https://img.shields.io/badge/arXiv-2210.13452-b31b1b.svg?style=flat" /></a>
<a href="https://github.com/Westlake-AI/AutoMix/blob/main/LICENSE" alt="license">
    <img src="https://img.shields.io/badge/license-Apache--2.0-%23B7A800" /></a>
<!-- <a href="https://colab.research.google.com/github/Westlake-AI/MogaNet/blob/main/demo.ipynb" alt="Colab">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" /></a> -->
</p>

We propose a novel automatic mixup (AutoMix) framework, where the mixup policy is parameterized and serves the ultimate classification goal directly. Specifically, AutoMix reformulates the mixup classification into two sub-tasks (i.e., mixed sample generation and mixup classification) with corresponding sub-networks and solves them in a bi-level optimization framework. For the generation, a learnable lightweight mixup generator, Mix Block, is designed to generate mixed samples by modeling patch-wise relationships under the direct supervision of the corresponding mixed labels. To prevent the degradation and instability of bi-level optimization, we further introduce a momentum pipeline to train AutoMix in an end-to-end manner. Extensive experiments on nine image benchmarks prove the superiority of AutoMix compared with state-of-the-arts in various classification scenarios and downstream tasks.

<p align="center">
<img src="https://user-images.githubusercontent.com/44519745/174272662-19ce57ad-7b08-4e73-81b1-3bb81fee2fe5.png" width=100% height=100% 
class="center">
</p>

<!-- <details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#catalog">Catalog</a></li>
    <li><a href="#image-classification">Image Classification</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#acknowledgement">Acknowledgement</a></li>
    <li><a href="#citation">Citation</a></li>
  </ol>
</details> -->

## Catalog

We plan to release this implementation of AutoMix in a few months. Please watch us for the latest release or use [OpenMixup](https://github.com/Westlake-AI/openmixup/tree/main/configs/classification/imagenet/automix/) implementations.

- [x] **CIFAR-10/100** and **Tiny-ImageNet** Training and Validation Code [[here](#small-scale-image-classification)]
- [ ] **ImageNet-1K** Training and Validation Code [[here](#imagenet-classification)]
- [x] Image Classification on Google Colab and Notebook Demo [[here](demo.ipynb)]

## Installation

Please check [INSTALL.md](INSTALL.md) for installation instructions.

## Small-scale Image Classification

TODO

## ImageNet Classification

### 1. Training and Validation

See [TRAINING.md](TRAINING.md) for ImageNet-1K training and validation instructions, or refer to our [OpenMixup](https://github.com/Westlake-AI/openmixup/tree/main/configs/classification/imagenet/automix/) implementations. We released pre-trained models on [OpenMixup](https://github.com/Westlake-AI/openmixup/).

Here is a notebook [demo](demo.ipynb) of AutoMix which run the steps to perform inference for image classification and generate mixup samples.

### 2. ImageNet-1K Trained Models

TODO.

<p align="right">(<a href="#top">back to top</a>)</p>

## License

This project is released under the [Apache 2.0 license](LICENSE).

## Acknowledgement

Our implementation is mainly based on the following codebases. We gratefully thank the authors for their wonderful works.

- [pytorch-image-models](https://github.com/rwightman/pytorch-image-models): PyTorch image models, scripts, pretrained weights.
- [OpenMixup](https://github.com/Westlake-AI/openmixup): CAIRI Supervised, Semi- and Self-Supervised Visual Representation Learning Toolbox and Benchmark.

## Citation

If you find this repository helpful, please consider citing:
```
@article{Li2022MogaNet,
  title={AutoMix: Unveiling the Power of Mixup for Stronger Classifiers},
  author={Zicheng Liu and Siyuan Li and Di Wu and Zhiyuan Chen and Lirong Wu and Jianzhu Guo and Stan Z. Li},
  journal={ArXiv},
  year={2021},
  volume={abs/2103.13027}
}
```

<p align="right">(<a href="#top">back to top</a>)</p>
