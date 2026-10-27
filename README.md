---
layout: home
title: Systems for Large-Scale Machine Learning
nav_exclude: true
permalink: /:path/
seo:
  type: Course
  name: Systems for large scale machine learning
---

# Cornell CS5470: Systems for Large-scale ML (Fall 2026)
This course explores the systems challenges of training and serving large-scale ML models like GPT, LLaMA, and DeepSeek. You will learn how to design and operate distributed training and inference on multi-accelerator hardware, with attention to performance, memory, communication, and fault tolerance. The emphasis is on both theory and practice so we will combine  with hands-on programming sessions, assignments and projects. By the end, you will have practical experience tackling the core bottlenecks of modern ML systems.

**Acknowledgement**: this course is supported by a [NERSC](https://www.nersc.gov/) Education Allocation Award.


# Access to GPU Compute resources
If you are enrolled in the class or you are on the waitlist, create a NERSC account by following the instructions [here](https://docs.nersc.gov/accounts/). Each created account undergoes vetting so please do this as soon as you can.

# Course Policies
You are allowed to use generative AI tools of your choice for graded components of the class. The submission may ask for which tools you used and the corresponding prompts.

# Academic Honesty Policies
You are not allowed to share any code and text (including reports, summaries and prompts) that you use to complete projects and assignments.

# Grading Policy:
- Class Participation (10%)
- Programming Assignments (40%)
- Course Project (45%)
- End of semester survey (5%)

# Programming Assignments
This course has 3 programming assignments. All of them run on the A100 GPUs of Perlmutter, and the instructions and starter code for each are in its GitHub repository. Post questions on [Ed](https://edstem.org/us/courses/104230/discussion).

## Assignment 1: vLLM benchmarking and profiling
[Instructions and starter code](https://github.com/jamalh110/CS5470_Assignment1) · Due Saturday, September 19, 11:59 PM · Submit `<netid>_a1.zip` on Canvas

- Serve Llama-3.1-8B with vLLM on 1, 2 and 4 GPUs (tensor parallelism) and measure the time to first token (TTFT) and the time per output token (TPOT)
- Plot how TTFT and TPOT change with the number of GPUs
- Profile the 4-GPU run with NVIDIA Nsight Systems to find the kernels that take the most time and the share spent in the AllReduce
- Pick a hypothesis for where scaling falls short, and test it by changing one server setting

## Assignment 2: Scheduling prompts
[Instructions and starter code](https://github.com/byungsoo-oh/CS5470_Assignment2) · Due Friday, October 16, 11:59 PM · Submit `<netid>_a2.zip` on Gradescope

- Serve CodeLlama-34B on 2 GPUs, send a burst of 50 requests, and plot TTFT, TPOT and KV cache usage
- Use the server logs to find what keeps vLLM from batching all the prompts at once
- Change vLLM's scheduler to a preemptive, fair policy, modeled on Linux's Completely Fair Scheduler, that swaps the KV cache of preempted prompts to CPU memory
- Sweep how often the scheduler preempts, and plot the tradeoff between TTFT and TPOT

## Assignment 3
To be announced.

For each assignment and hands-on session, we will allocate GPU hours on Perlmutter to every student. You should use these GPU hours carefully to not run out before you complete the activity.

# Course Projects
Students will do a course project in a group of four. We will design a speciic project for each group. Once you are assigned the project, you will scope the project out (one week, 10% of the project score). There will be midterm progress presentations (30% of the project score). At the end of the finals period, you will submit your code (30% of the project score) and project report (30% of the project report).
