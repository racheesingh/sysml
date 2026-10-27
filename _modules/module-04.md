---
title: Module 4 - Distributed training with data parallelism
---

Mon, Oct 5
: [Introduction to distributed training and data parallelism](https://canvas.cornell.edu/courses/92233/files/16258322)
  : Finishing RDMA (how OpenAI's MRC spreads traffic over many paths and recovers from loss, MRC in production), why the network matters for training, model FLOPs utilization (MFU), four ways to split a training step, data parallelism with the AllReduce, overlapping the AllReduce with the backward pass<br>Optional reading: (1) [PyTorch Distributed: Experiences on Accelerating Data Parallel Training](https://arxiv.org/abs/2006.15704)
    (2) [Resilient AI Supercomputer Networking using MRC and SRv6](https://arxiv.org/abs/2605.04333)
    (3) [The Ultra-Scale Playbook: Training LLMs on GPU Clusters](https://huggingface.co/spaces/nanotron/ultrascale-playbook) (Hugging Face), data parallelism section

Wed, Oct 7
: [Finishing data parallelism, and ZeRO-1](https://canvas.cornell.edu/courses/92233/files/16274002)
  : No in-person class: watch the [recorded lecture](https://canvas.cornell.edu/courses/92233/files/16310408). When the backward pass hides the AllReduce (tokens per GPU), bucketing gradients, gradient accumulation, three limits of data parallelism, 16 bytes of training state per parameter, ReduceScatter and AllGather, ZeRO-1 (sharding the optimizer state)<br>Optional reading: (1) [Mixed Precision Training](https://arxiv.org/abs/1710.03740)
    (2) [An Empirical Model of Large-Batch Training](https://arxiv.org/abs/1812.06162)
    (3) [ZeRO: Memory Optimizations Toward Training Trillion Parameter Models](https://arxiv.org/abs/1910.02054)

Mon, Oct 12
: No Class (Fall Break)

Wed, Oct 14
: [ZeRO-2, ZeRO-3 and FSDP](https://canvas.cornell.edu/courses/92233/files/16318025)
  : Each GPU owns a fixed part of the parameters, ZeRO-2 (sharding the gradients), ZeRO-3 (sharding the weights), memory per GPU for a 7.5B-parameter model on 64 GPUs, PyTorch Fully Sharded Data Parallel (FSDP) and prefetching the AllGathers<br>Optional reading: [PyTorch FSDP: Experiences on Scaling Fully Sharded Data Parallel](https://arxiv.org/abs/2304.11277)
