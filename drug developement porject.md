# Project A: Chinese Herbal Compound Fingerprinting Pipeline
# 方案 A：中藥分子指紋分析管道

**Duration:** 2–3 weeks (20–30 hours)
**時間：** 2–3 週（20–30 小時）
**Status:** Planning phase (pre-UCLA internship)
**進度：** 規劃階段（UCLA 實習前）
**Goal:** Build hands-on proof of concept connecting herbal medicine + cheminformatics, demonstrating readiness for UCLA Week 2–3 project.
**目標：** 建立中藥化學資訊學概念驗證，展示對 UCLA 第 2–3 週專案的準備

---

## How This Connects to Your UCLA Proposal
## 與你的 UCLA 提案的連結

### Your UCLA Interview Pitch
Your proposed project at UCLA: *"Build a pipeline: Chinese herbal compound → cheminformatics features → quantum-Bayesian inference for efficacy prediction."*

**This project is the first 50% of that pipeline.** You're building the crucial initial step:
1. **Herbal compound → cheminformatics features** (這個專案)
2. **Then at UCLA:** Add quantum-Bayesian layer (Weeks 4–8)

### Why This Matters for the Interview
This project demonstrates three critical things to UCLA faculty:

1. **You're ready from Day 1:** Most interns need 2 weeks to ramp up. You'll be ready in Week 2 because you've already validated the data pipeline.
2. **You understand problem decomposition:** You're not just doing quantum computing because it's trendy. You understand why fingerprinting is the necessary first step.
3. **You can execute independently:** You didn't wait for their resources. You built the proof of concept using open-source tools and public databases.

---

## Technical Scope
## 技術範圍

### What You're Building
A reproducible Python pipeline that extracts herbal compounds from Traditional Chinese Medicine databases and generates interpretable chemical features for bioactivity prediction.

### Project Inputs & Outputs

**Input:** One popular TCM remedy (e.g. Ginseng, Cordyceps, Goji Berry)
**輸入：** 一種常見中藥（例如人參、蟲草、紅棗）

**Output:**
**輸出：**
- Molecular fingerprints for all key compounds
- Chemical similarity matrix (herbal compounds vs. approved drugs)
- Visualisation dashboard (PCA plot, heatmap, property comparison)
- 1-page summary report: "Which herbal compounds are most drug-like?"

### Technical Stack
- **TCMID** (Traditional Chinese Medicine Integrated Database): structure data for 10,000+ herbal compounds
- **RDKit**: molecular descriptor calculation, similarity metrics
- **PubChem** (optional): reference drug structures (aspirin, paracetamol, metformin)
- **Pandas, NumPy, Matplotlib, Scikit-learn**: data processing and visualisation
- **GitHub**: version control, code hosting

---

## Week-by-Week Breakdown
## 周年週期分解

### Week 1: Setup + TCMID Integration (6–8 hours)
**第 1 週：設定 + TCMID 整合（6–8 小時）**

Tasks:
- [ ] Initialize GitHub repo: `herbal-drug-fingerprinting`
- [ ] Create Python virtual environment, install dependencies (RDKit, Pandas, Matplotlib)
- [ ] Connect to TCMID API or download compound CSV
- [ ] Query for one remedy: Red Ginseng (*Panax ginseng* C.A. Mey)
- [ ] Extract 8–12 key compounds (ginsenosides Rb1, Rb2, Rc, Rd, Re, Rg1, Rg2, Rh1, notoginsenoside R1)
- [ ] Validate SMILES strings for all compounds

**Deliverable:** `01_tcmid_query.ipynb`
Document: TCMID lookup, compound extraction, 簡短說明為什麼選擇人參

---

### Week 2: RDKit Fingerprinting (8–10 hours)
**第 2 週：RDKit 分子指紋（8–10 小時）**

Tasks:
- [ ] Load SMILES strings into RDKit
- [ ] Generate Morgan fingerprints (radius=2, 2048 bits) for each ginsenoside
- [ ] Calculate physicochemical properties (MW, LogP, HBA, HBD, RotBonds, TPSA)
- [ ] Build reference drug set (5 approved medications: aspirin, paracetamol, metformin, omeprazole, atorvastatin)
- [ ] Calculate pairwise Tanimoto similarity: ginseng compounds vs. drugs
- [ ] Create summary table: compound name, MW, LogP, most similar approved drug

