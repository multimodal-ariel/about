# Getting Started

Welcome to mm-ARIEL. This page helps new contributors get oriented quickly.

---

## Who is this project for?

mm-ARIEL is a research organization. Contributors are typically:
- Graduate students and postdocs working on specific subprojects
- Collaborating PIs integrating their own datasets or methods
- Research engineers building shared infrastructure

Most repositories are standalone research codebases — not a single monolithic system. You'll likely only need to work in one or two repos at a time.

---

## Step 1: Understand the big picture

Read [Research Areas](Research-Areas) to understand how the five themes relate. Then look at [Repository Overview](Repository-Overview) to find which repos are relevant to your subproject.

---

## Step 2: Find your entry point

| Your role | Start here |
|---|---|
| Working on clinical imaging / CDW | [visual-agentic-cdw](https://github.com/multimodal-ariel/visual-agentic-cdw) · [XRayFeatures](https://github.com/multimodal-ariel/XRayFeatures) |
| Working on machine unlearning | [UnLOK-VQA](https://github.com/multimodal-ariel/UnLOK-VQA) · [MedForget](https://github.com/multimodal-ariel/MedForget) |
| Working on 3D segmentation | [autoprompt3dseg](https://github.com/multimodal-ariel/autoprompt3dseg) · [ZS-DG-FM-3D-MedSeg](https://github.com/multimodal-ariel/ZS-DG-FM-3D-MedSeg) |
| Working on VLMs / representation learning | [qwen2-vl-finetune](https://github.com/multimodal-ariel/qwen2-vl-finetune) · [flex-moe](https://github.com/multimodal-ariel/flex-moe) |
| Working on cohort data | [unc-omop-cdw-cohorts](https://github.com/multimodal-ariel/unc-omop-cdw-cohorts) |

---

## Step 3: Environment setup basics

Most Python repositories use **conda** environments. The general pattern is:

```bash
# Clone the repo
git clone https://github.com/multimodal-ariel/<repo-name>
cd <repo-name>

# Create and activate conda environment
conda env create -f environment.yml   # or requirements.txt
conda activate <env-name>

# Or pip install
pip install -r requirements.txt
```

**Note:** `visual-agentic-cdw` is different — it uses *multiple* conda environments (one per segmentation tool). See its wiki for details.

---

## Step 4: Data access

Most datasets used in this project require credentialed access:

- **UNC CDW imaging data** — requires IRB approval and UNC system access. Contact the PI.
- **MIMIC-CXR** (used by MedForget) — requires a PhysioNet credentialed account at [physionet.org](https://physionet.org).
- **UK Biobank / All of Us** — requires approved project access through each program's application process.
- **TCGA** — publicly available via [GDC Data Portal](https://portal.gdc.cancer.gov/).
- **UnLOK-VQA dataset** — publicly available on [HuggingFace](https://huggingface.co/datasets/vaidehi99/UnLOK-VQA).
- **COCO images** (used by UnLOK-VQA) — publicly available.

---

## Step 5: GitHub conventions

- Each repo has its own `README.md` as the primary technical reference.
- Wikis (like this one) provide higher-level orientation and cross-repo context.
- Issues and pull requests are used within each repo independently.
- There is no shared CI/CD pipeline across repos — each manages its own.

---

## Questions?

Check the individual repo READMEs first. For org-level questions, open an issue in the [about](https://github.com/multimodal-ariel/about) repo.
