---
layout: page
title: ""
description: ""
permalink: /home
---

<style>
  :root {
    --tab-accent:#0a84ff;
    --site-header-h:56px;

    /* UNC-inspired palette */
    --unc-dark: #13294B;       /* UNC navy */
    --unc-gray: #4B4F54;       /* medium gray */
    --unc-bg-light: #A7C7E7;   /* pastel blue 1 */
    --unc-bg-lighter: #D4E6F9; /* pastel blue 2 */
  }

  body {
    font-family: 'Lato', system-ui, -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    font-size: 16px;
    line-height: 1.65;
    color: var(--unc-gray);
    background: linear-gradient(180deg, var(--unc-bg-lighter) 0%, var(--unc-bg-light) 100%);
  }

  main, .page-content { 
    overflow: visible; 
    max-width: 1200px;
    margin: 0 auto; 
    padding: 0 32px;
  }

  h1, h2, h3, h4, h5, h6 {
    font-family: 'Lato', system-ui, sans-serif;
    font-weight: 700;
    color: var(--unc-dark);
  }

  p, li { color: var(--unc-gray); font-size: 17px; line-height: 1.65; }

  /* ── Hide the theme’s auto page title completely ─────────────────────────── */
  .page__header,
  .page__title,
  .page-title,
  .page__header h1 {
    display: none !important;
  }

  /* Custom copyright footer */
  .custom-copy {
    max-width: 1200px;
    margin: 40px auto 24px;
    padding: 16px 32px 0;
    text-align: center;
    color: var(--unc-dark);
    font-size: 14px;
    opacity: .9;
    border-top: 1px solid rgba(19,41,75,.15);
  }

  /* Tabs bar — clean, light look */
  .tabs {
    position: sticky;
    top: 0;
    z-index: 10;
    background: #ffffffdd;
    border-bottom: 1px solid rgba(19,41,75,.15);
    backdrop-filter: blur(6px);
    padding: 10px 0;
    margin: 0 0 20px 0;
  }

  .tabs ul {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 22px;
    list-style: none;
    margin: 0;
    padding: 0;
  }

  .tabs a {
    display: inline-block;
    padding: 6px 10px;
    font-weight: 600;
    color: var(--unc-dark);
    text-decoration: none;
    border-radius: 6px;
    transition: all .18s ease;
  }

  .tabs a:hover {
    background: var(--tab-accent);
    color: #fff;
  }

  .tabs a.active {
    background: var(--unc-dark);
    color: #fff;
  }

  html { scroll-behavior: smooth; }
  h2[id], h3[id] { scroll-margin-top: calc(var(--site-header-h, 0px) + 60px); }
  .top-spacer { clear: both; margin-top: 20px; }
</style>

<nav class="tabs" aria-label="Section navigation">
  <ul>
    <li><a href="#research">Research</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#collaborations">Collaborations</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#teaching">Teaching</a></li>
    <li><a href="#talks">Academic Talks</a></li>
    <li><a href="#life">Life Before the Lab</a></li>
  </ul>
</nav>

<script>
  // Blur links after click to avoid Safari’s lingering outline
  document.querySelectorAll('.tabs a').forEach(a=>{
    a.addEventListener('click', ()=>a.blur(), {passive:true});
  });
</script>

<div class="top-spacer"></div>


## Research Focus {#research}
**Methodological Innovation**  
My research focuses on developing and disseminating advanced statistical methods to address the unique methodological challenges of psychological, behavioral, and social sciences. I primarily work across five statistical frameworks, often integrating them to create synergistic solutions that advance the field:

<div style="margin-top:14px;">
  <img src="{{ '/assets/images/research2.jpg' | relative_url }}"
       alt="Research approaches"
       style="max-width:1100px; width:100%; height:auto; border-radius:15px; display:block; margin:0;" />
</div>
<br>

My methodological work unfolds through three core pipelines:

- Adapting deep learning techniques to enhance traditional psychological methods and meet the demands of research using passive sensing and large-scale behavioral and physiological data  
- Drawing robust inference on intraindividual dynamic processes from limited samples and sparse time points  
- Rethinking imprecision in psychological scales — not merely as measurement error to minimize, but as a source of information to be actively leveraged in statistical modeling

