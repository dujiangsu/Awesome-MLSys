## Parallel Acceleration

### Tensor Parallelism 
- [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](http://arxiv.org/abs/1909.08053) by NVIDIA, 2020 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green">
> 1. Partition the layers of Transformer **vertically**. Different parts of one layer are assigned to different devices and calculated in parallel.
> 2. Need to sync, which introduces high communication overhead. 

<br/>

### Pipeline Parallelism 
- [GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://proceedings.neurips.cc/paper/2019/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf) by Google AI, NIPS 2019 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green">
> 1. Synchronous training.
> 2. Partition the network **horizontally** into several stages. Stages are assigned to different devices. Data flow through stages (pipeline) and communication only happens between stage bounds.
> 3. Use **re-materialization** to reduce memory usage, but introduce redundant computation.

- [PipeDream: Generalized Pipeline Parallelism for DNN Training](https://cs.stanford.edu/~matei/papers/2019/sosp_pipedream.pdf) by Microsoft, SOSP 2019 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green">
> 1. **Asynchronous** training.
> 2.  Further improve GPipe by carefully re-arranging the sequence of forward and backward stages, that is, **1F1B**(1-forward-1-backward) mode, to reduce bubbles.
> 3.  Use **weight stashing** to avoid possible inaccuracies caused by asynchronous computation.

- [DAPPLE: a pipelined data parallel approach for training large models](https://dl.acm.org/doi/10.1145/3437801.3441593) by Alibaba Cloud, PPoPP 2021 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green">
> 1. Synchronous training.
> 2. Use DAPPLE schedule to reduce memory usage. Similar to PipeDream, DAPPLE also re-arranges the sequence of forward and backward stages.
> 3. Use DAPPLE planner to automatically generate the optimal DP+PP hybrid parallel strategy and stage-to-device placement strategy.

- [Chimera: efficiently training large-scale neural networks with bidirectional pipelines](https://dl.acm.org/doi/10.1145/3458817.3476145) by ETH Zurich, SC 2021 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green"> 
> 1. Synchronous training.
> 2. Use a **bidirectional pipeline** which can balance pipeline efficiency, memory overhead, and model convergence.

<br/>

### Sequence Parallelism 
- [Sequence Parallelism: Long Sequence Training from System Perspective](https://aclanthology.org/2023.acl-long.134/) by NUS, ACL 2023 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green">
> 1. To solve the long sequence training problem from system perspective, the authors propose **Sequence Parallelism**, a memory-efficient parallelism which splits the input sequence into multiple chunks to its corresponding device.
> 2. To compute the attention output, Sequence Parallelism integrates ring-style communication with self-attention calculation and proposed **Ring Self-Attention**(RSA). 

<br/>

### Hybrid Parallelism 
- [Efficient Large-Scale Language Model Training on GPU Clusters using Megatron-LM](https://arxiv.org/abs/2104.04473) by NVIDIA, 2021 \
   <img src="https://img.shields.io/badge/Main-Parallel Acceleration-Green">
> 1.  Introduce PTD-P, a 3-D parallel training technique that combines Tenor Parallel(TP), Pipeline Parallel(PP) and Data Parallel(DP), which can scale model training to thousands of GPUs. 