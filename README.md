# \[ACL 2025\] Does Time Have Its Place? Temporal Heads: Where Language Models Recall Time-specific Information

## Overview
Does large language models (LLMs) specifically handle temporally evolving facts within their internal structures? 🤔    
We introduce the concept of **Temporal Heads**—dedicated attention heads within LLMs managing and processing time-sensitive information.    
(1) Method: We applied [Knowledge Circuit](https://arxiv.org/abs/2405.17969) analysis, then found out specific attention heads that are triggered by temporal signals for both explicit numeral dates (e.g., "In 2004") or more implicit textual temporal conditions (e.g., "In the year...").    
(2) Findings: It turns out that these Temporal Heads are pivotal in recalling and updating time-specific facts. When these heads are disabled, the models lose precision in temporal recall, though their overall reasoning and static knowledge remain mostly intact.    
(3) Possibility: Even more exciting is the potential to directly edit a model’s temporal knowledge by manipulating the values of these specific attention heads and applying them to cases where temporal knowledge is incorrect.

<p align="center">
  📃 <a href="https://arxiv.org/abs/2502.14258" target="_blank">Paper</a>
</p>

![](assets/overview.png)

## Updates
[May 30, 2025] We have released the code and data.     
[May 15, 2025] Our paper has been accepted to ACL 2025! 🎉     
[Feb 20, 2025] Our paper is preprinted.

## Installation
To ensure compatibiliity with other libraries, we recommend using the folliwng versions. You can adjust it based on your environments:

- Python >= 3.10.14
- PyTorch >= 2.4.0
- CUDA 12.2

Then, follow the order of installation.

1. Clone the repository:
   ```bash
   git clone https://github.com/dmis-lab/TemporalHead.git
   cd TemporalHead
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Implementation
Follow the order of each notebook file
   ```
   For circuit construction to find out Temporal Head
   1.circuit_construction.ipynb
   2.circuit_analysis.ipynb
   ```
   ```
   Check the attention values of each head
   3.logit_lens.ipynb
   ```
   ```
   Follow the ablation test examples
   4.ablation_example.ipynb
   5.compute-logprobs.ipynb
   6.visualize-logprobs.ipynb
   ```
   ```
   Try to add activation values for knowledge editing
   7.temporal_knowledge_edit.ipynb
   ```

### Citation and Acknowledgements

If you find our work is useful in your research, please consider citing our [paper](https://arxiv.org/abs/2502.14258):
```
@article{park2025does,
  title={Does Time Have Its Place? Temporal Heads: Where Language Models Recall Time-specific Information},
  author={Park, Yein and Yoon, Chanwoong and Park, Jungwoo and Jeong, Minbyul and Kang, Jaewoo},
  journal={arXiv preprint arXiv:2502.14258},
  year={2025}
}
```

We also gratefully acknowledge the following open-source repositories and kindly ask that you cite their accompanying papers as well.

    [1] https://github.com/zjunlp/KnowledgeCircuits
    [2] https://github.com/hannamw/eap-ig

### Contact
For any questions or issues, feel free to reach out to [522yein (at) korea.ac.kr].