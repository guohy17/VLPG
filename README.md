<div align="center">    
 
# Vision-Language Pre-training for Graph-based Handwritten Mathematical Expression Recognition

</div>

## Introduction
Vision-language pre-training models have shown promise in improving various downstream tasks. However, handwritten mathematical expression recognition (HMER), as a typical structured learning problem, can hardly benefit from existing pre-training methods due to the presence of multiple symbols and complicated structural relationships, as well as the scarcity of paired data. To overcome these problems, we propose a Vision-Language Pre-training paradigm for Graph-based HMER (VLPG), utilizing unpaired mathematical expression images and LaTeX labels. 

Our HMER model is built upon a graph parsing method with superior explainability, which is enhanced by the proposed graph-structure aware transformer decoder.

Based on this framework, the symbol localization pretext task and language modeling task are employed for vision-language pre-training. First, we make use of unlabeled mathematical symbol images to pre-train the visual feature extractor through the localization pretext task, improving the symbol localization and discrimination ability. Second, the structure understanding module is pre-trained using LaTeX corpora through language modeling task, which promotes the model's context comprehension ability. The pre-trained model is fine-tuned and aligned on the downstream HMER task using benchmark datasets. 


## Framework

## Results
| Method | CROHME 2014 ExpRate↑ | CROHME 2014 ≤1↑ | CROHME 2014 ≤2↑ | CROHME 2016 ExpRate↑ | CROHME 2016 ≤1↑ | CROHME 2016 ≤2↑ | CROHME 2019 ExpRate↑ | CROHME 2019 ≤1↑ | CROHME 2019 ≤2↑ |
|--------|----------------------|-----------------|-----------------|----------------------|-----------------|-----------------|----------------------|-----------------|-----------------|
| BTTR   | 53.96                | 66.02           | 70.28           | 52.31                | 63.90           | 68.61           | 52.96                | 65.97           | 69.14           |
| CoMER  | 59.33                | 71.70           | 75.66           | 59.81                | 74.37           | 80.03           | 62.97                | 77.40           | 81.40           |
| **VLPG** | ** 60.41±0.36**    | ** 74.14 **     | **78.90 **      | **60.51±0.79  **     | **75.50 **      | **79.86 **      | ** 62.34±0.30**      | **76.81 **      | **81.15 **      |



