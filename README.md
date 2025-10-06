# ReshmaKhan_Resume
Web Development assignment project — applying CSS concepts like selectors, positioning, flexbox, and responsive design to enhance my personal resume website.
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&family=Merriweather:ital,wght@0,400;0,700;1,400&display=swap" rel="stylesheet">

<body>
  <div class="container">
    <header class="site-header">
      <a class="brand" href="#">
        <div class="logo">RK</div>
        <h1>Reshma Khan</h1>
      </a>

      <nav class="nav" aria-label="Main navigation">
        <a href="#about">About</a>
        <a href="#experience">Experience</a>
        <a href="#projects">Projects</a>
        <a href="#contact" class="btn">Contact</a>
      </nav>
    </header>

    <section class="hero">
      <div class="hero-card">
        <div class="avatar">R</div>
        <div class="hero-info">
          <h2>Reshma Khan — BBA | BCA Student</h2>
          <p>Operations Strategy Intern applicant. Passion for UX, analytics and efficient product workflows.</p>
          <div class="contact-row">
            <span class="contact-pill">Mysore, India</span>
            <span class="contact-pill">reshma@example.com</span>
            <span class="contact-pill">+91 9XXXXXXXXX</span>
          </div>
        </div>
      </div>

      <div class="section">
        <h3>Profile</h3>
        <p>Short 2–3 line summary describing your strengths and what you’re looking for.</p>
        <div style="margin-top:0.6rem;">
          <a href="#projects" class="btn">See Projects</a>
          <a href="#resume.pdf" class="btn secondary" style="margin-left:0.5rem;">Download CV</a>
        </div>
      </div>
    </section>

    <main class="main">
      <div>
        <section id="experience" class="section">
          <h3>Experience</h3>
          <div class="item">
            <div class="meta">2024 — Present</div>
            <div class="body">
              <h4>Operations Strategy Intern — Project Catalyst</h4>
              <p>Worked on process optimization and student onboarding flows.</p>
            </div>
          </div>
          <!-- add more .item -->
        </section>

        <section id="projects" class="section" style="margin-top:0.8rem;">
          <h3>Projects</h3>
          <div class="item">
            <div class="meta">2025</div>
            <div class="body">
              <h4>Resume Website Redesign</h4>
              <p>Implemented responsive layout and improved accessibility.</p>
            </div>
          </div>
        </section>
      </div>

      <aside>
        <section class="section">
          <h3>Skills</h3>
          <div class="skills">
            <div class="skill-chip">Figma</div>
            <div class="skill-chip">HTML & CSS</div>
            <div class="skill-chip">Basic Python</div>
            <div class="skill-chip">Excel</div>
            <div class="skill-chip">Communication</div>
          </div>
        </section>

        <section id="contact" class="section" style="margin-top:0.8rem;">
          <h3>Contact</h3>
          <p>Email: reshma@example.com</p>
          <p>LinkedIn: linkedin.com/in/yourprofile</p>
        </section>
      </aside>
    </main>

    <footer class="site-footer">
      © 2025 Reshma Khan — Built with ❤️
    </footer>
  </div>
</body>

<link rel="stylesheet" href="css/style.css">
<meta name="viewport" content="width=device-width, initial-scale=1">
/* =========================
   Variables & Base
   ========================= */
:root{
  --bg: #F6F7FB;
  --card-bg: #FFFFFF;
  --muted: #6B7280;        /* gray text */
  --accent: #2B7A78;       /* teal-ish accent */
  --accent-2: #4FB0B0;     /* lighter accent */
  --shadow: 0 6px 18px rgba(15,23,42,0.06);
  --max-width: 1000px;
  --radius: 10px;
  --gap: 1rem;
}

