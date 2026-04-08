
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Resume Questionnaire — Banking Sales Candidates</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet" />
<style>
  :root {
    --navy: #0B1F3A;
    --navy-mid: #163560;
    --gold: #C9952A;
    --gold-light: #F0C96B;
    --cream: #FAF7F2;
    --cream-dark: #F0EBE1;
    --text: #1A1A2E;
    --text-muted: #5A6478;
    --border: #DDD5C8;
    --white: #FFFFFF;
    --success: #1A6B4A;
    --radius: 10px;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--text);
    min-height: 100vh;
  }

  /* Header */
  .header {
    background: var(--navy);
    padding: 1.5rem 1.25rem 1.25rem;
    position: relative;
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    top: -60px; right: -60px;
    width: 200px; height: 200px;
    border-radius: 50%;
    background: rgba(201,149,42,0.12);
  }
  .header::after {
    content: '';
    position: absolute;
    bottom: -40px; left: 40%;
    width: 140px; height: 140px;
    border-radius: 50%;
    background: rgba(201,149,42,0.07);
  }
  .header-inner { max-width: 680px; margin: 0 auto; position: relative; z-index: 1; }
  .header-tag {
    display: inline-block;
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--gold-light);
    background: rgba(201,149,42,0.18);
    padding: 4px 12px;
    border-radius: 20px;
    margin-bottom: 10px;
  }
  .header h1 {
    font-family: 'DM Serif Display', serif;
    font-size: 24px;
    color: var(--white);
    line-height: 1.25;
    margin-bottom: 6px;
  }
  .header h1 em { color: var(--gold-light); font-style: italic; }
  .header p {
    font-size: 13px;
    color: rgba(255,255,255,0.65);
    line-height: 1.6;
    max-width: 480px;
  }

  /* Progress */
  .progress-wrap { background: var(--navy-mid); padding: 0.75rem 1.25rem; }
  .progress-inner { max-width: 680px; margin: 0 auto; display: flex; align-items: center; gap: 12px; }
  .progress-bar { flex: 1; height: 3px; background: rgba(255,255,255,0.15); border-radius: 2px; }
  .progress-fill { height: 3px; background: var(--gold); border-radius: 2px; transition: width 0.4s ease; width: 14%; }
  .progress-label { font-size: 12px; color: rgba(255,255,255,0.5); white-space: nowrap; }
  .progress-step { font-size: 12px; font-weight: 600; color: var(--gold-light); white-space: nowrap; }

  /* Main */
  main { max-width: 680px; margin: 0 auto; padding: 1.25rem 1rem 5rem; }

  /* Section */
  .section { display: none; }
  .section.active { display: block; animation: fadeUp 0.3s ease; }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }

  .section-eyebrow {
    display: flex; align-items: center; gap: 10px; margin-bottom: 1rem;
  }
  .section-num {
    width: 32px; height: 32px; border-radius: 50%;
    background: var(--navy); color: var(--gold-light);
    font-size: 13px; font-weight: 600;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
  }
  .section-meta h2 { font-size: 17px; font-weight: 600; font-family: 'DM Serif Display', serif; }
  .section-meta p { font-size: 12px; color: var(--text-muted); margin-top: 2px; }

  /* Card */
  .card {
    background: var(--white);
    border: 1px solid var(--border);
    border-radius: var(--radius);
    padding: 1.1rem 1rem;
    margin-bottom: 1rem;
  }

  /* Fields */
  .field { margin-bottom: 1rem; }
  .field:last-child { margin-bottom: 0; }
  .field label {
    display: block;
    font-size: 13px;
    font-weight: 500;
    color: var(--text-muted);
    margin-bottom: 6px;
    line-height: 1.4;
  }
  .field label .req { color: var(--gold); margin-left: 2px; }
  .field input, .field textarea, .field select {
    width: 100%;
    padding: 12px 13px;
    font-size: 16px; /* 16px prevents iOS auto-zoom on focus */
    font-family: 'DM Sans', sans-serif;
    border: 1.5px solid var(--border);
    border-radius: 8px;
    background: var(--cream);
    color: var(--text);
    outline: none;
    transition: border 0.2s, background 0.2s;
    appearance: none;
    -webkit-appearance: none;
  }
  .field input:focus, .field textarea:focus, .field select:focus {
    border-color: var(--navy-mid);
    background: var(--white);
  }
  .field textarea { resize: vertical; line-height: 1.65; }
  .field .hint { font-size: 12px; color: var(--text-muted); margin-top: 5px; line-height: 1.5; }
  .two-col { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  @media (max-width: 520px) { .two-col { grid-template-columns: 1fr; } }

  /* Tags */
  .tag-grid { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 8px; }
  .tag {
    padding: 9px 14px; /* taller for easier tapping on mobile */
    border-radius: 20px;
    font-size: 13px;
    font-weight: 500;
    border: 1.5px solid var(--border);
    background: var(--cream);
    color: var(--text-muted);
    cursor: pointer;
    transition: all 0.15s;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
  }
  .tag:hover { border-color: var(--navy); color: var(--navy); }
  .tag.on { background: var(--navy); border-color: var(--navy); color: var(--white); }

  /* Nav */
  .nav { display: flex; align-items: center; gap: 8px; margin-top: 1.25rem; flex-wrap: wrap; }
  .btn {
    padding: 13px 22px; /* taller touch target */
    border-radius: 8px;
    font-size: 15px;
    font-weight: 500;
    font-family: 'DM Sans', sans-serif;
    cursor: pointer;
    border: 1.5px solid var(--border);
    background: var(--white);
    color: var(--text);
    transition: all 0.15s;
    min-height: 48px; /* minimum recommended touch target */
    -webkit-tap-highlight-color: transparent;
  }
  .btn:hover { background: var(--cream-dark); }
  .btn.primary {
    background: var(--navy);
    border-color: var(--navy);
    color: var(--white);
  }
  .btn.primary:hover { background: var(--navy-mid); }
  .nav-spacer { flex: 1; }
  .nav-counter { font-size: 12px; color: var(--text-muted); }

  @media (max-width: 380px) {
    .btn { padding: 12px 16px; font-size: 14px; }
  }

  /* Done screen */
  .done-screen { display: none; text-align: center; padding: 3rem 1rem; }
  .done-screen.active { display: block; animation: fadeUp 0.4s ease; }
  .done-icon {
    width: 64px; height: 64px; border-radius: 50%;
    background: #E8F5EE;
    margin: 0 auto 1.25rem;
    display: flex; align-items: center; justify-content: center;
  }
  .done-screen h2 { font-family: 'DM Serif Display', serif; font-size: 24px; margin-bottom: 0.75rem; }
  .done-screen p { font-size: 14px; color: var(--text-muted); line-height: 1.7; max-width: 460px; margin: 0 auto 1.5rem; }

  /* Submitting spinner */
  .submitting-msg { font-size: 14px; color: var(--text-muted); margin-top: 1rem; display: none; }
  .submitting-msg.visible { display: block; }
  .error-msg {
    font-size: 13px; color: #A32D2D; background: #FCEBEB;
    border: 1px solid #F09595; border-radius: 8px;
    padding: 10px 14px; margin-top: 1rem; display: none; line-height: 1.6;
  }
  .error-msg.visible { display: block; }

  /* Footer note */
  .footer-note {
    text-align: center;
    font-size: 12px;
    color: var(--text-muted);
    margin-top: 3rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--border);
  }
