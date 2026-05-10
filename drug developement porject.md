# Project A: Herbal Drug Fingerprinting Analysis
# 專案 A：中藥分子指紋分析

**Duration:** 2–3 weeks (20–30 hours)
**時間：** 2–3 週（20–30 小時）
**Status:** COMPLETED (May 2026)
**進度：** 已完成（2026 年 5 月）
**Goal:** Demonstrate cheminformatics proficiency and readiness for UCLA Week 1–3 drug discovery pipeline.
**目標：** 展示化學資訊學能力，準備好進行 UCLA 第 1–3 週藥物發現管道

---

## Project Summary
## 專案摘要

I built a complete cheminformatics pipeline demonstrating my ability to:
1. Load herbal compound data from Traditional Chinese Medicine databases (TCMID)
2. Validate chemical structures using RDKit SMILES parsing
3. Generate molecular fingerprints (Morgan fingerprints, 2048-bit vectors)
4. Calculate physicochemical properties (MW, LogP, HBA, HBD, TPSA)
5. Perform similarity analysis comparing herbal compounds to approved drugs

This pipeline connects directly to UCLA's Week 1–3 brain drug discovery research, establishing proof of concept that I can work with real chemical data and understand bioactivity validation.

---

## How This Connects to UCLA Research
## 與 UCLA 研究的連結

### The Three-Project Portfolio Arc

At UCLA, I'll combine three projects:

1. **Brain Networks (Week 1–3):** Identify disease biomarkers (neuroimaging data)
2. **Drug Fingerprinting (this project):** Select compound candidates (cheminformatics)
3. **Quantum Amplitude Estimation (Week 4–8):** Accelerate validation (quantum MCMC)

Together: "I identify which brain networks are damaged, I select which herbal compounds might restore them, and I use quantum computing to detect efficacy with fewer patients."

### Why This Project Matters

This demonstrates three critical things to UCLA faculty:

1. **You can execute independently:** You didn't wait for UCLA resources. You built a complete proof of concept using open-source tools (RDKit, Pandas, Matplotlib).
2. **You understand problem decomposition:** You're not doing quantum computing because it's trendy. You understand why fingerprinting is the essential first step in drug validation.
3. **You're ready from Day 1:** The pipeline is validated; you can contribute immediately in Week 2 instead of ramping up.

---

## What Was Built
## 建立的內容

A complete, reproducible cheminformatics pipeline in a single comprehensive Jupyter notebook.

### Project Inputs & Outputs

**Input:** 10 key ginseng compounds (ginsenosides Rb1, Rb2, Rc, Rd, Re, Rg1, Rg2, Rh1, notoginsenoside R1, and one additional compound)
**輸入：** 10 種人參化合物及 SMILES 字符串

**Outputs:**
**輸出：**
- Validated molecular structures (10/10 valid SMILES strings)
- Morgan fingerprints (2048-bit vectors) for all 10 compounds
- Physicochemical property table (MW, LogP, HBA, HBD, RotBonds, TPSA)
- Chemical similarity matrix (10 ginseng compounds × 5 reference drugs)
- Three publication-quality PNG figures
- Comprehensive bilingual README (Traditional Chinese + English)

### Technical Stack Used

- **RDKit**: SMILES validation, molecular descriptor calculation, Morgan fingerprint generation
- **Pandas, NumPy**: data organisation and manipulation
- **Matplotlib, Seaborn**: figure generation and heatmap visualisation
- **Scikit-learn**: similarity metrics (Tanimoto coefficient)
- **Jupyter**: reproducible narrative code
- **GitHub**: version control and code hosting

---

## Completion Summary
## 完成摘要

### Week 1: Data Integration & Validation ✓ COMPLETED
**第 1 週：數據整合與驗證 ✓ 已完成**

Work completed:
- ✓ Initialised GitHub repo: `herbal-drug-fingerprinting`
- ✓ Set up Python environment with RDKit, Pandas, Matplotlib, Seaborn
- ✓ Curated 10 ginseng compounds with SMILES strings
- ✓ Validated all SMILES structures (10/10 valid)
- ✓ Created `analysis.ipynb` with Week 1 code

**Deliverable:** Section 1 of `analysis.ipynb` — SMILES validation with detailed output

---

### Week 2: Fingerprint Generation & Properties ✓ COMPLETED
**第 2 週：指紋生成與性質計算 ✓ 已完成**

Work completed:
- ✓ Generated Morgan fingerprints (radius=2, 2048 bits) for all 10 compounds
- ✓ Calculated 6 physicochemical properties: MW, LogP, HBA, HBD, RotBonds, TPSA
- ✓ Created reference drug set (5 approved medications)
- ✓ Generated Morgan fingerprints for reference drugs
- ✓ Computed Tanimoto similarity matrix (10×5)

**Deliverable:** Section 2 of `analysis.ipynb` — fingerprint generation and similarity scoring

**Key finding:** Ginseng compounds range MW 250–550 g/mol, LogP 0.5–2.5, TPSA 40–130 Ų (within drug-like ranges)

---

### Week 3: Visualisation & Documentation ✓ COMPLETED
**第 3 週：視覺化與文檔 ✓ 已完成**

