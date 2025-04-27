# Write Once, Run Anywhere: Transcompiling Tensor Programs for Deep Learning Systems with a Neural-Symbolic Approach
<img src="docs/static/images/overview.png" style="zoom:50%;" /> 

Heterogeneous deep learning systems (DLS) such as GPUs and ASICs have been widely deployed in industrial data centers, which requires to develop multiple low-level tensor programs for different platforms. An attractive solution to relieve the programming burden is to transcompile the legacy code of one platform to others. However, current transcompilation techniques struggle with either tremendous manual efforts or functional incorrectness, rendering “Write Once, Run Any- where" of tensor programs an open question. We propose a novel transcompiler, i.e., FALCON, for auto-matically translating tensor programs across DLS via both large language models (LLMs) and symbolic program synthesis, i.e., neural-symbolic synthesis. The key insight is leveraging the powerful code generation ability of LLM to make costly search-based symbolic synthesis computationally tractable. Concretely, we propose multiple LLM-assisted compilation passes via pre-defined meta-prompts for program transformation. During each program transformation, efficient symbolic program synthesis is employed to repair incorrect code snippets with a limited scale. To attain high performance, we propose a hierarchical auto-tuning approach to systemically explore both the parameters and sequences of transformation passes. Experiments on 4 DLS with distinct programming interfaces, i.e., Intel DL Boost with VNNI, NVIDIA GPU with CUDA, AMD MI with HIP, and Cambricon MLU with BANG, demonstrate that FALCON correctly translates different tensor programs at the accuracy of 95% on average, and the performance of translated programs achieves up to 2.0× over vendor-provided manually-optimized libraries. As a result, the programming productivity of DLS is improved by up to 96.0× via transcompiling legacy tensor programs.


## Citation
Please cite using the following bibtex entry:

```
@InProceedings{
    title = 	 {Write Once, Run Anywhere: Transcompiling Tensor Programs for Deep Learning Systems with a Neural-Symbolic Approach},
    author =       {Shouyang Dong, Yuanbo Wen, Jun Bi, Di Huang, Jiaming Guo, Jianxing Xu, Ruibai Xu, Xinkai Song, Yifan Hao, Ling Li, Xuehai Zhou, Tianshi Chen, Qi Guo, Yunji Chen},
    year = 	 {2025}
}
```