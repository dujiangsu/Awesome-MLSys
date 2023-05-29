## Memory Reduction/Management
- Memory Reduction/Management
    - [ZeRO: memory optimizations toward training trillion parameter models](https://dl.acm.org/doi/pdf/10.5555/3433701.3433727) by Microsoft, SC 2020
    > 1. Reduce memory occupancy by dividing model states into different devices, including **optimizer status, gradients and parameters**, instead of replicating them.
    > 2. Introduce a few additional communication overhead.
- [FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](http://arxiv.org/abs/2205.14135) by Tri Dao(Standford) et al., ICML 2022
- [PatrickStar: Parallel Training of Pre-trained Models via Chunk-based Memory Management](http://arxiv.org/abs/2108.05818) by Wechat AI, TPDS 2022