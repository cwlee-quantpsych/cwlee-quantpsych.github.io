---
layout: page
title: ""
description: ""
permalink: /home
---

<style>
  :root {
    --tab-accent: #0a84ff;
    --site-header-h: 56px;

    /* UNC-inspired palette */
    --unc-navy: #13294B;      /* headings / emphasis */
    --unc-gray: #4B4F54;      /* body text */
    --unc-sky:  #E6F1FB;      /* pale sky blue background */

    /* Layout widths */
    --content-w: 90vw;        /* template text width (a bit wider than before) */
    --pill-overhang: 30vw;    /* how much wider the pill is than the content */
  }

  /* Kill theme header/footer completely */
  header[role="banner"], .masthead, .site-header, .page__header,
  .site-title, a.site-title, .masthead__title, .header__title, .navbar-brand,
  .page__footer, .site-footer, footer {
    display:none !important; visibility:hidden !important; pointer-events:none !important;
    margin:0 !important; padding:0 !important; height:0 !important; border:0 !important;
  }

  body {
    font-family: 'Lato', system-ui, -apple-system, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    font-size: 16px;
    line-height: 1.65;
    color: var(--unc-gray);
    background: var(--unc-sky);
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow-x: hidden;
  }

  h1, h2, h3, h4, h5, h6 {
    color: var(--unc-navy);
    font-weight: 800;
    letter-spacing: -.2px;
  }

  p, li { color: var(--unc-gray); }

  /* ===== Tabs-only sticky header ===== */
  .hero-wrap{
    position: sticky;
    top: 0;
    z-index: 50;
    padding: 14px 0 18px;
    backdrop-filter: blur(6px);
  }

  /* This defines the template’s center line */
  .hero-grid{
    max-width: var(--content-w);
    margin: 0 auto;
    position: relative;
  }

  /* The pill is wider than the template, but center-locked to it */
  .tabs-card{
    position: relative;
    left: 50%;
    transform: translateX(-50%);                          /* lock to template center */
    width: calc(100% + var(--pill-overhang));             /* extend symmetrically */
    max-width: min(90vw, 1400px);                         /* safety cap */
    background: #fff;
    border: 1px solid rgba(19,41,75,.14);
    border-radius: 28px;
    box-shadow: 0 8px 14px rgba(19,41,75,.08);
    padding: 18px 36px;
    overflow-x: auto;                                     /* keep one line; scroll only if necessary */
    -webkit-overflow-scrolling: touch;
    scrollbar-width: none;
  }

  .tabs-list{
    display: flex;
    flex-wrap: nowrap; white-space: nowrap;               /* ONE line */
    justify-content: center; align-items: center;
    gap: 0 40px;
    list-style: none; margin: 0; padding: 0;
  }

  .tabs-list a{
    font-weight: 700;
    color: var(--unc-navy);
    text-decoration: none;
    padding: 6px 8px;
    border-radius: 8px;
    transition: background .15s ease, color .15s ease, transform .08s ease;
  }
  .tabs-list a:hover{
    background: var(--tab-accent);
    color: #fff;
    transform: translateY(-1px);
  }
  .tabs-list a.active{
    background: var(--unc-navy);
    color: #fff;
  }

  /* Anchor offset so headings don’t hide under sticky pill */
  :root { --anchor-offset: 120px; } /* tweak to 110–150 if needed */
  h2[id], h3[id], section[id] { scroll-margin-top: var(--anchor-offset); }
  html { scroll-behavior: smooth; }

  /* Responsive adjustments */
  @media (max-width: 1280px){
    .tabs-list{ gap: 0 28px; }
  }
  @media (max-width: 980px){
    .hero-grid{ max-width: 90vw; }             /* give the template more room on phones */
    .tabs-card{ width: calc(100% + 8vw); }     /* reduce overhang a bit on narrow screens */
    .tabs-list a{ font-size: .95rem; }
  }

  /* Space below header */
  .top-spacer{ margin-top: 14px; }
</style>

<!-- HEADER: centered wide pill -->
<div class="hero-wrap" role="navigation" aria-label="Section navigation">
  <div class="hero-grid">
    <nav class="tabs-card" aria-label="Primary">
      <ul class="tabs-list">
        <li><a href="#research">Research</a></li>
        <li><a href="#publications">Publications</a></li>
        <li><a href="#collaborations">Collaborations</a></li>
        <li><a href="#education">Education</a></li>
        <li><a href="#teaching">Teaching</a></li>
        <li><a href="#life">Preludes to the Lab</a></li>
      </ul>
    </nav>
  </div>
