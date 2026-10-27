---
title: Module 5 - Distributed training with tensor, pipeline, sequence and expert parallelism
---

Mon, Oct 19
: [Finishing ZeRO, and tensor parallelism](https://canvas.cornell.edu/courses/92233/files/16356898)
  : FSDP in PyTorch (`fully_shard`, hybrid sharding), the cost of each ZeRO stage, the limits of ZeRO, splitting a matrix multiply by columns and by rows, tensor parallelism in the MLP and in attention (Megatron-LM), four AllReduces per layer, why throughput per GPU drops past one server<br>Optional reading: (1) [Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053)
    (2) [Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://arxiv.org/abs/2104.04473)
    (3) PyTorch documentation, [`fully_shard` (FSDP2)](https://docs.pytorch.org/docs/stable/distributed.fsdp.fully_shard.html)

Wed, Oct 21
: [Sequence and pipeline parallelism](https://canvas.cornell.edu/courses/92233/files/16378234)
  : Memory with tensor parallelism, tensor parallelism versus ZeRO-3, sequence parallelism (splitting LayerNorm and dropout along the tokens), pipeline parallelism: the bubble, micro-batches, and the all-forward-all-backward (AFAB) and one-forward-one-backward (1F1B) schedules<br>Optional reading: (1) [Reducing Activation Recomputation in Large Transformer Models](https://arxiv.org/abs/2205.05198)
    (2) [GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://arxiv.org/abs/1811.06965)
    (3) [PipeDream: Generalized Pipeline Parallelism for DNN Training](https://dl.acm.org/doi/10.1145/3341301.3359646)

Mon, Oct 26
: [Finishing pipeline parallelism, and mixture of experts](https://canvas.cornell.edu/courses/92233/files/16422420)
  : Shrinking the pipeline bubble (interleaved stages, DualPipe), pipeline parallelism versus ZeRO-3, mixture-of-experts layers (more parameters without more compute per token), routing tokens to the top-k experts, why routing is often unbalanced<br>Optional reading: (1) [Outrageously Large Neural Networks: The Sparsely-Gated Mixture-of-Experts Layer](https://arxiv.org/abs/1701.06538)
    (2) [Switch Transformers: Scaling to Trillion Parameter Models with Simple and Efficient Sparsity](https://arxiv.org/abs/2101.03961)
    (3) [DeepSeek-V3 Technical Report](https://arxiv.org/abs/2412.19437) (DualPipe)

Wed, Oct 28
: Expert parallelism, context parallelism and collectives in practice
  : Balancing the load across experts, expert parallelism with all-to-all dispatch and combine, case studies (Mixtral 8x7B, DeepSeek-V3), context parallelism with ring attention, putting the five parallelisms together, collectives in practice (ring AllReduce, switches that add, vLLM's custom AllReduce, DeepEP)<br>Optional reading: (1) [GShard: Scaling Giant Models with Conditional Computation and Automatic Sharding](https://arxiv.org/abs/2006.16668)
    (2) [Ring Attention with Blockwise Transformers for Near-Infinite Context](https://arxiv.org/abs/2310.01889)
    (3) [DeepEP: an efficient expert-parallel communication library](https://github.com/deepseek-ai/DeepEP) (DeepSeek)