**Deliverable:** `02_fingerprinting.ipynb`
Code: fingerprint generation, similarity scoring, property table export

---

### Week 3: Visualisation + Write-up (4–6 hours)
**第 3 週：視覺化 + 撰寫總結（4–6 小時）**

Tasks:
- [ ] Fit PCA on all compound fingerprints (herbal + drugs combined)
- [ ] Plot 2D PCA: colour by compound type (ginseng, drug, other TCM if added)
- [ ] Generate heatmap: Tanimoto similarity matrix (ginseng × drugs)
- [ ] Create property comparison bar charts (MW, LogP distributions)
- [ ] Write 1-page summary: motivation, methods, key findings, implications for UCLA quantum project
- [ ] Final code check: run entire pipeline end-to-end without errors

**Deliverable:** `03_visualisation.ipynb` + `RESULTS.md` + PNG figures

---

## Final GitHub Repo Structure
## 最終 GitHub 倉庫結構

```
herbal-drug-fingerprinting/
├── README.md 
│   (Project overview, UCLA connection, how to run)
├── 01_tcmid_query.ipynb
│   (TCMID lookup, compound extraction)
├── 02_fingerprinting.ipynb
│   (RDKit fingerprints, similarity scores)
├── 03_visualisation.ipynb
│   (PCA, heatmaps, property analysis)
├── data/
│   ├── ginseng_compounds.csv
│   ├── drug_reference.csv
│   └── fingerprints.pkl
├── figures/
│   ├── pca_plot.png
│   ├── similarity_heatmap.png
│   ├── property_comparison.png
│   └── ginsenoside_structures.png
├── RESULTS.md
│   (1-page summary for UCLA interview)
└── requirements.txt
    (dependencies: rdkit, pandas, matplotlib, numpy)
```

---

## The Interview Narrative
## 面試敘述

When Holbrook or faculty ask "What research have you done?" walk them through this:

> "Before coming to UCLA, I built a proof of concept connecting my two interests: herbal medicine and cheminformatics.
>
> [Share GitHub repo on your laptop]
>
> I queried TCMID for ginseng compounds, generated RDKit molecular fingerprints, and compared them to approved drugs. What I found is that ginsenoside compounds cluster in a distinct region of chemical space, with some overlap to immunomodulators but clear separation from most approved drugs.
>
> This is the critical insight: **herbal compounds live in a sparsely explored region of drug space.** Standard Bayesian methods struggle here because the trial sample sizes are small. That's where your quantum-MCMC work becomes essential. By accelerating the posterior sampling, we can validate herbal efficacy faster with fewer trials.
>
> At UCLA, I want to scale this to 50 herbal remedies and prototype the quantum inference layer using your hardware."

**Why this narrative works:**
- Shows you understand the problem (sparse data in herbal space)
- Connects cheminformatics → quantum computing (not arbitrary)
- Demonstrates you've thought beyond the tooling ("why quantum?" answered)
- Positions you as ready for Week 2 contribution

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

## Success Criteria
## 成功標準

By end of Week 3, you should have:
- ✓ Public GitHub repo with 3 clean, documented Jupyter notebooks
- ✓ End-to-end pipeline: TCMID → RDKit → visualisation (zero errors on full run)
- ✓ 1-page RESULTS.md suitable for printing or email to faculty
- ✓ PNG figures (PCA, heatmap) for presentation
- ✓ Clear 2-minute narrative connecting fingerprinting → UCLA quantum project
- ✓ README that explains UCLA context without over-claiming

This becomes your **portfolio evidence of research maturity**. Walk into the interview with working code and a documented research trajectory.

---

## Next Actions
## 下一步

1. Create GitHub repo: `herbal-drug-fingerprinting`
2. Begin Week 1 (TCMID setup) within next 3 days
3. Target completion: June 2026 (at least 1 week before UCLA interview)
4. Practice your 2-minute narrative in front of a mirror before the interview
5. Have laptop ready to show them the repo during the interview