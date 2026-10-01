---
title: Module 5 - Distributed training with tensor, pipeline, sequence and expert parallelism
---

Wed, Oct 14
: Tensor parallelism
  : Splitting a matrix multiply by columns and by rows, tensor parallelism in the MLP and in attention (Megatron-LM), four AllReduces per layer, tensor parallelism versus ZeRO-3

Mon, Oct 19
: Pipeline, sequence and context parallelism
  : Sequence parallelism, pipeline schedules (naive, all-forward-all-backward, 1F1B) and the pipeline bubble, context parallelism with ring attention and Ulysses

Wed, Oct 21
: Expert parallelism and hybrid parallelism
  : Mixture-of-experts models, expert parallelism, putting the parallelisms together

Mon, Oct 26
: Collective communication
  : All-reduce algorithms, NCCL
