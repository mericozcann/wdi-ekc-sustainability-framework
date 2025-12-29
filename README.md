# WDI–EKC Sustainability Assessment Framework  
**ASA International Data Quest (Türkiye) — Smyrna DataLab Team Submission**

This repository contains our end-to-end sustainability assessment workflow based on the **Environmental Kuznets Curve (EKC)** using the **World Development Indicators (WDI)** dataset. The work was prepared as part of the **ASA International Data Quest**, an annual data event sponsored by the **American Statistical Association (ASA) Committee on International Relations in Statistics**, starting in **Fall 2025**.

Our deliverables emphasize:
- **Statistical insight** (EKC modeling and interpretation),
- **Ethical practice** aligned with the **ASA Ethical Guidelines for Statistical Practice**,
- **Clear communication** through a 5-minute video and a concise slide deck.

---

## Competition Context (ASA International Data Quest)

**Format and timeline**
- The dataset is released on the **first Monday of October**.
- Teams work throughout **October**.
- Submissions are due on the **last Friday of October** and must include:
  - A **5-minute video presentation**
  - **Slides** (max **4 content slides**, excluding cover and references)

**Award categories (undergraduate and master’s levels, evaluated separately)**
- Best Data Visualization  
- Best Consideration of Ethics  
- Best Statistical Insight  

**Eligibility**
- Teams of **2–4** students (either **undergraduate** *or* **master’s**; no mixing categories)
- Students from **any discipline** may participate

---

## Repository Contents

- **WDI - EKC Sustainability Assessment Framework.ipynb**  
  Main notebook: data preparation, transformations, EKC modeling, and interpretation.

- **Database.ipynb**  
  Dataset handling utilities and structured extraction steps.

- **Final Analysis Report.pdf**  
  Consolidated results for 2000–2020 (including EKC shape interpretation and green growth candidates).

- **General EDA Report.pdf**  
  Dataset-wide exploratory diagnostics and high-level distributional findings.

- **DataLab Ethical Guidelines.pdf**  
  Applied ethics checklist aligned with ASA principles (transparency, assumptions, limitations, privacy).

- **Database Guidelines.pdf**  
  Dataset standards and handling guidance used in this work.

- **Development Guidelines After Final Analysis.pdf**  
  Post-final roadmap: FE/RE panel validation, optimization, turning-point computation, and reporting.

- **Exploratory Data Analysis.zip**  
  Supporting EDA artifacts (plots, summaries, intermediate outputs).

- **WDI_EKC_outputs.zip**  
  Exported outputs for reporting and visualization tooling (tables, candidates lists, figures).

- **Work Presentation.pptx**  
  Slide deck prepared for submission (concise, competition-compliant).

- **ASA DATA QUEST Smyrna DataLab Team Presentation by Meriç Özcan.mp4**  
  5-minute video presentation aligned with the slide deck.

---

## Project Workflow (Mermaid)

```mermaid
flowchart TD
  A[Dataset Release (First Monday of October)] --> B[Dataset Intake & Governance]
  B --> B1[Database Guidelines]
  B --> B2[Ethical Guidelines (ASA-aligned)]
  B --> C[Exploratory Data Analysis]
  C --> C1[Missingness & Coverage Diagnostics]
  C --> C2[Outliers & Scaling Checks]
  C --> C3[Regional/Topic Balance Checks]
  C --> D[Analysis Design]
  D --> D1[Define Time Window (e.g., 2000–2020)]
  D --> D2[Transformations (log GDP, winsorization if needed)]
  D --> E[EKC Modeling]
  E --> E1[Pooled OLS: CO2 ~ log(GDP) + log(GDP)^2]
  E --> E2[Model Diagnostics & Visual Validation]
  E --> F[Green Growth Identification]
  F --> F1[GDP Increase & CO2 Decrease (2000–2020)]
  F --> F2[Country Profiles & Evidence Plots]
  F --> G[Reporting & Communication]
  G --> G1[Final Analysis Report (PDF)]
  G --> G2[Slide Deck (PPTX)]
  G --> G3[5-Min Video (MP4)]
  G --> H[Post-Final Development]
  H --> H1[Panel FE/RE Validation + Hausman Test]
  H --> H2[GridSearchCV Optimization (Degree 1–3, Alpha 0.01–1000)]
  H --> H3[Turning Point Computation]
  H --> H4[Power BI/Tableau Templates & Executive Summary]
```