**Substantive Translation**  
<em>Precision psychology</em> is the motivating aim behind translating my core modeling frameworks and methodological innovations into meaningful applications across psychological, behavioral, and social sciences. This includes advancing individualized diagnosis and treatment of mental health conditions, uncovering brain–behavior dynamics, and supporting adaptive interventions in clinical and educational settings. 

---

## Publications {#publications}
### Published  

**Research Articles**  
- **Lee, C.\***, & Gates, K. M. (2025). Automated machine learning for classification and regression: A tutorial for psychologists. <em>Behavior Research Methods</em>, 57(2), 262. [DOI](https://doi.org/10.3758/s13428-025-02684-5)  
- **Lee, C.\***, Luo, L., Kuhlmann, S. L., Plumley, R. D., Panter, A. T., Bernacki, M. L., Greene, J. A., & Gates, K. M. (2025). Interpretable predictive analytics for online learning: A Markov-based machine learning approach. <em>Journal of Learning Analytics</em>, 12(2), 259–278. [DOI](https://doi.org/10.18608/jla.2025.8375)  
- **Lee, C.\***, Gates, K. M., Chun, J., Al Kontar, R., Kamali, M., McInnis, M. G., & Deldin, P. (2025). Suicide risk estimation in bipolar disorder using N200 and P300 event-related potentials and machine learning: A pilot study. <em>Journal of Affective Disorders Reports</em>, 20, 100875. [DOI](https://doi.org/10.1016/j.jadr.2025.100875)  
- Plumley, R. D., Bernacki, M. L., Greene, J. A., …, **Lee, C.\***, Panter, A. T., & Gates, K. M. (2024). Co-designing enduring learning analytics prediction and support tools in undergraduate biology courses. <em>British Journal of Educational Technology</em>, 55(5), 1860–1883. [DOI](https://doi.org/10.1111/bjet.13472)  
- **Lee, C.\*** (2023). An integrative machine learning approach for small samples and high-dimensional imbalanced data in psychological experiment [Master’s thesis, University of North Carolina at Chapel Hill].

**Software**  
- **Lee, C.\*** (2025). <em>flex: Fuzzy least squares estimation with explicit formula</em> (Version 0.1.0) [R package]. CRAN. [DOI](https://doi.org/10.32614/CRAN.package.flex)

### Accepted  
- **Lee, C.\***, & Gates, K. M. (publication expected May 7, 2026). Group-iterative multiple model estimation in clinical science. <em>Annual Review of Clinical Psychology</em>.

### Under Review  
- Rodebaugh, T. L., **Lee, C.\***, Gates, K. M., Frumkin, M. R., …, & Piccirillo, J. Modeling psychological processes in tinnitus disorder.  
- Yoon, J. H.\*, **Lee, C.\***, Kwon, S., & Bae, Y. C. Nonlinear and chaotic dynamics in generalized fuzzy opinion model.  

### Submission Pending
- **Lee, C.\*** No single approach fits all: Testing two generations of structural equation modeling estimation.  
- **Lee, C.\*** Modeling imprecision in psychological data: Fuzzy set theory and its application with fuzzy least squares regression.  
- **Lee, C.\*** FLEX: An R package for fuzzy numbers and fuzzy least squares regression.

---

## Research Collaborations {#collaborations}

I have collaborated on multiple interdisciplinary research projects, including:

- **EPICS Mood and Schizophrenia Lab (PI: Deldin, P.J., University of Michigan):**  
  Analyzed event-related potentials (ERP) to classify psychiatric patients and predict suicidality in individuals diagnosed with bipolar disorder, using deep learning and feature selection.  

- **PROACTIVE Project (PI: T. Manschreck, Harvard Medical School / Beth Israel Deaconess Medical Center):**  
  Investigated relationships between patients’ metabolic features and the effectiveness of schizophrenia treatments, including long-acting injectable Risperidone and oral antipsychotics.  

- **NSF IUSE Student Success Project (PIs: Gates, K., & Greene, J., UNC School of Education / Department of Psychology and Neuroscience):**  
  Applied machine learning and Markov modeling to learning management system (LMS) data to forecast student performance in undergraduate biology courses.  

- **Clinical Psychology Collaborations (PI: Rodebaugh, T.L., UNC Chapel Hill):**  
  Modeled dynamic time series of tinnitus symptoms using Group Iterative Multiple Model Estimation (GIMME).  

- **Mathematics and Engineering Collaborations (South Korea):**  
  Explored applications of fuzzy set theory and chaos theory to model complex dynamics in social opinion formation.  

---

## Education {#education}
**M.S. in Applied Statistics**  University of Michigan, Ann Arbor, MI, USA  
**M.A. in Economics**  Yonsei University, Seoul, South Korea  
**B.S. in Biology**  Yonsei University, Seoul, South Korea  

---

## Teaching & Instruction {#teaching}
At UNC Chapel Hill, I have served as a teaching/instructional assistant for PSYC 210 (Statistical Principles of Psychological Research) across multiple semesters since 2020. In this role, I led recitation sessions, assisted students with SPSS- and Jamovi-based data analysis, and provided individualized support. In recognition of strong student evaluations, I was honored twice with the Departmental Teaching Assistant Commendation.

---
## Academic Talks {#talks}
- **No Single Approach Fits All: Testing Two Generations of Structural Equation Modeling Estimation** — 23rd Annual Society of Multivariate Experimental Psychology (SMEP) Conference, University of Notre Dame, IN, USA. *Oct 2025*  
- **Chaotic Behaviors in Opinion Dynamics Models Influenced by External Forces** — 25th International Symposium on Advanced Intelligent Systems (ISIS 2024), Himeji, Japan. *Nov 2024*  
- **Integrative Classification Framework in Machine Learning for Small Samples and High-Dimensional Imbalanced Data** — Quant Forum, Department of Psychology and Neuroscience, UNC Chapel Hill. *Apr 2023*  
- **Sequence Analysis for Classification: Proposing a New Hybrid Markov Model – Machine Learning Approach** — Quant Forum, Department of Psychology and Neuroscience, UNC Chapel Hill. *Apr 2022*  
- **Prediction of Suicide Attempt by Bipolar Disorder Patients with Machine Learning Algorithms** — Quant Forum, Department of Psychology and Neuroscience, UNC Chapel Hill. *May 2021*

---
## Life Before the Lab {#life}
**Professionally Trained Classical Pianist**  
I began playing the piano at the age of 3 and pursued professional training at Yewon School and Seoul Arts High School, two of Korea’s most prestigious arts institutions. During my teenage years, I won several major national music competitions and performed extensively as both a soloist and an accompanist for violinists, cellists, and vocalists in concert and competition settings. I also collaborated with the Seoul Symphony Orchestra in a performance of Grieg’s Piano Concerto in A minor. At the age of 14, I was prestigiously selected as a musical prodigy by the Kumho Asiana Group—one of Korea’s leading conglomerates—which led to my own solo debut recital. My favorite repertoire includes Bach–Busoni’s *Chaconne*, Mendelssohn’s *Variations sérieuses*, Chopin’s Ballades, and more. 

<div align="center" style="margin: 20px 0;">
  <img src="{{ '/assets/images/chaewon2.JPG' | relative_url }}" alt="Chaewon Lee performing" width="400" style="border-radius: 12px;" />
</div>

**Former Investment Banker and Economist**  
Before entering academia, I worked at Korea Investment & Securities in Yeouido, Seoul, widely recognized as Korea’s wall street. I first served as a junior investment banker in the Equity Capital Market Department, where I worked on IPOs for KOSPI and KOSDAQ, conducting due diligence, accounting analysis, and preparing listing applications. I later transitioned to the Research Center as a junior economist, where I authored analytical reports on global macroeconomic trends and financial markets, and led forecasting for indicators such as exchange rates, crude oil prices, and international policy rates.

<div class="custom-copy">
  © 2025 Chaewon Lee. All rights reserved.
</div>