</div>

<script>
  // Precise offset scrolling that adapts to the pill height
  function getHeaderOffset(extra = 12) {
    const pill = document.querySelector('.hero-wrap');
    const h = pill ? pill.getBoundingClientRect().height : 0;
    return h + extra;
  }

  function scrollToId(id) {
    const el = document.querySelector(id);
    if (!el) return;
    const y = el.getBoundingClientRect().top + window.pageYOffset - getHeaderOffset();
    window.scrollTo({ top: y, behavior: 'smooth' });
  }

  // Intercept tab clicks
  document.querySelectorAll('.tabs-list a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      e.preventDefault();
      const id = a.getAttribute('href');
      history.pushState(null, '', id); // keep URL updated
      scrollToId(id);
    }, { passive: false });
  });

  // Correct initial hash position and on back/forward
  function handleHashOnLoad() {
    if (location.hash) scrollToId(location.hash);
  }
  window.addEventListener('load', handleHashOnLoad);
  window.addEventListener('popstate', handleHashOnLoad);

  // Re-nudge after resize (e.g., when fonts load)
  let resizeTimer;
  window.addEventListener('resize', () => {
    if (location.hash) {
      clearTimeout(resizeTimer);
      resizeTimer = setTimeout(() => scrollToId(location.hash), 150);
    }
  });
</script>

<div class="top-spacer"></div>


## Research Commitments {#research}
---
<br>

### Methodological Innovation
My research focuses on developing and disseminating advanced statistical methods to address the unique methodological challenges of psychological, behavioral, and social sciences. I primarily work across five statistical frameworks, often integrating them to create synergistic solutions that advance the field:

<div style="margin-top:14px;">
  <img src="{{ '/assets/images/research2.jpg' | relative_url }}"
       alt="Research approaches"
       style="width:100%; height:auto; max-width:1600px; border-radius:15px; display:block; margin:0;" />
</div>
<br>

**My methodological work unfolds through three core pipelines:**

- Adapting deep learning techniques to enhance traditional psychological methods and meet the demands of research using passive sensing and large-scale behavioral and physiological data  
- Drawing robust inference on intraindividual dynamic processes from limited samples and sparse time points  
- Rethinking imprecision in psychological scales — not merely as measurement error to minimize, but as a source of information to be actively leveraged in statistical modeling

### Substantive Translation

***Precision psychology*** is the motivating aim behind translating my core modeling frameworks and methodological innovations into meaningful applications across psychological, behavioral, and social sciences. This includes advancing individualized diagnosis and treatment of mental health conditions, uncovering brain–behavior dynamics, and supporting adaptive interventions in clinical, cognitive, and educational domains. 
<br><br>

## Publications {#publications}
---
<br>

