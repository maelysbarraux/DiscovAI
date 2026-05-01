<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>DiscovAI — Drug Discovery Pipeline</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet"/>
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    body { background: #faf7f4; color: #1a1218; font-family: 'DM Sans', sans-serif; font-weight: 300; }

    .hero { padding: 64px 48px 48px; border-bottom: 0.5px solid #e8ddd8; }
    .logo { font-family: 'Cormorant Garamond', serif; font-size: 54px; font-weight: 300; color: #1a1218; letter-spacing: 4px; line-height: 1; margin-bottom: 4px; }
    .logo span { color: #c9748a; }
    .tagline { font-size: 10px; letter-spacing: 5px; color: #b8a8a8; text-transform: uppercase; margin-bottom: 44px; }
    .hero-text { font-family: 'Cormorant Garamond', serif; font-size: 26px; font-weight: 300; font-style: italic; color: #c9748a; line-height: 1.6; max-width: 500px; margin-bottom: 28px; }
    .desc { font-size: 13px; line-height: 2; color: #8a7878; max-width: 440px; }

    .stats { display: grid; grid-template-columns: repeat(3, 1fr); border-bottom: 0.5px solid #e8ddd8; }
    .stat { padding: 32px; border-right: 0.5px solid #e8ddd8; }
    .stat:last-child { border-right: none; }
    .stat-num { font-family: 'Cormorant Garamond', serif; font-size: 40px; font-weight: 300; color: #c9748a; line-height: 1; margin-bottom: 6px; }
    .stat-label { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: #b8a8a8; }

    .pipeline { padding: 48px; border-bottom: 0.5px solid #e8ddd8; }
    .section-label { font-size: 10px; letter-spacing: 5px; text-transform: uppercase; color: #b8a8a8; margin-bottom: 32px; }
    .step { display: flex; align-items: flex-start; gap: 24px; padding: 18px 0; border-bottom: 0.5px solid #f0e8e4; }
    .step:last-child { border-bottom: none; }
    .step-num { font-family: 'Cormorant Garamond', serif; font-size: 14px; color: #c9748a; min-width: 24px; padding-top: 1px; }
    .step-name { font-size: 13px; font-weight: 500; color: #1a1218; margin-bottom: 3px; }
    .step-desc { font-size: 12px; color: #8a7878; line-height: 1.7; }

    .result { padding: 48px; border-bottom: 0.5px solid #e8ddd8; background: #fff; }
    .result-card { border: 0.5px solid #e8ddd8; padding: 32px; background: #faf7f4; }
    .result-label { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: #b8a8a8; margin-bottom: 12px; }
    .result-mol { font-family: 'Cormorant Garamond', serif; font-size: 24px; font-weight: 300; color: #1a1218; margin-bottom: 28px; }
    .result-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-bottom: 24px; }
    .metric-val { font-family: 'Cormorant Garamond', serif; font-size: 28px; color: #c9748a; line-height: 1; margin-bottom: 4px; }
    .metric-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #b8a8a8; }
    .bar-label { display: flex; justify-content: space-between; font-size: 11px; color: #b8a8a8; margin-bottom: 8px; }
    .bar { height: 1px; background: #e8ddd8; }
    .bar-fill { height: 1px; background: #c9748a; width: 77.8%; }

    .stack { padding: 48px; border-bottom: 0.5px solid #e8ddd8; }
    .pills { display: flex; flex-wrap: wrap; gap: 8px; }
    .pill { font-size: 11px; letter-spacing: 2px; text-transform: uppercase; color: #c9748a; border: 0.5px solid #e8c4cc; padding: 6px 16px; background: #fff8f9; }

    footer { padding: 28px 48px; display: flex; justify-content: space-between; align-items: center; border-top: 0.5px solid #e8ddd8; }
    .author { font-size: 11px; color: #b8a8a8; letter-spacing: 2px; text-transform: uppercase; }
    .gh { font-size: 11px; color: #c9748a; letter-spacing: 2px; text-transform: uppercase; text-decoration: none; border-bottom: 0.5px solid #c9748a; padding-bottom: 2px; }
  </style>
</head>
<body>

  <div class="hero">
    <p class="logo">Discov<span>AI</span></p>
    <p class="tagline">Drug discovery pipeline</p>
    <p class="hero-text">"Finding tomorrow's medicines in today's data."</p>
    <p class="desc">An open-source Python pipeline that automates early-stage molecular screening. Connects to ChEMBL, scores candidates on ADMET profile, and ranks them against any biological target of interest.</p>
  </div>

  <div class="stats">
    <div class="stat">
      <p class="stat-num">2M+</p>
      <p class="stat-label">Molecules accessible</p>
    </div>
    <div class="stat">
      <p class="stat-num">6</p>
      <p class="stat-label">Pipeline steps</p>
    </div>
    <div class="stat">
      <p class="stat-num">0.1</p>
      <p class="stat-label">Current version</p>
    </div>
  </div>

  <div class="pipeline">
    <p class="section-label">Pipeline</p>
    <div class="step">
      <span class="step-num">01</span>
      <div>
        <p class="step-name">ChEMBL fetch</p>
        <p class="step-desc">Retrieves active molecules against a given target from the world's largest open bioactivity database.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">02</span>
      <div>
        <p class="step-name">Molecular properties</p>
        <p class="step-desc">Calculates physicochemical descriptors — molecular weight, LogP, TPSA, hydrogen bond donors and acceptors.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">03</span>
      <div>
        <p class="step-name">Lipinski filter</p>
        <p class="step-desc">Applies the Rule of Five — the industry-standard drug-likeness filter used across pharmaceutical R&D.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">04</span>
      <div>
        <p class="step-name">ADMET scoring</p>
        <p class="step-desc">Scores absorption, distribution, metabolism, excretion and toxicity profile for each candidate.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">05</span>
      <div>
        <p class="step-name">Global ranking</p>
        <p class="step-desc">Combines efficacy (IC50) and ADMET into a single DiscovAI score — 60% potency, 40% pharmacokinetics.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">06</span>
      <div>
        <p class="step-name">2D visualization</p>
        <p class="step-desc">Renders molecular structures of top candidates directly in the notebook.</p>
      </div>
    </div>
  </div>

  <div class="result">
    <p class="section-label">Demo — BCL2 target / leukemia</p>
    <div class="result-card">
      <p class="result-label">Top candidate</p>
      <p class="result-mol">CHEMBL150332</p>
      <div class="result-grid">
        <div>
          <p class="metric-val">13 nM</p>
          <p class="metric-label">IC50</p>
        </div>
        <div>
          <p class="metric-val">80/100</p>
          <p class="metric-label">ADMET score</p>
        </div>
        <div>
          <p class="metric-val">77.8</p>
          <p class="metric-label">DiscovAI score</p>
        </div>
      </div>
      <div class="bar-label"><span>DiscovAI score</span><span>77.8 / 100</span></div>
      <div class="bar"><div class="bar-fill"></div></div>
    </div>
  </div>

  <div class="stack">
    <p class="section-label">Stack</p>
    <div class="pills">
      <span class="pill">Python</span>
      <span class="pill">RDKit</span>
      <span class="pill">ChEMBL API</span>
      <span class="pill">Pandas</span>
      <span class="pill">NumPy</span>
      <span class="pill">Jupyter</span>
    </div>
  </div>

  <footer>
    <span class="author">M2 Computational Chemistry · Cardiff · Oslo</span>
    <a class="gh" href="https://github.com/VOTRE_USERNAME/DiscovAI">GitHub →</a>
  </footer>

</body>
</html>    .result-label { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: #b8a8a8; margin-bottom: 12px; }
    .result-mol { font-family: 'Cormorant Garamond', serif; font-size: 24px; font-weight: 300; color: #1a1218; margin-bottom: 28px; }
    .result-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; margin-bottom: 24px; }
    .metric-val { font-family: 'Cormorant Garamond', serif; font-size: 28px; color: #c9748a; line-height: 1; margin-bottom: 4px; }
    .metric-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #b8a8a8; }
    .bar-label { display: flex; justify-content: space-between; font-size: 11px; color: #b8a8a8; margin-bottom: 8px; }
    .bar { height: 1px; background: #e8ddd8; }
    .bar-fill { height: 1px; background: #c9748a; width: 77.8%; }

    .stack { padding: 48px; border-bottom: 0.5px solid #e8ddd8; }
    .pills { display: flex; flex-wrap: wrap; gap: 8px; }
    .pill { font-size: 11px; letter-spacing: 2px; text-transform: uppercase; color: #c9748a; border: 0.5px solid #e8c4cc; padding: 6px 16px; background: #fff8f9; }

    footer { padding: 28px 48px; display: flex; justify-content: space-between; align-items: center; border-top: 0.5px solid #e8ddd8; }
    .author { font-size: 11px; color: #b8a8a8; letter-spacing: 2px; text-transform: uppercase; }
    .gh { font-size: 11px; color: #c9748a; letter-spacing: 2px; text-transform: uppercase; text-decoration: none; border-bottom: 0.5px solid #c9748a; padding-bottom: 2px; }
  </style>
</head>
<body>

  <div class="hero">
    <p class="logo">Discov<span>AI</span></p>
    <p class="tagline">Drug discovery pipeline</p>
    <p class="hero-text">"Finding tomorrow's medicines in today's data."</p>
    <p class="desc">An open-source Python pipeline that automates early-stage molecular screening. Connects to ChEMBL, scores candidates on ADMET profile, and ranks them against any biological target of interest.</p>
  </div>

  <div class="stats">
    <div class="stat">
      <p class="stat-num">2M+</p>
      <p class="stat-label">Molecules accessible</p>
    </div>
    <div class="stat">
      <p class="stat-num">6</p>
      <p class="stat-label">Pipeline steps</p>
    </div>
    <div class="stat">
      <p class="stat-num">0.1</p>
      <p class="stat-label">Current version</p>
    </div>
  </div>

  <div class="pipeline">
    <p class="section-label">Pipeline</p>
    <div class="step">
      <span class="step-num">01</span>
      <div>
        <p class="step-name">ChEMBL fetch</p>
        <p class="step-desc">Retrieves active molecules against a given target from the world's largest open bioactivity database.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">02</span>
      <div>
        <p class="step-name">Molecular properties</p>
        <p class="step-desc">Calculates physicochemical descriptors — molecular weight, LogP, TPSA, hydrogen bond donors and acceptors.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">03</span>
      <div>
        <p class="step-name">Lipinski filter</p>
        <p class="step-desc">Applies the Rule of Five — the industry-standard drug-likeness filter used across pharmaceutical R&D.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">04</span>
      <div>
        <p class="step-name">ADMET scoring</p>
        <p class="step-desc">Scores absorption, distribution, metabolism, excretion and toxicity profile for each candidate.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">05</span>
      <div>
        <p class="step-name">Global ranking</p>
        <p class="step-desc">Combines efficacy (IC50) and ADMET into a single DiscovAI score — 60% potency, 40% pharmacokinetics.</p>
      </div>
    </div>
    <div class="step">
      <span class="step-num">06</span>
      <div>
        <p class="step-name">2D visualization</p>
        <p class="step-desc">Renders molecular structures of top candidates directly in the notebook.</p>
      </div>
    </div>
  </div>

  <div class="result">
    <p class="section-label">Demo — BCL2 target / leukemia</p>
    <div class="result-card">
      <p class="result-label">Top candidate</p>
      <p class="result-mol">CHEMBL150332</p>
      <div class="result-grid">
        <div>
          <p class="metric-val">13 nM</p>
          <p class="metric-label">IC50</p>
        </div>
        <div>
          <p class="metric-val">80/100</p>
          <p class="metric-label">ADMET score</p>
        </div>
        <div>
          <p class="metric-val">77.8</p>
          <p class="metric-label">DiscovAI score</p>
        </div>
      </div>
      <div class="bar-label"><span>DiscovAI score</span><span>77.8 / 100</span></div>
      <div class="bar"><div class="bar-fill"></div></div>
    </div>
  </div>

  <div class="stack">
    <p class="section-label">Stack</p>
    <div class="pills">
      <span class="pill">Python</span>
      <span class="pill">RDKit</span>
      <span class="pill">ChEMBL API</span>
      <span class="pill">Pandas</span>
      <span class="pill">NumPy</span>
      <span class="pill">Jupyter</span>
    </div>
  </div>

  <footer>
    <span class="author">M2 Computational Chemistry · Cardiff · Oslo</span>
    <a class="gh" href="https://github.com/VOTRE_USERNAME/DiscovAI">GitHub →</a>
  </footer>

</body>
</html>
