```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Authority Engine | The Swimming Pool Journey</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />

  <!-- Brand typography: use Avenir Next if available, with Google‑font fallback -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700&display=swap"
    rel="stylesheet"
  />

  <style>
    :root {
      /* Brand colors */
      --authority-navy: #0d2c4f;
      --engine-blue: #005b9a;
      --ai-cyan: #00a9ff;
      --engine-gray: #22252a;
      --pure-white: #ffffff;
      --light-gray: #f0f2f5;

      /* Spacing scale (8‑pt grid) */
      --space-1: 0.5rem;
      --space-2: 1rem;
      --space-3: 1.5rem;
      --space-4: 2rem;
      --space-5: 3rem;
      --radius-card: 10px;
      --radius-button: 6px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Avenir Next", system-ui, -apple-system, BlinkMacSystemFont,
        "Segoe UI", Nunito, sans-serif;
      background-color: var(--light-gray);
      color: var(--engine-gray);
      line-height: 1.5;
      padding: var(--space-4) var(--space-2);
    }

    .page {
      max-width: 1120px;
      margin: 0 auto;
      background: var(--pure-white);
      border-radius: 16px;
      box-shadow: 0 18px 40px rgba(15, 23, 42, 0.16);
      padding: var(--space-4);
      display: grid;
      grid-template-columns: minmax(0, 3fr) minmax(260px, 2fr);
      gap: var(--space-4);
    }

    header {
      grid-column: 1 / -1;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      margin-bottom: var(--space-3);
    }

    .brand-lockup {
      display: flex;
      align-items: center;
      gap: var(--space-2);
    }

    .brand-lockup img {
      height: 40px;
      width: auto;
    }

    .brand-text h1 {
      font-size: 2.2rem;
      font-weight: 700;
      color: var(--authority-navy);
      margin-bottom: 0.25rem;
    }

    .brand-text p {
      font-size: 0.95rem;
      color: var(--engine-gray);
    }

    .primary-cta {
      align-self: center;
    }

    .btn-primary {
      background: var(--ai-cyan);
      color: var(--pure-white);
      font-weight: 600;
      font-size: 0.95rem;
      border: none;
      border-radius: var(--radius-button);
      padding: 0.8rem 1.6rem;
      cursor: pointer;
      box-shadow: 0 8px 18px rgba(0, 169, 255, 0.3);
      transition: background 0.15s ease, box-shadow 0.15s ease,
        transform 0.15s ease;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.35rem;
      white-space: nowrap;
    }

    .btn-primary:hover {
      background: #0093dc;
      box-shadow: 0 10px 24px rgba(0, 169, 255, 0.38);
      transform: translateY(-1px);
    }

    .btn-primary:disabled {
      opacity: 0.5;
      box-shadow: none;
      cursor: default;
      transform: none;
    }

    h2 {
      font-size: 1.6rem;
      font-weight: 700;
      color: var(--authority-navy);
      margin-bottom: var(--space-2);
    }

    h3 {
      font-size: 1.1rem;
      font-weight: 600;
      color: var(--authority-navy);
      margin-bottom: 0.35rem;
    }

    p {
      margin-bottom: 0.6rem;
      font-size: 0.98rem;
    }

    .intro {
      margin-bottom: var(--space-2);
      max-width: 640px;
    }

    .journey-grid {
      display: grid;
      gap: var(--space-2);
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    }

    .card {
      background: var(--light-gray);
      border-radius: var(--radius-card);
      padding: var(--space-2);
      border: 1px solid rgba(13, 44, 79, 0.06);
    }

    .stage-label {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: var(--engine-blue);
      margin-bottom: 0.25rem;
    }

    .quote {
      border-left: 3px solid var(--ai-cyan);
      background: #f7f9fc;
    }

    .quote p {
      margin-bottom: 0.4rem;
    }

    .quote strong {
      font-weight: 600;
    }

    .stats-grid {
      display: grid;
      gap: var(--space-2);
      grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
      margin-top: var(--space-1);
    }

    .stat {
      padding: var(--space-2);
      border-radius: var(--radius-card);
      background: var(--authority-navy);
      color: var(--pure-white);
      text-align: left;
    }

    .stat-value {
      font-size: 1.6rem;
      font-weight: 700;
      margin-bottom: 0.25rem;
    }

    .stat-label {
      font-size: 0.9rem;
      opacity: 0.9;
    }

    ul {
      margin-left: 1.2rem;
      margin-top: 0.25rem;
      margin-bottom: 0.75rem;
      padding-left: 0.5rem;
    }

    li {
      margin-bottom: 0.35rem;
      font-size: 0.96rem;
    }

    .side-panel {
      border-left: 1px solid rgba(13, 44, 79, 0.08);
      padding-left: var(--space-3);
    }

    .side-panel h2 {
      font-size: 1.4rem;
    }

    .side-panel p {
      font-size: 0.96rem;
    }

    @media (max-width: 900px) {
      .page {
        grid-template-columns: minmax(0, 1fr);
      }

      .side-panel {
        border-left: none;
        border-top: 1px solid rgba(13, 44, 79, 0.08);
        padding-left: 0;
        padding-top: var(--space-3);
      }
    }

    @media (max-width: 640px) {
      body {
        padding: var(--space-3) var(--space-2);
      }

      header {
        flex-direction: column;
        align-items: flex-start;
        gap: var(--space-2);
      }

      .brand-text h1 {
        font-size: 1.8rem;
      }
    }
  </style>
</head>
<body>
  <main class="page">
    <!-- HERO: logo + headline + CTA -->
    <header>
      <div class="brand-lockup">
        <img
          src="AE-2.jpg"
          alt="Authority Engine logo"
        />
        <div class="brand-text">
          <h1>The Swimming Pool Journey</h1>
          <p>Done‑for‑you positioning and visibility system for authority‑driven teams.</p>
        </div>
      </div>
      <div class="primary-cta">
        <a href="#journey" class="btn-primary">Book your strategy call</a>
      </div>
    </header>

    <!-- MAIN CONTENT LEFT COLUMN -->
    <section id="journey">
      <p class="intro">
        Every prospect moves through a predictable journey. This view shows how Authority Engine
        aligns awareness, consideration, decision, and loyalty so you build durable authority,
        protect visibility, and convert intent without friction.
      </p>

      <h2>Choose where you are today</h2>

      <div class="journey-grid">
        <article class="card">
          <div class="stage-label">Awareness</div>
          <h3>Exploring what’s possible</h3>
          <p>
            You are just discovering the space and mapping the opportunity. This stage focuses on
            clarity, education, and showing what an AI‑powered engine can unlock for your pipeline.
          </p>
        </article>

        <article class="card">
          <div class="stage-label">Consideration</div>
          <h3>Comparing serious options</h3>
          <p>
            You know what you need and you are evaluating approaches. Here we surface proof,
            case studies, and side‑by‑side views so the right decision is obvious.
          </p>
        </article>

        <article class="card">
          <div class="stage-label">Decision</div>
          <h3>Ready to activate the engine</h3>
          <p>
            You have done the research and validated the value. The focus now is on removing
            friction, aligning stakeholders, and launching the done‑for‑you system with confidence.
          </p>
        </article>

        <article class="card">
          <div class="stage-label">Loyalty</div>
          <h3>Scaling authority and impact</h3>
          <p>
            You are extending what already works. We deepen personalization, expand visibility
            across channels, and turn wins into repeatable playbooks for your team.
          </p>
        </article>
      </div>

      <h2 style="margin-top: var(--space-3);">What teams like yours experience</h2>

      <article class="card quote">
        <p>“We went from 2% to 8% qualified conversion in 90 days once the engine was live.”</p>
        <p><strong>Sarah</strong>, Head of Growth, B2B SaaS</p>
      </article>

      <article class="card quote">
        <p>“The aha moment was simple: different visitors needed different messages, and the system handled it for us.”</p>
        <p><strong>Marcus</strong>, Founder, SaaS Company</p>
      </article>

      <article class="card quote">
        <p>“Best investment in our funnel. It gave us authority, not just more traffic.”</p>
        <p><strong>Jenna</strong>, CMO, Enterprise B2B</p>
      </article>
    </section>

    <!-- SIDE PANEL: METRICS + FIRST 90 DAYS -->
    <aside class="side-panel" aria-label="Performance and first 90 days">
      <h2>What the engine typically delivers</h2>
      <div class="stats-grid">
        <div class="stat">
          <div class="stat-value">45%</div>
          <div class="stat-label">Average conversion lift across key journeys</div>
        </div>
        <div class="stat">
          <div class="stat-value">2.3×</div>
          <div class="stat-label">Return on investment within six months</div>
        </div>
        <div class="stat">
          <div class="stat-value">4.9 / 5</div>
          <div class="stat-label">Customer satisfaction from B2B growth teams</div>
        </div>
      </div>

      <h2 style="margin-top: var(--space-3);">First 90 days with Authority Engine</h2>
      <p>
        The first 90 days are structured to create momentum quickly while protecting long‑term
        visibility and authority.
      </p>
      <ul>
        <li>Clarify high‑value segments and how they actually buy.</li>
        <li>Design journey‑aligned messaging for awareness, consideration, decision, and loyalty.</li>
        <li>Deploy personalized experiences and AI‑powered routing across your core touchpoints.</li>
        <li>Measure lift weekly, remove friction, and turn early wins into a repeatable playbook.</li>
      </ul>
    </aside>
  </main>
</body>
</html>
```
