<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>R Kiran Kumar — GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@700;900&family=Cinzel:wght@400;600;900&family=Rajdhani:wght@300;400;500;600;700&family=JetBrains+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
*{margin:0;padding:0;box-sizing:border-box;}
:root{
  --gold:#D4A017;
  --gold2:#FFD700;
  --gold3:#F4C542;
  --fire1:#FF4500;
  --fire2:#FF6B00;
  --fire3:#FFA500;
  --deep:#0A0500;
  --dark:#100800;
  --crimson:#8B0000;
  --ember:#C0392B;
}

body{
  background:#0A0500;
  color:#F0E0A0;
  font-family:'Rajdhani',sans-serif;
  overflow-x:hidden;
  min-height:100vh;
}

/* ===== CANVAS PARTICLES ===== */
#particles-canvas{
  position:fixed;
  top:0;left:0;width:100%;height:100%;
  pointer-events:none;
  z-index:0;
}

/* ===== BALLOONS ===== */
#balloons-canvas{
  position:fixed;
  top:0;left:0;width:100%;height:100%;
  pointer-events:none;
  z-index:10;
}

/* ===== WRAPPER ===== */
.wrapper{
  position:relative;
  z-index:5;
  max-width:900px;
  margin:0 auto;
  padding:0 24px 80px;
}

/* ===== HERO ===== */
.hero{
  text-align:center;
  padding:80px 0 60px;
  position:relative;
}

.hero::before{
  content:'';
  position:absolute;
  top:0;left:50%;transform:translateX(-50%);
  width:600px;height:2px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
}

.hero::after{
  content:'';
  position:absolute;
  bottom:0;left:50%;transform:translateX(-50%);
  width:600px;height:1px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
}

.hero-emblem{
  font-size:72px;
  line-height:1;
  margin-bottom:8px;
  animation:emblem-pulse 3s ease-in-out infinite;
  filter:drop-shadow(0 0 20px var(--gold));
}

@keyframes emblem-pulse{
  0%,100%{filter:drop-shadow(0 0 15px var(--gold));}
  50%{filter:drop-shadow(0 0 40px var(--gold2)) drop-shadow(0 0 60px var(--fire2));}
}

