# Awesome-LLM-RL

[![Website](https://img.shields.io/website?url=https%3A%2F%2F0xWelt.github.io%2FAwesome-LLM-RL%2F&label=Live%20Site)](https://0xWelt.github.io/Awesome-LLM-RL/)
[![GitHub stars](https://img.shields.io/github/stars/0xWelt/Awesome-LLM-RL?style=social)](https://github.com/0xWelt/Awesome-LLM-RL)
[![GitHub forks](https://img.shields.io/github/forks/0xWelt/Awesome-LLM-RL?style=social)](https://github.com/0xWelt/Awesome-LLM-RL/fork)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A Curated List of Open-Source Projects, Tools, and Learning Resources about Reinforcement Learning with LLMs.

🌐 **Live Website**: [https://0xWelt.github.io/Awesome-LLM-RL/](https://0xWelt.github.io/Awesome-LLM-RL/)

## Table of Contents

- [Table of Contents](#table-of-contents)
- [RL Frameworks](#rl-frameworks)
    - [OpenRLHF](#openrlhf)
- [Runtime Engines](#runtime-engines)
  - [Inference Engines](#inference-engines)
    - [vLLM](#vllm)
    - [SGLang](#sglang)
  - [Training Engines](#training-engines)
    - [Megatron-LM](#megatron-lm)
    - [DeepSpeed](#deepspeed)
- [Star History](#star-history)
- [Contributors](#contributors)
- [License](#license)

## RL Frameworks

> Reinforcement learning frameworks for training and evaluating LLMs.

### [OpenRLHF](https://github.com/OpenRLHF/OpenRLHF)

OpenRLHF is the first easy-to-use, high-performance open-source RLHF framework built on Ray, vLLM, ZeRO-3 and HuggingFace Transformers, designed to make RLHF training simple and accessible. It leverages Ray for efficient distributed scheduling, separating Actor, Reward, Reference, and Critic models across different GPUs to enable scalable training for models up to 70B+ parameters. Powered by vLLM and Auto Tensor Parallelism, it delivers high-throughput, memory-efficient sample generation that reduces 80% of RLHF training time spent on sample generation. Built on DeepSpeed's ZeRO-3 and AutoTP, it enables large model training without heavyweight frameworks while maintaining seamless HuggingFace integration. Supporting comprehensive RL algorithms including PPO, REINFORCE++, GRPO, RLOO, and Dr. GRPO, along with advanced features like Hybrid Engine scheduling, asynchronous training, agent-based RLHF, DPO/KTO optimization, and multi-modal support.

### [verl](https://github.com/volcengine/verl)

verl is a flexible, efficient and production-ready RL training library initiated by ByteDance Seed team, implementing the HybridFlow framework for large language models. Built on a hybrid-controller programming model, it enables flexible representation and efficient execution of complex post-training dataflows, supporting diverse RL algorithms including PPO, GRPO, GSPO, ReMax, REINFORCE++, RLOO, PRIME, DAPO, and DrGRPO. Seamlessly integrating with existing LLM infrastructure through modular APIs, verl supports FSDP, FSDP2, Megatron-LM for training and vLLM, SGLang, HF Transformers for rollout generation. Featuring 3D-HybridEngine for efficient actor model resharding, multi-modal RL support for vision-language models, multi-turn agent training with tool calling, and scaling up to 671B models with expert parallelism. Compatible with Hugging Face Transformers and Modelscope Hub, verl powers state-of-the-art reasoning models like Seed-Thinking-v1.5 and enables breakthrough research including DAPO achieving 50 points on AIME 2024.

### [slime](https://github.com/THUDM/slime)

slime is a high-performance LLM post-training framework from Tsinghua University designed for RL scaling, providing SGLang-native integration with Megatron-LM for efficient training and flexible data generation workflows. Built on a modular architecture with training (Megatron), rollout (SGLang + router), and data buffer components, it enables seamless parameter synchronization and data management. Supporting dense models like GLM-4-9B and Qwen3-4B, MoE models including GLM-4.5, Qwen3-30B-A3B, and DeepSeek-R1, along with multi-turn agent training with tool calling capabilities. Featuring checkpoint format conversion between Hugging Face and Megatron torch_dist formats, Ray-based distributed training, and comprehensive examples for reasoning, coding, and search tasks. slime powers the training of GLM-4.5 and provides production-ready solutions for large-scale RL post-training with up to 128xH100 GPU configurations.

### [ROLL](https://github.com/alibaba/ROLL)

ROLL is an efficient and user-friendly RL library from Alibaba designed for Large Language Models utilizing Large Scale GPU resources, significantly enhancing LLM performance in human preference alignment, complex reasoning, and multi-turn agentic interaction scenarios. Leveraging a multi-role distributed architecture with Ray for flexible resource allocation and heterogeneous task scheduling, ROLL integrates cutting-edge technologies like Megatron-Core, SGLang and vLLM to accelerate model training and inference. Supporting multi-task RL training (RLVR) covering mathematics, coding, general reasoning, and agentic RL for multi-turn interactions, games, and tool use. Featuring over 20 rich RL strategy configurations, sample-level asynchronous parallel rollout, environment-level asynchronous parallel rollout, and comprehensive algorithm support including PPO, GRPO, Reinforce++, TOPR, RAFT++, GSPO, GiGPO, and StarPO. With AutoDeviceMapping for custom device mapping, extreme offload/reload capabilities, LoRA training support, and integrated observability with SwanLab, WandB, and TensorBoard. 


## Runtime Engines

> Runtime engines for executing and managing LLM-based reinforcement learning systems.

### Inference Engines

> Specialized engines for efficient LLM inference during RL training and deployment.

#### [vLLM](https://github.com/vllm-project/vllm)

vLLM is a high-throughput and memory-efficient inference and serving engine for LLMs that delivers state-of-the-art serving performance through PagedAttention memory management, continuous batching, and optimized CUDA kernels. It supports seamless integration with Hugging Face models, offers OpenAI-compatible APIs, and provides comprehensive quantization support (GPTQ, AWQ, INT4/8, FP8) along with distributed inference capabilities across NVIDIA, AMD, Intel, and TPU hardware. Originally developed at UC Berkeley's Sky Computing Lab, vLLM now serves as a community-driven project powering major platforms like LMSYS Vicuna and Chatbot Arena.

#### [SGLang](https://github.com/sgl-project/sglang)

SGLang is a fast serving framework for large language models and vision language models that co-designs backend runtime and frontend language for high-performance LLM applications. It features RadixAttention for prefix caching, zero-overhead CPU scheduler, prefill-decode disaggregation, speculative decoding, and continuous batching, while providing a Pythonic frontend for chained generation calls, advanced prompting, control flow, and multi-modal inputs. Supporting extensive model families (Llama, Qwen, DeepSeek, GPT, Gemma, etc.) and deployed at massive scale across 1M+ GPUs worldwide, SGLang powers trillions of tokens daily for leading enterprises including xAI, AMD, NVIDIA, Google Cloud, and Microsoft Azure.

### Training Engines

> High-performance training engines optimized for RL with large language models.

#### [Megatron-LM](https://github.com/NVIDIA/Megatron-LM)

Megatron-LM is NVIDIA's GPU-optimized library for training transformer models at scale, providing state-of-the-art distributed training capabilities with comprehensive parallelism strategies including tensor, pipeline, data, context, and expert parallelism. It features Megatron Core as a composable library with optimized building blocks, supporting models from 2B to 462B+ parameters across thousands of GPUs with up to 47% Model FLOP Utilization. Supporting extensive model architectures (LLaMA, GPT, DeepSeek, Qwen, Mixtral, Mamba) with advanced features like FP8 training, FlashAttention, activation checkpointing, and fault-tolerant training, Megatron-LM powers production-scale training for leading enterprises and research institutions worldwide.

#### [DeepSpeed](https://github.com/deepspeedai/DeepSpeed)

DeepSpeed is Microsoft's deep learning optimization library that revolutionizes distributed training and inference through four innovation pillars: training, inference, compression, and science applications. It features groundbreaking ZeRO (Zero Redundancy Optimizer) technology for memory optimization, enabling training of trillion-parameter models with ZeRO-Infinity, ZeRO-Offload, and ZeRO++ for extreme scale. Supporting 3D parallelism (data, tensor, pipeline), DeepSpeed-MoE for mixture-of-experts, and advanced compression techniques, it has powered world-record models like Megatron-Turing NLG 530B, BLOOM 176B, and Jurassic-1 178B. With seamless integration across PyTorch, Transformers, Lightning, and Azure, DeepSpeed delivers 15x speedup for ChatGPT-like RLHF training and unprecedented cost reduction at all scales.

#### [PyTorch FSDP](https://pytorch.org/tutorials/intermediate/FSDP_tutorial.html)

PyTorch Fully Sharded Data Parallel (FSDP) is a memory-efficient distributed training engine that shards model parameters, gradients, and optimizer states across GPUs to enable training of large models that cannot fit on a single device. FSDP2 represents a major evolution with DTensor-based sharding for easy parameter manipulation, improved memory management with deterministic GPU usage, and flexible mixed precision policies supporting bfloat16 computation with float32 gradient reduction. It offers both implicit and explicit prefetching for overlapping communication with computation, supports meta-device initialization for large models, and provides seamless integration with PyTorch optimizers and gradient clipping. With tensor subclass extensions for float8 and NF4 quantization, FSDP enables efficient training of billion-parameter models while maintaining full compatibility with the PyTorch ecosystem.

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=0xWelt/Awesome-LLM-RL&type=Date)](https://star-history.com/#0xWelt/Awesome-LLM-RL&Date)

## Contributors

This project exists thanks to all the people who contribute.

<a href="https://github.com/0xWelt/Awesome-LLM-RL/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=0xWelt/Awesome-LLM-RL" />
</a>

## License

[![Creative Commons License](http://i.creativecommons.org/l/by/4.0/88x31.png)](https://creativecommons.org/licenses/by/4.0/)

This work is licensed under a
[Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).
