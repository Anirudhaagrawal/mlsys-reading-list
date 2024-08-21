# LLM Inference Papers

## Table of Contents
- [LLM Serving Systems](#llm-serving-systems)
- [LLM Inference](#llm-inference)
- [Multi-Token Prediction ](#multi-token-prediction)
- [Hallucinations](#hallucinations)
- [New Architectures](#new-architectures)
- [MoE](#moe)
- [Hardware-Aware Algorithm Design](#hardware-aware-algorithm-design)
- [Parameter Efficient Fine Tuning Technique](#parameter-efficient-fine-tuning-techniques)
- [Training Papers](#training-papers)
- [Quantization and Compression](#quantization-and-compression)
- [Communication Collectives](#communication-collectives)

## LLM Serving Systems
- Clipper
  - Conference: NSDI'2017
  - [Link: Clipper: A Low-Latency Online Prediction Serving System](https://www.usenix.org/system/files/conference/nsdi17/nsdi17-crankshaw.pdf)

- InferLine
  - Conference: ACM'2018
  - [Link: InferLine: ML Inference Pipeline Composition Framework](https://arxiv.org/abs/1812.01776)

- Orca
  - Conference: OSDI'2022
  - [Link: Orca: Differentially Private Data Release for Large-Scale ML Models](https://usenix.org/system/files/osdi22-yu.pdf)
  - Orca tackles inefficiencies in traditional LLM inference caused by request-level scheduling, where a batch must wait for all requests to reach the EOS token before returning results, leading to increased latency for shorter requests. Orca introduces iteration-level scheduling, returning tokens at each generation step, thus reducing wait times.[Summary](https://medium.com/@pratishthagaur03/understanding-orca-a-research-synopsis-037797002039)

- FlexGen
  - Conference: ICLR'2023
  - [Link: FlexGen: High-Throughput Generation with Flexible Large Language Models](https://arxiv.org/abs/2303.06865)
  - [Code](https://github.com/FMInference/FlexGen)

- vLLM
  - Conference: ACM'2023
  - [Link: vLLM: A High-Throughput Transformer-Based Language Model Inference Engine](https://arxiv.org/abs/2309.06180)
  - [Code](https://github.com/vllm-project/vllm)
  - The paper introduces a new system for efficient serving of large language models using a novel technique called "paged attention" to improve memory management and throughput during inference.

- Sarathi-serve
  - Conference: OSDI'2024
  - [Link: Sarathi-serve: High Performance Serving for Deep Learning Models](https://arxiv.org/abs/2403.02310)
  - [Code](https://github.com/microsoft/sarathi-serve)


## LLM Inference

- Sarathi
  - [Link: SARATHI: Efficient LLM Inference by Piggybacking Decodes with Chunked Prefills](https://arxiv.org/pdf/2308.16369)
 
- Flash Decode
  - [Link: FlashDecoding++: Faster Large Language Model Inference on GPUs](https://arxiv.org/abs/2311.01282)

- Splitwise
  - Conference: IEEE'2023
  - [Link: Splitwise: Efficient generative LLM inference using phase splitting](https://arxiv.org/abs/2311.18677)
 
- SGLang
  - [Link: Efficiently Programming Large Language Models using SGLang](https://arxiv.org/html/2312.07104v1)

- DistServe
  -	Conference: OSDI'2024
  - [Link: DistServe: Disaggregating Prefill and Decoding for Goodput-optimized Large Language Model Serving](https://arxiv.org/abs/2401.09670)

- Fairness
  - Usenix'2020
  - [Link: Fairness in Serving Large Language Models](https://arxiv.org/abs/2401.00588)
  - [Code](https://github.com/Ying1123/VTC-artifact)

- APIServe
  - [Link: APIServe: Efficient API Support for Large-Language Model Inferencing](https://arxiv.org/html/2402.01869v1)

- LayerSkip
  - [Link: LayerSkip: Enabling Early Exit Inference and Self-Speculative Decoding](https://arxiv.org/abs/2404.16710)

- Parrot
  - Conference: OSDI'2024
  - [Link: Parrot: Efficient Serving of LLM-based Applications with Semantic Variable](https://arxiv.org/abs/2405.19888)



## Multi-Token Prediction 

- Speculative Decoding
  - Conference: ICML'2023
  - [Link: Fast Inference from Transformers via Speculative Decoding](https://arxiv.org/abs/2211.17192)

- Medusa
  - Conference: ICML'2024
  - [Link: Medusa: Simple LLM Inference Acceleration Framework with Multiple Decoding Heads](https://arxiv.org/abs/2401.10774)
  - [Code](https://github.com/FasterDecoding/Medusa)

- Lookahead Decoding
  - Conference: ICML'2024
  - [Link: Break the Sequential Dependency of LLM Inference Using Lookahead Decoding](https://arxiv.org/abs/2402.02057)
  - [Code](https://github.com/hao-ai-lab/LookaheadDecoding)

- Multi-Token Prediction
  - Conference: ICML'2024
  - [Link: Better & Faster Large Language Models via Multi-token Prediction](https://arxiv.org/abs/2404.19737)

## Multiple LLM and multiple LoRa serving

- s-LoRa
  - Conference: MLSys'2024
  - [Link: S-LoRA: Serving Thousands of Concurrent LoRA Adapters](https://arxiv.org/abs/2311.03285)
  - [Code](https://github.com/S-LoRA/S-LoRA)

- MuxServe
  - Conference: ICML'2024
  - [Link: MuxServe: Flexible Spatial-Temporal Multiplexing for Multiple LLM Serving](https://arxiv.org/abs/2404.02015)
  - [Code](https://github.com/hao-ai-lab/MuxServe)


## Hallucinations

- DoLa
  - Conference: ICLR'2024
  - [Link: DoLa: Decoding by Contrasting Layers Improves Factuality in Large Language Models](https://arxiv.org/abs/2309.03883)
  - [Code](https://github.com/voidism/DoLa)
    
## New Architectures

- Mamba
  - [Link: Mamba: Linear-Time Sequence Modeling with Selective State Spaces](https://arxiv.org/abs/2312.00752)
    
- Jamba
  - Conference: NeurIPS'2023
  - [Link: Jamba: A Hybrid Transformer-Mamba Language Model](https://arxiv.org/abs/2403.19887)
    
## MoE

- DeepSpeed-MoE
  - Conference: ICML'2022
  - [Link: DeepSpeed-MoE: Advancing Mixture-of-Experts Inference and Training to Power Next-Generation AI Scale](https://arxiv.org/abs/2201.05596)

- Tutel
  - Conference: MLSys'2023
  - [Link: Tutel: Adaptive Mixture-of-Experts at Scale](https://arxiv.org/abs/2206.03382)
    
- MegaBlocks 
  - Conference: MLSys'2023
  - [Link: MegaBlocks: Efficient Sparse Training with Mixture-of-Experts](https://arxiv.org/abs/2211.15841)
    
- Gshard
  - Conference: NeurIPS'2022
  - [Link: GShard: Scaling Giant Models with Conditional Computation and Automatic Sharding](https://arxiv.org/abs/2006.16668)

- Towards MoE Deployment
  - Conference: IEEE'2023
  - [Link: Towards MoE Deployment: Mitigating Inefficiencies in Mixture-of-Expert (MoE) Inference](https://arxiv.org/abs/2303.06182)

- SwapMoE
  - Conference: ACL'2024
  - [Link: SwapMoE: Serving Off-the-shelf MoE-based Large Language Models with Tunable Memory Budget](https://arxiv.org/abs/2308.15030)

## Hardware-Aware Algorithm Design

- Multi Query Attention
  - [Link: Fast Transformer Decoding: One Write-Head is All You Need](https://arxiv.org/abs/1911.02150v1)

- FlashAttention
  - Conference: NeurIPS'2022
  - [Link: FlashAttention: Fast and Memory-Efficient Exact Attention with IO-Awareness](https://arxiv.org/abs/2205.14135)

- FlashAttention 2
  - [Link: FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://arxiv.org/abs/2307.08691)

- Grouped Query Attention
  - Conference: EMNLP'2023
  - [Link: GQA: Training Generalized Multi-Query Transformer Models from Multi-Head Checkpoints](https://arxiv.org/abs/2305.13245v3)

- FlashAttention 3
  - [Link: FlashAttention-3: Fast and Accurate Attention with Asynchrony and Low-precision](https://tridao.me/publications/flash3/flash3.pdf)
  - [Code](https://github.com/Dao-AILab/flash-attention)


## Parameter Efficient Fine Tuning Techniques

- LoRa  
  - Conference: ICLR'2022  
  - [Link: https://arxiv.org/abs/2106.09685](https://arxiv.org/abs/2106.09685)

- QLoRa  
  - Conference: NeurIPS'2023  
  - [Link: https://arxiv.org/abs/2305.14314](https://arxiv.org/abs/2305.14314)

- Soft Prompt Tuning  
  - Conference: NeurIPS'2021  
  - [Link: https://arxiv.org/abs/2104.08691](https://arxiv.org/abs/2104.08691)

- Prefix Tuning 
  - Conference: ACL'2021  
  - [Link: https://arxiv.org/abs/2101.00190](https://arxiv.org/abs/2101.00190)

- DoRa  
  - Conference: ICLR'2024  
  - [Link: https://arxiv.org/abs/2402.09353](https://arxiv.org/abs/2402.09353)

- IA3  
  - Conference: NeurIPS'2022  
  - [Link: https://arxiv.org/pdf/2205.05638](https://arxiv.org/pdf/2205.05638)


## Training Papers

- GPipe
  - Conference - NeurIPS'2019
  - [Link: GPipe: Efficient Training of Giant Neural Networks using Pipeline Parallelism](https://arxiv.org/abs/1811.06965)

- Megatron LM 
  - Conference: ICML'2020
  - [Link: Megatron-LM: Training Multi-Billion Parameter Language Models Using Model Parallelism](https://arxiv.org/abs/1909.08053)

- ZeRO
  - [Link: ZeRO: Memory Optimizations Toward Training Trillion
Parameter Models](https://arxiv.org/pdf/1910.02054)

- PyTorch Distributed
  - [Link: PyTorch Distributed: Experiences on Accelerating Data Parallel Training](https://arxiv.org/abs/2006.15704)


- MegatronLM
  - Conference: ACM'2021
  - [Link: Efficient Large-Scale Language Model Training on GPU Clusters Using Megatron-LM](https://arxiv.org/abs/2104.04473)
  - [Code](https://github.com/nvidia/megatron-lm)


- Varuna
  - [Link: Varuna: Scalable, Low-cost Training of Massive Deep Learning Models](https://arxiv.org/abs/2111.04007)
  - [Code](https://github.com/microsoft/varuna)


- Alpa
  - Conference: OSDI'2022
  - [Link: Alpa: Automating Inter- and Intra-Operator Parallelism for Distributed Deep Learning](https://arxiv.org/abs/2201.12023)



- Llama 3.1
  - [Link: The Llama 3 Herd of Models]( https://ai.meta.com/research/publications/the-llama-3-herd-of-models/)


- [LLM Training Puzzles](https://github.com/srush/LLM-Training-Puzzles?tab=readme-ov-file)

# Tiny ML

## Quantization and Compression

- Deep Compression
  - Conference: ICLR'2015
  - [Link: Compressing Deep Neural Network with Pruning, Trained Quantization and Huffman Coding](https://arxiv.org/pdf/1510.00149)
  - Deep Compression aims to reduce the memory and energy requirements of large neural networks by compressing them to fit on-chip SRAM rather than relying on costly DRAM.[Summary](https://medium.com/@pratishthagaur03/understanding-deep-compression-a-research-synopsis-17657ededda4)


- Linear Quantization
  - Conference: IEEE'2018
  - [Link: Quantization and Training of Neural Networks for Efficient
Integer-Arithmetic-Only Inference](https://arxiv.org/pdf/1712.05877)


- GPTQ
  - Conference: ICLR'2023
  - [Link: GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers](https://arxiv.org/abs/2210.17323)


- SmoothQuant
  - Conference: ICML'2023
  - [Link: SmoothQuant: Accurate and Efficient Post-Training Quantization for Large Language Models](https://arxiv.org/abs/2211.10438)


- DynaQuant
  - Conference: ACM'2023
  - [Link: DynaQuant: Compressing Deep Learning Training Checkpoints via Dynamic Quantization](https://arxiv.org/abs/2306.11800)



# Communication Collectives

- [Collective Communication Review](https://www.cs.utexas.edu/~pingali/CSE392/2011sp/lectures/Conc_Comp.pdf)


- [Link: An In-Network Architecture for Accelerating
Shared-Memory Multiprocessor Collectives](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9138924)
  - Conference: IEEE'2020


- [Link: Breaking the Computation and Communication Abstraction
Barrier in Distributed Machine Learning Workloads](https://arxiv.org/pdf/2105.05720)
  - Conference: ACM'2022


- Synthesizing Optimal Collective Algorithms  
  - Conference: ACM'2021
  - [Link: Synthesizing Optimal Collective Algorithms](https://dl.acm.org/doi/pdf/10.1145/3437801.3441620)

- MSCCLang 
  - Conference: ACM'2023
  - [Link: MSCCLang: Microsoft Collective Communication Language](https://parsa.epfl.ch/course-info/cs723/papers/MSCCLang.pdf)

TACCL
  - NSDI'2023
  - [Link: TACCL: Guiding Collective Algorithm Synthesis
using Communication Sketches](https://www.usenix.org/system/files/nsdi23-shah.pdf)




# Contribution

## Contribute to Our ML Systems Reading List

We’re building a comprehensive and up-to-date GitHub repository of the most impactful papers in Machine Learning Systems (MLSys), and we need your help to keep it growing! Whether you’ve come across a groundbreaking paper, an insightful study, or an innovative idea in the MLSys domain, your contributions can make a difference.

**Why contribute?**

- **Stay Engaged:** Sharing papers not only helps others but also keeps you engaged with the latest research trends and developments in MLSys.
- **Community Growth:** Your contributions foster a collaborative learning environment, helping fellow researchers, engineers, and enthusiasts discover valuable resources.
- **Recognition:** Each contribution will be attributed to you, allowing you to build a visible presence in the MLSys community.

**How to contribute?**

1. **Find a Paper:** Identify a paper that you believe adds value to the repository.
2. **Fork the Repository:** Create a fork of the repository to make your changes.
3. **Add the Paper:** Include the paper in the appropriate section of the reading list, following the existing format.
4. **Open a Pull Request:** Once you’ve added the paper, open a Pull Request (PR) with a brief description of why you think the paper is important.
5. **Engage:** Engage with any feedback on your PR, making revisions as necessary.

By contributing, you’re not just adding a link—you’re helping to shape the learning resources for the next generation of MLSys practitioners. Let’s work together to make this repository the go-to place for anyone interested in the cutting-edge of ML Systems!

---












