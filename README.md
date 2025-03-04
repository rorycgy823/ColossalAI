# Colossal-AI
<div id="top" align="center">

   [![logo](https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/Colossal-AI_logo.png)](https://www.colossalai.org/)

   An integrated large-scale model training system with efficient parallelization techniques.

   <h3> <a href="https://arxiv.org/abs/2110.14883"> Paper </a> | 
   <a href="https://www.colossalai.org/"> Documentation </a> | 
   <a href="https://github.com/hpcaitech/ColossalAI-Examples"> Examples </a> |   
   <a href="https://github.com/hpcaitech/ColossalAI/discussions"> Forum </a> | 
   <a href="https://medium.com/@hpcaitech"> Blog </a></h3>

   [![Build](https://github.com/hpcaitech/ColossalAI/actions/workflows/build.yml/badge.svg)](https://github.com/hpcaitech/ColossalAI/actions/workflows/build.yml)
   [![Documentation](https://readthedocs.org/projects/colossalai/badge/?version=latest)](https://colossalai.readthedocs.io/en/latest/?badge=latest)
   [![CodeFactor](https://www.codefactor.io/repository/github/hpcaitech/colossalai/badge)](https://www.codefactor.io/repository/github/hpcaitech/colossalai)
   [![HuggingFace badge](https://img.shields.io/badge/%F0%9F%A4%97HuggingFace-Join-yellow)](https://huggingface.co/hpcai-tech)
   [![slack badge](https://img.shields.io/badge/Slack-join-blueviolet?logo=slack&amp)](https://join.slack.com/t/colossalaiworkspace/shared_invite/zt-z7b26eeb-CBp7jouvu~r0~lcFzX832w)
   [![WeChat badge](https://img.shields.io/badge/微信-加入-green?logo=wechat&amp)](https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/WeChat.png)
   

   | [English](README.md) | [中文](README-zh-Hans.md) |

</div>

## Table of Contents
<ul>
 <li><a href="#Why-Colossal-AI">Why Colossal-AI</a> </li>
 <li><a href="#Features">Features</a> </li>
 <li>
   <a href="#Parallel-Demo">Parallel Demo</a> 
   <ul>
     <li><a href="#ViT">ViT</a></li>
     <li><a href="#GPT-3">GPT-3</a></li>
     <li><a href="#GPT-2">GPT-2</a></li>
     <li><a href="#BERT">BERT</a></li>
     <li><a href="#PaLM">PaLM</a></li>
   </ul>
 </li>
 <li>
   <a href="#Single-GPU-Demo">Single GPU Demo</a> 
   <ul>
     <li><a href="#GPT-2-Single">GPT-2</a></li>
     <li><a href="#PaLM-Single">PaLM</a></li>
   </ul>
 </li>

 <li>
   <a href="#Installation">Installation</a>
   <ul>
     <li><a href="#PyPI">PyPI</a></li>
     <li><a href="#Install-From-Source">Install From Source</a></li>
   </ul>
 </li>
 <li><a href="#Use-Docker">Use Docker</a></li>
 <li><a href="#Community">Community</a></li>
 <li><a href="#contributing">Contributing</a></li>
 <li><a href="#Quick-View">Quick View</a></li>
   <ul>
     <li><a href="#Start-Distributed-Training-in-Lines">Start Distributed Training in Lines</a></li>
     <li><a href="#Write-a-Simple-2D-Parallel-Model">Write a Simple 2D Parallel Model</a></li>
   </ul>
 <li><a href="#Cite-Us">Cite Us</a></li>
</ul>

## Why Colossal-AI
<div align="center">
   <a href="https://youtu.be/KnXSfjqkKN0">
   <img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/JamesDemmel_Colossal-AI.png" width="600" />
   </a>

   Prof. James Demmel (UC Berkeley): Colossal-AI makes distributed training efficient, easy and scalable.
</div>

<p align="right">(<a href="#top">back to top</a>)</p>

## Features

Colossal-AI provides a collection of parallel training components for you. We aim to support you to write your
distributed deep learning models just like how you write your model on your laptop. We provide user-friendly tools to kickstart
distributed training in a few lines.

- Parallelism strategies
  - Data Parallelism
  - Pipeline Parallelism
  - 1D, [2D](https://arxiv.org/abs/2104.05343), [2.5D](https://arxiv.org/abs/2105.14500), [3D](https://arxiv.org/abs/2105.14450) Tensor Parallelism
  - [Sequence Parallelism](https://arxiv.org/abs/2105.13120)
  - [Zero Redundancy Optimizer (ZeRO)](https://arxiv.org/abs/2108.05818)

- Heterogeneous Memory Menagement 
  - [PatrickStar](https://arxiv.org/abs/2108.05818)

- Friendly Usage
  - Parallelism based on configuration file

<p align="right">(<a href="#top">back to top</a>)</p>

## Parallel Demo
### ViT
<p align="center">
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/ViT.png" width="450" />
</p>

- 14x larger batch size, and 5x faster training for Tensor Parallelism = 64

### GPT-3
<p align="center">
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/GPT3.png" width=700/>
</p>

- Save 50% GPU resources, and 10.7% acceleration

### GPT-2
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/GPT2.png" width=800/>

- 11x lower GPU memory consumption, and superlinear scaling efficiency with Tensor Parallelism

<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/(updated)GPT-2.png" width=800>

- 24x larger model size on the same hardware
- over 3x acceleration
### BERT
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/BERT.png" width=800/>

- 2x faster training, or 50% longer sequence length

### PaLM
- [PaLM-colossalai](https://github.com/hpcaitech/PaLM-colossalai): Scalable implementation of Google's Pathways Language Model ([PaLM](https://ai.googleblog.com/2022/04/pathways-language-model-palm-scaling-to.html)).

Please visit our [documentation and tutorials](https://www.colossalai.org/) for more details.

<p align="right">(<a href="#top">back to top</a>)</p>

## Single GPU Demo

### GPT-2
<p id="GPT-2-Single" align="center">
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/GPT2-GPU1.png" width=450/>
</p>

- 20x larger model size on the same hardware

### PaLM
<p id="PaLM-Single" align="center">
<img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/PaLM-GPU1.png" width=450/>
</p>

- 34x larger model size on the same hardware

<p align="right">(<a href="#top">back to top</a>)</p>

## Installation

### Download From Official Releases

You can visit the [Download](/download) page to download Colossal-AI with pre-built CUDA extensions.


### Download From Source

> The version of Colossal-AI will be in line with the main branch of the repository. Feel free to raise an issue if you encounter any problem. :)

```shell
git clone https://github.com/hpcaitech/ColossalAI.git
cd ColossalAI

# install dependency
pip install -r requirements/requirements.txt

# install colossalai
pip install .
```

If you don't want to install and enable CUDA kernel fusion (compulsory installation when using fused optimizer):

```shell
NO_CUDA_EXT=1 pip install .
```

<p align="right">(<a href="#top">back to top</a>)</p>

## Use Docker

Run the following command to build a docker image from Dockerfile provided.

```bash
cd ColossalAI
docker build -t colossalai ./docker
```

Run the following command to start the docker container in interactive mode.

```bash
docker run -ti --gpus all --rm --ipc=host colossalai bash
```

<p align="right">(<a href="#top">back to top</a>)</p>

## Community

Join the Colossal-AI community on [Forum](https://github.com/hpcaitech/ColossalAI/discussions),
[Slack](https://join.slack.com/t/colossalaiworkspace/shared_invite/zt-z7b26eeb-CBp7jouvu~r0~lcFzX832w),
and [WeChat](https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/WeChat.png "qrcode") to share your suggestions, feedback, and questions with our engineering team.

## Contributing

If you wish to contribute to this project, please follow the guideline in [Contributing](./CONTRIBUTING.md).

Thanks so much to all of our amazing contributors!

<a href="https://github.com/hpcaitech/ColossalAI/graphs/contributors"><img src="https://raw.githubusercontent.com/hpcaitech/public_assets/main/colossalai/img/contributor_avatar.png" width="800px"></a>

*The order of contributor avatars is randomly shuffled.*

<p align="right">(<a href="#top">back to top</a>)</p>

## Quick View

### Start Distributed Training in Lines

```python
parallel = dict(
    pipeline=2,
    tensor=dict(mode='2.5d', depth = 1, size=4)
)
```

### Start Heterogeneous Training in Lines

```python
zero = dict(
    model_config=dict(
        tensor_placement_policy='auto',
        shard_strategy=TensorShardStrategy(),
        reuse_fp16_shard=True
    ),
    optimizer_config=dict(initial_scale=2**5, gpu_margin_mem_ratio=0.2)
)

```

<p align="right">(<a href="#top">back to top</a>)</p>

## Cite Us

```
@article{bian2021colossal,
  title={Colossal-AI: A Unified Deep Learning System For Large-Scale Parallel Training},
  author={Bian, Zhengda and Liu, Hongxin and Wang, Boxiang and Huang, Haichen and Li, Yongbin and Wang, Chuanrui and Cui, Fan and You, Yang},
  journal={arXiv preprint arXiv:2110.14883},
  year={2021}
}
```

<p align="right">(<a href="#top">back to top</a>)</p>