**Published**
<br>
***Research Articles***  
- **Lee, C.\***, & Gates, K. M. (2025). Automated machine learning for classification and regression: A tutorial for psychologists. <em>Behavior Research Methods</em>, 57(2), 262. [DOI](https://doi.org/10.3758/s13428-025-02684-5)  
- **Lee, C.\***, Luo, L., Kuhlmann, S. L., Plumley, R. D., Panter, A. T., Bernacki, M. L., Greene, J. A., & Gates, K. M. (2025). Interpretable predictive analytics for online learning: A Markov-based machine learning approach. <em>Journal of Learning Analytics</em>, 12(2), 259–278. [DOI](https://doi.org/10.18608/jla.2025.8375)  
- **Lee, C.\***, Gates, K. M., Chun, J., Al Kontar, R., Kamali, M., McInnis, M. G., & Deldin, P. (2025). Suicide risk estimation in bipolar disorder using N200 and P300 event-related potentials and machine learning: A pilot study. <em>Journal of Affective Disorders Reports</em>, 20, 100875. [DOI](https://doi.org/10.1016/j.jadr.2025.100875)  
- Plumley, R. D., Bernacki, M. L., Greene, J. A., …, **Lee, C.\***, Panter, A. T., & Gates, K. M. (2024). Co-designing enduring learning analytics prediction and support tools in undergraduate biology courses. <em>British Journal of Educational Technology</em>, 55(5), 1860–1883. [DOI](https://doi.org/10.1111/bjet.13472)  
- **Lee, C.\*** (2023). An integrative machine learning approach for small samples and high-dimensional imbalanced data in psychological experiment [Master’s thesis, University of North Carolina at Chapel Hill].

***Software Program*** 
- **Lee, C.\*** (2025). <em>flex: Fuzzy least squares estimation with explicit formula</em> (Version 0.1.0) [R package]. CRAN. [DOI](https://doi.org/10.32614/CRAN.package.flex)

**Accepted**  
- **Lee, C.\***, & Gates, K. M. (publication expected May 7, 2026). Group-iterative multiple model estimation in clinical science. <em>Annual Review of Clinical Psychology</em>.

**Under Review**  
- Rodebaugh, T. L., **Lee, C.\***, Gates, K. M., Frumkin, M. R., …, & Piccirillo, J. Modeling psychological processes in tinnitus disorder.  
- Yoon, J. H.\*, **Lee, C.\***, Kwon, S., & Bae, Y. C. Nonlinear and chaotic dynamics in generalized fuzzy opinion model.  

**Submission Pending**
- **Lee, C.\*** No single approach fits all: Testing two generations of structural equation modeling estimation.  
- **Lee, C.\*** Modeling imprecision in psychological data: Least squares estimation with fuzzy numbers
- **Lee, C.\*** FLEX: An R package for fuzzy numbers and fuzzy linear regression.

<br><br>

## Research Collaborations {#collaborations}
---
<br>
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
  Explored applications of fuzzy set theory and chaos theory to model complex dynamics in social opinion formation.<br><br>  

## Education {#education}
---
<br>
**M.S. in Applied Statistics**  University of Michigan, Ann Arbor, MI, USA  
**M.A. in Economics**  Yonsei University, Seoul, South Korea  
**B.S. in Biology**  Yonsei University, Seoul, South Korea
<br><br> 

## Teaching {#teaching}
---
<br>
**University of North Carolina at Chapel Hill**<br>
***PSYC 210: Statistical Principles of Psychological Research***
- Instructional Assistant<br>
    May 2025 – Present; May 2022 – May 2024<br>
- Teaching Assistant<br>
    Aug 2020 – Apr 2021<br>
    Awarded Departmental Undergraduate Teaching Commendation (both semesters)<br>
<br>
I have served as a teaching/instructional assistant for an undergraduate-level introductory statistics course in the Department of Psychology and Neuroscience, across multiple semesters since 2020. My responsibilities included leading recitation sessions, providing hands-on support with data analysis using SPSS and Jamovi, and offering individualized guidance to help students develop statistical reasoning.<br><br> 

## Preludes to the Lab {#life}
---
<br>
***Professionally Trained Classical Pianist***<br>
I began playing the piano at the age of 3 and pursued professional training at Yewon School and Seoul Arts High School, two of Korea’s most prestigious arts institutions. During my teenage years, I won several major national music competitions and performed extensively as both a soloist and an accompanist for violinists, cellists, and vocalists in recital and competition settings. I also collaborated with the Seoul Symphony Orchestra in a performance of Grieg’s Piano Concerto in a minor. At the age of 14, I was prestigiously selected as a musical prodigy by the Kumho Asiana Group—one of Korea’s leading conglomerates—which led to my own solo debut recital. My favorite repertoire includes Bach–Busoni’s *Chaconne*, Mendelssohn’s *Variations sérieuses*, Chopin’s Ballades, and more. 

<div align="center" style="margin: 20px 0;">
  <img src="{{ '/assets/images/chaewon2.JPG' | relative_url }}" alt="Chaewon Lee performing" width="400" style="border-radius: 12px;" />
</div>

***Former Investment Banker and Economist***<br>
Prior to academia, I worked at Korea Investment & Securities, one of Korea’s top-tier securities firms headquartered in Yeouido, Seoul—often referred to as Korea’s Wall Street. I first served as a junior investment banker in the Equity Capital Market Department, where I worked on IPOs for KOSPI and KOSDAQ, conducting due diligence, accounting analysis, and preparing listing applications. I later transitioned to the Research Center as a junior economist, where I authored economic reports on global macro-financial trends and led forecasts for key indicators such as exchange rates, oil prices, and international policy rates.

<div class="custom-copy" style="max-width:96vw;margin:40px auto 24px;padding:16px 32px 0;text-align:center;color:var(--unc-dark);font-size:14px;opacity:.9;border-top:1px solid rgba(19,41,75,.15);">
  © 2025 Chaewon Lee. All rights reserved.
</div>
