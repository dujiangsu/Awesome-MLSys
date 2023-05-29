- Tensor Parallelism
    - [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](http://arxiv.org/abs/1909.08053) by NVIDIA, 2020
    > 1. Partition the layers of Transformer **vertically**. Different parts of one layer are assigned to different devices and calculated in parallel.
    > 2. Need to sync, which introduces high communication overhead. 