</style>
</head>
<body>

<div class="header">
  <div class="header-inner">
    <div class="header-tag">Banking Sales — Resume Intake Form</div>
    <h1>Tell us about <em>yourself</em></h1>
    <p>Answer all 7 sections honestly and in detail. Your responses will be used to build a personalised, one-page resume for your banking interviews.</p>
  </div>
</div>

<div class="progress-wrap">
  <div class="progress-inner">
    <div class="progress-bar"><div class="progress-fill" id="prog"></div></div>
    <span class="progress-step" id="prog-step">1 / 7</span>
  </div>
</div>

<main>

  <!-- Section 1 -->
  <div class="section active" id="s1">
    <div class="section-eyebrow">
      <div class="section-num">1</div>
      <div class="section-meta"><h2>Personal details</h2><p>Your resume header information</p></div>
    </div>
    <div class="card">
      <div class="two-col">
        <div class="field"><label>Full name <span class="req">*</span></label><input id="fullname" type="text" placeholder="As on official documents" /></div>
        <div class="field"><label>Mobile number <span class="req">*</span></label><input id="phone" type="tel" placeholder="+91 XXXXX XXXXX" /></div>
      </div>
      <div class="field"><label>Email address <span class="req">*</span></label><input id="email" type="email" placeholder="yourname@email.com" /><div class="hint">Use a professional-sounding email. Avoid nicknames.</div></div>
      <div class="two-col">
        <div class="field"><label>City / town</label><input id="city" type="text" placeholder="e.g. Mumbai, Bengaluru" /></div>
        <div class="field"><label>LinkedIn URL (if any)</label><input id="linkedin" type="text" placeholder="linkedin.com/in/yourname" /></div>
      </div>
    </div>
    <div class="nav">
      <span class="nav-counter">Step 1 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" onclick="go(2)">Next →</button>
    </div>
  </div>

  <!-- Section 2 -->
  <div class="section" id="s2">
    <div class="section-eyebrow">
      <div class="section-num">2</div>
      <div class="section-meta"><h2>Education</h2><p>Highest qualification first</p></div>
    </div>
    <div class="card">
      <div class="field">
        <label>Highest qualification <span class="req">*</span></label>
        <select id="highest-qual">
          <option value="">— Select —</option>
          <option>Class 12 / HSC</option>
          <option>Diploma (3-year)</option>
          <option>Bachelor's degree (B.Com / BBA / BA / BSc / other)</option>
          <option>Master's degree (MBA / M.Com / other)</option>
          <option>Professional degree (CA / CFA / other)</option>
        </select>
      </div>
      <div class="field"><label>Course / stream name <span class="req">*</span></label><input id="course" type="text" placeholder="e.g. B.Com (Finance), MBA (Marketing)" /></div>
      <div class="two-col">
        <div class="field"><label>College / university</label><input id="college" type="text" placeholder="Full institution name" /></div>
        <div class="field"><label>Year of passing</label><input id="pass-year" type="text" placeholder="e.g. 2023 or Pursuing" /></div>
      </div>
      <div class="field"><label>Percentage / CGPA</label><input id="marks" type="text" placeholder="e.g. 72% or 7.8 CGPA" /><div class="hint">Leave blank if you prefer not to mention it.</div></div>
      <div class="field"><label>Any other qualification (Class 10, short courses, diplomas)</label><textarea id="other-edu" rows="2" placeholder="e.g. Class 10 – 88%, CBSE. Completed a 3-month Tally course in 2022."></textarea></div>
    </div>
    <div class="nav">
      <button class="btn" onclick="go(1)">← Back</button>
      <span class="nav-counter">Step 2 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" onclick="go(3)">Next →</button>
    </div>
  </div>

  <!-- Section 3 -->
  <div class="section" id="s3">
    <div class="section-eyebrow">
      <div class="section-num">3</div>
      <div class="section-meta"><h2>Work experience</h2><p>Internships, part-time, family business — everything counts</p></div>
    </div>
    <div class="card">
      <div class="field">
        <label>Do you have any work experience? <span class="req">*</span></label>
        <select id="has-exp" onchange="toggleExp()">
          <option value="">— Select —</option>
          <option value="yes">Yes</option>
          <option value="no">No, this will be my first job</option>
        </select>
      </div>
      <div id="exp-fields" style="display:none">
        <div class="field" style="margin-top:14px"><label>Most recent job title & company</label><input id="job1-title" type="text" placeholder="e.g. Sales Executive – Bajaj Finserv, Pune" /></div>
        <div class="two-col">
          <div class="field"><label>Duration (from – to)</label><input id="job1-dur" type="text" placeholder="e.g. Jun 2022 – Mar 2024" /></div>
          <div class="field"><label>Employment type</label>
            <select id="job1-type">
              <option value="">— Select —</option>
              <option>Full-time</option><option>Part-time</option><option>Internship</option><option>Freelance / contract</option><option>Family business</option>
            </select>
          </div>
        </div>
        <div class="field"><label>Key responsibilities (2–3 sentences)</label><textarea id="job1-resp" rows="3" placeholder="e.g. Handled walk-in customer queries, cross-sold insurance products, maintained daily sales MIS, achieved 115% of monthly target in Q3 2023."></textarea><div class="hint">Include numbers, targets, or results wherever possible.</div></div>
        <div class="field"><label>Any previous job(s) — title, company, duration, brief role</label><textarea id="job2" rows="3" placeholder="e.g. Cashier – Big Bazaar, Nagpur (Jun 2021 – May 2022). Handled billing, customer complaints, daily cash reconciliation."></textarea></div>
      </div>
    </div>
    <div class="nav">
      <button class="btn" onclick="go(2)">← Back</button>
      <span class="nav-counter">Step 3 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" onclick="go(4)">Next →</button>
    </div>
  </div>

  <!-- Section 4 -->
  <div class="section" id="s4">
    <div class="section-eyebrow">
      <div class="section-num">4</div>
      <div class="section-meta"><h2>Skills</h2><p>Tap to select all that apply</p></div>
    </div>
    <div class="card">
      <div class="field">
        <label>Select your skills <span class="req">*</span></label>
        <div class="tag-grid" id="skill-tags">
          <span class="tag" onclick="toggleTag(this)">Customer service</span>
          <span class="tag" onclick="toggleTag(this)">Sales & cross-selling</span>
          <span class="tag" onclick="toggleTag(this)">Cash handling</span>
          <span class="tag" onclick="toggleTag(this)">MS Excel / spreadsheets</span>
          <span class="tag" onclick="toggleTag(this)">MS Word / documentation</span>
          <span class="tag" onclick="toggleTag(this)">Tally / accounting software</span>
          <span class="tag" onclick="toggleTag(this)">CRM tools (Salesforce etc.)</span>
          <span class="tag" onclick="toggleTag(this)">Data entry & MIS</span>
          <span class="tag" onclick="toggleTag(this)">Objection handling</span>
          <span class="tag" onclick="toggleTag(this)">Lead generation</span>
          <span class="tag" onclick="toggleTag(this)">KYC / documentation</span>
          <span class="tag" onclick="toggleTag(this)">Team collaboration</span>
          <span class="tag" onclick="toggleTag(this)">Problem solving</span>
          <span class="tag" onclick="toggleTag(this)">Time management</span>
        </div>
      </div>
      <div class="field"><label>Any other skills not listed above</label><input id="other-skills" type="text" placeholder="e.g. NISM certified, foreign exchange awareness, Marathi typing" /></div>
      <div class="field"><label>Computer / digital literacy</label><textarea id="digital" rows="2" placeholder="e.g. Comfortable with MS Office, UPI / mobile banking apps. Typing speed ~35 WPM."></textarea></div>
    </div>
    <div class="nav">
      <button class="btn" onclick="go(3)">← Back</button>
      <span class="nav-counter">Step 4 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" onclick="go(5)">Next →</button>
    </div>
  </div>

  <!-- Section 5 -->
  <div class="section" id="s5">
    <div class="section-eyebrow">
      <div class="section-num">5</div>
      <div class="section-meta"><h2>Achievements & awards</h2><p>Academic, professional, sports, volunteering — all count</p></div>
    </div>
    <div class="card">
      <div class="field">
        <label>List up to 3 achievements you are proud of <span class="req">*</span></label>
        <textarea id="achievements" rows="5" placeholder="1. Ranked 2nd in district-level commerce quiz (2022)&#10;2. Awarded 'Best Performer' at XYZ Company for exceeding Q2 target by 30%&#10;3. Organised annual college fest, managed a team of 15 volunteers"></textarea>
        <div class="hint">Include the year and a brief outcome wherever possible.</div>
      </div>
      <div class="field"><label>Positions of responsibility held (college or work)</label><textarea id="positions" rows="2" placeholder="e.g. Class representative (2021–22), NSS volunteer, captain of college cricket team"></textarea></div>
    </div>
    <div class="nav">
      <button class="btn" onclick="go(4)">← Back</button>
      <span class="nav-counter">Step 5 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" onclick="go(6)">Next →</button>
    </div>
  </div>

  <!-- Section 6 -->
  <div class="section" id="s6">
    <div class="section-eyebrow">
      <div class="section-num">6</div>
      <div class="section-meta"><h2>Languages & certifications</h2><p>Especially valuable for customer-facing banking roles</p></div>
    </div>
    <div class="card">
      <div class="field">
        <label>Languages known <span class="req">*</span></label>
        <input id="languages" type="text" placeholder="e.g. Hindi (fluent), English (proficient), Marathi (native)" />
        <div class="hint">Mention proficiency: native / fluent / proficient / basic.</div>
      </div>
      <div class="field">
        <label>Certifications or short courses completed</label>
        <textarea id="certifications" rows="3" placeholder="e.g. NISM Series V-A (Mutual Fund Distributor) – 2023&#10;Google Digital Marketing certificate – 2022&#10;Tally ERP 9 course – 6 months (2021)"></textarea>
        <div class="hint">Include ongoing certifications too, marking them as "In progress".</div>
      </div>
    </div>
    <div class="nav">
      <button class="btn" onclick="go(5)">← Back</button>
      <span class="nav-counter">Step 6 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" onclick="go(7)">Next →</button>
    </div>
  </div>

  <!-- Section 7 -->
  <div class="section" id="s7">
    <div class="section-eyebrow">
      <div class="section-num">7</div>
      <div class="section-meta"><h2>Career goal & context</h2><p>Helps us write a compelling, personalised summary</p></div>
    </div>
    <div class="card">
      <div class="field">
        <label>Why do you want to work in banking / financial services? <span class="req">*</span></label>
        <textarea id="why-banking" rows="3" placeholder="Write 2–4 sentences in your own words. What draws you to this field? What do you hope to build?"></textarea>
      </div>
      <div class="field">
        <label>One strength that will help you succeed in a frontline sales role</label>
        <textarea id="strength" rows="2" placeholder="e.g. I am patient with customers and good at explaining complex products simply."></textarea>
      </div>
      <div class="field">
        <label>Anything specific about your background you'd like highlighted</label>
        <textarea id="highlight" rows="2" placeholder="e.g. I grew up in a semi-rural area and am fluent in 3 dialects, which helps in reaching diverse customers."></textarea>
      </div>
      <div class="field">
        <label>Which type of bank or role are you most interested in?</label>
        <select id="bank-pref">
          <option value="">— Select (optional) —</option>
          <option>Public sector bank (SBI, PNB, Bank of Baroda, etc.)</option>
          <option>Private sector bank (HDFC, ICICI, Axis, Kotak, etc.)</option>
          <option>Small finance bank</option>
          <option>NBFC / housing finance company</option>
          <option>Open to any</option>
        </select>
      </div>
    </div>
    <div class="nav">
      <button class="btn" onclick="go(6)">← Back</button>
      <span class="nav-counter">Step 7 of 7</span>
      <div class="nav-spacer"></div>
      <button class="btn primary" id="submit-btn" onclick="finish()">Submit answers ✓</button>
    </div>
    <div class="submitting-msg" id="submitting-msg">Sending your answers to Google Sheets, please wait…</div>
    <div class="error-msg" id="error-msg"></div>
  </div>

  <!-- Done screen -->
  <div class="done-screen" id="done">
    <div class="done-icon">
      <svg width="28" height="28" viewBox="0 0 28 28" fill="none"><path d="M6 14.5l5.5 5.5L22 9" stroke="#1A6B4A" stroke-width="2.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
    </div>
    <h2>Answers submitted!</h2>
    <p>Your responses have been saved successfully. Your resume consultant will review your answers and prepare your personalised one-page resume shortly.</p>
  </div>

  <div class="footer-note">
    This form is confidential. Your answers are used solely to prepare your resume.
  </div>

