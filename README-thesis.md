# 📊 Factors Influencing E-Commerce Purchase Intention During COVID-19
### Structural Equation Modeling (SEM) Research — Ecuador, 2021

> **Undergraduate Thesis** · Universidad de las Fuerzas Armadas ESPE · Business Administration  
> Supervisor: PhD. Alfredo Salazar Baño · September 2021

---

## 🔍 Research Question

*What factors have influenced the purchase intention of consumers in Quito, Ecuador, regarding e-commerce since the COVID-19 pandemic?*

Ecuador's e-commerce sector grew rapidly before the pandemic (16M transactions, $1.29B in sales in 2018), but the COVID-19 crisis accelerated digital adoption at an unprecedented rate — while also exposing critical structural barriers to sustained e-commerce growth such as digital trust, service quality, and user experience.

---

## 🎯 Objectives

**General:** Determine the factors that have influenced online purchase intention among consumers in the Metropolitan District of Quito (DMQ) since the pandemic.

**Specific objectives:**
- Identify the factors that influence purchase intention in e-commerce
- Determine the most important factors that affected online purchasing behavior post-pandemic
- Formulate actionable proposals for food & beverage companies seeking to enter the e-commerce space in Quito

---

## 🧠 Theoretical Framework

The study is built on three theoretical pillars:

| Theory | Application |
|---|---|
| **UTAUT 2** (Venkatesh et al.) | Framework for technology acceptance — performance expectancy, social influence, facilitating conditions, hedonic motivation, habit |
| **Three-Component Model** (Rust & Oliver) | Measurement of perceived service quality in e-commerce contexts |
| **Maslow's Hierarchy of Needs** | Contextualizing consumer behavior and digital motivation |

The initial model was adapted from **Dakduk, Santalla et al. (2020)** — *"Acceptance of mobile commerce in low-income consumers: evidence from an emerging economy"* — and extended to include a **Service Quality (CSB)** construct.

---

## 🗂️ Study Design

| Parameter | Detail |
|---|---|
| Research approach | Mixed (quantitative + qualitative validation) |
| Study type | Correlational |
| Target population | Quito residents aged 18–65 who purchased online during the pandemic |
| Sampling method | Non-probabilistic, database-based |
| Data collection | 5-point Likert scale survey, applied online |
| Expert validation | 6 specialists (marketing, e-commerce, consulting) |
| Final sample | **n = 384 participants** |
| Software | SPSS · SPSS AMOS · R |

---

## 📐 Variables (Final Model)

After expert validation, pilot testing, EFA and CFA respecification, the final model retained **5 latent variables**:

| Code | Latent Variable | Items (final) | Cronbach's α | AVE | CR |
|---|---|---|---|---|---|
| **ER** | Performance Expectancy | 3 | 0.917 | 0.766 | 0.908 |
| **IS** | Social Influence | 3 | 0.892 | 0.697 | 0.873 |
| **CF** | Facilitating Conditions | 3 | 0.897 | 0.745 | 0.897 |
| **H** | Habit | 3 | 0.867 | 0.619 | 0.830 |
| **CSB** | Perceived Service Quality | 6 | 0.909 | 0.628 | 0.909 |

> Variables eliminated during analysis: Hedonic Motivation (MH), Perceived Trust/Security (SyCP), and Purchase Intention (IC) — the latter due to insufficient observable indicators after CFA respecification.

---

## 🔬 Methodology — Analytical Pipeline

```
Survey (n=384)
    ↓
Assumption checks
  · Normality: skewness/kurtosis (±1.5) + Royston test in R
  · Collinearity: r ≥ 0.30 between items
  · Multicollinearity: bivariate correlations < 0.85
    ↓
Cronbach's Alpha
  · Threshold: α ≥ 0.70
  · Action: removed SP3 to bring SP above threshold
    ↓
Exploratory Factor Analysis (EFA) — SPSS
  · Extraction: Principal Axis Factoring (non-normal data)
  · Rotation: Varimax (inter-item correlations < 0.70)
  · KMO = 0.962 (excellent) · Bartlett p < .001
  · 8 factors extracted · Factor 1 explains 45.95% of variance
    ↓
Cronbach's Alpha (post-EFA) — all constructs ≥ 0.70 ✓
    ↓
Confirmatory Factor Analysis (CFA) — SPSS AMOS
  · Method: Maximum Likelihood
  · Iterative respecification via Modification Indices (MI)
  · Convergent validity: AVE > 0.50, CR > 0.70
  · Two models compared (Model 1 vs Model 2)
    ↓
Structural Equation Modeling (SEM) — SPSS AMOS
  · Final model built on CFA output
  · Respecification: correlated errors in ER and H
  · Goodness-of-fit evaluated across 8 indices
```

