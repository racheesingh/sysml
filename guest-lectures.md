---
layout: page
title: Guest Lectures
description: Talk titles, abstracts and speaker bios for the CS5470 guest lectures.
---

# Guest Lectures

Guest lectures take place during regular class time (2:55–4:10 PM) in Hollister Hall B14.

## Mon, Nov 2: Abhinav Jangda (Microsoft Research)

**SubCubic-LLM: Faster LLM Inference using Strassen-like Algorithms for Matrix Multiplication**

The speaker joins remotely over Zoom.

**Abstract.** Generalized Matrix Multiplication (GeMM) is the basis of today's Large Language Models. Existing LLM serving and training systems employ extremely efficient implementations of the cubic algorithm. These implementations already achieve peak throughput on GPUs, CPUs, TPUs, and other accelerators. So, the natural question is how can we further reduce the serving runtime, cost, and energy of LLMs?

In this talk, I will present my work of implementing fast and efficient sub-cubic GeMM algorithms on NVIDIA GPUs. While sub-cubic algorithms, like the Strassen family of GeMM algorithms, have lower algorithmic complexity than the cubic algorithm, they are significantly harder to implement efficiently on GPUs because their recursive structure requires significantly more loads and stores. I will show that my compiler, SubCuber, generated CUDA kernels are up to 22% faster for 32-bit Floats and 18% faster for 16-bit Floats compared to NVIDIA cuBLAS and CUTLASS implementations of the cubic algorithm. I will also present SubCubic-LLM, an end-to-end serving system using sub-cubic kernels that ensure zero to very little accuracy drop while also providing up to 15% lower Time-to-First-Token and Time-per-Output-Token than state-of-the-art LLM serving systems.

**Bio.** Abhinav Jangda is a Principal Researcher at the RiSE Group in Microsoft Research Redmond. His research focuses on optimizing GPU kernels and LLM infrastructure to reduce the training and inference cost of LLMs. His work has been published in several high quality venues and has received several awards including Best Paper Award Honourable Mention at ASPLOS 2026, Best Paper Award at PACT 2020, and ACM SIGPLAN Distinguished Paper Award at OOPSLA 2019. He received his MS and PhD from University of Massachusetts, Amherst.

## Wed, Nov 4: Benjamin Klenk (NVIDIA Research)

**From the Chip to the Rack and Beyond: Architecture for Large Language Models**

The speaker joins remotely over Zoom.

**Abstract.** Frontier LLMs no longer fit on a single GPU, and the systems that run them have grown from a chip to a rack, and now to several racks working as one. The interconnect that ties those GPUs together has become one of the central problems in system design. We will look at how LLM training and inference shape the hardware underneath them, from the way parallelism shows up as traffic on the fabric to the architectural trade-offs that follow from it. I will discuss how the questions of bandwidth, latency, semantics, and energy are being answered differently in the LLM era, and what that means for how we build rack-scale systems and beyond. I will close with some of the open problems in this space and what we are working on at NVIDIA Research.

**Bio.** Benjamin Klenk joined NVIDIA in 2017 after completing his Ph.D. in Computer Engineering at Heidelberg University, Germany. His doctoral research was among the first to explore direct GPU-to-GPU communication models for GPU-accelerated high-performance computing. At NVIDIA, he contributed to several GPU on-chip networks and NVSwitch architectures, including in-network computing for collective operations. He now leads the Networking Research Group, whose research focuses on network and system architectures for energy-efficient, large-scale AI systems, heterogeneous accelerators, and multi-rack NVLink-class domains.

## Mon, Nov 30: To Be Announced

Speaker, title and abstract to be announced.
