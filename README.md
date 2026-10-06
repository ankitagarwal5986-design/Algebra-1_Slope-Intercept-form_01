<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Sopaan · Unit 5: Linear Functions, Slopes &amp; Regression</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,500;9..144,700&family=Source+Sans+3:wght@400;600;700&family=IBM+Plex+Mono:wght@500;600&display=swap">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.css">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/katex.min.js"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.16.8/dist/contrib/auto-render.min.js"></script>
<style>
  html,body{margin:0;} img{max-width:100%;} [hidden]{display:none !important;}
  :root{
    --navy:#16264A; --navy-2:#1F3B6B; --gold:#C79A3E; --gold-soft:#F3E7C9;
    --paper:#FBF9F4; --paper-2:#F1EAD8; --card:#FFFFFF;
    --ink:#211E1A; --ink-soft:#655D4C; --rule:#E4DCC8;
    --success:#2E8B57; --success-soft:#E1F2E7;
    --danger:#BF4B45; --danger-soft:#FAE3E1;
    --locked:#C7BEA9; --focus:#1F3B6B;
    --accent-text:#1F3B6B; --retry-text:#8A661F;
    color-scheme:light;
  }
  @media (prefers-color-scheme: dark){
    :root:not([data-theme="light"]){
      --navy:#0E1830; --navy-2:#16264A; --gold:#E0B75B; --gold-soft:#3A2F16;
      --paper:#141210; --paper-2:#1C1914; --card:#1C1914;
      --ink:#EDE7DA; --ink-soft:#B2A996; --rule:#3A342A;
      --success:#7BC79A; --success-soft:#1B2E22;
      --danger:#E38884; --danger-soft:#331D1B;
      --locked:#4A4436; --focus:#E0B75B;
      --accent-text:#E0B75B; --retry-text:#E0B75B;
      color-scheme:dark;
    }
  }
  :root[data-theme="dark"]{
    --navy:#0E1830; --navy-2:#16264A; --gold:#E0B75B; --gold-soft:#3A2F16;
    --paper:#141210; --paper-2:#1C1914; --card:#1C1914;
    --ink:#EDE7DA; --ink-soft:#B2A996; --rule:#3A342A;
    --success:#7BC79A; --success-soft:#1B2E22;
    --danger:#E38884; --danger-soft:#331D1B;
    --locked:#4A4436; --focus:#E0B75B;
    --accent-text:#E0B75B; --retry-text:#E0B75B;
    color-scheme:dark;
  }
  *{box-sizing:border-box;}
  body{background:var(--paper); color:var(--ink); font-family:'Source Sans 3',-apple-system,sans-serif; margin:0; padding:0;}
  h1,h2,h3{font-family:'Fraunces',Georgia,serif; text-wrap:balance; margin:0;}
  header.brand{
    background:linear-gradient(155deg,var(--navy) 0%, var(--navy-2) 100%);
    color:#F4EFDF; padding-block:calc(20px + env(safe-area-inset-top,0px)) 18px; padding-inline:20px;
  }
  .brand-row{display:flex; align-items:center; gap:12px; max-width:960px; margin:0 auto;}
  .crest{
    width:42px; height:42px; border-radius:10px; background:var(--gold); color:var(--navy);
    display:flex; align-items:center; justify-content:center; font-family:'Fraunces',serif; font-weight:700; font-size:18px; flex-shrink:0;
  }
  .brand-name{font-size:12px; letter-spacing:.08em; text-transform:uppercase; color:var(--gold); font-weight:700;}
  .series-name{font-size:19px; font-weight:700; font-family:'Fraunces',serif;}
  .chapter-eyebrow{max-width:960px; margin:14px auto 0; font-size:12px; letter-spacing:.06em; text-transform:uppercase; color:#AEB9D6;}
  .chapter-title{font-size:26px; max-width:960px; margin:2px auto 0;}
  .chapter-sub{font-size:14px; color:var(--gold); font-weight:700; max-width:960px; margin:3px auto 0;}
  .chapter-progress{max-width:960px; margin:14px auto 0; display:flex; align-items:center; gap:10px;}
  .cp-track{flex:1; height:6px; border-radius:99px; background:rgba(255,255,255,.18); overflow:hidden;}
  .cp-fill{height:100%; background:var(--gold); border-radius:99px; transition:width .3s ease;}
  .cp-label{font-size:11.5px; color:#CFD7EA; white-space:nowrap;}
  .who-row{max-width:960px; margin:12px auto 0; display:flex; flex-wrap:wrap; gap:8px; align-items:center;}
  .mode-pill{font-family:inherit; font-size:12.5px; font-weight:700; color:var(--navy); background:var(--gold); border:none; border-radius:99px; padding:6px 14px; cursor:pointer; display:inline-flex; align-items:center; gap:6px;}
  .who{display:inline-flex; flex-wrap:wrap; align-items:center; gap:6px; font-size:12.5px; color:#CFD7EA;}
  .who b{color:#F4EFDF;}
  .who button{font-family:inherit; font-size:12px; font-weight:700; color:#F4EFDF; background:rgba(255,255,255,.12); border:1px solid rgba(255,255,255,.22); border-radius:99px; padding:5px 11px; cursor:pointer;}
  .tabbar{position:sticky; top:env(safe-area-inset-top,0px); z-index:15; background:var(--paper); border-bottom:1px solid var(--rule); overflow-x:auto; white-space:nowrap;}
  .tabbar-inner{max-width:960px; margin:0 auto; display:flex; padding-inline:16px;}
  .tab-btn{font-family:inherit; font-size:13.5px; font-weight:600; color:var(--ink-soft); background:none; border:none; padding:13px 14px; cursor:pointer; position:relative; flex-shrink:0;}
  .tab-btn.active{color:var(--accent-text);}
  .tab-btn.active::after{content:''; position:absolute; left:10px; right:10px; bottom:0; height:3px; background:var(--gold); border-radius:3px 3px 0 0;}
  .tab-count{font-size:11px; color:var(--ink-soft); margin-left:4px;}
  .sec-sub{max-width:960px; margin:0 auto; padding:10px 16px 0; font-size:12.5px; font-weight:700; color:var(--accent-text);}
  .slide-progress{max-width:960px; margin:0 auto; padding:10px 16px 0; display:flex; align-items:center; gap:10px;}
  .sp-track{flex:1; height:5px; border-radius:99px; background:var(--rule); overflow:hidden;}
  .sp-fill{height:100%; background:var(--accent-text); border-radius:99px; transition:width .3s ease;}
  .sp-label{font-size:12px; color:var(--ink-soft); white-space:nowrap; font-weight:600;}
  .wrap{max-width:960px; margin:0 auto; padding:16px 16px calc(150px + env(safe-area-inset-bottom,0px));}
  .qcard{background:var(--card); border:1px solid var(--rule); border-radius:14px; padding:20px;}
  .qhead{display:flex; align-items:flex-start; gap:12px; margin-bottom:12px;}
  .qnum{width:32px; height:32px; border-radius:8px; background:var(--gold-soft); color:var(--accent-text); display:flex; align-items:center; justify-content:center; font-weight:700; font-family:'Fraunces',serif; flex-shrink:0; font-size:14px;}
  .qtext{font-size:15.5px; line-height:1.6; flex:1;}
  .qtag{font-size:10.5px; color:var(--gold); background:var(--gold-soft); padding:2px 7px; border-radius:99px; font-weight:700; margin-left:6px; white-space:nowrap;}
  .graph-container{display:flex; justify-content:center; align-items:center; margin:16px 0; background:var(--paper-2); padding:14px; border-radius:12px; border:1px solid var(--rule);}
  .graph-svg{max-width:300px; width:100%; height:auto; display:block; background:#fff; border-radius:8px; box-shadow:0 2px 6px rgba(0,0,0,0.06);}
  .options{display:flex; flex-direction:column; gap:8px; margin-top:12px;}
  .opt{display:flex; align-items:center; gap:10px; padding:11px 12px; border:1.5px solid var(--rule); border-radius:10px; cursor:pointer; font-size:15px; background:var(--paper); flex-wrap:wrap;}
  .opt-l{font-family:'IBM Plex Mono',monospace; font-size:13px; font-weight:600; color:var(--ink-soft);}
  .opt-t{flex:1; min-width:0;}
  .opt.is-correct{border-color:var(--success); background:var(--success-soft);}
  .opt.is-wrong{border-color:var(--danger); background:var(--danger-soft);}
  .opt.is-chosen:not(.is-correct):not(.is-wrong){border-color:var(--navy-2); background:var(--gold-soft);}
  .opt.locked{cursor:not-allowed;}
  .steps{display:flex; flex-direction:column; gap:12px;}
  .step-line{font-size:14.5px; line-height:1.9; background:var(--paper); border:1px dashed var(--rule); border-radius:10px; padding:10px 14px;}
  .blank-input{font-family:'IBM Plex Mono',monospace; font-size:15px; border:1.5px solid var(--rule); border-radius:6px; padding:4px 8px; width:130px; background:var(--card); color:var(--ink); margin:0 3px;}
  .blank-input.expr{width:180px; max-width:100%;}
  .blank-input:focus, .blank-input.active-focus{outline:none; border-color:var(--focus); box-shadow:0 0 0 3px var(--gold-soft);}
  .blank-input.is-correct{border-color:var(--success); background:var(--success-soft);}
  .blank-input.is-wrong{border-color:var(--danger); background:var(--danger-soft);}
  .reveal-note{font-size:12px; color:var(--danger); padding-left:4px; margin-top:-2px;}
  .solution{margin-top:16px; border:1px solid var(--rule); border-left:4px solid var(--gold); background:var(--paper-2); border-radius:10px; padding:12px 16px;}
  .sol-h{font-family:'Fraunces',Georgia,serif; font-weight:700; font-size:14px; color:var(--accent-text); margin-bottom:6px;}
  .sol-line{font-size:14px; line-height:1.7;}
  .feedback{font-size:13.5px; padding:10px 12px; border-radius:9px; margin-top:14px; display:none;}
  .feedback.show{display:block;}
  .feedback.ok{background:var(--success-soft); color:var(--success);}
  .feedback.retry{background:var(--gold-soft); color:var(--retry-text);}
  .feedback.reveal,.feedback.err{background:var(--danger-soft); color:var(--danger);}
  .attempts-dots{display:inline-flex; gap:4px; margin-left:4px; vertical-align:middle;}
  .attempts-dots span{width:6px; height:6px; border-radius:50%; background:var(--ink-soft); opacity:.3; display:inline-block;}
  .attempts-dots span.used{opacity:1; background:var(--danger);}
  .quiz-hint{font-size:12.5px; color:var(--ink-soft); background:var(--paper-2); border-radius:8px; padding:8px 12px; margin-bottom:12px;}

  .navbar{position:fixed; left:0; right:0; bottom:0; z-index:30; background:var(--paper); border-top:1px solid var(--rule); padding:10px 16px calc(10px + env(safe-area-inset-bottom,0px));}
  .navbar-inner{max-width:960px; margin:0 auto; display:flex; gap:8px; align-items:center;}
  .btn{font-family:inherit; font-size:13.5px; font-weight:700; padding:10px 14px; border-radius:9px; border:1.5px solid var(--rule); background:var(--card); color:var(--ink); cursor:pointer;}
  .btn:hover{border-color:var(--navy-2);}
  .btn:disabled{opacity:.4; cursor:not-allowed;}
  .btn-primary{background:var(--navy-2); color:#fff; border-color:var(--navy-2);}
  .navbar .spacer{flex:1;}
  
  .fab{position:fixed; right:16px; bottom:calc(66px + env(safe-area-inset-bottom,0px)); background:var(--gold); color:var(--navy); border:none; border-radius:999px; padding:10px 15px; font-weight:700; font-size:13px; display:flex; align-items:center; gap:6px; cursor:pointer; box-shadow:0 6px 16px rgba(0,0,0,.18); z-index:35;}
  .fab-scratch{position:fixed; left:16px; bottom:calc(66px + env(safe-area-inset-bottom,0px)); background:var(--navy-2); color:#fff; border:none; border-radius:999px; padding:10px 15px; font-weight:700; font-size:13px; display:flex; align-items:center; gap:6px; cursor:pointer; box-shadow:0 6px 16px rgba(0,0,0,.18); z-index:35;}
  .fab-badge{background:rgba(255,255,255,.55); border-radius:99px; padding:1px 7px; font-size:11px;}
  
  .scratchpad-overlay{position:fixed; inset:0; background:rgba(14,24,48,0.7); z-index:60; display:none; align-items:center; justify-content:center; padding:12px;}
  .scratchpad-overlay.show{display:flex;}
  .scratchpad-modal{background:var(--card); width:min(860px, 100%); height:82vh; border-radius:16px; display:flex; flex-direction:column; overflow:hidden; border:2px solid var(--rule); box-shadow:0 12px 32px rgba(0,0,0,0.3);}
  .sp-toolbar{background:var(--paper-2); padding:10px 14px; display:flex; align-items:center; gap:8px; border-bottom:1px solid var(--rule); flex-wrap:wrap;}
  .sp-title{font-family:'Fraunces',serif; font-size:16px; font-weight:700; color:var(--accent-text); margin-right:auto;}
  .sp-tool-btn{background:var(--card); border:1.5px solid var(--rule); border-radius:8px; padding:6px 12px; font-size:12.5px; font-weight:700; cursor:pointer;}
  .sp-tool-btn.active{background:var(--gold); color:var(--navy); border-color:var(--gold);}
  .sp-canvas-wrap{flex:1; position:relative; background:#FFFFFF; cursor:crosshair; touch-action:none;}
  #scratchCanvas{width:100%; height:100%; display:block;}
  
  .math-keypad{
    position:fixed; left:0; right:0; bottom:calc(56px + env(safe-area-inset-bottom,0px));
    background:var(--card); border-top:2px solid var(--gold); border-bottom:1px solid var(--rule);
    padding:8px 12px; z-index:32; box-shadow:0 -6px 20px rgba(0,0,0,0.12);
    display:none; transition:transform 0.2s ease;
  }
  .math-keypad.show{display:block;}
  .keypad-inner{max-width:760px; margin:0 auto; display:flex; flex-direction:column; gap:6px;}
  .keypad-header{display:flex; justify-content:space-between; align-items:center; font-size:12px; font-weight:700; color:var(--ink-soft); padding:0 4px;}
  .keypad-grid{display:grid; grid-template-columns:repeat(10, 1fr); gap:6px;}
  .kbtn{
    font-family:'IBM Plex Mono',monospace; font-size:14px; font-weight:700; height:38px;
    background:var(--paper); border:1.5px solid var(--rule); border-radius:8px; color:var(--ink);
    cursor:pointer; display:flex; align-items:center; justify-content:center; user-select:none;
  }
  .kbtn:hover{background:var(--paper-2); border-color:var(--navy-2);}
  .kbtn:active{transform:scale(0.96);}
  .kbtn-action{background:var(--gold-soft); color:var(--accent-text); font-family:inherit;}
  .kbtn-back{background:var(--danger-soft); color:var(--danger);}
  
  .overlay{position:fixed; inset:0; background:rgba(20,18,14,.45); z-index:50; display:none; align-items:flex-end; justify-content:center;}
  .overlay.show{display:flex;}
  .palette{background:var(--card); width:min(520px,100%); max-height:78vh; overflow-y:auto; border-radius:18px 18px 0 0; padding:18px; border:1px solid var(--rule); border-bottom:none;}
  @media (min-width:640px){ .overlay{align-items:center;} .palette{border-radius:18px; border-bottom:1px solid var(--rule); max-height:74vh;} }
  .palette-head{display:flex; align-items:center; justify-content:space-between; margin-bottom:6px;}
  .palette-close{background:none; border:none; font-size:20px; color:var(--ink-soft); cursor:pointer;}
  .chip-grid{display:grid; grid-template-columns:repeat(auto-fill,minmax(44px,1fr)); gap:7px; margin-top:12px;}
  .chip{border:1.5px solid var(--rule); border-radius:8px; padding:7px 2px; text-align:center; font-family:'IBM Plex Mono',monospace; font-size:12px; font-weight:600; cursor:pointer; background:var(--paper);}
  .chip[data-status="correct"]{border-color:var(--success); background:var(--success-soft); color:var(--success);}
  .chip[data-status="revealed"]{border-color:var(--danger); background:var(--danger-soft); color:var(--danger);}
  .chip[data-status="skipped"]{border-color:var(--gold); background:var(--gold-soft); color:var(--retry-text);}
  .chip[data-status="locked"]{border-color:var(--rule); color:var(--locked); cursor:not-allowed; background:var(--paper-2);}
  .chip[data-status="current"]{outline:2px solid var(--navy-2); outline-offset:1px;}
  .toast{position:fixed; left:50%; bottom:calc(140px + env(safe-area-inset-bottom,0px)); transform:translateX(-50%); background:var(--ink); color:var(--paper); padding:9px 16px; border-radius:99px; font-size:13px; opacity:0; pointer-events:none; transition:opacity .25s ease; z-index:70;}
  .toast.show{opacity:1;}
  .login-card{max-width:460px; margin:14px auto 0; background:var(--card); border:1px solid var(--rule); border-radius:16px; padding:22px;}
  .fld{display:flex; flex-direction:column; gap:5px; margin-bottom:12px;}
  .fld label{font-size:12px; font-weight:700; text-transform:uppercase; color:var(--ink-soft);}
  .fld input{font-size:15px; padding:10px 12px; border:1.5px solid var(--rule); border-radius:9px; background:var(--paper);}
  .fld-row{display:grid; grid-template-columns:1fr 1fr; gap:10px;}
  .mode-pick{display:flex; flex-direction:column; gap:14px; padding:8px 0 24px;}
  .mode-card{background:var(--card); border:1.5px solid var(--rule); border-radius:16px; padding:22px; cursor:pointer;}
  .done-card{text-align:center; padding:36px 20px;}
  .score-pills{display:flex; gap:10px; justify-content:center; flex-wrap:wrap; margin:16px 0;}
  .score-pill{padding:8px 16px; border-radius:99px; font-size:13px; font-weight:700;}
  .review-row{border:1px solid var(--rule); border-radius:10px; padding:11px 13px; margin-bottom:10px; text-align:left;}
  .review-tag{font-size:11.5px; font-weight:700; margin-bottom:4px; display:block;}
  .review-tag.ok{color:var(--success);} .review-tag.bad{color:var(--danger);} .review-tag.na{color:var(--ink-soft);}
  .review-q{font-size:13.5px; margin-bottom:6px; color:var(--ink-soft);}
  .review-ans{font-size:13px; margin-bottom:2px;}
  footer.brandfoot{max-width:960px; margin:14px auto 0; padding:0 16px calc(110px + env(safe-area-inset-bottom,0px)); text-align:center; font-size:12px; color:var(--ink-soft);}
</style>
</head>
<body>
<header class="brand">
  <div class="brand-row">
    <div class="crest">BM</div>
    <div>
      <div class="brand-name">Brain &amp; Mind Academy</div>
      <div class="series-name">Sopaan <span style="font-weight:400;font-size:14px;color:#CFD7EA;">Interactive Practice Series</span></div>
    </div>
  </div>
  <div class="chapter-eyebrow">Algebra I · Unit 5 Summary Assessment</div>
  <div class="chapter-title">Linear Equations, Slopes &amp; Regression</div>
  <div class="chapter-sub">Worksheets A5 – F5 · All 90 Questions with Scratchpad &amp; Math Keypad</div>
  <div class="chapter-progress">
    <div class="cp-track"><div class="cp-fill" id="cpFill"></div></div>
    <div class="cp-label" id="cpLabel">0% complete</div>
  </div>
  <div class="who-row"><button class="mode-pill" id="modePill" hidden>Choose a mode</button><span class="who" id="whoBar" hidden></span></div>
</header>

<nav class="tabbar"><div class="tabbar-inner" id="tabbar"></div></nav>
<div class="sec-sub" id="secSub"></div>
<div class="slide-progress"><div class="sp-track"><div class="sp-fill" id="spFill"></div></div><div class="sp-label" id="spLabel">Loading...</div></div>
<div class="wrap" id="wrap"></div>
<footer class="brandfoot">Brain &amp; Mind Academy · Sopaan Practice Series · Unit 5 Assessment (A5–F5)</footer>

<div class="navbar"><div class="navbar-inner" id="navbarInner"></div></div>

<button class="fab-scratch" id="scratchFab" title="Open Rough Work Scratchpad"><span>✏️ Scratchpad</span></button>
<button class="fab" id="paletteFab"><span>Questions</span><span class="fab-badge" id="fabBadge">0</span></button>

<div class="math-keypad" id="mathKeypad">
  <div class="keypad-inner">
    <div class="keypad-header">
      <span>🔢 Mathematical Expression Keypad</span>
      <button class="sp-tool-btn" id="closeKeypadBtn" style="padding:2px 8px;font-size:11px;">Hide ✕</button>
    </div>
    <div class="keypad-grid">
      <button class="kbtn" data-key="x">x</button>
      <button class="kbtn" data-key="y">y</button>
      <button class="kbtn" data-key="m">m</button>
      <button class="kbtn" data-key="b">b</button>
      <button class="kbtn" data-key="/">/</button>
      <button class="kbtn" data-key="(">(</button>
      <button class="kbtn" data-key=")">)</button>
      <button class="kbtn" data-key="=">=</button>
      <button class="kbtn kbtn-back" data-action="backspace">⌫</button>
      <button class="kbtn kbtn-action" data-action="clear">C</button>
      
      <button class="kbtn" data-key="7">7</button>
      <button class="kbtn" data-key="8">8</button>
      <button class="kbtn" data-key="9">9</button>
      <button class="kbtn" data-key="+">+</button>
      <button class="kbtn" data-key="-">−</button>
      <button class="kbtn" data-key="4">4</button>
      <button class="kbtn" data-key="5">5</button>
      <button class="kbtn" data-key="6">6</button>
      <button class="kbtn" data-key="*">∗</button>
      <button class="kbtn" data-key="^">^</button>

      <button class="kbtn" data-key="1">1</button>
      <button class="kbtn" data-key="2">2</button>
      <button class="kbtn" data-key="3">3</button>
      <button class="kbtn" data-key="0">0</button>
      <button class="kbtn" data-key=".">.</button>
      <button class="kbtn kbtn-action" data-key=" " style="grid-column: span 5;">Space ␣</button>
    </div>
  </div>
</div>

<div class="scratchpad-overlay" id="scratchOverlay">
  <div class="scratchpad-modal">
    <div class="sp-toolbar">
      <span class="sp-title">✏️ Rough Work Scratchpad</span>
      <button class="sp-tool-btn active" id="spToolPen">Pen</button>
      <button class="sp-tool-btn" id="spToolEraser">Eraser</button>
      <button class="sp-tool-btn" id="spToolClear">Clear Canvas</button>
      <button class="sp-tool-btn" id="spToolClose" style="background:var(--danger-soft);color:var(--danger);margin-left:auto;">Close ✕</button>
    </div>
    <div class="sp-canvas-wrap" id="spCanvasWrap">
      <canvas id="scratchCanvas"></canvas>
    </div>
  </div>
</div>

<div class="overlay" id="overlay">
  <div class="palette" role="dialog" aria-label="Question palette">
    <div class="palette-head"><h2>Question Palette</h2><button class="palette-close" id="paletteClose">&times;</button></div>
    <div class="chip-grid" id="paletteBody"></div>
  </div>
</div>
<div class="toast" id="toast"></div>

<script>
(function(){
"use strict";

/* Audio Synthesizer */
var audioCtx=null;
function ensureAudio(){ if(!audioCtx){ try{ audioCtx=new (window.AudioContext||window.webkitAudioContext)(); }catch(e){} } return audioCtx; }
function playTone(freqs,dur,type){
  var ctx=ensureAudio(); if(!ctx) return;
  try{
    var t0=ctx.currentTime;
    freqs.forEach(function(f,i){
      var o=ctx.createOscillator(), g=ctx.createGain();
      o.type=type||'sine'; o.frequency.value=f;
      var start=t0+i*dur;
      g.gain.setValueAtTime(0.0001,start);
      g.gain.exponentialRampToValueAtTime(0.16,start+0.02);
      g.gain.exponentialRampToValueAtTime(0.0001,start+dur);
      o.connect(g); g.connect(ctx.destination);
      o.start(start); o.stop(start+dur+0.02);
    });
  }catch(e){}
}
function playSuccess(){ playTone([523.25,659.25,783.99],0.11,'sine'); }
function playWrong(){ playTone([220,185],0.14,'square'); }
function playReveal(){ playTone([300,220],0.16,'triangle'); }

/* String Sanitizer & Evaluators */
function cleanText(s){
  return String(s||'').replace(/\+\]/g, '');
}
function norm(s){
  return String(s===undefined||s===null?'':s).trim().toLowerCase().replace(/\s+/g,'')
    .replace(/[×∗]/g,'*').replace(/[–—−]/g,'-').replace(/\^/g,'');
}
function parseNum(s){
  if(s===undefined||s===null) return null;
  var t=String(s).trim().replace(/,/g,'').replace(/[−–—]/g,'-').replace(/\s+/g,''); if(t==='') return null;
  var neg=false; if(t[0]==='-'){neg=true;t=t.slice(1);}
  var m=t.match(/^(\d+)\/(\d+)$/);
  if(m){ var v=parseInt(m[1],10)/parseInt(m[2],10); return neg?-v:v; }
  if(/^\d+(\.\d+)?$/.test(t)){ var v2=parseFloat(t); return neg?-v2:v2; }
  return null;
}
function exprPrep(s){
  return String(s).replace(/\s+/g,'').replace(/[×∗·]/g,'*').replace(/÷/g,'/').replace(/[−–—]/g,'-')
    .replace(/²/g,'^2').replace(/³/g,'^3');
}
function exprCompile(src){
  var s=exprPrep(src), i=0, toks=[];
  while(i<s.length){
    var ch=s[i];
    if(/[0-9.]/.test(ch)){ var j=i; while(j<s.length && /[0-9.]/.test(s[j])) j++; toks.push({k:'n',v:parseFloat(s.slice(i,j))}); i=j; continue; }
    if(/[a-zA-Z]/.test(ch)){ toks.push({k:'v',v:ch}); i++; continue; }
    if('+-*/^()'.indexOf(ch)>=0){ toks.push({k:ch}); i++; continue; }
    return null;
  }
  var out=[];
  for(var t=0;t<toks.length;t++){
    var a=toks[t], b=out[out.length-1];
    if(b && (b.k==='n'||b.k==='v'||b.k===')') && (a.k==='n'||a.k==='v'||a.k==='(')) out.push({k:'*'});
    out.push(a);
  }
  var p=0;
  function peek(){ return out[p]; }
  function parseE(){ var n=parseT(); while(peek() && (peek().k==='+'||peek().k==='-')){ var o=out[p++].k, r=parseT(); n=(function(l,r,o){return function(e){ return o==='+'?l(e)+r(e):l(e)-r(e); };})(n,r,o); } return n; }
  function parseT(){ var n=parseU(); while(peek() && (peek().k==='*'||peek().k==='/')){ var o=out[p++].k, r=parseU(); n=(function(l,r,o){return function(e){ return o==='*'?l(e)*r(e):l(e)/r(e); };})(n,r,o); } return n; }
  function parseU(){ if(peek() && peek().k==='-'){ p++; var u=parseU(); return function(e){ return -u(e); }; } if(peek() && peek().k==='+'){ p++; return parseU(); } return parseP(); }
  function parseP(){ var b=parseA(); if(peek() && peek().k==='^'){ p++; var x=parseU(); return function(e){ return Math.pow(b(e),x(e)); }; } return b; }
  function parseA(){
    var t=out[p++]; if(!t) throw 0;
    if(t.k==='n') return function(){ return t.v; };
    if(t.k==='v') return function(e){ return e[t.v]; };
    if(t.k==='('){ var n=parseE(); if(!peek()||peek().k!==')') throw 0; p++; return n; }
    throw 0;
  }
  try{ var f=parseE(); if(p!==out.length) return null; return f; }catch(e){ return null; }
}
function exprEqual(input,answer){
  var f=exprCompile(input), g=exprCompile(answer); if(!f||!g) return false;
  var hits=0;
  for(var trial=0;trial<8;trial++){
    var env={}; 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'.split('').forEach(function(c){ env[c]=1.5+Math.random()*4.0; });
    var x=f(env), y=g(env);
    if(!isFinite(x)||!isFinite(y)) continue;
    if(Math.abs(x-y)>1e-6*Math.max(1,Math.abs(x),Math.abs(y))) return false;
    hits++;
  }
  return hits>=3;
}
function answerMatches(input,answer,accept,expr){
  if(expr && input!==undefined && input!==null && String(input).trim()!==''){
    if(exprEqual(input,answer)) return true;
    return (accept||[]).some(function(a){ return exprEqual(input,a); });
  }
  if(input===undefined||input===null||String(input).trim()==='') return false;
  var n1=parseNum(input), n2=parseNum(answer);
  if(n1!==null && n2!==null) return Math.abs(n1-n2)<1e-3;
  var cands=[answer].concat(accept||[]); var ni=norm(input);
  for(var i=0;i<cands.length;i++){ if(norm(cands[i])===ni) return true; }
  return false;
}
function esc(s){ return cleanText(String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;')); }

/* SVG Coordinate Grid Generator */
function makeGridSVG(xmin, xmax, ymin, ymax, step, lines, dots){
  var w=280, h=280, pad=30;
  var pw=w-2*pad, ph=h-2*pad;
  function sx(x){ return pad + ((x - xmin)/(xmax - xmin))*pw; }
  function sy(y){ return h - pad - ((y - ymin)/(ymax - ymin))*ph; }
  var s='<svg class="graph-svg" viewBox="0 0 '+w+' '+h+'" xmlns="http://www.w3.org/2000/svg">';
  s+='<rect width="'+w+'" height="'+h+'" fill="#FAFAF8" rx="8"/>';
  for(var x=xmin; x<=xmax; x+=1){
    var stroke=(x===0)?'#16264A':(x%step===0?'#D6CEBD':'#EFECE4');
    var sw=(x===0)?1.8:1;
    s+='<line x1="'+sx(x)+'" y1="'+pad+'" x2="'+sx(x)+'" y2="'+(h-pad)+'" stroke="'+stroke+'" stroke-width="'+sw+'"/>';
  }
  for(var y=ymin; y<=ymax; y+=1){
    var stroke=(y===0)?'#16264A':(y%step===0?'#D6CEBD':'#EFECE4');
    var sw=(y===0)?1.8:1;
    s+='<line x1="'+pad+'" y1="'+sy(y)+'" x2="'+(w-pad)+'" y2="'+sy(y)+'" stroke="'+stroke+'" stroke-width="'+sw+'"/>';
  }
  for(var x=xmin; x<=xmax; x+=step){
    if(x===0) continue;
    s+='<text x="'+sx(x)+'" y="'+(sy(0)+12)+'" font-size="9" text-anchor="middle" fill="#655D4C">'+x+'</text>';
  }
  for(var y=ymin; y<=ymax; y+=step){
    if(y===0) continue;
    s+='<text x="'+(sx(0)-5)+'" y="'+(sy(y)+3)+'" font-size="9" text-anchor="end" fill="#655D4C">'+y+'</text>';
  }
  s+='<text x="'+(w-pad+10)+'" y="'+(sy(0)+4)+'" font-weight="bold" font-size="11" fill="#16264A">x</text>';
  s+='<text x="'+sx(0)+'" y="'+(pad-10)+'" font-weight="bold" font-size="11" text-anchor="middle" fill="#16264A">y</text>';
  (lines||[]).forEach(function(l){
    s+='<line x1="'+sx(l[0])+'" y1="'+sy(l[1])+'" x2="'+sx(l[2])+'" y2="'+sy(l[3])+'" stroke="#1F3B6B" stroke-width="2.5" stroke-linecap="round"/>';
  });
  (dots||[]).forEach(function(d){
    s+='<circle cx="'+sx(d[0])+'" cy="'+sy(d[1])+'" r="4.5" fill="#BF4B45" stroke="#16264A" stroke-width="1.5"/>';
  });
  s+='</svg>';
  return s;
}

/* =========================================================================
   CURRICULUM QUESTIONS (Worksheets A5 – F5)
   ========================================================================= */

var SLIDES_A5 = [
  {kind:'blank', p:"Find the slope of Line 1 graphed below through $(1, -1)$ and $(3, 5)$.", tag:"A5 #1", svg:makeGridSVG(-5,5,-5,5,1,[[-0.33,-5,3.33,6]],[[1,-1],[3,5]]), flat:[{t:"Rise: $5 - (-1) = $ __B1__", a:{B1:"6"}}, {t:"Run: $3 - 1 = $ __B1__", a:{B1:"2"}}, {t:"Slope $m = $ __B1__", a:{B1:"3"}}], sol:"m = (5 - (-1))/(3 - 1) = 6/2 = 3."},
  {kind:'blank', p:"Find the slope of Line 2 graphed below through $(-2, -2)$ and $(2, 3)$.", tag:"A5 #2", svg:makeGridSVG(-5,5,-5,5,1,[[-4.4,-5,3.6,5]],[[-2,-2],[2,3]]), flat:[{t:"Slope $m = \\frac{\\text{rise}}{\\text{run}} = $ __B1__", a:{B1:"5/4"}, accept:["1.25"]}], sol:"m = (3 - (-2))/(2 - (-2)) = 5/4 = 1.25."},
  {kind:'blank', p:"Find the slope of Line 3 graphed below on the $[-10, 10]$ grid through $(-2, 7)$ and $(5, -2)$.", tag:"A5 #3", svg:makeGridSVG(-10,10,-10,10,2,[[-3.5,9,8,-6]],[[-2,7],[5,-2]]), flat:[{t:"Vertical change $\\Delta y = -2 - 7 = $ __B1__", a:{B1:"-9"}}, {t:"Horizontal change $\\Delta x = 5 - (-2) = $ __B1__", a:{B1:"7"}}, {t:"Slope $m = $ __B1__", a:{B1:"-9/7"}}], sol:"m = (-2 - 7)/(5 - (-2)) = -9/7."},
  {kind:'blank', p:"Graph the line through $(-4, 2)$ and $(2, -3)$ and determine its slope.", tag:"A5 #4", svg:makeGridSVG(-5,5,-5,5,1,[[-5,2.83,4,-4.67]],[[-4,2],[2,-3]]), flat:[{t:"Slope $m = $ __B1__", a:{B1:"-5/6"}}], sol:"m = (-3 - 2)/(2 - (-4)) = -5/6."},
  {kind:'blank', p:"Graph the line through $(-2, 4)$ and $(3, 0)$ and determine its slope.", tag:"A5 #5", svg:makeGridSVG(-5,5,-5,5,1,[[-3.25,5,4.25,-1]],[[-2,4],[3,0]]), flat:[{t:"Slope $m = $ __B1__", a:{B1:"-4/5"}, accept:["-0.8"]}], sol:"m = (0 - 4)/(3 - (-2)) = -4/5."},
  {kind:'blank', p:"Graph the line through $(0, 5)$ and $(-4, -3)$ and determine its slope.", tag:"A5 #6", svg:makeGridSVG(-5,5,-5,5,1,[[-5,-5,0,5]],[[0,5],[-4,-3]]), flat:[{t:"Slope $m = $ __B1__", a:{B1:"2"}}], sol:"m = (-3 - 5)/(-4 - 0) = -8/(-4) = 2."},
  {kind:'blank', p:"Find the slope containing $(4, 0)$ and $(5, 7)$ using the slope formula.", tag:"A5 #7", flat:[{t:"$m = \\frac{7 - 0}{5 - 4} = $ __B1__", a:{B1:"7"}}], sol:"m = (7 - 0)/(5 - 4) = 7/1 = 7."},
  {kind:'blank', p:"Find the slope containing $(0, 8)$ and $(-3, 10)$.", tag:"A5 #8", flat:[{t:"$m = \\frac{10 - 8}{-3 - 0} = $ __B1__", a:{B1:"-2/3"}}], sol:"m = (10 - 8)/(-3 - 0) = 2/(-3) = -2/3."},
  {kind:'blank', p:"Find the slope containing $(3, -2)$ and $(5, -6)$.", tag:"A5 #9", flat:[{t:"$m = \\frac{-6 - (-2)}{5 - 3} = $ __B1__", a:{B1:"-2"}}], sol:"m = (-6 + 2)/(5 - 3) = -4/2 = -2."},
  {kind:'blank', p:"Find the slope containing $(0, 0)$ and $(2, -3)$.", tag:"A5 #10", flat:[{t:"$m = \\frac{-3 - 0}{2 - 0} = $ __B1__", a:{B1:"-3/2"}, accept:["-1.5"]}], sol:"m = (-3 - 0)/(2 - 0) = -3/2."},
  {kind:'blank', p:"Find the slope containing $(\\frac{3}{4}, \\frac{1}{2})$ and $(2, -3)$.", tag:"A5 #11", flat:[{t:"$m = \\frac{-3 - 0.5}{2 - 0.75} = $ __B1__", a:{B1:"-14/5"}, accept:["-2.8"]}], sol:"m = (-7/2) / (5/4) = -14/5 = -2.8."},
  {kind:'mcq', text:"What is the slope of the vertical line $x = -8$?", opts:["Zero slope", "Undefined slope", "-8", "1"], correct:1, tag:"A5 #12", sol:"Vertical lines have zero run (dx = 0), so division by zero makes the slope undefined."},
  {kind:'mcq', text:"What is the slope of the horizontal line $y = 2$?", opts:["Zero slope", "Undefined slope", "2", "-2"], correct:0, tag:"A5 #13", sol:"Horizontal lines have zero rise (dy = 0), so m = 0/dx = 0."},
  {kind:'mcq', text:"What is the slope of the line $x = 9$?", opts:["9", "Undefined slope", "Zero slope", "1/9"], correct:1, tag:"A5 #14", sol:"Vertical line x = 9 has an undefined slope."},
  {kind:'mcq', text:"What is the slope of the line $y = -9$?", opts:["-9", "Undefined slope", "Zero slope", "-1"], correct:2, tag:"A5 #15", sol:"Horizontal line y = -9 has zero slope."}
];

var SLIDES_B5 = [
  {kind:'blank', p:"Graph $x + 3y = 6$ by solving for $y$ and completing the 3-point table for $x \\in \\{0, 3, -3\\}$.", tag:"B5 #1", flat:[{t:"Solve for $y$: $y = $ __B1__", a:{B1:"-1/3*x+2"}, accept:["-x/3+2"], expr:true}, {t:"At $x=0$, $y = $ __B1__", a:{B1:"2"}}, {t:"At $x=3$, $y = $ __B1__", a:{B1:"1"}}, {t:"At $x=-3$, $y = $ __B1__", a:{B1:"3"}}], sol:"3y = -x + 6 => y = -x/3 + 2. Points: (0, 2), (3, 1), (-3, 3)."},
  {kind:'blank', p:"Graph $-x + 3y = 9$ using three points.", tag:"B5 #2", flat:[{t:"Solve for $y$: $y = $ __B1__", a:{B1:"1/3*x+3"}, accept:["x/3+3"], expr:true}, {t:"At $x=0$, $y = $ __B1__", a:{B1:"3"}}, {t:"At $x=3$, $y = $ __B1__", a:{B1:"4"}}], sol:"3y = x + 9 => y = x/3 + 3."},
  {kind:'blank', p:"Graph $2y - 2 = 6x$ using three points.", tag:"B5 #3", flat:[{t:"Solve for $y$: $y = $ __B1__", a:{B1:"3x+1"}, expr:true}, {t:"At $x=0$, $y = $ __B1__", a:{B1:"1"}}, {t:"At $x=1$, $y = $ __B1__", a:{B1:"4"}}], sol:"2y = 6x + 2 => y = 3x + 1."},
  {kind:'blank', p:"Find intercepts for $x - 1 = y$.", tag:"B5 #4", flat:[{t:"$x$-intercept ($y=0$): $x = $ __B1__", a:{B1:"1"}}, {t:"$y$-intercept ($x=0$): $y = $ __B1__", a:{B1:"-1"}}], sol:"x - 1 = 0 => x = 1; 0 - 1 = y => y = -1."},
  {kind:'blank', p:"Find intercepts for $2x - 1 = y$.", tag:"B5 #5", flat:[{t:"$x$-intercept: $x = $ __B1__", a:{B1:"1/2"}, accept:["0.5"]}, {t:"$y$-intercept: $y = $ __B1__", a:{B1:"-1"}}], sol:"2x - 1 = 0 => x = 1/2; y = -1."},
  {kind:'blank', p:"Find intercepts for $4x - 3y = 12$.", tag:"B5 #6", flat:[{t:"$x$-intercept: $x = $ __B1__", a:{B1:"3"}}, {t:"$y$-intercept: $y = $ __B1__", a:{B1:"-4"}}], sol:"4x = 12 => x = 3; -3y = 12 => y = -4."},
  {kind:'blank', p:"Find intercepts for $7x + 2y = 6$.", tag:"B5 #7", flat:[{t:"$y$-intercept ($x=0$): $y = $ __B1__", a:{B1:"3"}}, {t:"$x$-intercept fraction ($y=0$): $x = $ __B1__", a:{B1:"6/7"}}], sol:"2y = 6 => y = 3; 7x = 6 => x = 6/7."},
  {kind:'blank', p:"Find intercepts for $y = -4 - 4x$.", tag:"B5 #8", flat:[{t:"$y$-intercept: $y = $ __B1__", a:{B1:"-4"}}, {t:"$x$-intercept: $x = $ __B1__", a:{B1:"-1"}}], sol:"y-int = -4; 0 = -4 - 4x => 4x = -4 => x = -1."},
  {kind:'blank', p:"Rewrite $-3x = 6y - 2$ to find the $y$-intercept.", tag:"B5 #9", flat:[{t:"When $x=0$, $6y = 2 \\implies y = $ __B1__", a:{B1:"1/3"}}], sol:"6y = 2 => y = 1/3."},
  {kind:'blank', p:"Find intercepts for $3x - 6y = 12$.", tag:"B5 #10", flat:[{t:"$x$-intercept: $x = $ __B1__", a:{B1:"4"}}, {t:"$y$-intercept: $y = $ __B1__", a:{B1:"-2"}}], sol:"3x = 12 => x = 4; -6y = 12 => y = -2."},
  {kind:'blank', p:"Identify $b$ and $m$ for $y = \\frac{2}{3}x + 3$.", tag:"B5 #11", flat:[{t:"$b = $ __B1__", a:{B1:"3"}}, {t:"$m = $ __B1__", a:{B1:"2/3"}}], sol:"b = 3, m = 2/3."},
  {kind:'blank', p:"Identify $b$ and $m$ for $y = \\frac{5}{2}x - 1$.", tag:"B5 #12", flat:[{t:"$b = $ __B1__", a:{B1:"-1"}}, {t:"$m = $ __B1__", a:{B1:"5/2"}, accept:["2.5"]}], sol:"b = -1, m = 5/2."},
  {kind:'blank', p:"Identify $b$ and $m$ for $y = -\\frac{3}{2}x - 4$.", tag:"B5 #13", flat:[{t:"$b = $ __B1__", a:{B1:"-4"}}, {t:"$m = $ __B1__", a:{B1:"-3/2"}, accept:["-1.5"]}], sol:"b = -4, m = -3/2."},
  {kind:'blank', p:"Identify $b$ and $m$ for $y = -\\frac{1}{4}x + 3$.", tag:"B5 #14", flat:[{t:"$b = $ __B1__", a:{B1:"3"}}, {t:"$m = $ __B1__", a:{B1:"-1/4"}, accept:["-0.25"]}], sol:"b = 3, m = -1/4."},
  {kind:'blank', p:"Identify $b$ and $m$ for $y = 2x - 5$.", tag:"B5 #15", flat:[{t:"$b = $ __B1__", a:{B1:"-5"}}, {t:"$m = $ __B1__", a:{B1:"2"}}], sol:"b = -5, m = 2."},
  {kind:'blank', p:"Identify $b$ and $m$ for $y = 3x - 2$.", tag:"B5 #16", flat:[{t:"$b = $ __B1__", a:{B1:"-2"}}, {t:"$m = $ __B1__", a:{B1:"3"}}], sol:"b = -2, m = 3."},
  {kind:'blank', p:"Write $7x + 2y = 10$ in slope-intercept form.", tag:"B5 #17", flat:[{t:"$b = $ __B1__", a:{B1:"5"}}, {t:"$m = $ __B1__", a:{B1:"-7/2"}, accept:["-3.5"]}], sol:"2y = -7x + 10 => y = -7/2 x + 5."},
  {kind:'blank', p:"Write $3x + 5y = 10$ in slope-intercept form.", tag:"B5 #18", flat:[{t:"$b = $ __B1__", a:{B1:"2"}}, {t:"$m = $ __B1__", a:{B1:"-3/5"}, accept:["-0.6"]}], sol:"5y = -3x + 10 => y = -3/5 x + 2."},
  {kind:'blank', p:"Write $x - 4y = 12$ in slope-intercept form.", tag:"B5 #19", flat:[{t:"$b = $ __B1__", a:{B1:"-3"}}, {t:"$m = $ __B1__", a:{B1:"1/4"}, accept:["0.25"]}], sol:"-4y = -x + 12 => y = 1/4 x - 3."},
  {kind:'blank', p:"Write $2x - 5y = 15$ in slope-intercept form.", tag:"B5 #20", flat:[{t:"$b = $ __B1__", a:{B1:"-3"}}, {t:"$m = $ __B1__", a:{B1:"2/5"}, accept:["0.4"]}], sol:"-5y = -2x + 15 => y = 2/5 x - 3."}
];

var SLIDES_C5 = [
  {kind:'blank', p:"Find the equation of the line passing through $(2, 1)$ and $(-3, -14)$.", tag:"C5 #1", flat:[{t:"Slope $m = $ __B1__", a:{B1:"3"}}, {t:"Equation in $y = mx + b$: $y = $ __B1__", a:{B1:"3x-5"}, expr:true}], sol:"m = (-14 - 1)/(-3 - 2) = 3. y - 1 = 3(x - 2) => y = 3x - 5."},
  {kind:'blank', p:"Find the equation of the line passing through $(3, 1)$ and $(-2, 6)$.", tag:"C5 #2", flat:[{t:"Slope $m = $ __B1__", a:{B1:"-1"}}, {t:"Equation: $y = $ __B1__", a:{B1:"-x+4"}, expr:true}], sol:"m = (6 - 1)/(-2 - 3) = -1. y - 1 = -1(x - 3) => y = -x + 4."},
  {kind:'blank', p:"Find the equation of the line passing through $(-2, 7)$ and $(0, 1)$.", tag:"C5 #3", flat:[{t:"Slope $m = $ __B1__", a:{B1:"-3"}}, {t:"Equation: $y = $ __B1__", a:{B1:"-3x+1"}, expr:true}], sol:"m = (1 - 7)/(0 - (-2)) = -3. y = -3x + 1."},
  {kind:'blank', p:"Find the equation of the line passing through $(-4, 6)$ and $(1, -4)$.", tag:"C5 #4", flat:[{t:"Slope $m = $ __B1__", a:{B1:"-2"}}, {t:"Equation: $y = $ __B1__", a:{B1:"-2x-2"}, expr:true}], sol:"m = (-4 - 6)/(1 - (-4)) = -2. y + 4 = -2(x - 1) => y = -2x - 2."},
  {kind:'blank', p:"Find the equation of the line passing through $(1, 3)$ and $(0, -3)$.", tag:"C5 #5", flat:[{t:"Slope $m = $ __B1__", a:{B1:"6"}}, {t:"Equation: $y = $ __B1__", a:{B1:"6x-3"}, expr:true}], sol:"m = (-3 - 3)/(0 - 1) = 6. y = 6x - 3."},
  {kind:'blank', p:"Find the equation of the line through $(-2, -4)$ and parallel to $y = -x + 5$.", tag:"C5 #6", flat:[{t:"Slope $m = $ __B1__", a:{B1:"-1"}}, {t:"Equation: $y = $ __B1__", a:{B1:"-x-6"}, expr:true}], sol:"Parallel slope m = -1. y + 4 = -1(x + 2) => y = -x - 6."},
  {kind:'blank', p:"Find the equation of the line through $(2, 9)$ and parallel to $y = 5x - 1$.", tag:"C5 #7", flat:[{t:"Slope $m = $ __B1__", a:{B1:"5"}}, {t:"Equation: $y = $ __B1__", a:{B1:"5x-1"}, expr:true}], sol:"Parallel slope m = 5. y - 9 = 5(x - 2) => y = 5x - 1."},
  {kind:'blank', p:"Find the equation of the line through $(-1, 2)$ and perpendicular to $y = \\frac{1}{4}x - 5$.", tag:"C5 #8", flat:[{t:"Perpendicular slope $m = $ __B1__", a:{B1:"-4"}}, {t:"Equation: $y = $ __B1__", a:{B1:"-4x-2"}, expr:true}], sol:"Opposite reciprocal of 1/4 is -4. y - 2 = -4(x + 1) => y = -4x - 2."},
  {kind:'blank', p:"Find the equation of the line through $(4, -1)$ and perpendicular to $y = 2x + 4$.", tag:"C5 #9", flat:[{t:"Perpendicular slope $m = $ __B1__", a:{B1:"-1/2"}, accept:["-0.5"]}, {t:"Equation: $y = $ __B1__", a:{B1:"-1/2*x+1"}, accept:["-0.5x+1"], expr:true}], sol:"Opposite reciprocal of 2 is -1/2. y + 1 = -1/2(x - 4) => y = -1/2 x + 1."},
  {kind:'blank', p:"Find the equation of the line through $(-2, -3)$ and parallel to $y = 3x - 8$.", tag:"C5 #10", flat:[{t:"Slope $m = $ __B1__", a:{B1:"3"}}, {t:"Equation: $y = $ __B1__", a:{B1:"3x+3"}, expr:true}], sol:"Parallel slope m = 3. y + 3 = 3(x + 2) => y = 3x + 3."}
];

var SLIDES_D5 = [
  {kind:'mcq', text:"What type of relationship exists in Graph 1 (points cluster along a rising line)?", opts:["Positive Correlation", "Negative Correlation", "No Correlation", "Nonlinear"], correct:0, tag:"D5 #1", sol:"As x increases, y increases: positive correlation."},
  {kind:'mcq', text:"What type of relationship exists in Graph 2 (points cluster along a falling line)?", opts:["Positive Correlation", "Negative Correlation", "No Correlation", "Constant"], correct:1, tag:"D5 #2", sol:"As x increases, y decreases: negative correlation."},
  {kind:'mcq', text:"What type of relationship exists in Graph 3 (points scattered uniformly)?", opts:["Positive Correlation", "Negative Correlation", "No Correlation", "Strong Correlation"], correct:2, tag:"D5 #3", sol:"No linear pattern exists: no correlation."},
  {kind:'mcq', text:"What type of relationship exists in Graph 4 (points form a curved arc)?", opts:["Linear Positive", "Nonlinear / Curved Relationship", "No Relationship", "Negative Linear"], correct:1, tag:"D5 #4", sol:"Points follow a curved trajectory: nonlinear relationship."},
  {kind:'mcq', text:"What type of relationship exists in Graph 5 (random cloud)?", opts:["Positive Correlation", "Negative Correlation", "No Correlation", "Moderate Positive"], correct:2, tag:"D5 #5", sol:"A random cloud shows zero correlation."},
  {kind:'mcq', text:"What type of relationship exists in Graph 6 (tight downward trend)?", opts:["Positive Correlation", "Negative Correlation", "No Correlation", "Undefined"], correct:1, tag:"D5 #6", sol:"Downward sloping points indicate negative correlation."},
  {kind:'mcq', text:"What relationship do you expect between the weight of a sirloin steak and its selling price?", opts:["Positive Correlation", "Negative Correlation", "No Correlation"], correct:0, tag:"D5 #7", sol:"Heavier cuts of steak cost more: positive correlation."},
  {kind:'mcq', text:"What relationship do you expect between problems assigned and time spent doing homework?", opts:["Positive Correlation", "Negative Correlation", "No Correlation"], correct:0, tag:"D5 #8", sol:"More homework problems take more time: positive correlation."},
  {kind:'mcq', text:"What relationship do you expect between athletic ability and musical ability?", opts:["Positive Correlation", "Negative Correlation", "No Correlation"], correct:2, tag:"D5 #9", sol:"Independent human abilities: no correlation."},
  {kind:'mcq', text:"What relationship do you expect between math anxiety and math exam score?", opts:["Positive Correlation", "Negative Correlation", "No Correlation"], correct:1, tag:"D5 #10", sol:"Higher anxiety is generally associated with lower exam scores: negative correlation."},
  {kind:'mcq', text:"Based on the table of 12 students, what relationship exists between GPA ($x$) and Shoe Size ($y$)?", opts:["Strong Positive", "Negative Correlation", "No Correlation", "Curved"], correct:2, tag:"D5 #11", sol:"Shoe size does not determine academic GPA: no correlation."},
  {kind:'mcq', text:"Based on the table of 12 students, what relationship exists between Height ($x$) and Weight ($y$)?", opts:["Positive Correlation", "Negative Correlation", "No Correlation"], correct:0, tag:"D5 #12", sol:"Taller students generally weigh more: positive correlation."}
];

var SLIDES_E5 = [
  {kind:'blank', p:"Phone rate: 5 minutes ($m$) for $0.85 ($p$) and 10 minutes for $1.10. Assume a linear relationship.", tag:"E5 #1", flat:[{t:"Slope rate: $m_{\\text{rate}} = $ __B1__ dollars/min", a:{B1:"0.05"}}, {t:"Equation: $p = $ __B1__", a:{B1:"0.05*m+0.60"}, accept:["0.05m+0.6"], expr:true}, {t:"Cost of a 20-min call: $p(20) = $ $__B1__", a:{B1:"1.60"}, accept:["1.6"]}], sol:"Rate = (1.10 - 0.85)/5 = 0.05. Base fee = 0.85 - 0.25 = 0.60. p(20) = 0.05(20) + 0.60 = $1.60."},
  {kind:'blank', p:"At altitude $500\\text{ m}$, air temp is $10^\\circ\\text{C}$. At $2000\\text{ m}$, air temp is $-5^\\circ\\text{C}$.", tag:"E5 #2", flat:[{t:"Rate of temperature change: $m = $ __B1__ $^\\circ\\text{C/m}$", a:{B1:"-0.01"}}, {t:"Linear equation relating $t$ and $h$: $t = $ __B1__", a:{B1:"-0.01*h+15"}, expr:true}, {t:"Temperature at $1500\\text{ m}$: $t(1500) = $ __B1__ $^\\circ\\text{C}$", a:{B1:"0"}}], sol:"m = (-5 - 10)/(2000 - 500) = -0.01. b = 15. At 1500: -0.01(1500) + 15 = 0°C."},
  {kind:'blank', p:"School record in a race: in 1970 was 3.8 minutes; in 1990 was 3.65 minutes.", tag:"E5 #3", flat:[{t:"Rate per year: $m = $ __B1__ min/year", a:{B1:"-0.0075"}}, {t:"Predicted record in year 2000: $r = $ __B1__ minutes", a:{B1:"3.575"}}], sol:"m = (3.65 - 3.80)/20 = -0.0075. In 2000 (10 years later): 3.65 - 0.075 = 3.575 min."},
  {kind:'blank', p:"Tree diameter ($d$) vs age ($y$): $(4,1), (10,5), (40,20), (35,15), (25,10), (35,15), (20,20)$. Find the approximate slope of best fit.", tag:"E5 #4", flat:[{t:"Approximate rate of age per cm diameter: $m \\approx $ __B1__", a:{B1:"0.5"}, accept:["0.48", "0.52"]}], sol:"A linear fit through the cluster yields m ≈ 0.5 years per unit diameter."},
  {kind:'blank', p:"Motel distance ($d$ miles) vs room cost ($c$): $(1,80), (2,75), (2,55), (3,60), (3,45), (4,55), (5,40), (5,50), (6,35)$.", tag:"E5 #5", flat:[{t:"Estimated price decrease per mile from center: $\\Delta c \\approx $ __B1__ dollars", a:{B1:"-8"}, accept:["-7.5", "-8.5"]}], sol:"The downward trend drops roughly $40 over 5 miles, yielding a slope around -8."}
];

var SLIDES_F5 = [
  {kind:'blank', p:"State the formula for slope-intercept form.", tag:"F5 #1", flat:[{t:"Slope-intercept form: $y = $ __B1__", a:{B1:"mx+b"}, expr:true}], sol:"y = mx + b."},
  {kind:'blank', p:"State the formula for point-slope form.", tag:"F5 #2", flat:[{t:"Point-slope form: $y - y_1 = $ __B1__", a:{B1:"m(x-x1)"}, expr:true}], sol:"y - y_1 = m(x - x_1)."},
  {kind:'blank', p:"Find the slope of the line containing $(5, -3)$ and $(-2, 5)$.", tag:"F5 #3", flat:[{t:"Slope fraction $m = $ __B1__", a:{B1:"-8/7"}}], sol:"m = (5 - (-3))/(-2 - 5) = 8/(-7) = -8/7."},
  {kind:'blank', p:"Identify slope and $y$-intercept for $y = -5x + 7$.", tag:"F5 #4", flat:[{t:"Slope $m = $ __B1__", a:{B1:"-5"}}, {t:"$y$-intercept $b = $ __B1__", a:{B1:"7"}}], sol:"m = -5, b = 7."},
  {kind:'blank', p:"Write in slope-intercept form the line with $y$-intercept $-4$ and slope $-1$.", tag:"F5 #5", flat:[{t:"$y = $ __B1__", a:{B1:"-x-4"}, expr:true}], sol:"y = -1x - 4 = -x - 4."},
  {kind:'mcq', text:"What is the $y$-intercept of the line $15x = 5y - 10$?", opts:["-5", "-3", "2", "15"], correct:2, tag:"F5 #6", sol:"5y = 15x + 10 => y = 3x + 2. The y-intercept is 2."},
  {kind:'mcq', text:"What is the equation of the line whose slope is $-2$ and whose $y$-intercept is $8$?", opts:["y = 8x + 2", "y = 8x - 2", "y = 2x - 8", "y = -2x + 8"], correct:3, tag:"F5 #7", sol:"y = -2x + 8."},
  {kind:'blank', p:"Write an equation in slope-intercept form for the line graphed through $(0, 5)$ and $(2, 0)$.", tag:"F5 #8", svg:makeGridSVG(-5,5,-5,5,1,[[-1,7.5,3.5,-3.75]],[[0,5],[2,0]]), flat:[{t:"$y = $ __B1__", a:{B1:"-5/2*x+5"}, accept:["-2.5x+5"], expr:true}], sol:"m = (0 - 5)/(2 - 0) = -5/2. Equation: y = -5/2 x + 5."},
  {kind:'blank', p:"Graph $-\\frac{3}{4}x + y = 1$ using slope and $y$-intercept.", tag:"F5 #9", flat:[{t:"$y$-intercept: $b = $ __B1__", a:{B1:"1"}}, {t:"Slope: $m = $ __B1__", a:{B1:"3/4"}, accept:["0.75"]}], sol:"y = 3/4 x + 1. b = 1, m = 3/4."},
  {kind:'blank', p:"Graph $-3x + 2y = 7$ using slope and $y$-intercept.", tag:"F5 #10", flat:[{t:"$y$-intercept: $b = $ __B1__", a:{B1:"7/2"}, accept:["3.5"]}, {t:"Slope: $m = $ __B1__", a:{B1:"3/2"}, accept:["1.5"]}], sol:"2y = 3x + 7 => y = 3/2 x + 7/2."},
  {kind:'blank', p:"Find the intercepts to graph $3x - 5y = 15$.", tag:"F5 #11", flat:[{t:"$x$-intercept: $x = $ __B1__", a:{B1:"5"}}, {t:"$y$-intercept: $y = $ __B1__", a:{B1:"-3"}}], sol:"3x = 15 => x = 5; -5y = 15 => y = -3."},
  {kind:'blank', p:"Find intercepts to graph $y - 3 = -2x$.", tag:"F5 #12", flat:[{t:"$y$-intercept ($x=0$): $y = $ __B1__", a:{B1:"3"}}, {t:"$x$-intercept ($y=0$): $x = $ __B1__", a:{B1:"3/2"}, accept:["1.5"]}], sol:"2x + y = 3. y-int = 3, x-int = 3/2."},
  {kind:'blank', p:"Find intercepts to graph $-2x + 4y = 6$.", tag:"F5 #13", flat:[{t:"$x$-intercept: $x = $ __B1__", a:{B1:"-3"}}, {t:"$y$-intercept: $y = $ __B1__", a:{B1:"3/2"}, accept:["1.5"]}], sol:"-2x = 6 => x = -3; 4y = 6 => y = 3/2."},
  {kind:'blank', p:"Find slope and $y$-intercept for $4x + y = 3$.", tag:"F5 #14", flat:[{t:"Slope $m = $ __B1__", a:{B1:"-4"}}, {t:"$y$-intercept $b = $ __B1__", a:{B1:"3"}}], sol:"y = -4x + 3. m = -4, b = 3."},
  {kind:'blank', p:"Find intercepts for $x + 2y = 10$.", tag:"F5 #15", flat:[{t:"$x$-intercept: $x = $ __B1__", a:{B1:"10"}}, {t:"$y$-intercept: $y = $ __B1__", a:{B1:"5"}}], sol:"x = 10; 2y = 10 => y = 5."},
  {kind:'blank', p:"Find three points to graph $y = 4x - 6$.", tag:"F5 #16", flat:[{t:"At $x=0$, $y = $ __B1__", a:{B1:"-6"}}, {t:"At $x=1$, $y = $ __B1__", a:{B1:"-2"}}, {t:"At $x=2$, $y = $ __B1__", a:{B1:"2"}}], sol:"Points: (0, -6), (1, -2), (2, 2)."},
  {kind:'mcq', text:"What type of line is represented by $x = 5$?", opts:["Vertical line passing through x = 5", "Horizontal line passing through y = 5", "Slanted line with slope 5", "Line passing through origin"], correct:0, tag:"F5 #17", sol:"x = constant is always a vertical line."},
  {kind:'mcq', text:"What type of line is represented by $y = -2$?", opts:["Horizontal line passing through y = -2", "Vertical line passing through x = -2", "Line with undefined slope", "Slanted line"], correct:0, tag:"F5 #18", sol:"y = constant is always a horizontal line."},
  {kind:'mcq', text:"What is the geometric representation of $y = 0$?", opts:["The x-axis", "The y-axis", "A vertical line", "A line of slope 1"], correct:0, tag:"F5 #19", sol:"The line y = 0 is the x-axis."},
  {kind:'blank', p:"Write the equation for the horizontal line graphed through $(0, 4)$.", tag:"F5 #20", svg:makeGridSVG(-5,5,-5,5,1,[[-5,4,5,4]],[[0,4]]), flat:[{t:"Equation: __B1__", a:{B1:"y=4"}, accept:["y-4=0","4"]}], sol:"Horizontal line through y = 4 has equation y = 4."},
  {kind:'blank', p:"Find the equation of a line parallel to $y = 2x - 3$ with $y$-intercept $4$.", tag:"F5 #21", flat:[{t:"$y = $ __B1__", a:{B1:"2x+4"}, expr:true}], sol:"Parallel slope = 2. Equation: y = 2x + 4."},
  {kind:'blank', p:"Find the equation of a line perpendicular to $y = -3x + 7$ with $y$-intercept $-2$.", tag:"F5 #22", flat:[{t:"$y = $ __B1__", a:{B1:"1/3*x-2"}, accept:["x/3-2"], expr:true}], sol:"Opposite reciprocal of -3 is 1/3. Equation: y = 1/3 x - 2."},
  {kind:'blank', p:"Find the equation of a line parallel to $y = 2x - 1$ through $(6, 2)$.", tag:"F5 #23", flat:[{t:"$y = $ __B1__", a:{B1:"2x-10"}, expr:true}], sol:"m = 2. y - 2 = 2(x - 6) => y = 2x - 10."},
  {kind:'blank', p:"Find the equation of a line perpendicular to $y = \\frac{1}{3}x + 2$ through $(1, 7)$.", tag:"F5 #24", flat:[{t:"$y = $ __B1__", a:{B1:"-3x+10"}, expr:true}], sol:"m = -3. y - 7 = -3(x - 1) => y = -3x + 10."},
  {kind:'blank', p:"Snake length allometry: Snake 1 ($l=150\\text{ mm}, t=19\\text{ mm}$) and Snake 2 ($l=300\\text{ mm}, t=40\\text{ mm}$).", tag:"F5 #25", flat:[{t:"Slope $m = $ __B1__", a:{B1:"0.14"}}, {t:"Equation for tail length: $t = $ __B1__", a:{B1:"0.14*l-2"}, expr:true}, {t:"Tail length when $l = 200\\text{ mm}$: $t = $ __B1__ mm", a:{B1:"26"}}], sol:"m = (40 - 19)/(300 - 150) = 0.14. t = 0.14l - 2. When l=200, t = 28 - 2 = 26 mm."},
  {kind:'blank', p:"Diner burger prices: 1950 ($x=50$) was $0.25; 1998 ($x=98$) was $1.95. Let $x$ be years since 1900.", tag:"F5 #26-28", flat:[{t:"Rate of increase per year $m \\approx $ __B1__", a:{B1:"0.0354"}}, {t:"Equation: $y = 0.0354x - $ __B1__", a:{B1:"1.52"}}, {t:"Estimated burger price in 1990 ($x=90$): $__B1__", a:{B1:"1.67"}, accept:["1.66", "1.68"]}], sol:"m = 1.70/48 ≈ 0.0354. y = 0.0354x - 1.52. At x=90: y ≈ $1.67."}
];

var SLIDES = {
  a5: SLIDES_A5,
  b5: SLIDES_B5,
  c5: SLIDES_C5,
  d5: SLIDES_D5,
  e5: SLIDES_E5,
  f5: SLIDES_F5
};

var TAB_DEFS = [
  {id:'a5', label:'Worksheet A5', sub:'Finding & Counting Slopes (15 Questions)'},
  {id:'b5', label:'Worksheet B5', sub:'Graphing Equations & Intercepts (20 Questions)'},
  {id:'c5', label:'Worksheet C5', sub:'Writing Equations of Lines (10 Questions)'},
  {id:'d5', label:'Worksheet D5', sub:'Scatter Plots & Correlation (12 Questions)'},
  {id:'e5', label:'Worksheet E5', sub:'Linear Regression & Modeling (5 Questions)'},
  {id:'f5', label:'Worksheet F5', sub:'Unit 5 Cumulative Test Review (28 Questions)'}
];

/* Session Engine & Device State */
var SHEET_KEY = 'sopaan-linear-assessment-master-v3';
var ACC_KEY = 'sopaan-students-v1';
var student = null;
var appState = {mode:null, learning:null, quiz:null};
var state = null;
var MODE = null;
var activeTab = 'a5';
var records = [];
var currentFocusedInput = null;
var __flash = null;

function blankItem(slide){
  if(slide.kind==='mcq') return {status:'unanswered', attempts:0, choice:undefined};
  return {status:'unanswered', curStep:0, stepStates: slide.flat.map(function(){ return {status:'unanswered', attempts:0, inputs:{}}; })};
}
function defaultState(){
  var s={tabs:{}};
  TAB_DEFS.forEach(function(td){
    s.tabs[td.id] = { idx:0, maxReached:0, items: SLIDES[td.id].map(function(sl){ return blankItem(sl); }) };
  });
  return s;
}
function setMode(m){
  appState.mode = m;
  if(!appState[m]) appState[m] = defaultState();
  state = appState[m];
  MODE = m;
}
function lsGet(k){ try{ return JSON.parse(localStorage.getItem(k)); }catch(e){ return null; } }
function lsSet(k,v){ try{ localStorage.setItem(k, JSON.stringify(v)); return true; }catch(e){ return false; } }
function hashPin(pin,salt){ var h=2166136261, str=salt+'|'+pin; for(var i=0;i<str.length;i++){ h^=str.charCodeAt(i); h=Math.imul(h,16777619)>>>0; } return h.toString(36); }
function accKey(name,roll){ return (name.trim().toLowerCase().replace(/\s+/g,' ')+'#'+roll.trim().toLowerCase()); }
function accounts(){ return lsGet(ACC_KEY)||{students:{}}; }
function progKey(){ return SHEET_KEY+'::'+student.key; }

function loadState(){
  appState = {mode:null, learning:null, quiz:null}; records=[];
  var saved = lsGet(progKey());
  if(!saved) return;
  try{
    ['learning','quiz'].forEach(function(m){
      if(saved[m] && saved[m].tabs){
        var fresh = defaultState();
        TAB_DEFS.forEach(function(td){
          if(saved[m].tabs[td.id] && saved[m].tabs[td.id].items && saved[m].tabs[td.id].items.length===SLIDES[td.id].length){
            fresh.tabs[td.id] = saved[m].tabs[td.id];
          }
        });
        appState[m] = fresh;
      }
    });
    if(saved.mode==='learning'||saved.mode==='quiz') appState.mode = saved.mode;
    if(saved.activeTab && SLIDES[saved.activeTab]) activeTab = saved.activeTab;
    if(Array.isArray(saved.records)) records = saved.records;
  }catch(e){}
}
function saveState(){
  if(!student) return;
  lsSet(progKey(), {mode:appState.mode, learning:appState.learning, quiz:appState.quiz, activeTab:activeTab, records:records, updated:Date.now()});
  var acc=accounts(); if(acc.students[student.key]){ acc.students[student.key].last=Date.now(); lsSet(ACC_KEY,acc); }
}

function renderWho(){
  var el=document.getElementById('whoBar');
  if(!student){ el.hidden=true; el.innerHTML=''; return; }
  el.hidden=false;
  el.innerHTML='Signed in: <b>'+esc(student.name)+'</b> (Roll '+esc(student.roll)+') <button id="btnSignOut">Sign out</button>';
  document.getElementById('btnSignOut').addEventListener('click', signOut);
}
function signOut(){
  saveState(); student=null; state=null; MODE=null;
  document.getElementById('modePill').hidden=true;
  renderWho(); renderLogin();
}
function signIn(key){
  var acc=accounts(); var st=acc.students[key]; if(!st) return;
  student={key:key, name:st.name, roll:st.roll};
  acc.current=key; st.last=Date.now(); lsSet(ACC_KEY,acc);
  loadState(); renderWho();
  if(appState.mode==='learning' || appState.mode==='quiz'){
    setMode(appState.mode); document.getElementById('modePill').hidden=false; updateModePill();
    showChrome(true); buildTabbar(); renderSlide();
  } else {
    renderModePicker();
  }
}
function renderLogin(msg){
  showChrome(false);
  var h='<div class="login-card"><h2>Student Verification</h2><p style="color:var(--ink-soft);font-size:13.5px;">Sign in to preserve your work across all 90 assessment questions.</p>';
  if(msg) h+='<div style="color:var(--danger);margin-bottom:10px;font-size:13px;">'+esc(msg)+'</div>';
  h+='<form id="loginForm">'+
     '<div class="fld"><label>Full Name</label><input id="lgName" required></div>'+
     '<div class="fld-row"><div class="fld"><label>Roll Number</label><input id="lgRoll" required></div>'+
     '<div class="fld"><label>4-Digit PIN</label><input id="lgPin" type="password" maxlength="4" required></div></div>'+
     '<button class="btn btn-primary" type="submit" style="width:100%;">Sign in</button></form></div>';
  var wrap=document.getElementById('wrap'); wrap.innerHTML=h;
  document.getElementById('loginForm').addEventListener('submit', function(e){
    e.preventDefault();
    var name=document.getElementById('lgName').value.trim(), roll=document.getElementById('lgRoll').value.trim(), pin=document.getElementById('lgPin').value.trim();
    if(!name||!roll||!/^\d{4}$/.test(pin)){ renderLogin('Enter a valid name, roll number, and 4-digit PIN.'); return; }
    var k=accKey(name,roll); var acc=accounts();
    if(acc.students[k]){
      if(acc.students[k].pin!==hashPin(pin,k)){ renderLogin('PIN incorrect for this student profile.'); return; }
    } else {
      acc.students[k]={name:name, roll:roll, pin:hashPin(pin,k), created:Date.now()};
      lsSet(ACC_KEY,acc);
    }
    signIn(k);
  });
}

function buildTabbar(){
  var el=document.getElementById('tabbar');
  el.innerHTML = TAB_DEFS.map(function(t){
    return '<button class="tab-btn'+(t.id===activeTab?' active':'')+'" data-tab="'+t.id+'">'+t.label+'<span class="tab-count">'+SLIDES[t.id].length+'</span></button>';
  }).join('');
  el.querySelectorAll('.tab-btn').forEach(function(btn){
    btn.addEventListener('click', function(){ activeTab=btn.dataset.tab; buildTabbar(); renderSlide(); window.scrollTo({top:0,behavior:'smooth'}); });
  });
}

var LETTERS=['a','b','c','d'];
function renderSlide(){
  var ts = state.tabs[activeTab];
  var slides = SLIDES[activeTab];
  var idx = ts.idx;
  var slide = slides[idx];
  var item = ts.items[idx];
  var tdef = TAB_DEFS.find(function(t){return t.id===activeTab;});

  document.getElementById('spLabel').textContent = tdef.label+' · Question '+(idx+1)+' of '+slides.length;
  document.getElementById('secSub').textContent = tdef.label+' — '+tdef.sub;
  document.getElementById('spFill').style.width = Math.round(((idx)/(Math.max(slides.length-1,1)))*100)+'%';

  var h='<div class="qcard">';
  if(MODE==='quiz'){
    h+='<div class="quiz-hint">Quiz Mode active: Work through each question and advance. Final scoring and solution keys are revealed upon section submission.</div>';
  }
  if(slide.kind==='mcq'){
    h+='<div class="qhead"><div class="qnum">'+(idx+1)+'</div>';
    h+='<div class="qtext">'+cleanText(slide.text)+(slide.tag?'<span class="qtag">'+slide.tag+'</span>':'')+'</div></div>';
    var locked = MODE==='learning' && (item.status==='correct'||item.status==='revealed');
    h+='<div class="options">';
    slide.opts.forEach(function(opt,i){
      var cls='opt';
      if(locked){
        if(i===slide.correct) cls+=' is-correct';
        else if(item.choice===i) cls+=' is-wrong';
        cls+=' locked';
      }
      if(item.choice===i) cls+=' is-chosen';
      h+='<label class="'+cls+'"><input type="radio" name="choice" value="'+i+'" '+(item.choice===i?'checked':'')+' '+(locked?'disabled':'')+'> <span class="opt-l">('+LETTERS[i]+')</span> <span class="opt-t">'+cleanText(opt)+'</span></label>';
    });
    h+='</div>';
  } else {
    h+='<div class="qhead"><div class="qnum">'+(idx+1)+'</div><div class="qtext">'+cleanText(slide.p)+(slide.tag?'<span class="qtag">'+slide.tag+'</span>':'')+'</div></div>';
    if(slide.svg) h+='<div class="graph-container">'+slide.svg+'</div>';
    var total=slide.flat.length;
    var upto = (MODE==='quiz' || item.status==='correct'||item.status==='revealed') ? total-1 : item.curStep;
    h+='<div class="steps">';
    for(var i=0;i<=upto;i++){
      var step=slide.flat[i], ss=item.stepStates[i];
      var resolved = ss.status==='correct'||ss.status==='revealed';
      var line=cleanText(step.t);
      Object.keys(step.a).forEach(function(bk){
        var fs=ss.inputs['fs_'+bk]||'';
        var cls=fs==='correct'?'is-correct':(fs==='wrong'?'is-wrong':'');
        var val=ss.inputs[bk]||'';
        var dis=(MODE==='learning'&&resolved)?'disabled':'';
        var inp='<input class="blank-input '+cls+(step.expr?' expr':'')+'" data-step="'+i+'" data-bkey="'+bk+'" value="'+esc(val)+'" '+dis+'>';
        line=line.replace('__'+bk+'__', inp);
      });
      h+='<div class="step-line">'+line+'</div>';
      if(ss.status==='revealed') h+='<div class="reveal-note">Correct answer: '+Object.values(step.a).join(', ')+'</div>';
    }
    h+='</div>';
  }
  h+='<div class="feedback" id="feedbackBox"></div>';
  if(MODE==='learning' && (item.status==='correct'||item.status==='revealed') && slide.sol){
    h+='<div class="solution"><div class="sol-h">Step-by-Step Solution</div><div class="sol-line">'+cleanText(slide.sol)+'</div></div>';
  }
  h+='</div>';

  document.getElementById('wrap').innerHTML=h;
  wireSlideEvents(slide, item);
  restoreFeedback(item);
  renderNavbar(item);
  updateFab();
  saveState();
  applyKaTeX();
}

function restoreFeedback(item){
  var fb=document.getElementById('feedbackBox'); if(!fb) return;
  if(__flash){ fb.className='feedback show '+__flash.c; fb.innerHTML=__flash.h; __flash=null; return; }
  if(MODE==='quiz'){ fb.className='feedback'; fb.innerHTML=''; return; }
  if(item.status==='correct'){ fb.className='feedback show ok'; fb.innerHTML='<b>All done — correct!</b>'; }
  else if(item.status==='revealed'){ fb.className='feedback show reveal'; fb.innerHTML='<b>Answer revealed above.</b> Review the solution below and proceed.'; }
  else if(item.status==='skipped'){ fb.className='feedback show retry'; fb.innerHTML='Skipped — revisit anytime using the Question Palette.'; }
  else { fb.className='feedback'; fb.innerHTML=''; }
}

function applyKaTeX(){
  if(window.renderMathInElement){
    try{
      renderMathInElement(document.getElementById('wrap'), {delimiters:[{left:'$$',right:'$$',display:true},{left:'$',right:'$',display:false}]});
    }catch(e){}
  }
}

function wireSlideEvents(slide, item){
  document.querySelectorAll('input[type="radio"][name="choice"]').forEach(function(r){
    r.addEventListener('change', function(){
      item.choice=parseInt(r.value,10);
      document.querySelectorAll('.opt').forEach(function(l){ l.classList.remove('is-chosen'); });
      r.closest('.opt').classList.add('is-chosen');
      saveState();
    });
  });
  document.querySelectorAll('.blank-input').forEach(function(inp){
    inp.addEventListener('input', function(){
      var si=parseInt(inp.dataset.step,10), bk=inp.dataset.bkey;
      item.stepStates[si].inputs[bk]=inp.value;
      saveState();
    });
    inp.addEventListener('focus', function(){
      currentFocusedInput = inp;
      document.querySelectorAll('.blank-input').forEach(function(el){ el.classList.remove('active-focus'); });
      inp.classList.add('active-focus');
      document.getElementById('mathKeypad').classList.add('show');
    });
  });
}

function canProceed(item){
  return item.status==='correct'||item.status==='revealed'||item.status==='skipped';
}

function renderNavbar(item){
  var ts=state.tabs[activeTab], slides=SLIDES[activeTab], isLast=ts.idx===slides.length-1;
  var h='<button class="btn" id="btnPrev" '+(ts.idx===0?'disabled':'')+'>&larr; Prev</button>';
  if(MODE==='quiz'){
    h+='<button class="btn" id="btnSkip">Skip</button><span class="spacer"></span>';
    h+='<button class="btn btn-primary" id="btnNext">'+(isLast?'Finish &amp; Grade':'Next &rarr;')+'</button>';
  } else {
    h+='<button class="btn" id="btnSkip" '+(item.status!=='unanswered'?'disabled':'')+'>Skip</button><span class="spacer"></span>';
    h+='<button class="btn btn-primary" id="btnCheck" '+(item.status!=='unanswered'?'disabled':'')+'>Check</button>';
    h+='<button class="btn btn-primary" id="btnNext" '+(canProceed(item)?'':'disabled')+'>'+(isLast?'Finish Section':'Next &rarr;')+'</button>';
  }
  document.getElementById('navbarInner').innerHTML=h;
  
  document.getElementById('btnPrev').addEventListener('click', function(){ if(ts.idx>0){ ts.idx--; renderSlide(); } });
  
  if(MODE==='quiz'){
    document.getElementById('btnSkip').addEventListener('click', function(){
      item.status='skipped';
      advanceSlide(ts, slides);
    });
    document.getElementById('btnNext').addEventListener('click', function(){
      advanceSlide(ts, slides);
    });
  } else {
    document.getElementById('btnSkip').addEventListener('click', function(){
      if(item.status==='unanswered'){ item.status='skipped'; renderSlide(); }
    });
    document.getElementById('btnNext').addEventListener('click', function(){
      if(!canProceed(item)) return;
      advanceSlide(ts, slides);
    });
    document.getElementById('btnCheck').addEventListener('click', handleCheck);
  }
}

function advanceSlide(ts, slides){
  if(ts.idx < slides.length - 1){
    ts.idx++;
    ts.maxReached = Math.max(ts.maxReached, ts.idx);
    renderSlide();
  } else {
    renderFinished();
  }
}

function handleCheck(){
  var ts=state.tabs[activeTab], slide=SLIDES[activeTab][ts.idx], item=ts.items[ts.idx];
  var fb=document.getElementById('feedbackBox');
  if(slide.kind==='mcq'){
    if(item.choice===undefined){ fb.className='feedback show err'; fb.innerHTML='Please select an option first.'; return; }
    if(item.choice===slide.correct){
      item.status='correct'; playSuccess();
      __flash={c:'ok', h:'<b>Correct!</b> Well done.'};
    } else {
      item.attempts=(item.attempts||0)+1;
      if(item.attempts>=2){
        item.status='revealed'; playReveal();
        __flash={c:'reveal', h:'<b>Attempt limit reached.</b> Correct answer revealed below.'};
      } else {
        playWrong();
        fb.className='feedback show retry';
        fb.innerHTML='<b>Not quite — try again</b> (Attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>';
        __flash={c:'retry', h:'<b>Not quite — try again</b> (Attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'};
        return;
      }
    }
  } else {
    var step=slide.flat[item.curStep], ss=item.stepStates[item.curStep];
    var keys = Object.keys(step.a);
    var hasEmpty = keys.some(function(k){ return !ss.inputs[k] || String(ss.inputs[k]).trim()===''; });
    if(hasEmpty){
      fb.className='feedback show err';
      fb.innerHTML='Please fill in the blank before checking.';
      return;
    }
    var allGood=true;
    keys.forEach(function(k){
      var good=answerMatches(ss.inputs[k], step.a[k], step.accept, step.expr);
      ss.inputs['fs_'+k]=good?'correct':'wrong';
      if(!good) allGood=false;
    });
    if(allGood){
      ss.status='correct'; playSuccess();
      if(item.curStep < slide.flat.length - 1){
        item.curStep++;
        __flash={c:'ok', h:'<b>Step completed!</b> Keep going.'};
      } else {
        item.status='correct';
        __flash={c:'ok', h:'<b>All steps correct!</b>'};
      }
    } else {
      ss.attempts=(ss.attempts||0)+1;
      if(ss.attempts>=2){
        ss.status='revealed'; playReveal();
        if(item.curStep < slide.flat.length - 1){
          item.curStep++;
          __flash={c:'reveal', h:'Answer revealed. Moving to next step.'};
        } else {
          item.status='revealed';
          __flash={c:'reveal', h:'<b>Question finished.</b> Solution detailed below.'};
        }
      } else {
        playWrong();
        fb.className='feedback show retry';
        fb.innerHTML='<b>Check your work and try again</b> (Attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>';
        __flash={c:'retry', h:'<b>Check your work and try again</b> (Attempt 1 of 2) <span class="attempts-dots"><span class="used"></span><span></span></span>'};
        renderSlide();
        return;
      }
    }
  }
  renderSlide();
}

function isSlideCorrect(tabId, i){
  var slide = SLIDES[tabId][i], item = state.tabs[tabId].items[i];
  if(slide.kind==='mcq') return item.choice === slide.correct;
  return slide.flat.every(function(step, si){
    var ss = item.stepStates[si];
    return Object.keys(step.a).every(function(k){
      return answerMatches(ss.inputs[k], step.a[k], step.accept, step.expr);
    });
  });
}
function isSlideAttempted(tabId, i){
  var slide = SLIDES[tabId][i], item = state.tabs[tabId].items[i];
  if(slide.kind==='mcq') return item.choice !== undefined;
  return slide.flat.some(function(step, si){
    var ss = item.stepStates[si];
    return Object.keys(step.a).some(function(k){
      return ss.inputs[k] && String(ss.inputs[k]).trim() !== '';
    });
  });
}

function renderFinished(){
  var ts=state.tabs[activeTab], slides=SLIDES[activeTab];
  if(MODE==='quiz'){
    var correctCount=0, attemptedCount=0;
    var rowsHtml = slides.map(function(slide, i){
      var item = ts.items[i];
      var ok = isSlideCorrect(activeTab, i);
      var att = isSlideAttempted(activeTab, i);
      if(ok) correctCount++;
      if(att) attemptedCount++;
      var tagCls = ok ? 'ok' : (att ? 'bad' : 'na');
      var tagText = ok ? 'Correct' : (att ? 'Incorrect' : 'Not attempted');
      
      var yourAns = '—';
      var rightAns = '';
      if(slide.kind==='mcq'){
        yourAns = item.choice !== undefined ? '('+LETTERS[item.choice]+') '+cleanText(slide.opts[item.choice]) : '—';
        rightAns = '('+LETTERS[slide.correct]+') '+cleanText(slide.opts[slide.correct]);
      } else {
        yourAns = slide.flat.map(function(step, si){
          return Object.keys(step.a).map(function(k){ return item.stepStates[si].inputs[k] || '—'; }).join(', ');
        }).join(' | ');
        rightAns = slide.flat.map(function(step){
          return Object.values(step.a).join(', ');
        }).join(' | ');
      }
      
      var row = '<div class="review-row">';
      row += '<span class="review-tag '+tagCls+'">Q'+(i+1)+' · '+tagText+'</span>';
      row += '<div class="review-q">'+cleanText(slide.text || slide.p)+'</div>';
      row += '<div class="review-ans"><b>Your response:</b> '+esc(yourAns)+'</div>';
      if(!ok) row += '<div class="review-ans" style="color:var(--success);"><b>Correct key:</b> '+esc(rightAns)+'</div>';
      if(slide.sol) row += '<div class="sol-line" style="margin-top:6px;font-size:12.5px;color:var(--ink-soft);"><b>Explanation:</b> '+esc(cleanText(slide.sol))+'</div>';
      row += '</div>';
      return row;
    }).join('');

    var h = '<div class="qcard done-card" style="text-align:left;">';
    h += '<div style="text-align:center;"><div style="font-size:38px;">🏁</div><h2>Quiz Assessment Results</h2>';
    h += '<p style="color:var(--ink-soft);font-size:14px;">Score: <b>'+correctCount+' / '+slides.length+'</b> correct ('+attemptedCount+' attempted)</p></div>';
    h += '<div style="margin-top:16px;">'+rowsHtml+'</div>';
    h += '<div style="text-align:center;margin-top:16px;"><button class="btn btn-primary" id="btnRestart">Review Section</button></div>';
    h += '</div>';
    document.getElementById('wrap').innerHTML = h;
    document.getElementById('navbarInner').innerHTML = '';
    document.getElementById('btnRestart').addEventListener('click', function(){ ts.idx=0; renderSlide(); });
    playSuccess();
    applyKaTeX();
    return;
  }

  var correct = ts.items.filter(function(i){ return i.status==='correct'; }).length;
  var revealed = ts.items.filter(function(i){ return i.status==='revealed'; }).length;
  var skipped = ts.items.filter(function(i){ return i.status==='skipped'; }).length;

  var h='<div class="qcard done-card"><div style="font-size:38px;">🎉</div><h2>Section Complete</h2>'+
     '<div class="score-pills">'+
     '<span class="score-pill" style="background:var(--success-soft);color:var(--success);">'+correct+' Correct</span>'+
     '<span class="score-pill" style="background:var(--danger-soft);color:var(--danger);">'+revealed+' Revealed</span>'+
     '<span class="score-pill" style="background:var(--gold-soft);color:var(--retry-text);">'+skipped+' Skipped</span>'+
     '</div>'+
     '<button class="btn btn-primary" id="btnRestart">Review from Question 1</button></div>';
  document.getElementById('wrap').innerHTML=h;
  document.getElementById('navbarInner').innerHTML='';
  document.getElementById('btnRestart').addEventListener('click', function(){ ts.idx=0; renderSlide(); });
  updateChapterProgress();
}

function updateChapterProgress(){
  var total=0, done=0;
  TAB_DEFS.forEach(function(td){
    state.tabs[td.id].items.forEach(function(it){
      total++; if(it.status==='correct'||it.status==='revealed'||it.status==='skipped') done++;
    });
  });
  var pct = total>0?Math.round((done/total)*100):0;
  document.getElementById('cpFill').style.width=pct+'%';
  document.getElementById('cpLabel').textContent=pct+'% complete';
}

function updateFab(){
  var slides=SLIDES[activeTab], done=state.tabs[activeTab].items.filter(function(it){ return it.status!=='unanswered'; }).length;
  document.getElementById('fabBadge').textContent=done+'/'+slides.length;
}

function buildPalette(){
  var slides=SLIDES[activeTab], body=document.getElementById('paletteBody'), html='';
  for(var i=0;i<slides.length;i++){
    var st = state.tabs[activeTab].items[i].status;
    if(i === state.tabs[activeTab].idx) st = 'current';
    html += '<div class="chip" data-status="'+st+'" data-idx="'+i+'">'+(i+1)+'</div>';
  }
  body.innerHTML = html;
  body.querySelectorAll('.chip').forEach(function(c){
    c.addEventListener('click', function(){
      state.tabs[activeTab].idx=parseInt(c.dataset.idx,10);
      document.getElementById('overlay').classList.remove('show');
      renderSlide();
    });
  });
}

document.getElementById('paletteFab').addEventListener('click', function(){ buildPalette(); document.getElementById('overlay').classList.add('show'); });
document.getElementById('paletteClose').addEventListener('click', function(){ document.getElementById('overlay').classList.remove('show'); });

/* =========================================================================
   VIRTUAL MATH KEYPAD LOGIC
   ========================================================================= */
document.querySelectorAll('.kbtn').forEach(function(btn){
  btn.addEventListener('pointerdown', function(e){ e.preventDefault(); });
  btn.addEventListener('click', function(e){
    e.preventDefault();
    if(!currentFocusedInput) return;
    var key = btn.dataset.key;
    var action = btn.dataset.action;
    var val = currentFocusedInput.value || '';
    var start = currentFocusedInput.selectionStart !== null ? currentFocusedInput.selectionStart : val.length;
    var end = currentFocusedInput.selectionEnd !== null ? currentFocusedInput.selectionEnd : val.length;

    if(action === 'backspace'){
      if(start > 0 || start !== end){
        if(start === end){
          currentFocusedInput.value = val.slice(0, start - 1) + val.slice(end);
          currentFocusedInput.setSelectionRange(start - 1, start - 1);
        } else {
          currentFocusedInput.value = val.slice(0, start) + val.slice(end);
          currentFocusedInput.setSelectionRange(start, start);
        }
      }
    } else if(action === 'clear'){
      currentFocusedInput.value = '';
    } else if(key !== undefined){
      currentFocusedInput.value = val.slice(0, start) + key + val.slice(end);
      currentFocusedInput.setSelectionRange(start + key.length, start + key.length);
    }
    currentFocusedInput.dispatchEvent(new Event('input', {bubbles: true}));
  });
});

document.getElementById('closeKeypadBtn').addEventListener('click', function(){
  document.getElementById('mathKeypad').classList.remove('show');
});

/* =========================================================================
   SCRATCHPAD (CANVAS) DRAWING ENGINE
   ========================================================================= */
var scratchCanvas = document.getElementById('scratchCanvas');
var ctx = scratchCanvas.getContext('2d');
var isDrawing = false;
var currentTool = 'pen';
var canvasInitialized = false;

function initCanvasSize(){
  var wrap = document.getElementById('spCanvasWrap');
  if(!wrap.clientWidth || !wrap.clientHeight) return;
  var dpr = window.devicePixelRatio || 1;
  scratchCanvas.width = wrap.clientWidth * dpr;
  scratchCanvas.height = wrap.clientHeight * dpr;
  ctx.scale(dpr, dpr);
  redrawGridBackground();
  canvasInitialized = true;
}

function redrawGridBackground(){
  var w = scratchCanvas.width / (window.devicePixelRatio || 1);
  var h = scratchCanvas.height / (window.devicePixelRatio || 1);
  ctx.save();
  ctx.strokeStyle = '#F0ECE1';
  ctx.lineWidth = 1;
  var step = 20;
  for(var x = 0; x < w; x += step){
    ctx.beginPath(); ctx.moveTo(x, 0); ctx.lineTo(x, h); ctx.stroke();
  }
  for(var y = 0; y < h; y += step){
    ctx.beginPath(); ctx.moveTo(0, y); ctx.lineTo(w, y); ctx.stroke();
  }
  ctx.restore();
}

function getPos(e){
  var rect = scratchCanvas.getBoundingClientRect();
  return {
    x: e.clientX - rect.left,
    y: e.clientY - rect.top
  };
}

scratchCanvas.addEventListener('pointerdown', function(e){
  isDrawing = true;
  scratchCanvas.setPointerCapture(e.pointerId);
  var pos = getPos(e);
  ctx.beginPath();
  ctx.moveTo(pos.x, pos.y);
  ctx.strokeStyle = currentTool === 'eraser' ? '#FFFFFF' : '#16264A';
  ctx.lineWidth = currentTool === 'eraser' ? 18 : 2.5;
  ctx.lineCap = 'round';
  ctx.lineJoin = 'round';
});

scratchCanvas.addEventListener('pointermove', function(e){
  if(!isDrawing) return;
  var pos = getPos(e);
  ctx.lineTo(pos.x, pos.y);
  ctx.stroke();
});

scratchCanvas.addEventListener('pointerup', function(e){
  isDrawing = false;
  try{ scratchCanvas.releasePointerCapture(e.pointerId); }catch(err){}
});
scratchCanvas.addEventListener('pointercancel', function(){ isDrawing = false; });

document.getElementById('spToolPen').addEventListener('click', function(){
  currentTool = 'pen';
  this.classList.add('active');
  document.getElementById('spToolEraser').classList.remove('active');
});

document.getElementById('spToolEraser').addEventListener('click', function(){
  currentTool = 'eraser';
  this.classList.add('active');
  document.getElementById('spToolPen').classList.remove('active');
});

document.getElementById('spToolClear').addEventListener('click', function(){
  var w = scratchCanvas.width / (window.devicePixelRatio || 1);
  var h = scratchCanvas.height / (window.devicePixelRatio || 1);
  ctx.clearRect(0, 0, w, h);
  redrawGridBackground();
});

document.getElementById('scratchFab').addEventListener('click', function(){
  document.getElementById('scratchOverlay').classList.add('show');
  if(!canvasInitialized) setTimeout(initCanvasSize, 50);
});

document.getElementById('spToolClose').addEventListener('click', function(){
  document.getElementById('scratchOverlay').classList.remove('show');
});

function showChrome(show){
  document.querySelector('.tabbar').style.display = show?'':'none';
  document.querySelector('.slide-progress').style.display = show?'':'none';
  document.querySelector('.navbar').style.display = show?'':'none';
  document.getElementById('paletteFab').style.display = show?'':'none';
  document.getElementById('scratchFab').style.display = show?'':'none';
}
function updateModePill(){
  document.getElementById('modePill').textContent = MODE==='quiz'?'📝 Quiz Mode · switch':'📘 Learning Sheet · switch';
}
function renderModePicker(){
  showChrome(false);
  var wrap=document.getElementById('wrap');
  wrap.innerHTML='<div class="mode-pick">'+
    '<div class="mode-card" data-pick="learning"><h3>📘 Learning Sheet</h3><p>Step-by-step guidance with live hints and immediate retries.</p></div>'+
    '<div class="mode-card" data-pick="quiz"><h3>📝 Quiz Mode</h3><p>Exam simulation with score summaries revealed at the end.</p></div>'+
    '</div>';
  wrap.querySelectorAll('[data-pick]').forEach(function(card){
    card.addEventListener('click', function(){
      setMode(card.dataset.pick);
      document.getElementById('modePill').hidden=false;
      updateModePill(); showChrome(true); buildTabbar(); renderSlide();
    });
  });
}

document.getElementById('modePill').addEventListener('click', function(){
  setMode(MODE==='quiz'?'learning':'quiz');
  updateModePill(); buildTabbar(); renderSlide();
});

window.addEventListener('load', function(){
  applyKaTeX();
});

renderLogin();
})();
</script>
</body>
</html>
