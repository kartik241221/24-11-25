<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Happy Birthday — For Her</title>
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg1: #ff9a9e;
    --bg2: #fad0c4;
    --accent: #ff6b81;
    --accent2: #7ee8fa;
    --text: #2b2b2b;
    --glass: rgba(255,255,255,0.12);
  }
  *{box-sizing:border-box}
  html,body{height:100%}
  body{
    margin:0;
    font-family: 'Poppins',system-ui,Segoe UI,Roboto,Arial;
    color:var(--text);
    -webkit-font-smoothing:antialiased;
    -moz-osx-font-smoothing:grayscale;
    background: linear-gradient(120deg,var(--bg1),var(--bg2));
    overflow:hidden;
    display:flex;
    align-items:center;
    justify-content:center;
  }

  /* main container */
  .card{
    width:min(1100px,95vw);
    height:min(700px,90vh);
    background: linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.02));
    border-radius:20px;
    box-shadow: 0 10px 40px rgba(0,0,0,0.18);
    position:relative;
    overflow:hidden;
    padding:30px;
    display:grid;
    grid-template-columns: 1fr 420px;
    gap:24px;
    backdrop-filter: blur(6px) saturate(120%);
  }

  /* left area: big message */
  .hero{
    padding:28px;
    display:flex;
    flex-direction:column;
    justify-content:center;
    gap:18px;
    position:relative;
  }
  .greeting{
    font-family: 'Great Vibes', cursive;
    font-size: clamp(40px,6.5vw,84px);
    color: white;
    letter-spacing:1px;
    text-shadow: 0 6px 30px rgba(0,0,0,0.25);
    line-height:0.9;
  }
  .subtitle{
    color: rgba(255,255,255,0.95);
    font-weight:500;
    font-size:clamp(14px,2vw,18px);
    max-width:60ch;
    text-shadow: 0 2px 8px rgba(0,0,0,0.12);
  }

  /* typing effect */
  .typewriter {
    font-weight:600;
    font-size:clamp(16px,1.6vw,20px);
    color: #fff;
    display:inline-block;
    white-space:nowrap;
    overflow:hidden;
    border-right: .14em solid rgba(255,255,255,0.6);
    animation: typing 5s steps(40,end), blink-caret .7s step-end infinite;
    max-width:95%;
    box-decoration-break:clone;
    text-shadow: 0 3px 8px rgba(0,0,0,0.14);
  }
  @keyframes typing {
    from { width:0%; }
    to { width:100%; }
  }
  @keyframes blink-caret {
    50% { border-color: transparent; }
  }

  /* right area: interactive card */
  .panel{
    padding:20px;
    border-radius:16px;
    background: linear-gradient(180deg, rgba(255,255,255,0.04), rgba(255,255,255,0.02));
    box-shadow: inset 0 1px 0 rgba(255,255,255,0.02);
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    gap:18px;
  }

  .gift {
    width:180px;height:180px;border-radius:18px;
    background:linear-gradient(135deg,var(--accent), #ffb199);
    position:relative;
    display:flex;align-items:center;justify-content:center;
    cursor:pointer;
    transition: transform .28s cubic-bezier(.2,.9,.3,1);
    box-shadow: 0 10px 30px rgba(0,0,0,0.25);
    border: 4px solid rgba(255,255,255,0.12);
  }
  .gift:hover{ transform: translateY(-10px) rotate(-2deg) scale(1.02); }
  .ribbon{
    position:absolute; inset:0; pointer-events:none;
    display:flex; align-items:center; justify-content:center;
  }
  .ribbon::before,
  .ribbon::after{
    content:"";
    position:absolute;
    width:40%; height:24%;
    background: linear-gradient(90deg, rgba(255,255,255,0.55), rgba(255,255,255,0.1));
    transform: rotate(20deg);
    border-radius:8px;
    filter:drop-shadow(0 2px 6px rgba(0,0,0,0.25));
  }
  .ribbon::after{ transform: rotate(-20deg); width:60%; height:18%; }

  .bow{
    width:70px;height:70px;border-radius:50%;
    background: radial-gradient(circle at 30% 30%, rgba(255,255,255,.9), rgba(255,255,255,.18) 30%, transparent 40%), linear-gradient(90deg,#fff0,#ffffff10);
    border:3px solid rgba(255,255,255,0.18);
    transform-origin:center;
    animation: bowFloat 3s ease-in-out infinite;
  }
  @keyframes bowFloat {
    0%,100% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-6px) rotate(6deg); }
  }

  .hint{ color: rgba(255,255,255,0.9); font-size:14px; text-align:center; max-width:260px; }
  .btn-row{ display:flex; gap:10px; align-items:center; }

  .btn{
    background: rgba(255,255,255,0.12);
    color:white;
    padding:10px 14px;
    border-radius:10px;
    border:1px solid rgba(255,255,255,0.06);
    cursor:pointer;
    font-weight:600;
    transition:transform .18s ease, background .18s ease;
  }
  .btn:hover{ transform: translateY(-4px); background: rgba(255,255,255,0.18); }

  /* balloons & little hearts */
  .balloon{
    position:absolute;
    width:60px;height:84px;border-radius:50% 50% 45% 45%;
    background: radial-gradient(circle at 30% 20%, rgba(255,255,255,0.8), rgba(255,255,255,0.06) 15%), var(--accent);
    opacity:0.95;
    transform-origin:center bottom;
    animation: floatUp linear infinite;
  }
  @keyframes floatUp{
    from{ transform: translateY(20vh) rotate(-6deg); opacity:0 }
    10%{opacity:1}
    to{ transform: translateY(-140vh) rotate(6deg); opacity:0.9 }
  }
  .string{
    position:absolute; left:50%; top:90%; width:2px; height:80px; background: rgba(0,0,0,0.08);
    transform-origin:top; border-radius:2px;
  }

  /* floating heart particles */
  .heart{
    position:absolute;
    width:28px;height:28px;
    transform: rotate(-45deg) scale(.9);
    animation: drift .6s linear infinite;
    opacity:.95;
  }
  .heart:before,
  .heart:after{
    content:""; position:absolute; width:28px;height:28px; background:var(--accent);
    border-radius:50%;
  }
  .heart:before{ top:-14px; left:0; }
  .heart:after{ left:14px; top:0; }

  @keyframes drift{
    0%{ transform:translateY(0) translateX(0) rotate(-45deg) scale(.8) }
    50%{ transform:translateY(-40px) translateX(18px) rotate(-10deg) scale(1) }
    100%{ transform:translateY(-80px) translateX(-8px) rotate(20deg) scale(.9) }
  }

  /* modal note */
  .note-modal{
    position: fixed;
    inset:0;
    display:flex;
    align-items:center;
    justify-content:center;
    background: rgba(10,10,12,0.45);
    z-index:99;
    opacity:0;
    pointer-events:none;
    transition: opacity .28s ease;
  }
  .note-modal.show{ opacity:1; pointer-events:auto; }
  .note{
    width:min(900px,92vw);
    max-height:86vh;
    background: linear-gradient(180deg,#fffefc, #fff7f4);
    border-radius:14px;
    box-shadow: 0 25px 80px rgba(0,0,0,0.35);
    padding:26px;
    overflow:auto;
    position:relative;
  }
  .close{
    position:absolute; top:12px; right:12px; background:transparent; border:0; font-size:22px; cursor:pointer;
  }

  /* SVG handwritten effect */
  .handwriting{
    width:100%;
    height:auto;
    display:block;
    margin:10px 0 14px;
  }
  .stroke{
    stroke: #a53b57; stroke-width:2.4; fill:none;
    stroke-linecap:round; stroke-linejoin:round;
    stroke-dasharray: 1000;
    stroke-dashoffset: 1000;
    animation: draw 3.6s ease forwards;
  }
  @keyframes draw{
    to{ stroke-dashoffset: 0; }
  }

  .note p{ color:#333; font-size:18px; line-height:1.6; margin:14px 0; }
  .note .signature{ font-family: 'Great Vibes', cursive; font-size:40px; color:var(--accent); display:block; margin-top:18px; }

  /* confetti canvas */
  #confettiCanvas{ position:absolute; inset:0; pointer-events:none; z-index:9; }

  /* responsive */
  @media (max-width:950px){
    .card{ grid-template-columns: 1fr; grid-auto-rows:auto; height:auto; padding:18px; gap:12px; }
    .panel{ order:-1; }
  }
</style>
</head>
<body>
<div class="card" role="main" aria-label="Birthday card for her">
  <!-- confetti canvas -->
  <canvas id="confettiCanvas"></canvas>

  <!-- left: hero -->
  <div class="hero">
    <div class="greeting" aria-hidden="true">Happy Birthday, <span id="herName">My Love</span> 💖</div>
    <div class="subtitle">
      <span class="typewriter" id="typedMessage">
        <!-- Default message — customize below in JS -->
      </span>
    </div>

    <div style="display:flex; gap:12px; margin-top:12px; align-items:center;">
      <button class="btn" id="openNoteBtn" aria-haspopup="dialog">Open Your Special Note ✨</button>
      <button class="btn" id="surpriseBtn">Surprise Me — Gift 🎁</button>
    </div>

    <!-- scattered hearts -->
    <div aria-hidden="true">
      <div class="heart" style="left:8%; bottom:6%; animation-duration:1.2s;"></div>
      <div class="heart" style="left:24%; bottom:14%; animation-duration:1.0s; background:transparent;"></div>
      <div class="heart" style="left:62%; bottom:22%; animation-duration:1.5s;"></div>
      <div class="heart" style="left:82%; bottom:8%; animation-duration:1.3s;"></div>
    </div>
  </div>

  <!-- right: interactive panel -->
  <div class="panel" aria-hidden="false">
    <div class="gift" id="giftBox" tabindex="0" role="button" aria-label="Open gift box">
      <div class="ribbon"></div>
      <div class="bow" aria-hidden="true"></div>
    </div>

    <div class="hint">Click the gift for a confetti surprise and open your special handwritten birthday note.</div>
    <div class="btn-row">
      <button class="btn" id="toggleBalloons">Toggle Balloons</button>
      <button class="btn" id="downloadNote">Save Note</button>
    </div>
  </div>

  <!-- floating balloons (generated by JS) -->
</div>

<!-- modal note -->
<div class="note-modal" id="noteModal" role="dialog" aria-modal="true" aria-labelledby="noteTitle">
  <div class="note" role="document">
    <button class="close" id="closeNote" aria-label="Close note">✕</button>
    <svg class="handwriting" viewBox="0 0 1000 120" preserveAspectRatio="xMidYMid meet">
      <!-- stylized "Happy Birthday" scripted stroke path (approximate) -->
      <path class="stroke" d="M20 80 C80 30, 180 10, 260 70 C320 120, 380 20, 460 60 C540 100, 620 10, 700 60 C780 110, 840 30, 920 70"/>
    </svg>

    <h2 id="noteTitle" style="margin:6px 0 0; font-size:22px; color:#8b2f4b;">A little note for <span id="noteName">My Love</span></h2>

    <p id="noteText">
      <!-- default — customizable in JS below -->
    </p>

    <span class="signature" id="signedName">With all my heart, — Yours</span>
  </div>
</div>

<script>
/* ---------- CUSTOMIZE THESE VALUES ---------- */
/* Change the name and the messages here */
const HER_NAME = "Anaya"; // <-- put her name here
const TYPING_MESSAGES = [
  To ${HER_NAME}, the one who lights up my every day.,
  Today we celebrate you — your smile, your soul, your magic.,
  I love you now, always, and forever.
];
const NOTE_TEXT = `My dearest ${HER_NAME},

On your birthday I wish for you laughter that never ends, quiet moments that heal, dreams that feel within reach and adventures that make your heart race. Thank you for being the warmth in my life — the gentle voice when I'm afraid, the wild spark when I need to dance, and the safe place to call home.

May this year give you all the joy you give me every day.
Happy Birthday, my love.`;

const SIGNATURE = "— Kartik"; // <-- change your signature here
/* -------------------------------------------- */

document.getElementById('herName').textContent = HER_NAME;
document.getElementById('noteName').textContent = HER_NAME;
document.getElementById('noteText').textContent = NOTE_TEXT;
document.getElementById('signedName').textContent = SIGNATURE;

/* typing effect tweaks (cycles through TYPING_MESSAGES) */
const typedEl = document.getElementById('typedMessage');
let idx = 0;
function startTypeCycle(){
  const text = TYPING_MESSAGES[idx % TYPING_MESSAGES.length];
  // simple type animation reset by switching content & restart CSS animation
  typedEl.style.animation = 'none';
  void typedEl.offsetWidth;
  typedEl.textContent = text;
  typedEl.style.animation = '';
  idx++;
}
startTypeCycle();
setInterval(startTypeCycle, 5200);


/* ---------- BALLOONS GENERATION ---------- */
let balloonsOn = true;
const card = document.querySelector('.card');

const balloonColors = [
  'linear-gradient(135deg,#ff7eb3,#ff758c)',
  'linear-gradient(135deg,#7ef6ff,#7ee8fa)',
  'linear-gradient(135deg,#ffd89b,#f6a6a6)',
  'linear-gradient(135deg,#c7f9cc,#92e3a9)'
];

function createBalloon(xPercent, delay, size=60, colorIndex=0){
  const b = document.createElement('div');
  b.className = 'balloon';
  b.style.left = xPercent+'%';
  b.style.bottom = '-10%';
  b.style.width = size+'px';
  b.style.height = Math.round(size*1.25)+'px';
  b.style.background = balloonColors[colorIndex % balloonColors.length];
  b.style.animationDuration = (8 + Math.random()*8) + 's';
  b.style.animationDelay = (delay || 0) + 's';
  const s = document.createElement('div');
  s.className = 'string';
  s.style.height = Math.max(60, size*1.2)+'px';
  b.appendChild(s);
  document.body.appendChild(b);
  return b;
}
let balloonEls = [];
function spawnBalloons(){
  // clear existing
  balloonEls.forEach(e=>e.remove());
  balloonEls = [];
  for(let i=0;i<8;i++){
    balloonEls.push(createBalloon(5 + i*11 + Math.random()*6, Math.random()*3, 48 + Math.random()*50, i));
  }
}
spawnBalloons();

/* toggle balloons */
document.getElementById('toggleBalloons').addEventListener('click', ()=>{
  balloonsOn = !balloonsOn;
  balloonEls.forEach(el => el.style.display = balloonsOn ? 'block' : 'none');
});

/* ---------- CONFETTI (canvas) ---------- */
const canvas = document.getElementById('confettiCanvas');
const ctx = canvas.getContext('2d');
let W=canvas.width=innerWidth;
let H=canvas.height=innerHeight;
window.addEventListener('resize', ()=>{ W=canvas.width=innerWidth; H=canvas.height=innerHeight; });

class Confetto {
  constructor(){
    this.reset();
  }
  reset(){
    this.x = Math.random()*W;
    this.y = -10 - Math.random()*H*0.2;
    this.size = 6 + Math.random()*10;
    this.color = ['#ffc0cb','#ff7b7b','#ffd166','#9be7ff','#ffb6c1'][Math.floor(Math.random()*5)];
    this.gravity = 0.3 + Math.random()*0.6;
    this.velX = -2 + Math.random()*4;
    this.velY = 2 + Math.random()*4;
    this.spin = Math.random()*0.3;
    this.tilt = Math.random()*Math.PI;
  }
  update(){
    this.x += this.velX;
    this.y += this.velY;
    this.velY += this.gravity*0.03;
    this.tilt += this.spin;
    if(this.y > H + 30 || this.x < -50 || this.x > W + 50) this.reset();
  }
  draw(ctx){
    ctx.save();
    ctx.translate(this.x, this.y);
    ctx.rotate(Math.sin(this.tilt));
    ctx.fillStyle = this.color;
    ctx.beginPath();
    ctx.rect(-this.size/2, -this.size/2, this.size, this.size*0.6);
    ctx.fill();
    ctx.restore();
  }
}
let confetti = [];
for(let i=0;i<80;i++) confetti.push(new Confetto());

let confettiActive = false;
function render(){
  ctx.clearRect(0,0,W,H);
  if(confettiActive){
    confetti.forEach(c=>{ c.update(); c.draw(ctx); });
  }
  requestAnimationFrame(render);
}
render();

function burstConfetti(){
  confettiActive = true;
  // initial burst: boost velocities
  confetti.forEach(c => { c.x = W/2 + (Math.random()-0.5)*200; c.y = H/2 + (Math.random()-0.5)*100; c.velX = -6 + Math.random()*12; c.velY = -10 + Math.random()*8; });
  setTimeout(()=> confettiActive = false, 3000);
}

/* ---------- GIFT BOX interactions ---------- */
const gift = document.getElementById('giftBox');
const openNoteBtn = document.getElementById('openNoteBtn');

gift.addEventListener('click', ()=> {
  gift.classList.add('opened');
  burstConfetti();
  showNote();
  // tiny bounce
  gift.animate([{transform:'translateY(0)'},{transform:'translateY(-18px)'},{transform:'translateY(0)'}], { duration:420, easing:'cubic-bezier(.2,.9,.3,1)' });
});
gift.addEventListener('keydown', (e) => { if(e.key === 'Enter' || e.key === ' ') gift.click(); });
document.getElementById('surpriseBtn').addEventListener('click', ()=> { gift.click(); });

openNoteBtn.addEventListener('click', showNote);

/* ---------- NOTE modal ---------- */
const modal = document.getElementById('noteModal');
const closeBtn = document.getElementById('closeNote');
function showNote(){
  modal.classList.add('show');
  // replay handwriting SVG animation by reflow
  const stroke = document.querySelector('.stroke');
  stroke.style.animation = 'none';
  void stroke.offsetWidth;
  stroke.style.animation = '';
}
closeBtn.addEventListener('click', ()=> modal.classList.remove('show'));
modal.addEventListener('click', (e)=> { if(e.target === modal) modal.classList.remove('show'); });

/* ---------- Download the note as text file (simple) ---------- */
document.getElementById('downloadNote').addEventListener('click', ()=>{
  const content = ${document.getElementById('noteText').textContent}\n\n${SIGNATURE || ''};
  const blob = new Blob([content], {type:'text/plain'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url; a.download = ${HER_NAME}-birthday-note.txt;
  document.body.appendChild(a); a.click(); a.remove();
  URL.revokeObjectURL(url);
});

/* ---------- small entrance animations ---------- */
document.querySelector('.card').animate([{opacity:0, transform:'scale(.98)'},{opacity:1, transform:'scale(1)'}], {duration:800, easing:'cubic-bezier(.2,.9,.28,1)'});

/* ---------- Accessibility tweak: focus styles ---------- */
gift.addEventListener('focus', ()=> gift.style.outline='3px solid rgba(255,255,255,0.14)');
gift.addEventListener('blur', ()=> gift.style.outline='none');

/* ---------- Optional: small keyboard shortcut to toggle note (N) ---------- */
document.addEventListener('keyup', (e)=> { if(e.key.toLowerCase() === 'n') modal.classList.toggle('show'); });

/* ---------- END ---------- */
</script>

</body>
</html>
