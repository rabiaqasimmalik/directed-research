# Rabia Qasim | Research Portfolio

Welcome to my research portfolio! I'm Rabia, an Economics student who is super passionate about uncovering the forces that drive human and economic decisions. I love blending behavioral economics with public policy to tackle real-world development challenges.

To bring these empirical puzzles to life, I’ve built a versatile and robust toolkit: I handle heavy-duty econometric modeling in Stata, write clean data-driven code in Python, and typeset polished research papers in LaTeX. I am highly adaptable, constantly curious, and always ready to master whatever new tool or methodology is required to turn raw data into meaningful impact!

[📩 Email Me](mailto:rabiaaaa101@gmail.com) | [💼 LinkedIn](/https://www.linkedin.com/in/rabia-qasim-480526309/?isSelfProfile=false) | [📄 View Resume](./Rabia%20Qasim%20CV.docx)
---

## My Data Toolkit & Research Powers

* **Econometric Modeling (Stata & Python):** Applying rigorous causal inference techniques—including OLS, Instrumental Variables (IV), Difference-in-Differences (DiD), and Panel Data to evaluate policy questions.
* **Data Management & Wrangling:** Merging, cleaning, and structuring large-scale administrative datasets and national household surveys to build reliable, analysis-ready datasets.
* **Visualization:** Transforming complex quantitative data into clean, interactive, and highly intuitive visuals for diverse stakeholders.
* **Typesetting & Reporting (LaTeX):** Currently wokring on how to produce publication-ready research papers with professional mathematical formatting, dynamic tables, and precise referencing.
* **Reproducible Research:** Generating journal-standard regression outputs using `estout` and `outreg2`, and designing custom `twoway` data visualizations in Stata to ensure completely reproducible workflows.

---

## 📁 Featured Research Projects
 
  ### 1. [Empirical Analysis of Female Labor Force Participation (FLFP) in Urban Pakistan](./Informal-Economy-Research)
* **Objective:** Investigated the determinants of FLFP, testing the "Feminization U-Hypothesis" and examining why rising female educational attainment hasn't fully translated into proportional labor market entry.
* **Dataset:** Utilized the individual-level microdata from the **Pakistan Social and Living Standards Measurement (PSLM) Survey**, cleaning and merging demographic, education, and household asset modules.
* **Methodology:** 
  * Estimated a binary **Probit Model** using Maximum Likelihood Estimation (MLE) to compute marginal effects of education and household wealth.
  * Controlled for regional labor market disparities using **District-Level Fixed Effects**.
  * Addressed heteroskedasticity by **clustering standard errors** at the community/PSU (Primary Sampling Unit) level.
* **Key Findings:** Confirmed a strong household "income effect," where middle-class wealth correlation acts as a barrier to participation. The positive "substitution effect" of education only becomes statistically and economically significant at the tertiary level, indicating structural barriers for moderately educated women.
* **Key Files:** 
  * [`cleaning_and_probit.do`](./Informal-Economy-Research/code/cleaning_and_probit.do) — Stata replication do-file (fully commented).
  * [`econometric_paper.pdf`](./Informal-Economy-Research/documents/econometric_paper.pdf) — Complete research paper typeset in LaTeX.
 
  * ### 1. [Empirical Analysis of Female Labor Force Participation (FLFP) in Urban Pakistan](./Informal-Economy-Research)

*   **Objective:** Investigated the microeconomic and cultural determinants of FLFP in urban Pakistan, specifically testing the "Feminization U-Hypothesis" and measuring the competing substitution and household income effects on female labor supply.
*   **Microdata & Wrangling Nuances:**
    *   Utilized individual-level microdata from the **Pakistan Social and Living Standards Measurement (PSLM) Survey**.
    *   Executed complex data-cleaning in Stata, merging multiple raw ASCII modules (Education, Employment, and Demographics) using unique geographic and household identifiers (`hhcode`, `iec`).
    *   Built a continuous **Asset-Based Wealth Index** using Principal Component Analysis (PCA) on household-level assets to proxy for unobserved household lifetime income.
*   **Econometric Methodology:**
    *   **Model:** Estimated a binary **Probit Model** using Maximum Likelihood Estimation (MLE) to compute Average Marginal Effects (AMEs).
    *   **Identification Strategy:** Controlled for localized labor market and social variations by introducing **District-Level Fixed Effects**.
    *   **Standard Errors:** Addressed intra-cluster correlation by **clustering standard errors at the primary sampling unit (PSU) level** to prevent overstating $t$-statistics.
    *   **Robustness Check:** Addressed selection bias in female wage equations using a two-step **Heckman Selection Correction Model** (using the presence of infants/children as an exclusion restriction/instrument).
*   **Key Academic Conclusions:** 
    *   Empirically validated the **Feminization U-Hypothesis**. Lower-educated women exhibit high distress-driven informal employment. Rising middle-class household wealth triggers a strong household "income effect," which, coupled with conservative social norms, suppresses FLFP. 
    *   The positive "substitution effect" only dominates at the tertiary education level (undergraduate degree and above), where the opportunity cost of remaining outside the formal workforce becomes too high to ignore.
*   **Key Stata Code Features:**
    *   [`merge_and_clean.do`](./Informal-Economy-Research/code/merge_and_clean.do) — Appending/merging raw survey rounds and executing PCA for the wealth index.
    *   [`probit_models.do`](./Informal-Economy-Research/code/probit_models.do) — Probit estimation, calculating AMEs, exporting journal-quality tables with `esttab`/`estout`.