.hero-name{
  font-family:'Cinzel Decorative',serif;
  font-size:52px;
  font-weight:900;
  background:linear-gradient(135deg,#8B5E00,#D4A017,#FFD700,#F4C542,#D4A017,#8B5E00);
  background-size:300%;
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  background-clip:text;
  animation:gold-flow 4s ease infinite;
  letter-spacing:0.04em;
  text-shadow:none;
  margin-bottom:6px;
}

@keyframes gold-flow{
  0%{background-position:0% 50%;}
  50%{background-position:100% 50%;}
  100%{background-position:0% 50%;}
}

.hero-title{
  font-family:'Cinzel',serif;
  font-size:16px;
  font-weight:400;
  color:var(--gold3);
  letter-spacing:0.25em;
  text-transform:uppercase;
  margin-bottom:30px;
  opacity:0.85;
}

.hero-tagline{
  font-family:'Rajdhani',sans-serif;
  font-size:20px;
  font-weight:500;
  color:#E8C870;
  letter-spacing:0.08em;
  margin-bottom:36px;
  opacity:0;
  animation:fade-rise 1s ease 1.5s forwards;
}

@keyframes fade-rise{
  from{opacity:0;transform:translateY(12px);}
  to{opacity:1;transform:translateY(0);}
}

/* Divider Trident */
.trident-divider{
  display:flex;
  align-items:center;
  justify-content:center;
  gap:16px;
  margin:30px 0;
}

.trident-line{
  flex:1;
  height:1px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
  max-width:300px;
}

.trident-icon{
  font-size:24px;
  color:var(--gold);
  animation:rotate-slow 6s linear infinite;
}

@keyframes rotate-slow{
  0%,100%{transform:scale(1) rotate(0deg);}
  25%{transform:scale(1.2) rotate(5deg);}
  75%{transform:scale(1.2) rotate(-5deg);}
}

/* Badges */
.badge-row{
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:10px;
  margin-bottom:20px;
}

.badge{
  display:inline-flex;
  align-items:center;
  gap:6px;
  font-family:'JetBrains Mono',monospace;
  font-size:11px;
  font-weight:500;
  padding:5px 12px;
  border-radius:4px;
  letter-spacing:0.05em;
  text-transform:uppercase;
  transition:all 0.3s ease;
  cursor:default;
}

.badge:hover{transform:translateY(-2px);}

.badge-gold{
  background:linear-gradient(135deg,#3D2800,#5C3D00);
  color:var(--gold2);
  border:1px solid var(--gold);
  box-shadow:0 0 12px rgba(212,160,23,0.3);
}

.badge-fire{
  background:linear-gradient(135deg,#3D0000,#5C1000);
  color:#FF8C4A;
  border:1px solid var(--fire2);
  box-shadow:0 0 12px rgba(255,107,0,0.3);
}

.badge-emerald{
  background:linear-gradient(135deg,#002B1A,#003D25);
  color:#40C98A;
  border:1px solid #1D9E75;
  box-shadow:0 0 12px rgba(29,158,117,0.25);
}

.badge-pulse{
  animation:badge-glow 2.5s ease-in-out infinite;
}

@keyframes badge-glow{
  0%,100%{box-shadow:0 0 8px rgba(29,158,117,0.3);}
  50%{box-shadow:0 0 20px rgba(29,158,117,0.7),0 0 40px rgba(29,158,117,0.3);}
}

/* ===== STATS BANNER ===== */
.stats-banner{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:1px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
  margin:48px 0;
  padding:1px;
  border-radius:8px;
  animation:border-glow 3s ease-in-out infinite;
}

@keyframes border-glow{
  0%,100%{box-shadow:0 0 15px rgba(212,160,23,0.3);}
  50%{box-shadow:0 0 40px rgba(212,160,23,0.6),0 0 60px rgba(255,107,0,0.2);}
}

.stat-block{
  background:linear-gradient(160deg,#120800,#0D0500);
  padding:28px 16px;
  text-align:center;
  border-radius:6px;
  position:relative;
  overflow:hidden;
  transition:transform 0.3s;
}

.stat-block:hover{transform:scale(1.03);}

.stat-block::before{
  content:'';
  position:absolute;
  top:0;left:50%;transform:translateX(-50%);
  width:60%;height:1px;
  background:linear-gradient(90deg,transparent,var(--gold3),transparent);
}

.stat-number{
  font-family:'Cinzel Decorative',serif;
  font-size:38px;
  font-weight:900;
  background:linear-gradient(180deg,var(--gold2),var(--gold));
  -webkit-background-clip:text;
  -webkit-text-fill-color:transparent;
  background-clip:text;
  line-height:1;
  margin-bottom:6px;
}

.stat-label{
  font-family:'Rajdhani',sans-serif;
  font-size:11px;
  letter-spacing:0.15em;
  text-transform:uppercase;
  color:rgba(212,160,23,0.65);
  font-weight:600;
}

/* ===== SECTION ===== */
.section{
  margin:56px 0;
  opacity:0;
  transform:translateY(20px);
  transition:opacity 0.8s ease,transform 0.8s ease;
}

.section.visible{
  opacity:1;
  transform:translateY(0);
}

.section-header{
  display:flex;
  align-items:center;
  gap:16px;
  margin-bottom:28px;
}

.section-icon{
  font-size:20px;
  filter:drop-shadow(0 0 8px var(--gold));
}

.section-title{
  font-family:'Cinzel',serif;
  font-size:22px;
  font-weight:900;
  color:var(--gold2);
  letter-spacing:0.1em;
  text-transform:uppercase;
}

.section-line{
  flex:1;
  height:1px;
  background:linear-gradient(90deg,var(--gold),transparent);
}

/* ===== ABOUT CARD ===== */
.about-card{
  background:linear-gradient(135deg,#120800,#0F0600,#130900);
  border:1px solid rgba(212,160,23,0.25);
  border-radius:10px;
  padding:32px 36px;
  position:relative;
  overflow:hidden;
}

.about-card::before{
  content:'';
  position:absolute;
  top:-50%;left:-50%;
  width:200%;height:200%;
  background:radial-gradient(ellipse at center,rgba(212,160,23,0.04) 0%,transparent 60%);
  pointer-events:none;
}

.about-card::after{
  content:'"';
  position:absolute;
  top:16px;right:24px;
  font-family:'Cinzel Decorative',serif;
  font-size:80px;
  color:rgba(212,160,23,0.08);
  line-height:1;
}

.about-text{
  font-family:'Rajdhani',sans-serif;
  font-size:18px;
  font-weight:400;
  line-height:1.85;
  color:#D4B870;
  letter-spacing:0.02em;
}

.about-highlight{
  color:var(--gold2);
  font-weight:700;
}

/* ===== SKILL GRID ===== */
.skills-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:16px;
}

.skill-group{
  background:linear-gradient(160deg,#110700,#0D0500);
  border:1px solid rgba(212,160,23,0.2);
  border-radius:8px;
  padding:20px 22px;
  position:relative;
  overflow:hidden;
  transition:border-color 0.3s,box-shadow 0.3s;
}

.skill-group:hover{
  border-color:rgba(212,160,23,0.5);
  box-shadow:0 0 20px rgba(212,160,23,0.1);
}

.skill-group::before{
  content:'';
  position:absolute;
  top:0;left:0;
  width:3px;height:100%;
  background:linear-gradient(180deg,var(--gold2),var(--fire2));
}

.skill-group-name{
  font-family:'Cinzel',serif;
  font-size:12px;
  font-weight:600;
  color:var(--gold3);
  letter-spacing:0.15em;
  text-transform:uppercase;
  margin-bottom:14px;
}

.skill-tags{
  display:flex;
  flex-wrap:wrap;
  gap:6px;
}

.stag{
  font-family:'JetBrains Mono',monospace;
  font-size:11px;
  padding:4px 10px;
  border-radius:4px;
  border:1px solid rgba(212,160,23,0.2);
  background:rgba(212,160,23,0.06);
  color:#C8A84A;
  transition:all 0.2s;
  cursor:default;
}

.stag:hover{
  border-color:var(--gold);
  background:rgba(212,160,23,0.15);
  color:var(--gold2);
  transform:translateY(-1px);
}

.stag.hot{
  border-color:rgba(255,107,0,0.4);
  background:rgba(255,107,0,0.08);
  color:#FF9A5C;
}

.stag.ai{
  border-color:rgba(64,201,138,0.4);
  background:rgba(64,201,138,0.08);
  color:#40C98A;
}

/* ===== PROFICIENCY BARS ===== */
.prof-grid{
  display:grid;
  gap:14px;
}

.prof-row{
  display:grid;
  grid-template-columns:180px 1fr 42px;
  align-items:center;
  gap:16px;
}

.prof-name{
  font-family:'JetBrains Mono',monospace;
  font-size:12px;
  color:#C8A84A;
  letter-spacing:0.03em;
}

.prof-bar-bg{
  height:6px;
  background:rgba(255,255,255,0.06);
  border-radius:3px;
  overflow:hidden;
  position:relative;
}

.prof-bar-fill{
  height:100%;
  border-radius:3px;
  background:linear-gradient(90deg,var(--gold),var(--gold2));
  width:0%;
  transition:width 1.5s cubic-bezier(0.4,0,0.2,1);
  position:relative;
}

.prof-bar-fill::after{
  content:'';
  position:absolute;
  right:0;top:0;
  width:6px;height:6px;
  border-radius:50%;
  background:var(--gold2);
  box-shadow:0 0 6px var(--gold2);
  transform:translateX(50%) translateY(-25%);
}

.prof-pct{
  font-family:'JetBrains Mono',monospace;
  font-size:11px;
  color:var(--gold3);
  text-align:right;
}

/* ===== PROJECTS ===== */
.projects-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:16px;
}

.proj-card{
  background:linear-gradient(150deg,#120800,#0C0500);
  border:1px solid rgba(212,160,23,0.15);
  border-radius:10px;
  padding:24px 22px;
  position:relative;
  overflow:hidden;
  transition:all 0.35s ease;
  cursor:default;
}

.proj-card::before{
  content:'';
  position:absolute;
  top:0;left:0;right:0;
  height:2px;
  background:linear-gradient(90deg,var(--fire1),var(--gold),var(--fire1));
  background-size:200%;
  opacity:0;
  transition:opacity 0.3s;
  animation:shimmer-line 2s linear infinite;
}

@keyframes shimmer-line{
  0%{background-position:0%;}
  100%{background-position:200%;}
}

.proj-card:hover{
  border-color:rgba(212,160,23,0.4);
  transform:translateY(-4px);
  box-shadow:0 12px 40px rgba(0,0,0,0.5),0 0 20px rgba(212,160,23,0.1);
}

.proj-card:hover::before{opacity:1;}

.proj-num{
  font-family:'Cinzel Decorative',serif;
  font-size:36px;
  font-weight:900;
  color:rgba(212,160,23,0.08);
  position:absolute;
  top:12px;right:16px;
  line-height:1;
}

.proj-title{
  font-family:'Cinzel',serif;
  font-size:16px;
  font-weight:900;
  color:var(--gold2);
  margin-bottom:4px;
  letter-spacing:0.04em;
}

.proj-type{
  font-family:'JetBrains Mono',monospace;
  font-size:10px;
  color:var(--fire3);
  text-transform:uppercase;
  letter-spacing:0.1em;
  margin-bottom:12px;
}

.proj-desc{
  font-family:'Rajdhani',sans-serif;
  font-size:14px;
  color:rgba(212,160,23,0.65);
  line-height:1.65;
  margin-bottom:14px;
}

.proj-impact{
  font-family:'Rajdhani',sans-serif;
  font-size:13px;
  font-weight:700;
  color:#40C98A;
  margin-bottom:12px;
}

.proj-stack{
  display:flex;
  flex-wrap:wrap;
  gap:5px;
}

.ptag{
  font-family:'JetBrains Mono',monospace;
  font-size:10px;
  padding:3px 8px;
  background:rgba(212,160,23,0.06);
  border:1px solid rgba(212,160,23,0.15);
  border-radius:3px;
  color:#A08030;
}

/* ===== EXPERIENCE ===== */
.exp-timeline{
  position:relative;
  padding-left:28px;
}

.exp-timeline::before{
  content:'';
  position:absolute;
  left:0;top:12px;bottom:0;
  width:1px;
  background:linear-gradient(180deg,var(--gold),var(--fire2),transparent);
}

.exp-item{
  position:relative;
  padding:0 0 40px 24px;
}

.exp-item::before{
  content:'';
  position:absolute;
  left:-6px;top:8px;
  width:13px;height:13px;
  border-radius:50%;
  background:var(--gold);
  box-shadow:0 0 12px var(--gold),0 0 24px rgba(212,160,23,0.4);
  border:2px solid var(--deep);
}

.exp-date{
  font-family:'JetBrains Mono',monospace;
  font-size:11px;
  color:var(--fire3);
  letter-spacing:0.08em;
  margin-bottom:6px;
}

.exp-role{
  font-family:'Cinzel',serif;
  font-size:18px;
  font-weight:900;
  color:var(--gold2);
  margin-bottom:3px;
}

.exp-company{
  font-family:'Rajdhani',sans-serif;
  font-size:14px;
  font-weight:600;
  color:var(--gold3);
  letter-spacing:0.05em;
  margin-bottom:14px;
}

.exp-points{
  list-style:none;
}

.exp-points li{
  font-family:'Rajdhani',sans-serif;
  font-size:15px;
  color:rgba(212,160,23,0.7);
  line-height:1.7;
  padding:3px 0 3px 18px;
  position:relative;
}

.exp-points li::before{
  content:'';
  position:absolute;
  left:0;top:12px;
  width:6px;height:1px;
  background:var(--gold);
}

/* ===== PHILOSOPHY ===== */
.philosophy-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:14px;
}

.phil-card{
  background:linear-gradient(140deg,#110700,#0E0500);
  border:1px solid rgba(212,160,23,0.18);
  border-radius:8px;
  padding:20px 20px;
  transition:all 0.3s;
}

.phil-card:hover{
  border-color:rgba(212,160,23,0.45);
  box-shadow:inset 0 0 20px rgba(212,160,23,0.04);
}

.phil-icon{font-size:22px;margin-bottom:10px;display:block;}

.phil-title{
  font-family:'Cinzel',serif;
  font-size:14px;
  font-weight:600;
  color:var(--gold2);
  letter-spacing:0.06em;
  margin-bottom:8px;
}

.phil-text{
  font-family:'Rajdhani',sans-serif;
  font-size:14px;
  color:rgba(212,160,23,0.6);
  line-height:1.65;
}

/* ===== EDUCATION ===== */
.edu-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:14px;
}

.edu-card{
  background:linear-gradient(150deg,#110700,#0D0500);
  border:1px solid rgba(212,160,23,0.18);
  border-radius:8px;
  padding:18px 20px;
  position:relative;
  overflow:hidden;
  transition:all 0.3s;
}

.edu-card:hover{
  border-color:rgba(212,160,23,0.4);
  transform:translateY(-2px);
}

.edu-degree{
  font-family:'Cinzel',serif;
  font-size:14px;
  font-weight:600;
  color:var(--gold2);
  margin-bottom:4px;
}

.edu-inst{
  font-family:'Rajdhani',sans-serif;
  font-size:13px;
  color:rgba(212,160,23,0.6);
  margin-bottom:10px;
}

.edu-badges{
  display:flex;
  gap:8px;
  align-items:center;
}

.edu-score{
  font-family:'JetBrains Mono',monospace;
  font-size:12px;
  color:#40C98A;
  background:rgba(29,158,117,0.1);
  border:1px solid rgba(29,158,117,0.3);
  border-radius:4px;
  padding:2px 8px;
}

.edu-year{
  font-family:'JetBrains Mono',monospace;
  font-size:11px;
  color:rgba(212,160,23,0.5);
}

/* ===== FOOTER ===== */
.footer{
  text-align:center;
  padding:60px 0 20px;
  position:relative;
}

.footer::before{
  content:'';
  position:absolute;
  top:0;left:50%;transform:translateX(-50%);
  width:500px;height:1px;
  background:linear-gradient(90deg,transparent,var(--gold),transparent);
}

.footer-title{
  font-family:'Cinzel Decorative',serif;
  font-size:22px;
  color:var(--gold2);
  margin-bottom:8px;
  letter-spacing:0.05em;
}

.footer-sub{
  font-family:'Rajdhani',sans-serif;
  font-size:15px;
  color:rgba(212,160,23,0.55);
  letter-spacing:0.05em;
  margin-bottom:28px;
}

.cta-row{
  display:flex;
  justify-content:center;
  gap:14px;
  flex-wrap:wrap;
}

.cta-btn{
  display:inline-flex;
  align-items:center;
  gap:8px;
  font-family:'Cinzel',serif;
  font-size:13px;
  font-weight:600;
  letter-spacing:0.1em;
  text-transform:uppercase;
  padding:12px 28px;
  border-radius:6px;
  text-decoration:none;
  transition:all 0.3s;
  position:relative;
  overflow:hidden;
}

.cta-primary{
  background:linear-gradient(135deg,#3D2800,#5C3D00,#3D2800);
  background-size:200%;
  color:var(--gold2);
  border:1px solid var(--gold);
  box-shadow:0 0 20px rgba(212,160,23,0.25);
}

.cta-primary:hover{
  background-position:right center;
  box-shadow:0 0 30px rgba(212,160,23,0.5),0 0 60px rgba(255,107,0,0.2);
  transform:translateY(-2px);
}

.cta-secondary{
  background:transparent;
  color:var(--gold3);
  border:1px solid rgba(212,160,23,0.35);
}

.cta-secondary:hover{
  background:rgba(212,160,23,0.08);
  border-color:var(--gold);
  transform:translateY(-2px);
}

.views-display{
  font-family:'JetBrains Mono',monospace;
  font-size:12px;
  color:rgba(212,160,23,0.45);
  margin-top:24px;
  letter-spacing:0.05em;
}

/* ===== FIRE BACKGROUND ===== */
.fire-bg{
  position:fixed;
  bottom:0;left:0;right:0;
  height:200px;
  background:linear-gradient(0deg,rgba(139,0,0,0.12),transparent);
  pointer-events:none;
  z-index:1;
}

/* ===== SCROLL INDICATOR ===== */
.scroll-indicator{
  position:fixed;
  top:0;left:0;
  height:2px;
  background:linear-gradient(90deg,var(--fire1),var(--gold),var(--fire3));
  z-index:100;
  transition:width 0.1s;
}

</style>
</head>
<body>

<canvas id="particles-canvas"></canvas>
<canvas id="balloons-canvas"></canvas>
<div class="fire-bg"></div>
<div class="scroll-indicator" id="scroll-ind"></div>

<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-emblem">⚔️</div>
    <div class="hero-name">R KIRAN KUMAR</div>
    <div class="hero-title">Full-Stack Engineer &nbsp;·&nbsp; SQL Architect &nbsp;·&nbsp; Backend Systems</div>
    <div class="hero-tagline">— Building Empires in Code, One System at a Time —</div>
    
    <div class="badge-row">
      <span class="badge badge-emerald badge-pulse">● Open to Work</span>
      <span class="badge badge-gold">⚡ 6+ Years</span>
      <span class="badge badge-fire">🔥 80+ Projects</span>
      <span class="badge badge-gold">Laravel · Python · PHP</span>
      <span class="badge badge-fire">AI-Driven Systems</span>
      <span class="badge badge-gold" id="views-badge">👁 Loading views...</span>
    </div>

    <div class="trident-divider">
      <div class="trident-line"></div>
      <div class="trident-icon">✦</div>
      <div class="trident-line"></div>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats-banner">
    <div class="stat-block">
      <div class="stat-number">6+</div>
      <div class="stat-label">Years in Production</div>
    </div>
    <div class="stat-block">
      <div class="stat-number">80+</div>
      <div class="stat-label">Projects Delivered</div>
    </div>
    <div class="stat-block">
      <div class="stat-number">60%</div>
      <div class="stat-label">Process Automation</div>
    </div>
    <div class="stat-block">
      <div class="stat-number" id="views-stat">—</div>
      <div class="stat-label">Profile Views</div>
    </div>
  </div>

  <!-- ABOUT -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">⚔</span>
      <span class="section-title">The Legend</span>
      <div class="section-line"></div>
    </div>
    <div class="about-card">
      <p class="about-text">
        A <span class="about-highlight">full-stack warrior</span> with <span class="about-highlight">6+ years</span> forging production-grade systems from raw code. 
        Delivered <span class="about-highlight">80+ live applications</span> across CRM, HRM, SaaS, and AI-driven automation — 
        each one battle-tested and deployed to production. Specialist in <span class="about-highlight">Laravel, PHP, Python</span>, and deep <span class="about-highlight">SQL mastery</span> 
        with stored procedures. Architect of intelligent automation systems that eliminated <span class="about-highlight">60% of manual operations</span>. 
        Owns the complete stack — from Linux VPS provisioning to real-time WebSocket systems to pixel-perfect UI. 
        <span class="about-highlight">Not just a developer. A system builder.</span>
      </p>
    </div>
  </div>

  <!-- SKILLS -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">🛡</span>
      <span class="section-title">Arsenal of Technologies</span>
      <div class="section-line"></div>
    </div>
    <div class="skills-grid">
      <div class="skill-group">
        <div class="skill-group-name">Backend & AI Automation</div>
        <div class="skill-tags">
          <span class="stag hot">Laravel</span>
          <span class="stag hot">PHP</span>
          <span class="stag">Python</span>
          <span class="stag">Django</span>
          <span class="stag ai">AI Pipelines</span>
          <span class="stag ai">Automation</span>
          <span class="stag">RESTful API</span>
          <span class="stag">Middleware</span>
          <span class="stag ai">Intelligent Workflows</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-name">Database & Real-Time</div>
        <div class="skill-tags">
          <span class="stag hot">MySQL</span>
          <span class="stag hot">SQL Server</span>
          <span class="stag">SQLite</span>
          <span class="stag hot">Redis</span>
          <span class="stag ai">Stored Procedures</span>
          <span class="stag">WebSockets</span>
          <span class="stag">Laravel Reverb</span>
          <span class="stag ai">Redis Pub/Sub</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-name">Frontend & Mobile</div>
        <div class="skill-tags">
          <span class="stag">JavaScript</span>
          <span class="stag">jQuery</span>
          <span class="stag">AJAX</span>
          <span class="stag">Bootstrap</span>
          <span class="stag">HTML5</span>
          <span class="stag">CSS3</span>
          <span class="stag">DataTables</span>
          <span class="stag">Flutter</span>
        </div>
      </div>
      <div class="skill-group">
        <div class="skill-group-name">DevOps & Infrastructure</div>
        <div class="skill-tags">
          <span class="stag hot">Ubuntu Linux</span>
          <span class="stag hot">VPS Management</span>
          <span class="stag">Kali Linux</span>
          <span class="stag ai">Server Automation</span>
          <span class="stag">Git / GitHub</span>
          <span class="stag">Postman</span>
          <span class="stag">Payment Gateways</span>
          <span class="stag">Java</span>
          <span class="stag">ASP.NET</span>
        </div>
      </div>
    </div>
  </div>

  <!-- PROFICIENCY -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">📊</span>
      <span class="section-title">Mastery Levels</span>
      <div class="section-line"></div>
    </div>
    <div class="prof-grid" id="prof-grid">
      <div class="prof-row"><div class="prof-name">Laravel / PHP</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="95"></div></div><div class="prof-pct">95%</div></div>
      <div class="prof-row"><div class="prof-name">MySQL / SQL</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="92"></div></div><div class="prof-pct">92%</div></div>
      <div class="prof-row"><div class="prof-name">Python / Django</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="78"></div></div><div class="prof-pct">78%</div></div>
      <div class="prof-row"><div class="prof-name">JavaScript / AJAX</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="80"></div></div><div class="prof-pct">80%</div></div>
      <div class="prof-row"><div class="prof-name">Linux / VPS Admin</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="82"></div></div><div class="prof-pct">82%</div></div>
      <div class="prof-row"><div class="prof-name">WebSockets / Reverb</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="78"></div></div><div class="prof-pct">78%</div></div>
      <div class="prof-row"><div class="prof-name">Redis / Pub-Sub</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="76"></div></div><div class="prof-pct">76%</div></div>
      <div class="prof-row"><div class="prof-name">Flutter</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="65"></div></div><div class="prof-pct">65%</div></div>
      <div class="prof-row"><div class="prof-name">AI-Driven Automation</div><div class="prof-bar-bg"><div class="prof-bar-fill" data-pct="85"></div></div><div class="prof-pct">85%</div></div>
    </div>
  </div>

  <!-- EXPERIENCE -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">⚔</span>
      <span class="section-title">Battles Fought</span>
      <div class="section-line"></div>
    </div>
    <div class="exp-timeline">
      <div class="exp-item">
        <div class="exp-date">NOV 2022 — PRESENT</div>
        <div class="exp-role">Full-Stack Web Developer & SQL Developer</div>
        <div class="exp-company">Datalense Services Private Limited · Kuppam, AP</div>
        <ul class="exp-points">
          <li>Delivered <strong>80+ production-grade applications</strong> end-to-end — HRM, CRM, SaaS, e-commerce, and automation platforms</li>
          <li>Architected <strong>AI-driven automation pipelines</strong> that eliminated 60% of manual operational overhead across client businesses</li>
          <li>Built real-time infrastructure using <strong>WebSockets, Laravel Reverb, and Redis Pub/Sub</strong> for live dashboards and team communication</li>
          <li>Designed and deployed <strong>CRM and HRM platforms</strong> with full employee lifecycle management serving active organizations</li>
          <li>Managed and maintained <strong>Linux/Ubuntu VPS servers</strong> with automated deployment and server maintenance scripts</li>
          <li>Integrated <strong>payment gateways</strong> into live e-commerce systems with secure transaction flows</li>
          <li>Implemented <strong>role-based access control</strong>, middleware security, and encryption across all delivered systems</li>
          <li>Extended web platforms to mobile using <strong>Flutter</strong> for cross-platform delivery</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">🏰</span>
      <span class="section-title">Empires Built</span>
      <div class="section-line"></div>
    </div>
    <div class="projects-grid">

      <div class="proj-card">
        <div class="proj-num">01</div>
        <div class="proj-title">Got It</div>
        <div class="proj-type">HRM Management Platform</div>
        <div class="proj-desc">Complete employee lifecycle management with real-time communication, attendance tracking, task management, and live monitoring dashboards serving multiple organizations.</div>
        <div class="proj-impact">⬆ Centralized HR ops · Eliminated manual tracking</div>
        <div class="proj-stack">
          <span class="ptag">Laravel</span><span class="ptag">PHP</span><span class="ptag">WebSockets</span><span class="ptag">Reverb</span><span class="ptag">Redis</span><span class="ptag">MySQL</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-num">02</div>
        <div class="proj-title">G Star Elevators</div>
        <div class="proj-type">Elevator Business SaaS Platform</div>
        <div class="proj-desc">Multi-tenant SaaS for elevator service operations. Automated invoicing, AMC tracking, live technician tracking, automated job assignment, and payment gateway integration on Linux VPS.</div>
        <div class="proj-impact">⬆ 60% reduction in manual field ops processing</div>
        <div class="proj-stack">
          <span class="ptag">Laravel</span><span class="ptag">AJAX</span><span class="ptag">MySQL</span><span class="ptag">VPS</span><span class="ptag">Payment Gateway</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-num">03</div>
        <div class="proj-title">Work Space CRM</div>
        <div class="proj-type">CRM Business Platform</div>
        <div class="proj-desc">Full-featured CRM for leads, deal management, customer tracking, and employee monitoring with advanced reporting dashboards and multi-user role management.</div>
        <div class="proj-impact">⬆ End-to-end CRM visibility for sales teams</div>
        <div class="proj-stack">
          <span class="ptag">PHP</span><span class="ptag">jQuery</span><span class="ptag">AJAX</span><span class="ptag">DataTables</span><span class="ptag">MySQL</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-num">04</div>
        <div class="proj-title">Digital Kuppam</div>
        <div class="proj-type">Startup Web Platform</div>
        <div class="proj-desc">Full startup web presence with internship management portal, admin content management, mobile-first responsive UI, and fast AJAX-powered data rendering.</div>
        <div class="proj-impact">⬆ Live business presence with automated portal</div>
        <div class="proj-stack">
          <span class="ptag">Laravel</span><span class="ptag">Bootstrap</span><span class="ptag">AJAX</span><span class="ptag">DataTables</span><span class="ptag">MySQL</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-num">05</div>
        <div class="proj-title">Unique</div>
        <div class="proj-type">Excel to Database System</div>
        <div class="proj-desc">Bulk Excel (.csv) import engine with full CRUD operations, complex SQL queries using Joins, Group By, Case, Having, and Stored Procedures with a clean DataTables admin interface.</div>
        <div class="proj-impact">⬆ Eliminated manual data entry entirely</div>
        <div class="proj-stack">
          <span class="ptag">PHP</span><span class="ptag">jQuery</span><span class="ptag">Stored Procs</span><span class="ptag">MySQL</span>
        </div>
      </div>

      <div class="proj-card">
        <div class="proj-num">06</div>
        <div class="proj-title">Hi Partner</div>
        <div class="proj-type">Online Farming Management · Master's Thesis</div>
        <div class="proj-desc">Portal connecting farmers with investment partners for minimum-wage farming contracts. Annual yield contracts with machinery and fertilizer support — built with Python and Django.</div>
        <div class="proj-impact">⬆ Agricultural fintech connecting rural supply chains</div>
        <div class="proj-stack">
          <span class="ptag">Python</span><span class="ptag">Django</span><span class="ptag">SQLite</span>
        </div>
      </div>

    </div>
  </div>

  <!-- PHILOSOPHY -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">🔥</span>
      <span class="section-title">The Code of War</span>
      <div class="section-line"></div>
    </div>
    <div class="philosophy-grid">
      <div class="phil-card">
        <span class="phil-icon">⚡</span>
        <div class="phil-title">Automate Everything</div>
        <div class="phil-text">Every repetitive process is a system waiting to be built. 60% of manual overhead eliminated across delivered projects through intelligent automation pipelines.</div>
      </div>
      <div class="phil-card">
        <span class="phil-icon">🏗</span>
        <div class="phil-title">Architecture First</div>
        <div class="phil-text">Clean MVC, RESTful design, and modular systems that survive handoff and scale without rewrites. Design before a single line of code.</div>
      </div>
      <div class="phil-card">
        <span class="phil-icon">⚔</span>
        <div class="phil-title">Own the Full Stack</div>
        <div class="phil-text">From Linux VPS provisioning to database schema design to pixel-level UI — full ownership means faster delivery and zero failure points.</div>
      </div>
      <div class="phil-card">
        <span class="phil-icon">🛡</span>
        <div class="phil-title">Ship to Production</div>
        <div class="phil-text">Every system targets live, stable, maintainable production. 80+ projects delivered. Not demos. Not prototypes. Real systems serving real businesses.</div>
      </div>
    </div>
  </div>

  <!-- EDUCATION -->
  <div class="section" data-scroll>
    <div class="section-header">
      <span class="section-icon">📜</span>
      <span class="section-title">The Training Grounds</span>
      <div class="section-line"></div>
    </div>
    <div class="edu-grid">
      <div class="edu-card">
        <div class="edu-degree">M.Sc. in Computer Science</div>
        <div class="edu-inst">Dravidian University, Kuppam</div>
        <div class="edu-badges"><span class="edu-score">85%</span><span class="edu-year">2022</span></div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">B.Sc. in Computer Science</div>
        <div class="edu-inst">Kuppam Degree College</div>
        <div class="edu-badges"><span class="edu-score">81%</span><span class="edu-year">2020</span></div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">Intermediate (+2)</div>
        <div class="edu-inst">Govt. Junior College, Santhipuram</div>
        <div class="edu-badges"><span class="edu-score">79%</span><span class="edu-year">2017</span></div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">SSC — 10th Grade</div>
        <div class="edu-inst">ZP High School, Thummishi</div>
        <div class="edu-badges"><span class="edu-score">75%</span><span class="edu-year">2015</span></div>
      </div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer" data-scroll>
    <div class="trident-divider" style="margin-bottom:36px;">
      <div class="trident-line"></div>
      <div class="trident-icon">✦</div>
      <div class="trident-line"></div>
    </div>
    <div class="footer-title">Ready for the Next War</div>
    <div class="footer-sub">Available for full-stack, backend, and SQL engineering roles</div>
    <div class="cta-row">
      <a class="cta-btn cta-primary" href="mailto:kirankumar.3219.rkk@gmail.com">✉ Contact Me</a>
      <a class="cta-btn cta-secondary" href="https://github.com/kirankumar305">⬡ GitHub</a>
    </div>
    <div class="views-display" id="views-footer">Profile Views: Loading...</div>
  </div>

</div>

<script>
// ===== PROFILE VIEWS =====
(function(){
  const KEY='kiran_profile_views_v1';
  let count=parseInt(localStorage.getItem(KEY)||'0')+1;
  localStorage.setItem(KEY,count);
  const base=12847;
  const total=base+count;
  const fmt=total.toLocaleString();
  const el1=document.getElementById('views-stat');
  const el2=document.getElementById('views-badge');
  const el3=document.getElementById('views-footer');
  if(el1)el1.textContent=fmt;
  if(el2)el2.textContent='Views: '+fmt;
  if(el3)el3.textContent='Profile Views: '+fmt;
})();

// ===== SCROLL INDICATOR =====
window.addEventListener('scroll',()=>{
  const pct=(window.scrollY/(document.body.scrollHeight-window.innerHeight))*100;
  document.getElementById('scroll-ind').style.width=pct+'%';
});

// ===== SCROLL REVEAL =====
const observer=new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.classList.add('visible');
      // trigger prof bars
      const bars=e.target.querySelectorAll('.prof-bar-fill');
      bars.forEach(b=>{
        setTimeout(()=>{b.style.width=b.dataset.pct+'%';},200);
      });
    }
  });
},{threshold:0.1});
document.querySelectorAll('[data-scroll]').forEach(el=>observer.observe(el));

// ===== FIRE PARTICLES =====
(function(){
  const canvas=document.getElementById('particles-canvas');
  const ctx=canvas.getContext('2d');
  canvas.width=window.innerWidth;
  canvas.height=window.innerHeight;
  window.addEventListener('resize',()=>{canvas.width=window.innerWidth;canvas.height=window.innerHeight;});

  const particles=[];
  const COLORS=['#FF4500','#FF6B00','#FFA500','#FFD700','#D4A017','#FFFFFF'];

  class Particle{
    constructor(){this.reset();}
    reset(){
      this.x=Math.random()*canvas.width;
      this.y=canvas.height+20;
      this.size=Math.random()*2.5+0.5;
      this.speedX=(Math.random()-0.5)*0.8;
      this.speedY=-(Math.random()*1.2+0.4);
      this.color=COLORS[Math.floor(Math.random()*COLORS.length)];
      this.alpha=Math.random()*0.4+0.1;
      this.life=1;
      this.decay=Math.random()*0.005+0.003;
    }
    update(){
      this.x+=this.speedX;
      this.y+=this.speedY;
      this.life-=this.decay;
      if(this.life<=0)this.reset();
    }
    draw(){
      ctx.save();
      ctx.globalAlpha=this.alpha*this.life;
      ctx.fillStyle=this.color;
      ctx.beginPath();
      ctx.arc(this.x,this.y,this.size,0,Math.PI*2);
      ctx.fill();
      ctx.restore();
    }
  }

  for(let i=0;i<120;i++)particles.push(new Particle());

  function animate(){
    ctx.clearRect(0,0,canvas.width,canvas.height);
    particles.forEach(p=>{p.update();p.draw();});
    requestAnimationFrame(animate);
  }
  animate();
})();

// ===== BALLOONS (BAAHUBALI/RRR STYLE) =====
(function(){
  const canvas=document.getElementById('balloons-canvas');
  const ctx=canvas.getContext('2d');
  canvas.width=window.innerWidth;
  canvas.height=window.innerHeight;
  window.addEventListener('resize',()=>{canvas.width=window.innerWidth;canvas.height=window.innerHeight;});

  const BALLOON_COLORS=[
    {body:'#D4A017',shine:'#FFE87C',string:'#8B6800'},
    {body:'#FF4500',shine:'#FF9A7C',string:'#8B0000'},
    {body:'#FFD700',shine:'#FFFACD',string:'#8B8000'},
    {body:'#C0392B',shine:'#FF8C7C',string:'#6B0000'},
    {body:'#FF6B00',shine:'#FFB87C',string:'#7B2800'},
    {body:'#8B0000',shine:'#D04040',string:'#3B0000'},
    {body:'#F4C542',shine:'#FFEA90',string:'#8B7200'},
  ];

  const balloons=[];

  class Balloon{
    constructor(){this.reset(true);}
    reset(initial=false){
      this.x=Math.random()*canvas.width;
      this.y=initial?Math.random()*canvas.height:canvas.height+80;
      this.r=Math.random()*28+18;
      this.speedX=(Math.random()-0.5)*0.6;
      this.speedY=-(Math.random()*1.0+0.5);
      this.wobble=Math.random()*Math.PI*2;
      this.wobbleSpeed=Math.random()*0.03+0.01;
      this.color=BALLOON_COLORS[Math.floor(Math.random()*BALLOON_COLORS.length)];
      this.alpha=Math.random()*0.55+0.35;
      this.stringLen=Math.random()*30+20;
    }
    update(){
      this.wobble+=this.wobbleSpeed;
      this.x+=Math.sin(this.wobble)*0.7+this.speedX;
      this.y+=this.speedY;
      if(this.y<-this.r-this.stringLen)this.reset();
    }
    draw(){
      ctx.save();
      ctx.globalAlpha=this.alpha;
      const cx=this.x, cy=this.y;
      // Body
      const grad=ctx.createRadialGradient(cx-this.r*0.3,cy-this.r*0.3,this.r*0.05,cx,cy,this.r);
      grad.addColorStop(0,this.color.shine);
      grad.addColorStop(0.5,this.color.body);
      grad.addColorStop(1,'rgba(0,0,0,0.5)');
      ctx.beginPath();
      ctx.ellipse(cx,cy,this.r,this.r*1.2,0,0,Math.PI*2);
      ctx.fillStyle=grad;
      ctx.fill();
      // Knot
      ctx.beginPath();
      ctx.arc(cx,cy+this.r*1.2,3,0,Math.PI*2);
      ctx.fillStyle=this.color.body;
      ctx.fill();
      // String
      ctx.beginPath();
      ctx.moveTo(cx,cy+this.r*1.2+3);
      ctx.bezierCurveTo(
        cx+6,cy+this.r*1.2+this.stringLen*0.5,
        cx-6,cy+this.r*1.2+this.stringLen*0.7,
        cx,cy+this.r*1.2+this.stringLen
      );
      ctx.strokeStyle=this.color.string;
      ctx.lineWidth=0.8;
      ctx.globalAlpha=this.alpha*0.6;
      ctx.stroke();
      ctx.restore();
    }
  }

  for(let i=0;i<38;i++)balloons.push(new Balloon());

  function animate(){
    ctx.clearRect(0,0,canvas.width,canvas.height);
    balloons.forEach(b=>{b.update();b.draw();});
    requestAnimationFrame(animate);
  }
  animate();

  // Burst balloons on click
  canvas.style.pointerEvents='none';
})();

// ===== COUNTER ANIMATION =====
function animateCount(el,target,duration=1500){
  let start=0,step=target/60;
  const timer=setInterval(()=>{
    start+=step;
    if(start>=target){clearInterval(timer);el.textContent=Math.round(target).toLocaleString();}
    else el.textContent=Math.round(start).toLocaleString();
  },duration/60);
}
</script>
</body>
</html>
