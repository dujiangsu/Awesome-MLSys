# Awesome-Transformer-System
![Awesome](https://awesome.re/badge.svg) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/dujiangsu/Awesome-Large-Model-Inference/pulls)

A curated list of awesome projects and papers for Transformer System on **Data-center/Mobile**. Everything is continuously updating. Welcome contribution!

## Contents

- [Papers](#papers)
  - [Parallelism Acceleration](#Parallelism-Acceleration)
  - [Resouce-efficient Transformer](#Resouce-efficient-Transformer)
  - [Transformer Serving](#Transformer-Serving)

## Papers

### Parallelism Acceleration

#### 1. Pipeline Parallelism

- [GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://proceedings.neurips.cc/paper/2019/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf) by Google AI, NIPS 2019

#### 2. Tensor Parallelism

- [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](http://arxiv.org/abs/1909.08053) by NVIDIA, 2020

### Resouce-efficient Transformer

#### 1. Computational Optimization

- [TurboTransformers: An Efficient GPU Serving System For Transformer Models](https://dl.acm.org/doi/pdf/10.1145/3437801.3441578) by Wechat AI, PPoPP 2021

#### 2. Memory Reduction/Management

- [FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](http://arxiv.org/abs/2205.14135) by Tri Dao(Standford) et al., ICML 2022
- [PatrickStar: Parallel Training of Pre-trained Models via Chunk-based Memory Management](http://arxiv.org/abs/2108.05818) by Wechat AI, TPDS 2022

### Transformer Serving

#### 1. Inference Latency Optimization

- [DeepSpeed Inference: Enabling Efficient Inference of Transformer Models at Unprecedented Scale](http://arxiv.org/abs/2207.00032) by Microsoft, SC 2022

#### 2. Variable-Length Inputs for LLM

- [ByteTransformer: A High-Performance Transformer Boosted for Variable-Length Inputs](http://arxiv.org/abs/2210.03052) by ByteDance, 2023