/* Mobile-first reset */
*{box-sizing:border-box}
html,body{height:100%}
body{
  margin:0;
  font-family: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
  background: linear-gradient(180deg, var(--bg), #ffffff 60%);
  color:#0F172A;
  line-height:1.45;
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  padding:1.25rem;
}

/* Center container */
.container{
  max-width:var(--max-width);
  margin:0 auto;
  display:flex;
  flex-direction:column;
  gap:var(--gap);
}

/* =========================
   Header / Nav
   ========================= */
.site-header{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:1rem;
  padding:0.5rem;
}

.brand{
  display:flex;
  align-items:center;
  gap:0.75rem;
  text-decoration:none;
  color:inherit;
}
.brand .logo{
  width:48px;
  height:48px;
  border-radius:8px;
  background:linear-gradient(135deg,var(--accent),var(--accent-2));
  display:inline-flex;
  align-items:center;
  justify-content:center;
  color:white;
  font-weight:700;
  box-shadow:var(--shadow);
}
.brand h1{
  font-size:1rem;
  margin:0;
  font-weight:600;
  letter-spacing:0.2px;
}
.nav{
  display:flex;
  gap:0.75rem;
  align-items:center;
}
.nav a{
  text-decoration:none;
  color:var(--muted);
  padding:0.4rem 0.65rem;
  border-radius:6px;
  font-weight:600;
  font-size:0.9rem;
}
.nav a:hover{ background:rgba(43,122,120,0.08); color:var(--accent); }

/* =========================
   Hero / Intro
   ========================= */
.hero{
  display:grid;
  grid-template-columns: 1fr;
  gap:1rem;
  align-items:center;
  background:transparent;
  padding:0.75rem;
}
.hero-card{
  background:var(--card-bg);
  border-radius:var(--radius);
  box-shadow:var(--shadow);
  padding:1rem;
  display:flex;
  gap:1rem;
  align-items:center;
}
.avatar{
  width:92px;
  height:92px;
  border-radius:12px;
  background:linear-gradient(135deg,var(--accent-2),var(--accent));
  flex-shrink:0;
  display:inline-flex;
  align-items:center;
  justify-content:center;
  color:white;
  font-weight:700;
  font-size:1.4rem;
}
.hero-info h2{
  margin:0;
  font-family: "Merriweather", serif;
  font-size:1.25rem;
  font-weight:700;
}
.hero-info p{ margin:0.25rem 0 0; color:var(--muted); }

/* quick contact row */
.contact-row{
  display:flex;
  gap:0.75rem;
  flex-wrap:wrap;
  margin-top:0.5rem;
}
.contact-pill{
  background:rgba(43,122,120,0.06);
  color:var(--accent);
  padding:0.35rem 0.6rem;
  border-radius:999px;
  font-weight:600;
  font-size:0.85rem;
}

/* =========================
   Main content columns (desktop)
   ========================= */
.main{
  display:grid;
  grid-template-columns: 1fr;
  gap:1rem;
}

/* Cards grid for sections like Experience, Education, Projects */
.section{
  background:var(--card-bg);
  border-radius:var(--radius);
  padding:0.9rem;
  box-shadow:var(--shadow);
}
.section h3{
  margin:0 0 0.55rem 0;
  font-size:1.05rem;
  color: #05224A;
}

/* Experience/Project list */
.item{
  border-left:3px solid transparent;
  padding:0.6rem 0;
  display:flex;
  gap:0.75rem;
  align-items:flex-start;
}
.item + .item{ margin-top:0.4rem; }
.item .meta{
  min-width:92px;
  font-size:0.85rem;
  color:var(--muted);
}
.item .body h4{ margin:0; font-size:1rem; font-weight:600; }
.item .body p{ margin:0.25rem 0 0; color:var(--muted); font-size:0.95rem; }

/* Skills grid */
.skills{
  display:grid;
  grid-template-columns: repeat(2, 1fr);
  gap:0.5rem;
}
.skill-chip{
  background:rgba(6,95,93,0.06);
  padding:0.45rem 0.6rem;
  border-radius:8px;
  font-weight:600;
  font-size:0.9rem;
  color: #0A3B3B;
}

/* CTA / Buttons */
.btn{
  display:inline-block;
  text-decoration:none;
  background:var(--accent);
  color:white;
  padding:0.5rem 0.75rem;
  border-radius:8px;
  font-weight:700;
}
.btn.secondary{
  background:transparent;
  border:1.5px solid rgba(6,95,93,0.12);
  color:var(--accent);
}

/* =========================
   Footer
   ========================= */
.site-footer{
  text-align:center;
  color:var(--muted);
  font-size:0.9rem;
  padding:0.75rem 0;
}

/* =========================
   Responsive */
@media (min-width:700px){
  .hero{ grid-template-columns: 1fr 2fr; }
  .main{ grid-template-columns: 2.2fr 1fr; align-items:start; }
  .skills{ grid-template-columns: repeat(3, 1fr); }
}

/* =========================
   Print styles (neat)
   ========================= */
@media print {
  body{ background:white; color:black; padding:0; }
  .site-header, .site-footer, .nav, .btn{ display:none !important; }
  .container{ max-width:720px; margin:0; }
  .hero-card, .section{ box-shadow:none; border-radius:0; }
  .avatar{ display:none; }
}