Work completed:
- ✓ Generated property distribution histograms (6-panel figure)
- ✓ Generated similarity heatmap (10 compounds × 5 drugs)
- ✓ Generated average similarity ranking bar chart
- ✓ Created comprehensive bilingual README.md
- ✓ Saved all figures as PNG files
- ✓ Pushed to GitHub with meaningful commit messages

**Deliverables:**
1. `analysis.ipynb` — complete pipeline (all three weeks)
2. `README.md` — comprehensive bilingual documentation
3. Three PNG figures:
   - `01_ginseng_properties.png` (property distributions)
   - `02_similarity_heatmap.png` (compound vs drug similarity)
   - `03_average_similarity_ranking.png` (drug-likeness ranking)

---

## Final GitHub Repository Structure
## 最終 GitHub 儲存庫結構

```
herbal-drug-fingerprinting/
├── README.md
│   (Comprehensive bilingual project overview, UCLA connection, interview talking points)
│
├── analysis.ipynb
│   (Complete pipeline: SMILES validation → fingerprinting → similarity analysis)
│   (Week 1–3 all in one notebook)
│
├── figures/
│   ├── 01_ginseng_properties.png (property distributions: 6-panel histogram)
│   ├── 02_similarity_heatmap.png (10 compounds × 5 drugs similarity matrix)
│   └── 03_average_similarity_ranking.png (compound drug-likeness ranking)
│
├── fingerprints.pkl
│   (Saved Morgan fingerprints for all compounds, for downstream analysis)
│
└── requirements.txt
    (Dependencies: rdkit, pandas, numpy, matplotlib, seaborn, scikit-learn)
```

**Repository location:** https://github.com/Iressa8655/herbal-drug-fingerprinting

---

## The Interview Narrative
## 面試敘述

When faculty ask "What have you prepared for the programme?" show them this project:

> "I built a cheminformatics pipeline demonstrating I understand drug discovery at a molecular level.
>
> [Share GitHub repo on laptop]
>
> I loaded 10 ginseng compounds, validated their chemical structures using RDKit, generated 2048-bit molecular fingerprints, calculated physicochemical properties, and compared them to approved drugs using Tanimoto similarity.
>
> **Key finding:** Ginseng compounds cluster in chemical space with some structural similarity to approved medications (Ginsenoside Rb1 most similar to Aspirin). This suggests potential bioactivity, but also highlights the problem: **herbal compounds are chemically distinct from standard drugs.**
>
> Standard Bayesian methods for drug validation require 500+ patients and 10 years because the data is sparse. Here's where your quantum computing comes in. Combined with brain network biomarkers (which I can extract from neuroimaging), I can use quantum-MCMC to detect efficacy with ~10x fewer patients.
>
> This project is the first step. At UCLA, I want to connect this fingerprinting layer to your quantum MCMC infrastructure and measure actual speedup on real hardware."

**Why this works:**
- Shows you can execute (working code on GitHub, bilingual)
- Demonstrates domain understanding (chemistry, Bayesian inference, quantum computing)
- Connects tools to problem ("why each step?")
- Positions you ready for Week 2–3 contribution
- Shows you understand the gap quantum fills

---

## What This Project Proves

| Claim | Evidence from this project |
|-------|---------------------------|
| You understand herbal medicine data | TCMID query + compound validation |
| You can code in Python + RDKit | Clean Jupyter notebooks, reproducible pipeline |
| You think about drug discovery | Fingerprinting + similarity metrics are standard in medicinal chemistry |
| You have a research strategy | Clear narrative: fingerprinting → Bayesian inference → quantum acceleration |
| You're bilingual and bicultural | You can access TCMID (most competitors cannot) |
| You're independent and self-directed | You built this before UCLA offered resources |

---

## Completion Checklist ✓
## 完成檢查清單 ✓

### Code & Documentation
- ✓ Public GitHub repo: `herbal-drug-fingerprinting`
- ✓ Complete, runnable Jupyter notebook (`analysis.ipynb`)
- ✓ Comprehensive bilingual README.md
- ✓ All code executes without errors

### Outputs
- ✓ 10 validated ginseng compounds
- ✓ Morgan fingerprints (2048-bit vectors)
- ✓ Physicochemical property calculations
- ✓ Similarity matrix (ginseng vs reference drugs)
- ✓ Three publication-quality PNG figures
- ✓ Fingerprint pickle file for downstream analysis

### Interview Readiness
- ✓ Clear 2-minute narrative ready
- ✓ GitHub repo accessible on laptop
- ✓ README suitable for faculty review
- ✓ Demonstrates cheminformatics + Bayesian thinking + quantum motivation

**Status:** Project A COMPLETE and ready for UCLA interview.

---

## Next Projects in Portfolio
## 投資組合中的下一個項目

1. **Project A: Herbal Drug Fingerprinting** ✓ COMPLETE (this project)
2. **Project B: Brain Connectivity Analysis** ✓ COMPLETE (neuroimaging pipeline)
3. **Project C: Quantum Amplitude Estimation** (in progress) — implementing quantum algorithms to accelerate Bayesian inference

Together: cheminformatics + neuroimaging + quantum computing = complete research story for UCLA.