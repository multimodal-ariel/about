# Research Areas

mm-ARIEL's work spans five interconnected research themes, all oriented toward the goal of early, fair lupus detection using multimodal AI.

---

## 1. Clinical Imaging Pipeline (CDW)

**Central question:** How do we reliably process thousands of heterogeneous clinical images (CT, MRI, X-ray) from a real hospital data warehouse?

The UNC Clinical Data Warehouse contains imaging data in highly variable formats — different scanners, protocols, anatomies, and quality levels. Our agentic pipeline ([visual-agentic-cdw](https://github.com/multimodal-ariel/visual-agentic-cdw)) uses LLMs to:
- Inspect image metadata and decide which segmentation tools to apply
- Route to appropriate tool-specific conda environments (TotalSegmentator, VISTA3D, MRSegmentator, etc.)
- Run multi-tier quality control, including LLM-based clinical interpretation (MedGemma-27B)
- Extract radiomics features for downstream analysis

For 2D X-rays specifically, [XRayFeatures](https://github.com/multimodal-ariel/XRayFeatures) extracts both handcrafted radiomics and MedSAM deep embeddings. [xray_atlas_builder](https://github.com/multimodal-ariel/xray_atlas_builder) builds population atlases from hand radiographs to study structural variation.

**Why this matters for lupus:** Lupus causes joint damage visible in hand X-rays and systemic organ involvement detectable in CT/MRI. Reliable feature extraction at scale is the foundation for any downstream ML model.

---

## 2. Machine Unlearning & Privacy

**Central question:** When a patient asks to have their data removed from a trained model, how do we actually do that — especially for multimodal models that have learned from images and text together?

[UnLOK-VQA](https://github.com/multimodal-ariel/UnLOK-VQA) introduced the first multimodal unlearning benchmark, showing that combined image+text attacks are significantly more effective at recovering "forgotten" knowledge than unimodal attacks.

[MedForget](https://github.com/multimodal-ariel/MedForget) extends this to the medical domain, where data has a hierarchical structure (institution → patient → study → section). The CHIP method (Cross-modal Hierarchy-Informed Projection) removes targeted information via orthogonal weight projection without any gradient updates — making it fast enough for clinical deployment.

**Why this matters for lupus:** Medical AI trained on electronic health records must comply with HIPAA and GDPR. Unlearning is the technical mechanism that makes "right to be forgotten" practical.

---

## 3. 3D Medical Image Segmentation

**Central question:** How do we apply foundation models (trained on broad data) to segment specific anatomical structures in CT/MRI without requiring large labeled datasets from the target domain?

[ZS-DG-FM-3D-MedSeg](https://github.com/multimodal-ariel/ZS-DG-FM-3D-MedSeg) studies zero-shot domain generalization — using a single foundation model across modalities and anatomies without domain-specific fine-tuning.

[autoprompt3dseg](https://github.com/multimodal-ariel/autoprompt3dseg) takes an atlas-driven approach: by registering images to a population atlas, anatomical prompts can be generated automatically, removing the need for manual annotation to drive segmentation.

**Why this matters for lupus:** Lupus nephritis, carditis, and pleuritis require accurate organ segmentation in CT/MRI. Label-efficient methods are critical because lupus imaging data is scarce.

---

## 4. Multimodal Representation Learning

**Central question:** How do we build representations that jointly encode imaging, clinical text, and structured EHR data in a way that is both powerful and fair?

This theme covers VLM fine-tuning ([qwen2-vl-finetune](https://github.com/multimodal-ariel/qwen2-vl-finetune)), mixture-of-experts architectures ([moe-retriever](https://github.com/multimodal-ariel/moe-retriever), [flex-moe](https://github.com/multimodal-ariel/flex-moe)) for handling heterogeneous modalities, and recurrent multimodal reasoning ([multimodal-recurrent-reasoning](https://github.com/multimodal-ariel/multimodal-recurrent-reasoning)).

Fairness is a core constraint: representations must perform consistently across sex, race, and age groups, given lupus's uneven demographic distribution.

**Why this matters for lupus:** No single modality captures lupus fully. Joint representation learning is the path to models that can reason across labs, imaging, and notes simultaneously.

---

## 5. Data & Cohort Infrastructure

**Central question:** What data do we actually have, and how do we document it so the whole team can use it consistently?

[unc-omop-cdw-cohorts](https://github.com/multimodal-ariel/unc-omop-cdw-cohorts) documents the UNC OMOP CDW cohorts — the clinical backbone of the project. [UKB_AllofUs](https://github.com/multimodal-ariel/UKB_AllofUs) provides cross-cohort analysis with UK Biobank and the NIH All of Us program, enabling external validation. [tcga](https://github.com/multimodal-ariel/tcga) supports cancer-adjacent immunology work.

**Why this matters for lupus:** Cohort quality determines everything downstream. OMOP standardization allows reproducible cohort definitions across healthcare systems.
