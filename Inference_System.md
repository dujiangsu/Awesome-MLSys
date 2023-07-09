## Transformer Serving

### Inference Latency Optimization

- [DeepSpeed Inference: Enabling Efficient Inference of Transformer Models at Unprecedented Scale](http://arxiv.org/abs/2207.00032) by Microsoft, SC 2022

### Variable-Length Inputs for LLM

- [ByteTransformer: A High-Performance Transformer Boosted for Variable-Length Inputs](http://arxiv.org/abs/2210.03052) by ByteDance, 2023


### Mobile Serving

  - [CoDL: efficient CPU-GPU co-execution for deep learning inference on mobile devices](https://dl.acm.org/doi/10.1145/3498361.3538932) by  Centrel South University & Microsoft, MobileSys 2022
  > 1. Introduce **CoDL**, a DL CPU-GPU concurrent inference framework on mobile devices which can utilize heterogeneous processors to seepdup model inference.
  > 2. Use hybrid-type-friendly data sharing to allow each processor to use its efficient data type for inference.
  > 3. Use a lightweight and accurate latency predictor to direct the operator partition while inferencing.


  - [NN-Stretch: Automatic Neural Network Branching for Parallel Inference on Heterogeneous Multi-Processors](https://dl.acm.org/doi/abs/10.1145/3581791.3596870) by Jianyu Wei (USTC & Microsoft), MobileSys 2023 
  > 1. Propose **NN-Stretch**, a new model inference adaption strategy for heterogeneous processors (CPU, GPU, DSP) on mobile devices. NN-Stretch can accelerate inference while preserving accuracy.
  > 2. The key idea is to horizontally stretch a model structure, from a long and narrow model to a short and wide one with multiple branches, named as "**Branch Parallelsim**".
