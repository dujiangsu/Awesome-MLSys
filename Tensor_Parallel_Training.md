- Tensor Parallelism
    - [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](http://arxiv.org/abs/1909.08053) by NVIDIA, 2020
    > 1. Partition the layers of Transformer **vertically**. Different parts of one layer are assigned to different devices and calculated in parallel.
    > 2. Need to sync, which introduces high communication overhead. 
    
    - [Efficient Large-Scale Language Model Training on GPU Clusters using Megatron-LM](https://arxiv.org/abs/2104.04473)  by NVIDIA, 2021
    > 1. Introduce **PTD-P**, a big model parallel training technique that combines Tenor Parallel(TP), Pipeline Parallel(PP) and Data Parallel(DP), which can scale model training to thousands of GPUs.