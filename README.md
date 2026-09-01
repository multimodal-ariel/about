# Multimodal Automated Reasoning and Interpretation for Early Lupus detection (ARIEL)

ARIEL is funded by the National Institutes of Health (NIH) under Other Transactions [1OT2OD038045-01: Unified and fair multimodal representation learning for autoimmune diseases](https://reporter.nih.gov/search/nwCLPGKJck-f8g6Jr68IWQ/project-details/11091113). The views and conclusions contained in our work and related publications are those of the authors and should not be interpreted as representing official policies, either expressed or implied, of the NIH.

*Project leadership*:
- [Saira Sheikh](https://www.med.unc.edu/medicine/rheumatology-allergy-immunology/people/saira-z-sheikh-md/) (PI), UNC
- [Yueh Lee](https://www.med.unc.edu/radiology/people/yueh-z-lee/) (PI), UNC
- [Marc Niethammer](https://cseweb.ucsd.edu/~mniethammer/author/marc-niethammer/) (PI), UCSD
- [Mohit Bansal](https://www.cs.unc.edu/~mbansal/) (Investigator), UNC
- [Tianlong Chen](https://tianlong-chen.github.io/) (Investigator), UNC
- [Junier Oliva](https://sites.google.com/cs.unc.edu/joliva/home) (Investigator), UNC
- [Hongtu Zhu](https://sph.unc.edu/adv_profile/hongtu-zhu-phd/) (Investigator), UNC

## Table of Contents
- [Background](#background)
- [Software](#software)
- [Publications](#main-publications)

## Background

Autoimmune diseases affect 1 in 10 people. Commonly, patients needlessly suffer for years due to delays in diagnosis and referral delays to specialists. Systemic lupus erythematosus (SLE) is a classic example due to its nonspecific symptoms and potential to mimic other diseases. It affects women 9 to 1 with average diagnostic delays of over 5 years, increasing the chances of life-limiting end-organ damage. A diagnosis typically requires an experienced rheumatologist to carefully consider and integrate various data sources. Our project develops technology that will allow 1) using many different datatypes (e.g., electronic health records, full-body imaging, clinical measures, and tabular data); 2) adding data sources to the multimodal model as needed; 3) supporting missing modalities by cross-modal generative learning; 4) providing inherent end-to-end interpretable results; and 5) patient-specific disease predictions and patient-personalized multimodal information acquisition plans. While motivated by lupus diagnosis our approaches are often generally applicable to multimodal learning. They target significantly earlier diagnoses for autoimmune diseases, strategies to recommend suitable additional diagnostic tests, and the ability to identify patients at greatest risk for the worst outcomes for which more aggressive treatments may be recommended.

## Software

The project has developed many different software packages geared at lupus diagnosis but often with more general applicability. 

| Software | Description |
|----------|-------------|
| [SLICC](https://github.com/multimodal-ariel/SLICC) (currently private) | Automatic computation of SLICC score |
| Baseline prediction models (link to be added) | Simple machine learning approaches using OMOP data for early lupus prediction |
| [NOCTA](https://github.com/multimodal-ariel/afa-adni-oai) | Approaches to recommend what tests to request |
| [Template-based AFA](https://github.com/multimodal-ariel/template-afa) | AFA framework learning a library of informative feature subsets |
| [Multiple debating and collaborating VLMs](https://github.com/multimodal-ariel/multi-agent-detection-cdw) | A flexible approach to reasoning via multiple vision language models |
| [Multimodal medical segmentation](https://github.com/multimodal-ariel/SpatioSemanticMedMICS) | A robust in-context segmentation approach for multimodal image segmentation |
| [Multimodal image biomarker extraction](https://github.com/multimodal-ariel/unified-medical-imaging-pipeline) | Unified processing of large-scale heterogeneous clinical imaging data |
| [Radiology feature extraction](https://github.com/multimodal-ariel/radiology-feature-extraction) | Image feature extraction of 2D and 3D images |
| [Multimodal atlas building](https://github.com/multimodal-ariel/atlas-builder) (currently private) | An atlas building approach for multimodal image data |
| [Flex-MoE](https://github.com/multimodal-ariel/flex-moe) | Flexible mixture-of-experts modeling for arbitrary combinations of available modalities |
| [MoE-Retriever](https://github.com/multimodal-ariel/moe-retriever) | Generative retrieval of missing-modality representations using mixture-of-experts routing |
| [Adaptive Modality Token Re-balancing (AMC)](https://github.com/multimodal-ariel/amc) | Adaptive modality fusion for multimodal learning |
| [YODO](https://github.com/multimodal-ariel/yodo) | A single trained model supporting adjustable accuracy-fairness trade-offs at inference time |
| [Multi-organ lupus prediction](https://github.com/multimodal-ariel/multi-organ-lupus-prediction) | Organ-aware prediction from longitudinal laboratory data for early lupus detection |
| [Medical hierarchy-aware multimodal unlearning](https://github.com/multimodal-ariel/MedForget) | a hierarchy-aware multimodal unlearning benchmark and algorithm |


## Main publications

### Image Analysis

| Title | Authors | Venue | Year |
|-------|---------|-------|------|
| [Uncertainty-Aware Spatio-Semantic Contextual Prompts for Multimodal Medical Segmentation](https://soumitri2001.github.io/assets/uncertainty_aware_spatio_semantic_contextual_prompts_miccai26_preprint.pdf) | Chattopadhyay, Soumitri and Demir, Basar and Niethammer, Marc | MICCAI | 2026 | 
| [On the Robustness of Foundational 3D Medical Image Segmentation Models Against Imprecise Visual Prompts](https://ieeexplore.ieee.org/abstract/document/11515686) | Chattopadhyay, Soumitri and Demir, Basar and Niethammer, Marc | ISBI | 2026 |
| [How Useful Are Vision Foundation Model Features for Out-of-the-Box Disease Progression Prediction?](https://openaccess.thecvf.com/content/CVPR2026W/CV4Clinic2026/papers/Demir_How_Useful_Are_Vision_Foundation_Model_Features_for_Out-of-the-Box_Disease_CVPRW_2026_paper.pdf) | Demir, Basar and Chattopadhyay, Soumitri and Greer, Hasting, and Chen Boqi and Niethammer, Marc | CVPR Workshop | 2026 |

### Multimodal Learning and Fairness

| Title | Authors | Venue | Year |
|-------|---------|-------|------|
| [Flex-MoE: Modeling Arbitrary Modality Combination via the Flexible Mixture-of-Experts](https://proceedings.neurips.cc/paper_files/paper/2024/hash/b2f2af5403042b1344f4e93b35fb67d9-Abstract-Conference.html) | Yun, Sukwon and Choi, Inyoung and Peng, Jie and Wu, Yangfan and Bao, Jingxuan and Zhang, Qiyiwen and Xin, Jiayi and Long, Qi and Chen, Tianlong | NeurIPS | 2024 |
| [Generate, Then Retrieve: Addressing Missing Modalities in Multimodal Learning via Generative AI and MoE](https://openreview.net/forum?id=aUpA5gulZ4) | Yun, Sukwon and Xin, Jiayi and Choi, Inyoung and Peng, Jie and Ding, Ying and Long, Qi and Chen, Tianlong | GenAI4Health at AAAI | 2025 |
| [Modalities Contribute Unequally: Enhancing Medical Multi-modal Learning through Adaptive Modality Token Re-balancing](https://proceedings.mlr.press/v267/peng25a.html) | Peng, Jie and Ballard, Jenna and Zhang, Mohan and Yun, Sukwon and Xin, Jiayi and Long, Qi and Zhang, Yanyong and Chen, Tianlong | ICML | 2025 |
| [You Only Debias Once: Towards Flexible Accuracy-Fairness Trade-offs at Inference Time](https://proceedings.mlr.press/v280/han25a.html) | Han, Xiaotian and Chen, Tianlong and Zhou, Kaixiong and Jiang, Zhimeng and Wang, Zhangyang and Hu, Xia | CPAL | 2025 |
| [Mexa: Towards general multimodal reasoning with dynamic multi-expert aggregation](https://aclanthology.org/anthology-files/anthology-files/pdf/findings/2025.findings-emnlp.1233.pdf) | Yu, Shoubin and Zhang, Yue and Wang, Ziyang and Yoon, Jaehong and Bansal, Mohit | EMNLP Findings | 2025 |
| [DART: Leveraging Multi-Agent Disagreement for Tool Recruitment in Multimodal Reasoning](https://aclanthology.org/2026.eacl-long.253/) | Sivakumaran, Nithin and Chen, Justin and Wan, David and Zhang, Yue and Yoon, Jaehong and Stengel-Eskin, Elias and Bansal, Mohit | EACL | 2026 |
| [Hierarchy-Aware Multimodal Unlearning for Medical AI](https://openreview.net/forum?id=TVSIhLqIkf) | Wu, Fengli and Patil, Vaidehi and Yoon, Jaehong and Zhang, Yue and Bansal, Mohit | TMLR | 2026 |
