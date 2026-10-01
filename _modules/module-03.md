---
title: Module 3 - Hardware infrastructure for machine learning
---

Mon, Sep 21
: [AI infrastructure I: from one GPU to many](https://canvas.cornell.edu/courses/92233/files/16129018)
  : Using the roofline model, communication as the third resource, the bandwidth hierarchy, scale-up versus scale-out, xAI's Colossus<br>Optional reading: [xAI's Colossus 2: First Gigawatt Datacenter in the World](https://newsletter.semianalysis.com/p/xais-colossus-2-first-gigawatt-datacenter) (SemiAnalysis)

Wed, Sep 23
: [AI infrastructure II: scale-up domains and TPUs](https://canvas.cornell.edu/courses/92233/files/16195074)
  : NVIDIA DGX servers, NVLink and NVSwitch, GB200 NVL72, the TPU chip and its systolic array<br>Optional reading: (1) [NVIDIA Hopper Architecture In-Depth](https://developer.nvidia.com/blog/nvidia-hopper-architecture-in-depth/)
    (2) [NVIDIA GB200 NVL72](https://www.nvidia.com/en-us/data-center/gb200-nvl72/)
    (3) How to Scale Your Model, [How to Think About TPUs](https://jax-ml.github.io/scaling-book/tpus/)

Mon, Sep 28
: [AI infrastructure III: TPU pods and scale-out networks](https://canvas.cornell.edu/courses/92233/files/16195597)
  : TPU generations, the ICI torus and optical circuit switches, Clos and rail-optimized fabrics<br>Optional reading: (1) [TPU v4: An Optically Reconfigurable Supercomputer for Machine Learning](https://arxiv.org/abs/2304.01433)
    (2) [A Scalable, Commodity Data Center Network Architecture](https://dl.acm.org/doi/10.1145/1402958.1402967)
    (3) [NVIDIA DGX SuperPOD reference architecture: network fabrics](https://docs.nvidia.com/dgx-superpod/reference-architecture-scalable-infrastructure-h100/latest/network-fabrics.html)

Wed, Sep 30
: [AI infrastructure IV: RDMA](https://canvas.cornell.edu/courses/92233/files/16223660)
  : Why not TCP, registered memory and queue pairs, InfiniBand and RoCE, priority flow control (PFC), what breaks at 100,000 GPUs, OpenAI's Multipath Reliable Connection (MRC)<br>Optional reading: (1) [RDMA lecture slides](https://courses.physics.illinois.edu/cs598hpn/fa2022/slides/lect18-rdma.pdf) (Radhika Mittal, UIUC)
    (2) [RDMA over Ethernet for Distributed AI Training at Meta Scale](https://dl.acm.org/doi/10.1145/3651890.3672233)
    (3) [The Multipath Reliable Connection (MRC) Transport](https://arxiv.org/abs/2606.18170)

Try it on your own
: [Train a small LLM from scratch](https://www.manning.com/books/build-a-large-language-model-from-scratch)
  : Not a class meeting; work through the notebook before Module 4 starts