</main>

<script>
  let current = 1;
  const total = 7;

  function go(n) {
    document.getElementById('s' + current).classList.remove('active');
    current = n;
    document.getElementById('s' + current).classList.add('active');
    const pct = Math.round((n / total) * 100);
    document.getElementById('prog').style.width = pct + '%';
    document.getElementById('prog-step').textContent = n + ' / ' + total;
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  function toggleExp() {
    const v = document.getElementById('has-exp').value;
    document.getElementById('exp-fields').style.display = v === 'yes' ? 'block' : 'none';
  }

  function toggleTag(el) { el.classList.toggle('on'); }

  function val(id) {
    const el = document.getElementById(id);
    return el ? el.value.trim() || '—' : '—';
  }

  function selectedTags() {
    return Array.from(document.querySelectorAll('#skill-tags .tag.on')).map(t => t.textContent).join(', ') || '—';
  }

  const SHEET_URL = 'https://script.google.com/macros/s/AKfycbzgRtwteGXRcJaGqAf6Mw4ltFnNBnFp6qFJyDjFzjZJAu6epSDJWg6HDmYjp3sOwFWWdw/exec';

  function finish() {
    const submitBtn = document.getElementById('submit-btn');
    const submittingMsg = document.getElementById('submitting-msg');
    const errorMsg = document.getElementById('error-msg');

    submitBtn.disabled = true;
    submitBtn.textContent = 'Submitting…';
    submittingMsg.classList.add('visible');
    errorMsg.classList.remove('visible');

    const payload = {
      fullname:    val('fullname'),
      phone:       val('phone'),
      email:       val('email'),
      city:        val('city'),
      linkedin:    val('linkedin'),
      highestQual: val('highest-qual'),
      course:      val('course'),
      college:     val('college'),
      passYear:    val('pass-year'),
      marks:       val('marks'),
      otherEdu:    val('other-edu'),
      hasExp:      val('has-exp'),
      job1Title:   val('job1-title'),
      job1Dur:     val('job1-dur'),
      job1Type:    val('job1-type'),
      job1Resp:    val('job1-resp'),
      job2:        val('job2'),
      skills:      selectedTags(),
      otherSkills: val('other-skills'),
      digital:     val('digital'),
      achievements: val('achievements'),
      positions:   val('positions'),
      languages:   val('languages'),
      certifications: val('certifications'),
      whyBanking:  val('why-banking'),
      strength:    val('strength'),
      highlight:   val('highlight'),
      bankPref:    val('bank-pref')
    };

    fetch(SHEET_URL, {
      method: 'POST',
      mode: 'no-cors',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(payload)
    })
    .then(() => {
      document.getElementById('s7').classList.remove('active');
      document.getElementById('prog').style.width = '100%';
      document.getElementById('prog-step').textContent = '✓ Done';
      submittingMsg.classList.remove('visible');
      document.getElementById('done').classList.add('active');
      window.scrollTo({ top: 0, behavior: 'smooth' });
    })
    .catch(() => {
      submitBtn.disabled = false;
      submitBtn.textContent = 'Submit answers ✓';
      submittingMsg.classList.remove('visible');
      errorMsg.textContent = 'Something went wrong while sending your answers. Please check your internet connection and try again.';
      errorMsg.classList.add('visible');
    });
  }
</script>
</body>
</html>
