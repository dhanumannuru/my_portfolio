<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="theme-color" content="#080b16" />
  <meta name="description" content="Portfolio of Dhanush Kumar Reddy — Computer Science and Engineering student specializing in AI and Machine Learning." />
  <title>Dhanush Kumar Reddy | AI/ML Portfolio</title>
  <style>
    :root{--bg:#080b16;--panel:#111629;--panel2:#151c32;--text:#eef2ff;--muted:#a6b0cb;--line:rgba(167,184,255,.16);--accent:#8b7cff;--cyan:#53e0d0;--pink:#ff7ac6;--radius:22px;--max:1120px}
    *{box-sizing:border-box;margin:0;padding:0}
    html{scroll-behavior:smooth;scroll-padding-top:86px}
    body{font-family:Inter,ui-sans-serif,system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;background:var(--bg);color:var(--text);line-height:1.65;overflow-x:hidden}
    a{color:inherit;text-decoration:none} button{font:inherit}
    .ambient{position:fixed;inset:0;z-index:-2;overflow:hidden;pointer-events:none;background:radial-gradient(ellipse at 15% 5%,rgba(98,75,255,.17),transparent 40%),radial-gradient(ellipse at 90% 30%,rgba(26,204,194,.10),transparent 35%),var(--bg)}
    .ambient:before,.ambient:after{content:"";position:absolute;width:420px;height:420px;border:1px solid rgba(139,124,255,.13);border-radius:50%;filter:blur(.2px);animation:float 18s ease-in-out infinite alternate}
    .ambient:before{top:8%;left:-230px;box-shadow:0 0 0 50px rgba(139,124,255,.025),0 0 0 100px rgba(139,124,255,.02)}
    .ambient:after{right:-250px;top:50%;border-color:rgba(83,224,208,.13);animation-delay:-8s}
    @keyframes float{to{transform:translateY(70px) rotate(22deg)}}
    .grid-bg{position:fixed;inset:0;z-index:-1;pointer-events:none;opacity:.18;background-image:linear-gradient(rgba(145,160,215,.07) 1px,transparent 1px),linear-gradient(90deg,rgba(145,160,215,.07) 1px,transparent 1px);background-size:52px 52px;mask-image:linear-gradient(to bottom,black,transparent 90%)}
    .container{width:min(var(--max),calc(100% - 40px));margin:auto}
    header{position:sticky;top:0;z-index:20;backdrop-filter:blur(18px);background:rgba(8,11,22,.78);border-bottom:1px solid var(--line)}
    .nav{height:74px;display:flex;align-items:center;justify-content:space-between;gap:20px}
    .brand{font-weight:800;letter-spacing:-.04em;font-size:1.06rem}.brand span{color:var(--cyan)}
    .navlinks{display:flex;align-items:center;gap:26px;color:var(--muted);font-size:.9rem}
    .navlinks a:hover,.navlinks a.active{color:var(--text)}
    .navlinks a.active:after{content:"";display:block;height:2px;background:var(--cyan);border-radius:5px}
    .menu-btn{display:none;background:transparent;color:var(--text);border:1px solid var(--line);border-radius:10px;padding:7px 11px;cursor:pointer}
    .hero{min-height:calc(92vh - 74px);display:grid;grid-template-columns:1.2fr .8fr;align-items:center;gap:48px;padding:80px 0 90px}
    .eyebrow{display:inline-flex;align-items:center;gap:9px;padding:7px 12px;border:1px solid var(--line);border-radius:999px;color:#c7c9ff;background:rgba(139,124,255,.08);font-size:.82rem}
    .dot{width:8px;height:8px;background:var(--cyan);border-radius:50%;box-shadow:0 0 15px var(--cyan)}
    h1{font-size:clamp(2.7rem,6.2vw,5.3rem);line-height:1.02;letter-spacing:-.065em;margin:25px 0 20px}
    .gradient{background:linear-gradient(100deg,#a99cff 8%,#68e9dc 55%,#ff9bd7);-webkit-background-clip:text;background-clip:text;color:transparent}
    .hero p{color:var(--muted);max-width:620px;font-size:1.08rem}
    .hero-actions{display:flex;flex-wrap:wrap;gap:12px;margin:30px 0 28px}
    .btn{display:inline-flex;align-items:center;justify-content:center;gap:9px;padding:12px 18px;border-radius:13px;border:1px solid var(--line);font-weight:700;font-size:.92rem;transition:transform .2s,border-color .2s,background .2s;cursor:pointer}
    .btn:hover{transform:translateY(-3px);border-color:rgba(83,224,208,.55)}
    .btn-primary{background:linear-gradient(120deg,#8b7cff,#6559d9);border-color:transparent;box-shadow:0 10px 35px rgba(105,89,217,.23)}
    .btn-secondary{background:rgba(255,255,255,.025)}
    .quick-info{display:flex;flex-wrap:wrap;gap:18px;color:var(--muted);font-size:.88rem}
    .quick-info span{display:flex;align-items:center;gap:7px}
    .hero-art{display:flex;justify-content:center;align-items:center;position:relative;min-height:390px}
    .orbit{width:min(350px,80vw);aspect-ratio:1;border:1px solid rgba(139,124,255,.38);border-radius:50%;display:grid;place-items:center;position:relative;box-shadow:0 0 80px rgba(139,124,255,.10),inset 0 0 70px rgba(139,124,255,.07);animation:rotate 30s linear infinite}
    .orbit:before,.orbit:after{content:"";position:absolute;inset:25px;border:1px dashed rgba(83,224,208,.35);border-radius:50%}
    .orbit:after{inset:58px;border-style:solid;border-color:rgba(255,122,198,.25)}
    @keyframes rotate{to{transform:rotate(360deg)}}
    .core{width:150px;height:150px;border-radius:36px;display:grid;place-items:center;text-align:center;transform:rotate(-45deg);background:linear-gradient(140deg,rgba(139,124,255,.24),rgba(83,224,208,.12));border:1px solid rgba(193,188,255,.5);box-shadow:0 0 60px rgba(139,124,255,.18)}
    .core-inner{transform:rotate(45deg)}.core strong{display:block;font-size:2.5rem;letter-spacing:-.08em}.core small{color:var(--cyan);letter-spacing:.14em;font-size:.7rem}
    .orbit-tag{position:absolute;z-index:2;padding:9px 12px;border-radius:12px;background:#141a2e;border:1px solid var(--line);box-shadow:0 10px 30px #0004;font-size:.82rem;color:#d9ddf5;animation:floatTag 4s ease-in-out infinite alternate}
    .orbit-tag.t1{top:12%;left:0}.orbit-tag.t2{top:20%;right:-4%;animation-delay:-1s}.orbit-tag.t3{bottom:16%;left:-5%;animation-delay:-2s}.orbit-tag.t4{bottom:9%;right:5%;animation-delay:-3s}
    @keyframes floatTag{to{translate:0 -10px}}
    section{padding:88px 0}
    .section-head{display:flex;align-items:end;justify-content:space-between;gap:20px;margin-bottom:34px}
    .kicker{color:var(--cyan);font-size:.78rem;font-weight:800;text-transform:uppercase;letter-spacing:.18em}
    h2{font-size:clamp(2rem,4vw,3rem);letter-spacing:-.05em;line-height:1.15;margin-top:8px}
    .section-desc{color:var(--muted);max-width:490px}
    .about-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:22px}
    .panel{background:linear-gradient(145deg,rgba(21,28,50,.92),rgba(13,18,34,.92));border:1px solid var(--line);border-radius:var(--radius);padding:26px}
    .panel p{color:var(--muted)}
    .stats{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
    .stat{padding:20px;border:1px solid var(--line);border-radius:17px;background:rgba(255,255,255,.025)}
    .stat strong{font-size:2rem;letter-spacing:-.05em;display:block}.stat span{font-size:.82rem;color:var(--muted)}
    .timeline{display:grid;gap:14px}
    .timeline-item{display:grid;grid-template-columns:120px 1fr;gap:18px;padding:21px 0;border-bottom:1px solid var(--line)}
    .timeline-item:last-child{border-bottom:0}.date{color:var(--cyan);font-size:.85rem;font-weight:800}
    .timeline-item h3{font-size:1.05rem;margin-bottom:4px}.timeline-item p{color:var(--muted);font-size:.92rem}
    .skill-groups{display:grid;grid-template-columns:repeat(3,1fr);gap:16px}
    .skill-group h3{display:flex;align-items:center;gap:9px;margin-bottom:16px;font-size:1.03rem}
    .skill-icon{display:grid;place-items:center;width:34px;height:34px;border-radius:10px;background:rgba(139,124,255,.15);color:#b9b0ff}
    .chips{display:flex;flex-wrap:wrap;gap:8px}
    .chip{border:1px solid var(--line);background:rgba(255,255,255,.025);border-radius:999px;padding:7px 11px;color:#d3daf0;font-size:.82rem}
    .skill-bars{margin-top:20px;display:grid;gap:15px}
    .skill-row{display:grid;gap:7px}.skill-label{display:flex;justify-content:space-between;font-size:.85rem;color:#d9def1}.bar{height:7px;border-radius:999px;background:#252d46;overflow:hidden}.bar span{height:100%;display:block;border-radius:999px;background:linear-gradient(90deg,var(--accent),var(--cyan));width:var(--level);transform-origin:left;animation:grow 1.3s ease both}
    @keyframes grow{from{transform:scaleX(0)}to{transform:scaleX(1)}}
    .projects{display:grid;grid-template-columns:repeat(2,1fr);gap:18px}
    .project{padding:0;overflow:hidden;transition:transform .25s,border-color .25s}.project:hover{transform:translateY(-5px);border-color:rgba(139,124,255,.5)}
    .project-top{padding:25px 25px 18px;background:radial-gradient(circle at 100% 0,rgba(139,124,255,.17),transparent 45%)}
    .project-symbol{width:48px;height:48px;border-radius:14px;display:grid;place-items:center;font-size:1.4rem;background:rgba(139,124,255,.14);border:1px solid var(--line);margin-bottom:18px}
    .project h3{font-size:1.25rem;line-height:1.3;margin-bottom:9px}.project p{color:var(--muted);font-size:.93rem}
    .project-bottom{padding:0 25px 25px}.project-bottom .chips{margin-bottom:18px}
    .project-note{font-size:.8rem;color:#aab5d1;border-top:1px solid var(--line);padding-top:14px}
    .internship{display:grid;grid-template-columns:auto 1fr;gap:20px;align-items:start}
    .cloud-mark{width:64px;height:64px;border-radius:18px;display:grid;place-items:center;font-size:1.7rem;background:linear-gradient(140deg,rgba(83,224,208,.18),rgba(139,124,255,.18));border:1px solid var(--line)}
    .internship h3{font-size:1.2rem}.subline{color:var(--cyan);font-size:.88rem;margin:4px 0 12px}.internship ul{padding-left:19px;color:var(--muted)}.internship li{margin:5px 0}
    .achievement-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
    .achievement{display:flex;gap:13px;align-items:flex-start}.achievement .symbol{font-size:1.3rem}.achievement p{color:var(--muted);font-size:.9rem}
    .contact-box{padding:clamp(25px,5vw,55px);border-radius:28px;border:1px solid rgba(139,124,255,.32);background:radial-gradient(ellipse at 10% 0,rgba(139,124,255,.16),transparent 45%),linear-gradient(145deg,#141a30,#0d1222);display:flex;align-items:center;justify-content:space-between;gap:25px}
    .contact-box p{color:var(--muted);max-width:600px;margin-top:12px}
    .contact-actions{display:flex;flex-wrap:wrap;gap:10px}
    footer{padding:28px 0;border-top:1px solid var(--line);color:var(--muted);font-size:.84rem}
    .footer-inner{display:flex;justify-content:space-between;gap:18px;flex-wrap:wrap}
    .reveal{opacity:0;transform:translateY(18px);transition:opacity .7s ease,transform .7s ease}.reveal.visible{opacity:1;transform:translateY(0)}
    .to-top{position:fixed;right:22px;bottom:22px;width:44px;height:44px;border-radius:13px;border:1px solid var(--line);background:#171d33;color:white;cursor:pointer;display:none;z-index:10}
    .to-top.show{display:block}
    @media(max-width:850px){.hero{grid-template-columns:1fr;gap:30px;padding-top:65px}.hero-art{min-height:330px;grid-row:1}.hero-copy{grid-row:2}.orbit{width:285px}.core{width:120px;height:120px}.core strong{font-size:2rem}.about-grid{grid-template-columns:1fr}.skill-groups{grid-template-columns:repeat(2,1fr)}.achievement-grid{grid-template-columns:repeat(2,1fr)}.contact-box{align-items:flex-start;flex-direction:column}}
    @media(max-width:620px){.container{width:min(100% - 28px,var(--max))}.nav{height:66px}.menu-btn{display:block}.navlinks{display:none;position:absolute;top:66px;left:0;right:0;padding:18px 22px 22px;background:rgba(8,11,22,.97);border-bottom:1px solid var(--line);flex-direction:column;align-items:flex-start;gap:16px}.navlinks.open{display:flex}.navlinks a.active:after{display:none}.hero{min-height:auto;padding:46px 0 60px}.hero-art{min-height:270px}.orbit{width:240px}.orbit-tag{font-size:.72rem;padding:7px 9px}.orbit-tag.t2{right:-7%}.orbit-tag.t3{left:-8%}h1{font-size:clamp(2.65rem,13vw,4rem)}section{padding:62px 0}.section-head{display:block}.section-desc{margin-top:13px}.skill-groups,.projects,.achievement-grid{grid-template-columns:1fr}.timeline-item{grid-template-columns:1fr;gap:4px}.stats{gap:9px}.stat{padding:16px}.stat strong{font-size:1.7rem}.panel{padding:21px}.internship{grid-template-columns:1fr}.contact-actions{width:100%}.contact-actions .btn{flex:1}}
    @media(prefers-reduced-motion:reduce){*,*:before,*:after{scroll-behavior:auto!important;animation:none!important;transition:none!important}.reveal{opacity:1;transform:none}}
  </style>
</head>
<body>
  <div class="ambient"></div><div class="grid-bg"></div>
  <header>
    <div class="container nav">
      <a class="brand" href="#home">DK<span>.</span></a>
      <button class="menu-btn" id="menuBtn" aria-label="Toggle navigation" aria-expanded="false">☰</button>
      <nav class="navlinks" id="navLinks" aria-label="Main navigation">
        <a href="#about">About</a><a href="#education">Education</a><a href="#skills">Skills</a><a href="#projects">Projects</a><a href="#experience">Internship</a><a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main>
    <section class="container hero" id="home">
      <div class="hero-copy">
        <div class="eyebrow"><span class="dot"></span> AI &amp; Machine Learning Student · 2023–2027</div>
        <h1>Building ideas<br>into <span class="gradient">intelligent</span><br>solutions.</h1>
        <p>I'm <strong>M. Dhanush Kumar Reddy</strong>, a Computer Science and Engineering student specializing in AI &amp; ML. I’m interested in building data-driven systems that help solve real-world problems.</p>
        <div class="hero-actions">
          <a class="btn btn-primary" href="#projects">Explore my projects <span>↗</span></a>
          <a class="btn btn-secondary" href="#contact">Contact me <span>→</span></a>
          <a class="btn btn-secondary" href="Dhanush_Kumar_Reddy_Resume.pdf" download>Download resume ↓</a>
        </div>
        <div class="quick-info">
          <span>⌖ Tirupati, Andhra Pradesh</span><span>✉ mallularajreddy1456@gmail.com</span>
        </div>
      </div>
      <div class="hero-art" aria-label="Animated AI-inspired graphic">
        <div class="orbit">
          <div class="core"><div class="core-inner"><strong>AI<span style="color:var(--cyan)">/</span>ML</strong><small>BUILD · LEARN</small></div></div>
          <span class="orbit-tag t1">⌘ Python</span><span class="orbit-tag t2">◈ Deep Learning</span><span class="orbit-tag t3">▦ Data Science</span><span class="orbit-tag t4">☁ Cloud</span>
        </div>
      </div>
    </section>

    <section id="about">
      <div class="container">
        <div class="section-head reveal"><div><div class="kicker">01 / About me</div><h2>Curious mind. Practical focus.</h2></div><p class="section-desc">A growing AI/ML skill set, backed by academic projects, hands-on datasets, and cloud fundamentals.</p></div>
        <div class="about-grid">
          <article class="panel reveal"><p>I’m pursuing a B.Tech in Computer Science and Engineering (AI &amp; ML) at Mohan Babu University. My interests include machine learning, deep learning, data analysis, cloud computing, and applying AI to meaningful challenges. I enjoy learning new tools, collaborating with a team, and turning concepts into working prototypes.</p></article>
          <div class="stats reveal">
            <div class="stat"><strong class="gradient">8.74</strong><span>B.Tech CGPA / 10</span></div>
            <div class="stat"><strong>2</strong><span>Featured AI/ML projects</span></div>
            <div class="stat"><strong>5 <small style="font-size:1rem">weeks</small></strong><span>Google Cloud internship</span></div>
            <div class="stat"><strong>2027</strong><span>Expected graduation</span></div>
          </div>
        </div>
      </div>
    </section>

    <section id="education">
      <div class="container">
        <div class="section-head reveal"><div><div class="kicker">02 / Education</div><h2>Academic journey</h2></div></div>
        <div class="panel timeline reveal">
          <div class="timeline-item"><div class="date">2023 – 2027</div><div><h3>B.Tech — Computer Science and Engineering (AI &amp; ML)</h3><p>Mohan Babu University, Tirupati · CGPA: 8.74 / 10</p></div></div>
          <div class="timeline-item"><div class="date">2021 – 2023</div><div><h3>Intermediate — MPC</h3><p>Sri Chaitanya Junior College, Tirupati · 88%</p></div></div>
          <div class="timeline-item"><div class="date">2020 – 2021</div><div><h3>SSC</h3><p>Ratnam Global School, Tirupati · 98%</p></div></div>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="container">
        <div class="section-head reveal"><div><div class="kicker">03 / Technical toolkit</div><h2>Skills I’m building with</h2></div><p class="section-desc">A snapshot of the tools and concepts listed in my resume. Progress bars are visual indicators, not formal proficiency ratings.</p></div>
        <div class="skill-groups">
          <article class="panel skill-group reveal"><h3><span class="skill-icon">⌘</span> Programming</h3><div class="chips"><span class="chip">Python</span><span class="chip">Java</span><span class="chip">SQL</span></div><div class="skill-bars"><div class="skill-row"><div class="skill-label"><span>Python</span><span>Focus</span></div><div class="bar"><span style="--level:78%"></span></div></div><div class="skill-row"><div class="skill-label"><span>Java</span><span>Learning</span></div><div class="bar"><span style="--level:58%"></span></div></div></div></article>
          <article class="panel skill-group reveal"><h3><span class="skill-icon">◉</span> AI &amp; Data</h3><div class="chips"><span class="chip">Machine Learning</span><span class="chip">Deep Learning</span><span class="chip">Pandas</span><span class="chip">NumPy</span><span class="chip">Data Preprocessing</span><span class="chip">Graph Neural Networks</span></div></article>
          <article class="panel skill-group reveal"><h3><span class="skill-icon">☁</span> Cloud &amp; Tools</h3><div class="chips"><span class="chip">Google Cloud Platform</span><span class="chip">MySQL</span><span class="chip">NoSQL fundamentals</span><span class="chip">Git</span><span class="chip">GitHub</span><span class="chip">Jupyter</span><span class="chip">VS Code</span></div></article>
        </div>
      </div>
    </section>

    <section id="projects">
      <div class="container">
        <div class="section-head reveal"><div><div class="kicker">04 / Selected work</div><h2>Projects with a purpose</h2></div><p class="section-desc">Academic projects exploring security analytics and AI-assisted disaster response.</p></div>
        <div class="projects">
          <article class="panel project reveal">
            <div class="project-top"><div class="project-symbol">⌁</div><h3>Intrusion Detection System using Deep Learning</h3><p>A deep-learning-based approach for identifying suspicious network activity and classifying network intrusions.</p></div>
            <div class="project-bottom"><div class="chips"><span class="chip">CNN / LSTM</span><span class="chip">NSL-KDD</span><span class="chip">CICIDS2017</span><span class="chip">UNSW-NB15</span></div><p class="project-note"><strong>Focus:</strong> Model evaluation using accuracy, precision, recall, ROC-AUC, and false-positive rate. Team Lead · Jan–Apr 2024.</p></div>
          </article>
          <article class="panel project reveal">
            <div class="project-top"><div class="project-symbol">⌖</div><h3>Adaptive Disaster Damage Assessment using Satellite Images</h3><p>An AI/ML project exploring image-analysis and deep-learning techniques to identify damaged structures after natural disasters.</p></div>
            <div class="project-bottom"><div class="chips"><span class="chip">Satellite Imagery</span><span class="chip">Computer Vision</span><span class="chip">Deep Learning</span><span class="chip">Disaster Response</span></div><p class="project-note"><strong>Goal:</strong> Support faster post-disaster assessment and help responders prioritize damage review. 2026.</p></div>
          </article>
        </div>
        <p style="color:var(--muted);font-size:.82rem;margin-top:15px">Note: Add GitHub repository links, dataset references, screenshots, and measured results when they are ready. No repository links or performance metrics were provided in the resume.</p>
      </div>
    </section>

    <section id="experience">
      <div class="container">
        <div class="section-head reveal"><div><div class="kicker">05 / Internship</div><h2>Cloud foundations</h2></div></div>
        <article class="panel internship reveal">
          <div class="cloud-mark">☁</div><div><h3>Google Cloud Computing Foundations</h3><div class="subline">EduSkills · 5-Week Internship</div><ul><li>Learned cloud computing fundamentals and service models.</li><li>Studied cloud infrastructure, storage, SQL/NoSQL databases, APIs, and Pub/Sub.</li><li>Explored VPC, IAM, networking, security, firewalls, and load balancing.</li><li>Gained exposure to BigQuery, Dataflow, Dataproc, Vertex AI, and AutoML.</li></ul></div>
        </article>
      </div>
    </section>

    <section id="highlights">
      <div class="container">
        <div class="section-head reveal"><div><div class="kicker">06 / Highlights</div><h2>Beyond the code</h2></div></div>
        <div class="achievement-grid">
          <article class="panel achievement reveal"><span class="symbol">✦</span><div><h3>Project experience</h3><p>Completed academic projects in AI, ML, and deep learning.</p></div></article>
          <article class="panel achievement reveal"><span class="symbol">☁</span><div><h3>Cloud learning</h3><p>Practical exposure to Google Cloud computing concepts through internship training.</p></div></article>
          <article class="panel achievement reveal"><span class="symbol">◎</span><div><h3>Team leadership</h3><p>Served as team lead for the intrusion detection project.</p></div></article>
          <article class="panel achievement reveal"><span class="symbol">◇</span><div><h3>Problem solving</h3><p>Worked with multiple datasets for machine learning and network intrusion detection.</p></div></article>
          <article class="panel achievement reveal"><span class="symbol">↗</span><div><h3>Communication</h3><p>Participated in academic presentations and technical learning activities.</p></div></article>
          <article class="panel achievement reveal"><span class="symbol">◎</span><div><h3>Languages</h3><p>English · Telugu · Hindi</p></div></article>
        </div>
      </div>
    </section>

    <section id="contact">
      <div class="container">
        <div class="contact-box reveal">
          <div><div class="kicker">07 / Get in touch</div><h2>Let’s connect and build.</h2><p>Open to discussing AI/ML projects, internship opportunities, and entry-level roles where I can learn, contribute, and grow.</p></div>
          <div class="contact-actions"><a class="btn btn-primary" href="mailto:mallularajreddy1456@gmail.com">✉ Email me</a><button class="btn btn-secondary" id="copyEmail" type="button">Copy email</button><a class="btn btn-secondary" href="tel:+918519966235">☎ Call</a></div>
        </div>
      </div>
    </section>
  </main>
  <footer><div class="container footer-inner"><span>© <span id="year"></span> M. Dhanush Kumar Reddy</span><span>Designed with curiosity · Built with HTML, CSS &amp; JavaScript</span></div></footer>
  <button class="to-top" id="toTop" aria-label="Back to top">↑</button>
  <script>
    const menuBtn=document.getElementById('menuBtn');
    const navLinks=document.getElementById('navLinks');
    menuBtn.addEventListener('click',()=>{const open=navLinks.classList.toggle('open');menuBtn.setAttribute('aria-expanded',String(open));menuBtn.textContent=open?'✕':'☰';});
    navLinks.querySelectorAll('a').forEach(a=>a.addEventListener('click',()=>{navLinks.classList.remove('open');menuBtn.setAttribute('aria-expanded','false');menuBtn.textContent='☰';}));
    document.getElementById('year').textContent=new Date().getFullYear();
    const observer=new IntersectionObserver(entries=>entries.forEach(entry=>{if(entry.isIntersecting){entry.target.classList.add('visible');observer.unobserve(entry.target);}}),{threshold:.12});
    document.querySelectorAll('.reveal').forEach(el=>observer.observe(el));
    const toTop=document.getElementById('toTop');
    window.addEventListener('scroll',()=>toTop.classList.toggle('show',window.scrollY>550),{passive:true});
    toTop.addEventListener('click',()=>window.scrollTo({top:0,behavior:'smooth'}));
    const sections=[...document.querySelectorAll('main section[id]')],links=[...navLinks.querySelectorAll('a')];
    const activeObserver=new IntersectionObserver(entries=>entries.forEach(entry=>{if(entry.isIntersecting){links.forEach(link=>link.classList.toggle('active',link.getAttribute('href')==='#'+entry.target.id));}}),{rootMargin:'-35% 0px -55% 0px'});
    sections.forEach(section=>activeObserver.observe(section));
    document.getElementById('copyEmail').addEventListener('click',async()=>{const button=document.getElementById('copyEmail');try{await navigator.clipboard.writeText('mallularajreddy1456@gmail.com');button.textContent='Email copied ✓';}catch{button.textContent='mallularajreddy1456@gmail.com';}setTimeout(()=>button.textContent='Copy email',2200);});
  </script>
</body>
</html>
