---
layout: page
title: "Chaewon Chloe Lee"
description: ""
permalink: /home
---

<style>
  :root { --tab-accent:#0a84ff; --site-header-h:56px; }
  main, .page-content { overflow: visible; }

  /* Tabs bar */
  .tabs {
    position: static;                 /* not sticky */
    z-index: 1;
    background: rgba(15,20,24,.85);
    border-bottom: 1px solid rgba(127,127,127,.2);
    padding: 10px 0;
    margin: 0 0 16px 0;
    -webkit-backdrop-filter: saturate(160%) blur(6px);
    backdrop-filter: saturate(160%) blur(6px);
  }

  .tabs ul {
    display:flex;
    flex-wrap:wrap;
    gap:10px 14px;
    list-style:none;
    margin:0;
    padding:6px 2px;
    align-items:center;   /* ensure even vertical centering */
  }

  .tabs li {
    display:flex;
    align-items:center;   /* normalize vertical alignment */
  }

  /* Base link styles */
  .tabs a {
    text-decoration:none;
    font-weight:600;
    padding:8px 12px;
    color: var(--tab-accent);
    display:inline-flex;
    align-items:center;
    line-height:1.2;          /* normalize across fonts */
    outline:none;
    -webkit-tap-highlight-color: transparent;
    border:none;
    box-shadow:none;
  }
  .tabs a:hover { text-decoration: underline; }

  /* Active tab style (underline only, no box) */
  .tabs a.active {
    background: none;
    border: none;
    text-decoration: underline;
  }

  /* Accessibility: suppress default browser focus glow */
  .tabs a:focus,
  .tabs a:focus-visible {
    outline:none;
    box-shadow:none;
  }

  html { scroll-behavior: smooth; }

  /* offset for in-page anchors if you have a site header */
  h2[id], h3[id] {
    scroll-margin-top: calc(var(--site-header-h, 0px) + 26px);
  }

  .top-spacer { clear: both; margin-top: 18px; }
</style>

<nav class="tabs">
  <ul>
    <li><a href="#research">Research</a></li>
    <li><a href="#publications">Publications</a></li>
    <li><a href="#collaborations">Collaborations</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#teaching">Teaching</a></li>
    <li><a href="#conferences">Conferences</a></li>
    <li><a href="#life">Life Before the Lab</a></li>
  </ul>
</nav>

<!-- JS only to remove focus ring after mouse/touch click -->
<script>
  document.querySelectorAll('.tabs a').forEach(a => {
    a.addEventListener('click', () => a.blur(), {passive:true});
  });
</script>

<div class="top-spacer"></div>

## Research Focus {#research}
### Methodological Innovation
My research focuses on developing and disseminating advanced statistical methods to address the unique methodological challenges of psychological, behavioral, and social sciences. I primarily work across five statistical frameworks, often integrating them to create synergistic solutions that advance the field:

<div style="margin-top:14px;">
  <img src="{{ '/assets/images/research1.JPG' | relative_url }}"
       alt="Research approaches"
       style="max-width:1100px; width:100%; height:auto; border-radius:15px; display:block; margin:0;" />
</div>
<br>

My methodological work unfolds through three core pipelines:

1. Adapting deep learning techniques to enhance traditional psychological methods and meet the demands of research using passive sensing and large-scale behavioral and physiological data;
2. Drawing robust inference on intraindividual dynamic processes from limited samples and sparse time points
3. Rethinking imprecision in psychological scales — not merely as measurement error to minimize, but as a source of information to be actively leveraged in statistical modeling.

### Substantive Translation
**Precision psychology** is the motivating aim behind translating my core modeling frameworks and methodological innovations into meaningful applications across psychological, behavioral, and social sciences. This includes advancing individualized diagnosis and treatment of mental health conditions, uncovering brain–behavior dynamics, and supporting adaptive interventions in clinical and educational settings. 

## Publications {#publications}

### Published

#### Research Articles
- **Lee, C.\*** & Gates, K.M. (2025). *Automated machine learning for classification and regression: A tutorial for psychologists.* _Behavior Research Methods_, 57, 262. [DOI](https://doi.org/10.3758/s13428-025-02684-5)  
- **Lee, C.\***, Luo, L., Kuhlmann, S. L., Plumley, R. D., Panter, A. T., Bernacki, M. L., Greene, J. A., & Gates, K. M. (2025). *Interpretable Predictive Analytics for Online Learning: A Markov-Based Machine Learning Approach.* _Journal of Learning Analytics_, 12(2), 259–278. [DOI](https://doi.org/10.18608/jla.2025.8375)  
- **Lee, C.\***, Gates, K. M., Chun, J., Al Kontar, R., Kamali, M., McInnis, M. G., & Deldin, P. (2025). *Suicide risk estimation in bipolar disorder using N200 and P300 event-related potentials and machine learning: A pilot study.* _Journal of Affective Disorders Reports_, 20, 100875. [DOI](https://doi.org/10.1016/j.jadr.2025.100875)  
- Plumley, R.D., Bernacki, M.L., Greene, J.A., …, **Lee, C.\***, Panter, A.T., & Gates, K.M. (2024). *Co‐designing enduring learning analytics prediction and support tools in undergraduate biology courses.* _British Journal of Educational Technology_, 55(5), 1860–1883. [DOI](https://doi.org/10.1111/bjet.13472)  
- **Lee, C.\*** (2023). *An Integrative Machine Learning Approach for Small Samples and High-Dimensional Imbalanced Data in Psychological Experiment* (Master's thesis, The University of North Carolina at Chapel Hill)

#### Software Program
- **Lee, C.\*** (2025). *flex: Fuzzy least squares estimation with explicit formula* (Version 0.1.0) [R package]. _CRAN_. [DOI](https://doi.org/10.32614/CRAN.package.flex)

### Accepted

- **Lee, C.\*** & Gates, K.M. (Expected May 7, 2026). *Group-iterative multiple model estimation in clinical science.* _Annual Review of Clinical Psychology_

### Under Review

- Rodebaugh, T.L., **Lee, C.\***, Gates, K.M., Frumkin, M.R., …, & Piccirillo, J. *Modeling psychological processes in Tinnitus disorder.*  
- **Yoon, J.H.\***, **Lee, C.\***, Kwon, S., & Bae, Y.C. *Nonlinear and chaotic dynamics in generalized fuzzy opinion model.*

### Submission Pending

- *No single approach fits all: Testing two generations of structural equation modeling estimation.*  
- *Modeling imprecise psychological data: Fuzzy set theory and its application with fuzzy least squares regression.*  
- *FLEX: An R Package for Fuzzy Numbers and Fuzzy Least Squares Regression*

## Research Collaborations {#collaborations}

I have collaborated on multiple interdisciplinary research projects, including:

- The EPICS Mood and Schizophrenia Lab (PI: Deldin, P.J.) at the University of Michigan, where I analyzed event-related potentials (ERP) to classify psychiatric patients and predict suicidality of individuals diagnosed with bipolar disorder using techniques such as deep learning and feature selection.

- PROACTIVE Project (PI: T. Manschreck), in collaboration with researchers at Harvard Medical School / Beth Israel Deaconess Medical Center, where I focused on identifying the relationship between a patient’s metabolic features and the effectiveness of schizophrenia treatments, including long-acting injectable Risperidone and oral antipsychotic medications.

- The NSF IUSE Student Success Project (PIs: Gates, K., & Greene, J.) at the UNC School of Education and the Department of Psychology and Neuroscience, where I applied machine learning and Markov modeling to learning management system (LMS) data to forecast student performance in undergraduate biology courses.

- Collaborations with Dr. Tom Rodebaugh’s clinical psychology team at UNC Chapel Hill on dynamic time series modeling of tinnitus symptoms, using Group Iterative Multiple Model Estimation (GIMME).

- Ongoing collaborations with mathematicians and engineers in South Korea, exploring the application of fuzzy set theory and chaos theory to model complex dynamics in social opinion formation.

## Education {#education}

Before embarking on my Ph.D. training, I earned an M.S. in Applied Statistics from the University of Michigan, an M.A. in Economics from Yonsei University in Seoul, South Korea, and a B.S. in Biology also from Yonsei University.

## Teaching & Instruction {#teaching}

At UNC Chapel Hill, I have served as a teaching/instructional assistant for PSYC 210 (Statistical Principles of Psychological Research) across multiple semesters since 2020. In this role, I led recitation sessions, assisted students with SPSS- and Jamovi-based data analysis, and provided individualized support. In recognition of strong student evaluations, I was honored twice with the Departmental Teaching Assistant Commendation.

## Conferences {#conferences}

- Lee, C.*, Yoon, J.H., & Bae, Y.C. (2024, November). Chaotic behaviors in opinion dynamics models influenced by external forces. Paper presented at the 25th International Symposium on Advanced Intelligent Systems (ISIS 2024), Himeji, Japan.
- Lee, C.* (2025, October). No single approach fits all: Testing two generations of structural equation modeling estimation. Poster to be presented at the 23rd Annual Society of Multivariate Experimental Psychology (SMEP) Graduate Student Conference, University of Notre Dame, Indiana, USA.

## Life Before the Lab {#life}

### Classically Trained Pianist, Since Age 3
I began playing the piano at the age of 3 and pursued professional training at Yewon School and Seoul Arts High School, two of Korea’s most prestigious arts institutions. During my teenage years, I won several major national music competitions and performed extensively as both a soloist and an accompanist for violinists, cellists, and vocalists in concert and competition settings. I also collaborated with the Seoul Symphony Orchestra in a performance of Grieg’s Piano Concerto in A minor. At the age of 14, I was prestigiously selected as a musical prodigy by the Kumho Asiana Group—one of Korea’s leading conglomerates—which led to my own solo debut recital. My favorite repertoire includes Bach–Busoni’s *Chaconne*, Mendelssohn’s *Variations sérieuses*, Chopin’s Ballades, and more. 

<div align="center" style="margin: 20px 0;">
  <img src="{{ '/assets/images/chaewon2.JPG' | relative_url }}" alt="Chaewon Lee performing" width="400" style="border-radius: 12px;" />
</div>

### Former Investment Banker and Economist, Based in Korea’s Wall Street
Before entering academia, I worked at Korea Investment & Securities in Yeouido, Seoul, widely recognized as Korea’s financial hub. I first served as a junior investment banker in the Equity Capital Market Department, where I worked on IPOs for KOSPI and KOSDAQ, conducting due diligence, accounting analysis, and preparing listing applications. I later transitioned to the Research Center as a junior economist, where I authored analytical reports on global macroeconomic trends and financial markets, and led forecasting for indicators such as exchange rates, crude oil prices, and international policy rates.
