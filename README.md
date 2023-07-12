# MOSS-RLHF

### *MOSS-RLHF & "Secrets of RLHF in Large Language Models Part I: PPO" <br>👉 <a href="https://arxiv.org/abs/2307.04964" target="_blank">[Technical report]</a>  <a href="https://github.com/OpenLMLab/MOSS-RLHF" target="_blank">[Open-source code]*


<p align="center" width="100%">
<a href="https://arxiv.org/abs/2307.04964" target="_blank"><img src="./assets/img/moss.png" alt="MOSS" style="width: 50%; min-width: 300px; display: block; margin: auto;"></a>

[![Code License](https://img.shields.io/badge/Code%20License-Apache_2.0-brightgreen.svg)](./LICENSE)
[![Data License](https://img.shields.io/badge/Data%20License-CC%20BY--NC%204.0-blue.svg)](./DATA_LICENSE)
[![Model License](https://img.shields.io/badge/Model%20License-GNU%20AGPL%203.0-red.svg)](./MODEL_LICENSE)

## 🌠 Introduction

Due to the challenges of reward design, environment interaction, and agent training, coupled with huge trial and error cost of large language models, there is a significant barrier for AI researchers to motivate the development of technical alignment and safe landing of LLMs. The stable training of RLHF has still been a puzzle.
In this technical report, we intend to help researchers to train their models stably with human feedback.

Contributions are summarized as follows: 
1) We release competitive Chinese and English reward models, respectively, which have good cross-model generalization ability, alleviating the cost of relabeling human preference data; 
2) We conduct in-depth analysis on the inner workings of PPO algorithm and propose the PPO-max algorithm to ensure stable model training;
3) We release the complete PPO-max codes to ensure that the LLMs in the current SFT stage can be better aligned with humans.

<div align="center" width="100%">
<img style="width: 80%; min-width: 500px; display: block; margin: auto; margin-bottom: 20px" alt="MOSS-RLHF" src="./assets/img/img1.jpg">
</div>

<div align="center" width="100%">
<img style="width: 80%; min-width: 500px; display: block; margin: auto; margin-bottom: 20px" alt="MOSS-RLHF" src="./assets/img/img2.jpg">
</div>

## 🧾 Open-source List
- A 7B Chinese reward model based on openChineseLlama.
- A 7B English reward model based on Llama-7B.
- Open source code for RL training in large language models.
- ...

## ✨ Start training your own model!

Run code in a few steps.

### 🔩 Requirements & Setup

This repository works on Python 3.8 and PyTorch 1.13.1.

We recommend using the **conda** virtual environment to run the code.

#### Step 1: create a new Python virtual environment
```bash
conda update conda -n base -c defaults
conda create -n rlhf python=3.8
conda activate rlhf
```
#### Step 2: install PyTorch and TensorBoard
```bash
conda install pytorch==1.13.1 pytorch-cuda=11.7 tensorboard -c pytorch -c nvidia
```

#### Step 3: install the remaining dependencies
```bash
conda install datasets accelerate safetensors chardet cchardet -c huggingface -c conda-forge
pip3 install transformers sentencepiece einops triton==1.0.0 rouge jionlp==1.4.14 nltk sacrebleu cpm_kernels

apt install libaio-dev
DS_BUILD_OPS=1 pip install deepspeed
```

### 👉 Start Training

TODO, To be finalised before 15. July 2023

## Citation

```bibtex
@article{zheng2023secrets,
  title={Secrets of RLHF in Large Language Models Part I: PPO}, 
  author={Rui Zheng and Shihan Dou and Songyang Gao and Yuan Hua and Wei Shen and Binghai Wang and Yan Liu and Senjie Jin and Qin Liu and Yuhao Zhou and Limao Xiong and Lu Chen and Zhiheng Xi and Nuo Xu and Wenbin Lai and Minghao Zhu and Cheng Chang and Zhangyue Yin and Rongxiang Weng and Wensen Cheng and Haoran Huang and Tianxiang Sun and Hang Yan and Tao Gui and Qi Zhang and Xipeng Qiu and Xuanjing Huang},
  year={2023}
}
```
