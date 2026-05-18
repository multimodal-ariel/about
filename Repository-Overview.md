# Repository Overview

All mm-ARIEL repositories, organized by research theme.

---

## 🏥 Clinical Imaging Pipeline (CDW)

Repositories for processing and analyzing clinical imaging data from the UNC Clinical Data Warehouse.

| Repository | Description |
|---|---|
| [visual-agentic-cdw](https://github.com/multimodal-ariel/visual-agentic-cdw) | End-to-end LLM-orchestrated pipeline for CT/MRI: metadata → planning → segmentation → QC → radiomics. Uses Qwen3-8B for planning and MedGemma-27B for QC. |
| [XRayFeatures](https://github.com/multimodal-ariel/XRayFeatures) | Feature extraction for 2D chest and hand radiographs using handcrafted PyRadiomics and MedSAM deep embeddings, applied to BiomedParse segmentation masks. |
| [XraySegmenter](https://github.com/multimodal-ariel/XraySegmenter) | Segmentation of 2D X-ray images. |
| [xray_atlas_builder](https://github.com/multimodal-ariel/xray_atlas_builder) | Builds population atlases from 2D hand X-ray images using multiGradICON registration. Two-stage training pipeline with atlas refinement iterations. |
| [hand-diffusion](https://github.com/multimodal-ariel/hand-diffusion) | Diffusion model training on hand X-ray images for image generation and feature extraction. |
| [multi-agent-detection-cdw](https://github.com/multimodal-ariel/multi-agent-detection-cdw) | Multi-agent detection framework for CDW clinical imaging data. |
| [headneck_segment_interative](https://github.com/multimodal-ariel/headneck_segment_interative) | Interactive segmentation of head and neck structures. |
| [demo](https://github.com/multimodal-ariel/demo) | Demonstration code and notebooks for the project. |

---

## 🧠 Machine Unlearning & Privacy

Repositories for removing sensitive information from trained models, motivated by HIPAA/GDPR requirements in medical AI.

| Repository | Description |
|---|---|
| [UnLOK-VQA](https://github.com/multimodal-ariel/UnLOK-VQA) | Benchmark and attack-defense evaluation framework for multimodal unlearning. Includes the UnLOK-VQA dataset (~500 entries) and evaluation of 6 defense strategies against multimodal attacks on LLaVA. |
| [MedForget](https://github.com/multimodal-ariel/MedForget) | Hierarchy-aware multimodal unlearning benchmark built on MIMIC-CXR. Introduces CHIP (Cross-modal Hierarchy-Informed Projection), a training-free unlearning method. ArXiv: 2512.09867. |
| [unlearning-debias](https://github.com/multimodal-ariel/unlearning-debias) | Machine unlearning for debiasing multimodal medical models. |

---

## 🫁 3D Medical Image Segmentation

Foundation model adaptation and atlas-driven approaches for volumetric medical image segmentation.

| Repository | Description |
|---|---|
| [autoprompt3dseg](https://github.com/multimodal-ariel/autoprompt3dseg) | [Ongoing] Atlas-driven auto-promptable 3D medical segmentation. Automatically generates prompts from atlas priors. |
| [ZS-DG-FM-3D-MedSeg](https://github.com/multimodal-ariel/ZS-DG-FM-3D-MedSeg) | Zero-shot domain generalization of foundation models for 3D medical image segmentation. Experimental study across modalities and anatomies. |
| [multitask_m3d](https://github.com/multimodal-ariel/multitask_m3d) | Multi-task learning with the M3D framework for 3D medical imaging. |

---

## 🤖 Multimodal Representation Learning

VLM fine-tuning, mixture-of-experts architectures, and multimodal reasoning.

| Repository | Description |
|---|---|
| [qwen2-vl-finetune](https://github.com/multimodal-ariel/qwen2-vl-finetune) | Fine-tuning Qwen2-VL for medical vision-language tasks. Apache 2.0 license. |
| [mexa](https://github.com/multimodal-ariel/mexa) | Multimodal explanation or cross-modal alignment tool (Python). |
| [moe-retriever](https://github.com/multimodal-ariel/moe-retriever) | Mixture-of-experts retrieval model for multimodal medical data. |
| [flex-moe](https://github.com/multimodal-ariel/flex-moe) | Flexible mixture-of-experts architecture. |
| [freebar](https://github.com/multimodal-ariel/freebar) | Python utility related to representation learning or evaluation. |
| [yodo](https://github.com/multimodal-ariel/yodo) | Python research code (purpose TBD — check README). |
| [multimodal-recurrent-reasoning](https://github.com/multimodal-ariel/multimodal-recurrent-reasoning) | Recurrent reasoning over multimodal inputs. |
| [afa-adni-oai](https://github.com/multimodal-ariel/afa-adni-oai) | Adaptive feature aggregation applied to ADNI and OAI datasets. |
| [template-afa](https://github.com/multimodal-ariel/template-afa) | Template/scaffold for adaptive feature aggregation (AFA) projects. |

---

## 📊 Data & Cohort Infrastructure

Dataset construction, cohort documentation, and EHR data access.

| Repository | Description |
|---|---|
| [unc-omop-cdw-cohorts](https://github.com/multimodal-ariel/unc-omop-cdw-cohorts) | Overview of UNC OMOP Common Data Model datasets from the CDW, including cohort descriptions, clinical domains (conditions, measurements, etc.). |
| [UKB_AllofUs](https://github.com/multimodal-ariel/UKB_AllofUs) | Analysis notebooks for UK Biobank and All of Us datasets. |
| [tcga](https://github.com/multimodal-ariel/tcga) | Analysis notebooks for TCGA (The Cancer Genome Atlas) data. |
| [eular-acl2019](https://github.com/multimodal-ariel/eular-acl2019) | Code from EULAR / ACL 2019 work on clinical NLP for rheumatology. |
| [SLICC](https://github.com/multimodal-ariel/SLICC) | Code related to SLICC (Systemic Lupus International Collaborating Clinics) criteria or scoring. |

---

## 📁 Project Management & Community

| Repository | Description |
|---|---|
| [about](https://github.com/multimodal-ariel/about) | Org-level mission, NIH grant info, and project overview. |
| [Deliverables](https://github.com/multimodal-ariel/Deliverables) | NIH project deliverables and milestone tracking. |
| [CommunityEngagement](https://github.com/multimodal-ariel/CommunityEngagement) | Community engagement materials and outreach resources. |
