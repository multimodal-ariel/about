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

## Background

Autoimmune diseases affect 1 in 10 people. Commonly, patients needlessly suffer for years due to delays in diagnosis and referral delays to specialists. Systemic lupus erythematosus (SLE) is a classic example due to its nonspecific symptoms and potential to mimic other diseases. It affects women 9 to 1 with average diagnostic delays of over 5 years, increasing the chances of life-limiting end-organ damage. A diagnosis typically requires an experienced rheumatologist to carefully consider and integrate various data sources. Our project develops technology that will allow 1) using many different datatypes (e.g., electronic health records, full-body imaging, clinical measures, and tabular data); 2) adding data sources to the multimodal model as needed; 3) supporting missing modalities by cross-modal generative learning; 4) providing inherent end-to-end interpretable results; and 5) patient-specific disease predictions and patient-personalized multimodal information acquisition plans. While motivated by lupus diagnosis our approaches are often generally applicable to multimodal learning. They target significantly earlier diagnoses for autoimmune diseases, strategies to recommend suitable additional diagnostic tests, and the ability to identify patients at greatest risk for the worst outcomes for which more aggressive treatments may be recommended.

## Software

The project has developed many different software packages geared at lupus diagnosis but often with more general applicability. 

| Software | Description |
|----------|-------------|
| [SLICC](https://github.com/multimodal-ariel/SLICC) (currently private) | Automatic computation of SLICC score |
| Baseline prediction models (link to be added) | Simple machine learning approaches using OMOP data for early lupus prediction |
| [Multi-organ prediction](https://github.com/multimodal-ariel/OSAN) (currently private) | Prediction approaches based on multi-organ reasoning |
| [Active feature acquisition (AFA)](https://github.com/multimodal-ariel/afa-adni-oai) | Approaches to recommend what tests to request |
| [Template-based AFA](https://github.com/multimodal-ariel/template-afa) (currently private) | AFA framework learning a library of informative feature subsets |
| [Multiple debating and collaborating VLMs](https://github.com/multimodal-ariel/multi-agent-detection-cdw) | A flexible approach to reasoning via multiple vision language models |
| [Multimodal medical segmentation](https://github.com/multimodal-ariel/SpatioSemanticMedMICS) | A robust in-context segmentation approach for multimodal image segmentation |
| [Multimodal image biomarker extraction](https://github.com/multimodal-ariel/unified-medical-imaging-pipeline) | Unified processing of large-scale heterogeneous clinical imaging data |
| [Radiology feature extraction](https://github.com/multimodal-ariel/radiology-feature-extraction) | Image feature extraction of 2D and 3D images |
| [Multimodal atlas building](https://github.com/multimodal-ariel/atlas-builder) (currently private) | An atlas building approach for multimodal image data |




