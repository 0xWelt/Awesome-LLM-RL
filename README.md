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

#### [OpenRLHF](https://github.com/OpenRLHF/OpenRLHF)

OpenRLHF is the first easy-to-use, high-performance open-source RLHF framework built on Ray, vLLM, ZeRO-3 and HuggingFace Transformers, designed to make RLHF training simple and accessible.


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
