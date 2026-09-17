<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Naaz Parween — Profile Banner</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500;600;700&family=Space+Grotesk:wght@500;600;700&display=swap');

  :root{
    --bg: #060a14;
    --bg2: #0a0f1e;
    --panel: #0d1324;
    --panel-border: #1c2740;
    --purple: #a78bfa;
    --purple2: #7c6df2;
    --blue: #60a5fa;
    --cyan: #22d3ee;
    --orange: #f5a35c;
    --pink: #f472b6;
    --green: #4ade80;
    --text: #e6ebf5;
    --dim: #7c8aa8;
  }

  *{ box-sizing:border-box; margin:0; padding:0; }

  body{
    background: radial-gradient(circle at 80% 0%, #14203a 0%, var(--bg) 45%), var(--bg);
    font-family: 'Fira Code', monospace;
    color: var(--text);
    padding: 40px;
  }

  .banner{
    max-width: 1400px;
    margin: 0 auto;
    background: linear-gradient(180deg, var(--bg2) 0%, var(--bg) 100%);
    border: 1px solid var(--panel-border);
    border-radius: 18px;
    padding: 36px 44px 30px;
    position: relative;
    overflow: hidden;
  }

  .dots{ display:flex; gap:8px; margin-bottom: 22px; }
  .dot{ width:11px; height:11px; border-radius:50%; }
  .dot.r{ background:#ff5f57; } .dot.y{ background:#febc2e; } .dot.g{ background:#28c840; }

  .whoami{ color: var(--dim); font-size: 14px; margin-bottom: 26px; }
  .whoami span{ color: var(--cyan); }

  .hero{ display:flex; justify-content:space-between; gap: 40px; }
  .hero-left{ flex: 1.3; min-width: 320px; }
  .hero-right{ flex: 1; display:flex; align-items:flex-start; justify-content:flex-end; position:relative; min-height: 260px; }

  .iam{ font-family:'Space Grotesk', sans-serif; font-size: 30px; color:#fff; font-weight:600; margin-bottom: 6px;}

  .name{
    font-family:'Space Grotesk', sans-serif;
    font-size: 62px;
    font-weight: 700;
    line-height: 1.05;
    background: linear-gradient(90deg, var(--purple2), var(--blue));
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    display:inline-block;
    margin-bottom: 18px;
  }

  .wave{
    font-size: 40px; margin-left: 10px;
    display: inline-block;
    transform-origin: 70% 70%;
    animation: wave-hand 2.2s ease-in-out infinite;
  }
  @keyframes wave-hand{
    0%   { transform: rotate(0deg); }
    10%  { transform: rotate(18deg); }
    20%  { transform: rotate(-8deg); }
    30%  { transform: rotate(18deg); }
    40%  { transform: rotate(-8deg); }
    50%  { transform: rotate(10deg); }
    60%  { transform: rotate(0deg); }
    100% { transform: rotate(0deg); }
  }

  .welcome{
    color: var(--dim);
    font-size: 16px;
    margin-bottom: 14px;
    letter-spacing: 0.3px;
  }
  .welcome b{ color: #fff; font-weight: 500; }

  .roles{ color: var(--cyan); font-size: 17px; margin-bottom: 18px; letter-spacing: 0.3px; }
  .roles b{ color: var(--cyan); font-weight: 500; }
  .roles .sep{ color: var(--dim); margin: 0 10px; }

  .tagline{ color: var(--blue); font-size: 16px; }
  .tagline .cur{ display:inline-block; width:9px; height:18px; background:var(--blue); margin-left:4px; vertical-align:-3px; animation: blink 1s steps(1) infinite; }
  @keyframes blink{ 50%{opacity:0;} }

  .illustration{ width: 340px; height: 260px; position: relative; }
  .note{
    position:absolute; top:-6px; right:10px;
    font-family:'Space Grotesk', sans-serif; font-style: italic;
    color:#d9dfef; font-size: 13px; text-align:center; line-height:1.3;
    transform: rotate(-4deg);
  }
  .note::after{ content:"♥"; color: var(--pink); display:block; font-style:normal; }

  .sticky{
    position:absolute; width:150px; padding:12px 14px;
    background: var(--panel); border:1px solid var(--panel-border);
    border-radius:10px; font-size:12px; color:var(--blue); line-height:1.7;
  }
  .sticky.top{ top: 20px; left: 0; }
  .sticky.top div:first-child{ color: var(--dim); margin-bottom:2px; }

  .codeicon{
    position:absolute; top: 92px; left: 20px;
    width:78px; height:78px; border-radius:10px;
    background: var(--panel); border:1px solid var(--panel-border);
    display:flex; align-items:center; justify-content:center;
    color: var(--purple); font-size:22px; font-weight:600;
  }

  .avatar{
    position:absolute; bottom:0; right:0;
    width: 250px; height: 190px;
    background: linear-gradient(160deg, #1a2340, #0b1024);
    border-radius: 14px 14px 60px 14px;
    border: 1px solid var(--panel-border);
    display:flex; align-items:center; justify-content:center;
    color: var(--dim); font-size:13px; text-align:center; padding:14px;
  }

  .heart{ position:absolute; bottom: 210px; right: 40px; color: var(--pink); font-size: 26px; }

  .cards{ display:flex; gap: 22px; margin-top: 38px; }
  .card{ flex:1; background: var(--panel); border:1px solid var(--panel-border); border-radius: 14px; padding: 22px 24px; }
  .card h3{ font-family:'Space Grotesk', sans-serif; font-size:17px; font-weight:600; display:flex; align-items:center; gap:10px; margin-bottom: 10px; }
  .card h3 .arrow{ color: var(--dim); font-weight:400; margin-left:auto; }
  .card p{ color:#c3cbe0; font-size: 13.5px; line-height:1.5; margin-bottom: 10px; }
  .card .snippet{ color: var(--dim); font-size: 12.5px; margin-bottom: 16px; }
  .pills{ display:flex; flex-wrap:wrap; gap:8px; }
  .pill{ font-size: 12px; padding: 5px 12px; border-radius: 20px; border:1px solid; }

  .c1 h3{ color: var(--cyan); } .c2 h3{ color: var(--orange); } .c3 h3{ color: var(--purple); }

  .pill.blue{ color:var(--blue); border-color: rgba(96,165,250,0.4); background: rgba(96,165,250,0.08);}
  .pill.cyan{ color:var(--cyan); border-color: rgba(34,211,238,0.4); background: rgba(34,211,238,0.08);}
  .pill.green{ color:var(--green); border-color: rgba(74,222,128,0.4); background: rgba(74,222,128,0.08);}
  .pill.purple{ color:var(--purple); border-color: rgba(167,139,250,0.4); background: rgba(167,139,250,0.08);}
  .pill.orange{ color:var(--orange); border-color: rgba(245,163,92,0.4); background: rgba(245,163,92,0.08);}
  .pill.pink{ color:var(--pink); border-color: rgba(244,114,182,0.4); background: rgba(244,114,182,0.08);}

  .bottom{ display:flex; gap:22px; margin-top: 22px; }
  .panel{ background: var(--panel); border:1px solid var(--panel-border); border-radius: 14px; padding: 22px 26px; }
  .panel h4{ font-family:'Space Grotesk', sans-serif; font-size:16px; font-weight:600; display:flex; align-items:center; gap:10px; margin-bottom: 16px; }
  .panel.quick{ flex: 1; } .panel.quick h4{ color: var(--green); }
  .quick ul{ list-style:none; }
  .quick li{ display:flex; gap:10px; font-size: 13.5px; color:#c3cbe0; padding: 6px 0; }

  .panel.projects{ flex: 1.3; } .panel.projects h4{ color: var(--blue); }
  .proj{ display:flex; justify-content:space-between; align-items:center; padding: 12px 0; border-top: 1px solid var(--panel-border); }
  .proj:first-of-type{ border-top:none; }
  .proj-title{ font-size: 14.5px; color:#fff; margin-bottom:4px; }
  .proj-tags{ font-size: 12px; color: var(--dim); }
  .proj-arrow{ color: var(--dim); }

  .panel.code{ flex: 1; }
  .code-body{ font-size: 13px; line-height: 1.7; }
  .kw{ color: var(--pink); } .str{ color: var(--green); } .fn{ color: var(--blue); }

  .footer{ text-align:center; margin-top: 40px; }
  .footer .thanks{ font-family:'Space Grotesk', sans-serif; font-style: italic; color: var(--purple); font-size: 22px; }
  .footer .sub{ color: var(--dim); font-size: 13px; margin-top: 10px; letter-spacing: 1px; }
  .footer .sub .dot{ color: var(--purple); margin: 0 10px; }
</style>
</head>
<body>

<div class="banner">

  <div class="dots"><span class="dot r"></span><span class="dot y"></span><span class="dot g"></span></div>
  <div class="whoami">naaz@github:~$ <span>whoami</span></div>

  <div class="hero">
    <div class="hero-left">
      <div class="iam">Hi, I am<span class="wave">👋</span></div>
      <div class="name">Naaz Parween</div>
      <div class="welcome">Welcome to <b>my GitHub</b> ✨</div>
      <div class="roles">&lt; <b>fullstack dev</b> <span class="sep">|</span> <b>java developer</b> <span class="sep">|</span> <b>ai/ml enthusiast</b> /&gt;</div>
      <div class="tagline">Building ideas into reality with code...<span class="cur"></span></div>
    </div>

    <div class="hero-right">
      <div class="illustration">
        <div class="note">just a girl<br>who loves<br>code</div>
        <div class="sticky top"><div>Better Code</div><div>Better Tomorrow ♥</div></div>
        <div class="codeicon">&lt;/&gt;</div>
        <div class="heart">♥</div>
        <div class="avatar">// coding by lamplight<br>with a cat nearby 🐱</div>
      </div>
    </div>
  </div>

  <div class="cards">
    <div class="card c1">
      <h3><span class="icon">🌐</span> Full Stack Development <span class="arrow">→</span></h3>
      <p>From ideas to interactive web applications.</p>
      <div class="snippet">&lt; frontend + backend + databases /&gt;</div>
      <div class="pills">
        <span class="pill blue">React</span>
        <span class="pill cyan">Node.js</span>
        <span class="pill green">MongoDB</span>
        <span class="pill purple">Tailwind</span>
      </div>
    </div>
    <div class="card c2">
      <h3><span class="icon">☕</span> Java Developer <span class="arrow">→</span></h3>
      <p>Building scalable and reliable applications.</p>
      <div class="snippet">&lt; write • build • solve /&gt;</div>
      <div class="pills">
        <span class="pill orange">Java</span>
        <span class="pill blue">Spring Boot</span>
        <span class="pill cyan">REST APIs</span>
      </div>
    </div>
    <div class="card c3">
      <h3><span class="icon">🧠</span> AI / ML Enthusiast <span class="arrow">→</span></h3>
      <p>Exploring data, models, and intelligent solutions.</p>
      <div class="snippet">&lt; learn • experiment • grow /&gt;</div>
      <div class="pills">
        <span class="pill purple">Python</span>
        <span class="pill blue">NLP</span>
        <span class="pill cyan">Computer Vision</span>
        <span class="pill pink">ML</span>
      </div>
    </div>
  </div>

  <div class="bottom">
    <div class="panel quick">
      <h4>&gt;_ Quick Peek</h4>
      <ul>
        <li>🎓 B.Tech CSE @ Aliah University</li>
        <li>🚀 AI/ML Intern @ ISI, Kolkata</li>
        <li>💡 Learning Java, Spring Boot, React &amp; DSA</li>
        <li>🏆 SIH 2025 Team Leader</li>
        <li>⭐ Hacktoberfest 2024 Participant</li>
      </ul>
    </div>

    <div class="panel projects">
      <h4>📁 Featured Projects</h4>
      <div class="proj">
        <div><div class="proj-title">Patient Care Video Analytics</div><div class="proj-tags">Python • Computer Vision</div></div>
        <div class="proj-arrow">→</div>
      </div>
      <div class="proj">
        <div><div class="proj-title">AI Resume Job Analyzer</div><div class="proj-tags">Python • NLP • Streamlit</div></div>
        <div class="proj-arrow">→</div>
      </div>
      <div class="proj">
        <div><div class="proj-title">AgriCarbon MRV</div><div class="proj-tags">React • TypeScript • Tailwind</div></div>
        <div class="proj-arrow">→</div>
      </div>
    </div>

    <div class="panel code">
      <div class="dots"><span class="dot r"></span><span class="dot y"></span><span class="dot g"></span></div>
      <div class="code-body">
        <span class="kw">const</span> goals = [<br>
        &nbsp;&nbsp;<span class="str">"Build amazing projects"</span>,<br>
        &nbsp;&nbsp;<span class="str">"Keep learning"</span>,<br>
        &nbsp;&nbsp;<span class="str">"Create positive impact"</span><br>
        ];<br><br>
        <span class="fn">console</span>.log(<span class="str">"On it... 🚀"</span>);
      </div>
    </div>
  </div>

  <div class="footer">
    <div class="thanks">&gt; Thank you for visiting! ♥</div>
    <div class="sub">Keep coding <span class="dot">•</span> Keep growing <span class="dot">•</span> Always ♥</div>
  </div>

</div>

</body>
</html>