---

## 📊 Key Results

### Exploratory Factor Analysis (EFA)

| Metric | Value | Assessment |
|---|---|---|
| KMO | 0.962 | Excellent (> 0.90) |
| Bartlett's test | p < .001 | Valid for FA |
| Variance explained (4 factors) | 61.30% | — |
| Factor 1 variance | 45.95% | Dominant factor |

### CFA — Goodness of Fit (Final Model vs Initial)

| Index | Threshold | CFA Initial | CFA Final | SEM Final |
|---|---|---|---|---|
| GFI | → 1 | 0.821 | 0.949 | **0.931** |
| RMSEA | ≤ 0.05 | 0.055 ❌ | 0.048 ✅ | **0.046** ✅ |
| NFI | > 0.90 | 0.878 | 0.947 ✅ | **0.950** ✅ |
| TLI/NNFI | ≥ 0.90 | 0.929 ✅ | 0.972 ✅ | **0.974** ✅ |
| CFI | > 0.90 | 0.935 ✅ | 0.977 ✅ | **0.979** ✅ |
| PGFI | → 1 | 0.710 | 0.679 | 0.675 |
| AIC | → 0 | 1543.0 | 309.6 | **301.4** |

### SEM — Hypothesis Testing

| Structural Path | p-value | Result |
|---|---|---|
| Social Influence (IS) → Habit (H) | p < .001 | ✅ Supported |
| Facilitating Conditions (CF) → Habit (H) | p < .001 | ✅ Supported |
| Performance Expectancy (ER) → Habit (H) | p = .333 | ❌ Not supported |
| ER ↔ IS (correlation) | p < .001 | ✅ Supported |
| ER ↔ CF (correlation) | p < .001 | ✅ Supported |
| IS ↔ CF (correlation) | p < .001 | ✅ Supported |

---

## 💡 Conclusions

The original objective of identifying factors influencing **purchase intention** (IC) could not be fully tested because the IC variable was eliminated during CFA respecification due to insufficient observable indicators. However, the study produced a valid and well-fitted alternative model explaining **Perceived Service Quality (CSB)**.

Key findings:
- **Social Influence and Facilitating Conditions** are significant predictors of Habit in e-commerce usage
- **Performance Expectancy does not significantly predict Habit** (p = .333), suggesting that in Quito's e-commerce context, perceived usefulness alone does not drive behavioral habits
- **Habit shows a strong correlation with Service Quality (CSB)**, indicating that habitual users have higher service quality expectations
- The constructs ER, IS and CF are strongly correlated with each other, suggesting they capture overlapping aspects of technology acceptance

---

## 📁 Repository Structure

```
ecommerce-purchase-intention-sem/
├── README.md                             ← This file
├── thesis-dashboard.html                 ← Interactive statistical results dashboard
├── FINAL_TESIS_MARROQUIN_DANIEL.docx     ← Full thesis document
```

---

## 🛠️ Tools & Techniques

| Tool | Purpose |
|---|---|
| **SPSS** | Descriptive statistics, Cronbach's α, EFA (KMO, Bartlett, factor extraction & rotation) |
| **SPSS AMOS** | CFA, SEM, modification indices, goodness-of-fit |
| **R** | Multivariate normality test (Royston) |
| **Microsoft Excel** | Data cleaning and preliminary descriptives |

**Statistical methods:** Exploratory Factor Analysis · Confirmatory Factor Analysis · Structural Equation Modeling · Principal Axis Factoring · Varimax Rotation · Maximum Likelihood Estimation · Cronbach's Alpha · AVE · Composite Reliability

---

## 📖 Key References

- Dakduk, S., Santalla, Z., & Siqueira, J. (2020). Acceptance of mobile commerce in low-income consumers: evidence from an emerging economy. *Heliyon, 6*(11).
- Venkatesh, V. et al. (2012). Consumer acceptance and use of information technology: extending the unified theory. *MIS Quarterly, 36*(1).
- Lévy, J. P., & Varela, J. (2006). *Modelización con Estructuras de Covarianzas en Ciencias Sociales.*
- Escobedo, M. et al. (2016). Modelos de Ecuaciones Estructurales. *Cienc Trab, 18*(55).

---

*Research by Daniel Marroquín · Vancouver, BC · Open to roles in Research, Data Analytics, and Finance in Canada*  
*[View interactive dashboard →](./thesis-dashboard.html)*
