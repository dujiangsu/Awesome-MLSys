### Baisc Pipeline Parallelism 
- [GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://proceedings.neurips.cc/paper/2019/file/093f65e080a295f8076b1c5722a46aa2-Paper.pdf) by Google AI, NIPS 2019 \
[<img src="https://img.shields.io/badge/Main-Pipeline Training-Green.svg?logo=LOGO">](<LINK>)
> 1. Synchronous training.
> 2. Partition the network **horizontally** into several stages. Stages are assigned to different devices. Data flow through stages (pipeline) and communication only happens between stage bounds.
> 3. Use **re-materialization** to reduce memory usage, but introduce redundant computation.

- [PipeDream: Generalized Pipeline Parallelism for DNN Training](https://cs.stanford.edu/~matei/papers/2019/sosp_pipedream.pdf) by Microsoft, SOSP 2019 \
[<img src="https://img.shields.io/badge/Main-Pipeline Training-Green.svg?logo=LOGO">](<LINK>)
> 1. **Asynchronous** training.
> 2.  Further improve GPipe by carefully re-arranging the sequence of forward and backward stages, that is, **1F1B**(1-forward-1-backward) mode, to reduce bubbles.
> 3.  Use **weight stashing** to avoid possible inaccuracies caused by asynchronous computation.

- [DAPPLE: a pipelined data parallel approach for training large models](https://dl.acm.org/doi/10.1145/3437801.3441593) by Alibaba Cloud, PPoPP'21 \
[<img src="https://img.shields.io/badge/Main-Pipeline Training-Green.svg?logo=LOGO">](<LINK>)
> 1. Synchronous training.
> 2. Use DAPPLE schedule to reduce memory usage. Similar to PipeDream, DAPPLE also re-arranges the sequence of forward and backward stages.
> 3. Use DAPPLE planner to automatically generate the optimal DP+PP hybrid parallel strategy and stage-to-device placement strategy.

- [Chimera: efficiently training large-scale neural networks with bidirectional pipelines](https://dl.acm.org/doi/10.1145/3458817.3476145) by ETH Zurich, SC'21 \
[<img src="https://img.shields.io/badge/Main-Pipeline Training-Green.svg?logo=LOGO">](<LINK>)
> 1. Synchronous training.
> 2. Use a **bidirectional pipeline** which can balance pipeline efficiency, memory overhead, and model convergence.



