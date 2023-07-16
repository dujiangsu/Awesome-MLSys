## Resouce-efficient Training

### Efficient Attention
- [Synthesizer: Rethinking Self-Attention for Transformer Models](http://proceedings.mlr.press/v139/tay21a.html) by Google Research, ICML 2021 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Propose SYNTHESIZER model,  a Transformer model with self-attention modules replaced with Synthetic Attention modules. 
> 2. In Dense Synthesizers, they use two feed-forward layers with ReLU activations to replace the QV^T dot product self-attention. In Random Synthesizers, the attention weights are initialized to random values.
> 3. Synthetic attention demonstrates competitive performance compared to vanilla self-attention on a wide range of language tasks.


- [Fixed Encoder Self-Attention Patterns in Transformer-Based Machine Translation](https://aclanthology.org/2020.findings-emnlp.49.pdf) by UH, EMNLP 2020 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. It investigated the replacement of learnable encoder self-attention heads by fixed, non-learnable attentive patterns.
> 2. The fixed patterns reflect the importance of locality and figure out that maybe not all encoder self-attention heads need to be learned to achieve SOTA results in machine translation.

- [Linformers: Self-attention with linear complexity](https://arxiv.org/abs/2101.10277) by Facebook, 2020 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Propose a new self-attention mechanism, Linformer, which use a low-rank matrix to approximate self-attention mechanism. 
> 2. Linformer shows competitive performance to the standard Transformer models while being much more memory- and time-efficient.

- [Reformer: The Efficient Transformer](https://iclr.cc/virtual_2020/poster_rkgNKkHtvB.html) by Berkeley & Google Research, ICLR 2020 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Propose Reformer, which uses two techniques to improve the efficiency of Transformers. It replaces dot-product attention by one that uses locality-sensitive hashing (LSH), and uses reversible residual layers instead of the standard residuals.
> 2. Reformer shows competitive performance compared to villina Transformer while being more memory-efficient and much faster on long sequences.



<br/>

### Memory Reduction/Management
- [ZeRO: memory optimizations toward training trillion parameter models](https://dl.acm.org/doi/pdf/10.5555/3433701.3433727) by Microsoft, SC 2020 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Reduce memory occupancy by dividing model states into different devices, including **optimizer status, gradients and parameters**, instead of replicating them.
> 2. Introduce a few additional communication overhead.

- [CAME: Confidence-guided Adaptive Memory Efficient Optimization](https://aclanthology.org/2023.acl-long.243.pdf) by NUS & Huawei, ACL 2023 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Propose CAME, a memory-efficient optimizer which compensates for parameter updates based on confidence level and trades a small amount of extra computation for memory savings, capable of mathematical approximation.

- [PatrickStar: Parallel Training of Pre-trained Models via Chunk-based Memory Management](http://arxiv.org/abs/2108.05818) by Wechat AI, TPDS 2022 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">

<br/>

### I/O Optimization 
- [Data movement is all you need：A case study on optimization Transformers](https://proceedings.mlsys.org/paper_files/paper/2021/file/bc86e95606a6392f51f95a8de106728d-Paper.pdf) by ETH Zurich, MLSys 2021 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Present a recipe for globally optimizing data movement in transformers. They first build a dataflow graph to classify the operators into three types, and then try to fuse kernels to maximum data reuse for data movement reducement.

- [ FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://arxiv.org/abs/2205.14135) By Standford, ICML workshop 2022 \
   <img src="https://img.shields.io/badge/Main-Efficient Training-Green">
> 1. Propose FlashAttention, an IO-aware exact attention algorithm that uses tiling to reduce the number of memory reads/writes between GPU high bandwidth memory (HBM) and GPU on-chip SRAM. With the optimization, the training of Transformer can be faster and more memory-efficient.