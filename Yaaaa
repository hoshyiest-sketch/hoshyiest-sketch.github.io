# hoshyiest-sketch.github.io
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Kink Jars</title>
<meta name="description" content="Fill your jars, pick your color, save your picture.">
<meta property="og:title" content="Kink Jars">
<meta property="og:description" content="Fill your jars, pick your color, save your picture.">
<meta name="robots" content="noindex">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@500;600;700&family=Permanent+Marker&family=Nunito:wght@400;700;800&display=swap" rel="stylesheet">
<style>
  :root{--c:#e63946;--on-c:#fff;--ink:#1d1a17;--bg:#fbf6ef;--card:#fff;--muted:#6b625a;--line:#e9e0d5}
  *{box-sizing:border-box}
  html{-webkit-text-size-adjust:100%}
  body{margin:0;background:var(--bg);color:var(--ink);font-family:Nunito,system-ui,sans-serif;font-size:18px;line-height:1.45;padding-bottom:110px}
  @media(min-width:960px){body{padding-bottom:40px}}
  .wrap{max-width:1180px;margin:0 auto;padding:28px 16px}
  header{margin-bottom:22px}
  header h1{font-family:Oswald,sans-serif;font-weight:700;font-size:clamp(44px,9vw,68px);margin:0;line-height:1}
  header h1 span{color:var(--c);-webkit-text-stroke:2px var(--ink);paint-order:stroke fill}
  header p{margin:10px 0 0;color:var(--muted);max-width:640px}
  .layout{display:grid;gap:24px}
  @media(min-width:960px){.layout{grid-template-columns:minmax(0,1fr) 430px}.side{position:sticky;top:20px;align-self:start}}
  .panel{background:var(--card);border:2px solid var(--line);border-radius:22px;padding:20px;margin-bottom:20px}
  .step{font-family:Oswald,sans-serif;font-weight:600;font-size:14px;letter-spacing:.1em;text-transform:uppercase;color:var(--muted)}
  h2{font-family:Oswald,sans-serif;font-weight:600;font-size:27px;margin:2px 0 12px;line-height:1.15}
  .hint{color:var(--muted);font-size:16px;margin:-4px 0 14px}
  input[type=text]{font:inherit;font-size:20px;width:100%;padding:14px 16px;border:2px solid var(--line);border-radius:14px;background:#fff;color:var(--ink)}
  input[type=text]:focus{border-color:var(--ink);outline:none}
  button{font:inherit;cursor:pointer;color:var(--ink)}
  button:focus-visible,input:focus-visible{outline:3px solid var(--ink);outline-offset:3px}

  /* color picker */
  .picker{display:grid;gap:18px}
  @media(min-width:620px){.picker{grid-template-columns:1fr 170px;align-items:center}}
  .swatches{display:grid;grid-template-columns:repeat(6,1fr);gap:10px;max-width:420px}
  .sw{aspect-ratio:1;border-radius:50%;border:3px solid #fff;box-shadow:0 0 0 2px var(--line);padding:0;min-width:40px}
  .sw[aria-pressed=true]{box-shadow:0 0 0 3px var(--ink)}
  .sliders{display:grid;gap:12px;margin-top:16px;max-width:420px}
  .sl{display:grid;grid-template-columns:52px 1fr 44px;align-items:center;gap:10px;font-weight:700;font-size:16px}
  .sl output{text-align:right;color:var(--muted);font-variant-numeric:tabular-nums}
  input[type=range]{-webkit-appearance:none;appearance:none;width:100%;height:26px;border-radius:13px;border:2px solid var(--ink);margin:0;background:#ccc}
  input[type=range]::-webkit-slider-thumb{-webkit-appearance:none;width:30px;height:30px;border-radius:50%;background:#fff;border:3px solid var(--ink);box-shadow:0 2px 4px rgba(0,0,0,.25)}
  input[type=range]::-moz-range-thumb{width:26px;height:26px;border-radius:50%;background:#fff;border:3px solid var(--ink)}
  .hexrow{display:flex;gap:10px;align-items:center;margin-top:14px;flex-wrap:wrap}
  .hexrow input{width:130px;font-size:18px;padding:10px 12px;font-family:ui-monospace,Menlo,monospace;text-transform:uppercase}
  .ghost{background:#fff;border:2px solid var(--ink);border-radius:999px;padding:9px 16px;font-weight:700;font-size:16px}
  .ghost:hover{background:var(--bg)}
  .preview-jars{display:flex;justify-content:center;gap:2px}
  .preview-jars canvas{width:62px;height:101px}

  /* questions */
  .q{display:grid;grid-template-columns:76px 1fr;gap:14px;align-items:center;padding:14px 0;border-top:2px dashed var(--line)}
  .q:first-of-type{border-top:0}
  .q canvas{width:76px;height:124px}
  .qnum{font-size:14px;color:var(--muted);font-weight:700}
  .qlabel{font-family:Oswald,sans-serif;font-weight:600;font-size:25px;line-height:1.1;margin:2px 0 10px}
  .scale{display:grid;grid-template-columns:repeat(5,1fr);gap:7px;max-width:380px}
  .scale button{height:52px;border-radius:14px;border:2px solid var(--ink);background:#fff;font-family:Oswald,sans-serif;font-weight:600;font-size:22px;transition:transform .08s}
  .scale button:active{transform:scale(.94)}
  .scale button[aria-pressed=true]{background:var(--c);color:var(--on-c);box-shadow:0 3px 0 var(--ink)}
  .ends{display:flex;justify-content:space-between;max-width:380px;font-size:13px;color:var(--muted);font-weight:700;margin-top:5px}

  /* poster + save */
  .poster{width:100%;height:auto;display:block;border-radius:12px;border:2px solid var(--line);background:#fff}
  .big{display:block;width:100%;margin-top:16px;padding:18px 20px;border-radius:18px;border:3px solid var(--ink);background:var(--c);color:var(--on-c);font-family:Oswald,sans-serif;font-weight:700;font-size:26px;letter-spacing:.02em;box-shadow:0 5px 0 var(--ink)}
  .big:active{transform:translateY(3px);box-shadow:0 2px 0 var(--ink)}
  .small-links{display:flex;justify-content:space-between;gap:10px;margin-top:14px;font-size:15px;color:var(--muted)}
  .linkbtn{background:none;border:0;padding:4px 0;text-decoration:underline;color:var(--muted);font-size:15px}

  .bar{position:fixed;left:0;right:0;bottom:0;background:rgba(251,246,239,.96);border-top:2px solid var(--line);backdrop-filter:blur(6px);z-index:5}
  .bar-in{max-width:1180px;margin:0 auto;padding:10px 16px calc(10px + env(safe-area-inset-bottom));display:flex;align-items:center;gap:14px}
  .bar-in span{font-weight:700;font-size:15px;color:var(--muted);flex:1}
  .bar .big{width:auto;margin:0;padding:12px 22px;font-size:21px;box-shadow:0 4px 0 var(--ink)}
  @media(min-width:960px){.bar{display:none}}

  #modal{position:fixed;inset:0;background:rgba(20,16,12,.6);display:flex;align-items:center;justify-content:center;padding:16px;z-index:10}
  #modal[hidden]{display:none}
  .sheet{background:#fff;border-radius:22px;padding:20px;max-width:440px;width:100%;max-height:92vh;overflow:auto;text-align:center}
  .sheet h3{font-family:Oswald,sans-serif;font-size:28px;margin:0 0 6px}
  .sheet p{margin:0 0 12px;color:var(--muted);font-size:16px}
  .sheet img{width:100%;border-radius:10px;border:2px solid var(--line)}
  .privacy{font-size:14px;color:var(--muted);text-align:center;margin-top:8px}
</style>
</head>
<body>
<div class="wrap">
  <header>
    <h1>Fill your <span>jars</span></h1>
    <p>Pick a color, rate each one from 1 (a little) to 5 (overflowing), then save your picture. Not your thing? Skip it and the jar stays empty.</p>
  </header>

  <div class="layout">
    <main>
      <section class="panel">
        <div class="step">Step 1</div>
        <h2>What's your name?</h2>
        <p class="hint">It goes on the blank line at the top. Nickname is fine, or leave it blank.</p>
        <input type="text" id="name" maxlength="24" autocomplete="off" placeholder="Your name">
      </section>

      <section class="panel">
        <div class="step">Step 2</div>
        <h2>Pick your color</h2>
        <div class="picker">
          <div>
            <div class="swatches" id="swatches" aria-label="Color choices"></div>
            <div class="sliders">
              <label class="sl">Red<input type="range" id="r" min="0" max="255"><output id="rv"></output></label>
              <label class="sl">Green<input type="range" id="g" min="0" max="255"><output id="gv"></output></label>
              <label class="sl">Blue<input type="range" id="b" min="0" max="255"><output id="bv"></output></label>
            </div>
            <div class="hexrow">
              <input type="text" id="hex" maxlength="7" spellcheck="false" aria-label="Color code">
              <button class="ghost" id="surprise" type="button">Surprise me</button>
            </div>
          </div>
          <div class="preview-jars" aria-hidden="true">
            <canvas id="pv1"></canvas><canvas id="pv2"></canvas><canvas id="pv3"></canvas>
          </div>
        </div>
      </section>

      <section class="panel">
        <div class="step">Step 3</div>
        <h2>Fill your jars</h2>
        <p class="hint">Tap a number. Tap it again to empty the jar.</p>
        <div id="questions"></div>
      </section>
    </main>

    <aside class="side">
      <section class="panel" id="done">
        <div class="step">Step 4</div>
        <h2>Your jars</h2>
        <canvas class="poster" id="poster" aria-label="Preview of your filled jars"></canvas>
        <button class="big" id="save" type="button">Save my jars</button>
        <div class="small-links">
          <span>Nothing leaves your phone.</span>
          <button class="linkbtn" id="reset" type="button">Start over</button>
        </div>
      </section>
    </aside>
  </div>
</div>

<div class="bar"><div class="bar-in"><span id="progress">0 of 28 filled</span><button class="big" id="saveBar" type="button">Save my jars</button></div></div>

<div id="modal" hidden role="dialog" aria-modal="true" aria-labelledby="mt">
  <div class="sheet">
    <h3 id="mt">Here are your jars!</h3>
    <p>If it didn't download, press and hold the picture (or right-click it) and choose “Save image.”</p>
    <img id="modalImg" alt="Your filled jars">
    <button class="big" id="closeModal" type="button">Done</button>
  </div>
</div>

<script>
/* ===== Edit the jars here. Each array is the label, one entry per line. ===== */
const JARS = [
  ["being","a dom"],["being","a sub"],["being","a switch"],["choking"],["being","choked"],["spanking"],["being","spanked"],
  ["ddlg / mdlb"],["age","play"],["doing stuff","in public"],["wax","play"],["water","sports"],["role","play"],["consensual","non consent"],
  ["having","orgasms","controlled"],["controlling","orgasms"],["gags"],["feet"],["anal"],["being","tied up"],["tying","people up"],
  ["humiliating","or","degrading"],["being","humiliated","or","degraded"],["bdsm"],["threesomes"],["sadism"],["masochism"],["spit"]
];
const PRESETS = ["#e63946","#ff5d8f","#ff8c42","#ffd23f","#7bd389","#2ec4b6","#3a86ff","#5b2a86","#c77dff","#8d1d3a","#8d5524","#2b2d42"];
const COLS = 7, INK = "#151311", PW = 1200;
const ROWS = Math.ceil(JARS.length / COLS);
const PH = 260 + (ROWS - 1) * 345 + 360;
const STORE = "kinkjars-v1";

/* ===== state ===== */
let state = { name: "", color: "#e63946", answers: JARS.map(() => 0) };
try {
  const s = JSON.parse(localStorage.getItem(STORE) || "null");
  if (s && Array.isArray(s.answers)) state = { ...state, ...s, answers: JARS.map((_, i) => s.answers[i] || 0) };
} catch (e) {}
const persist = () => { try { localStorage.setItem(STORE, JSON.stringify(state)); } catch (e) {} };

/* ===== color helpers ===== */
const hexToRgb = h => { h = h.replace("#", ""); if (h.length === 3) h = [...h].map(x => x + x).join(""); const n = parseInt(h, 16); return [n >> 16 & 255, n >> 8 & 255, n & 255]; };
const rgbToHex = a => "#" + a.map(v => Math.round(v).toString(16).padStart(2, "0")).join("");
const mix = (a, b, t) => a.map((v, i) => v + (b[i] - v) * t);
const css = (a, al = 1) => `rgba(${a.map(Math.round).join(",")},${al})`;
const lighten = (a, t) => css(mix(a, [255, 255, 255], t));
const darken = (a, t) => css(mix(a, [0, 0, 0], t));
const lum = ([r, g, b]) => (0.299 * r + 0.587 * g + 0.114 * b) / 255;

function rng(seed) { return () => { seed = seed + 0x6D2B79F5 | 0; let t = Math.imul(seed ^ seed >>> 15, 1 | seed); t = t + Math.imul(t ^ t >>> 7, 61 | t) ^ t; return ((t ^ t >>> 14) >>> 0) / 4294967296; }; }

/* ===== jar drawing (local box: 96 wide, 170 tall, lid at top) ===== */
function roundRect(c, x, y, w, h, r) { c.moveTo(x + r, y); c.arcTo(x + w, y, x + w, y + h, r); c.arcTo(x + w, y + h, x, y + h, r); c.arcTo(x, y + h, x, y, r); c.arcTo(x, y, x + w, y, r); c.closePath(); }
function bodyPath(c) {
  c.beginPath(); c.moveTo(14, 32);
  c.quadraticCurveTo(4, 36, 4, 60); c.lineTo(4, 146); c.quadraticCurveTo(4, 170, 28, 170);
  c.lineTo(68, 170); c.quadraticCurveTo(92, 170, 92, 146); c.lineTo(92, 60); c.quadraticCurveTo(92, 36, 82, 32);
  c.closePath();
}
function drawLid(c, dx = 0, dy = 0, rot = 0) {
  c.save(); c.translate(48 + dx, 12 + dy); c.rotate(rot); c.translate(-48, -12);
  c.beginPath(); roundRect(c, 6, 0, 84, 24, 6); c.fillStyle = "#fff"; c.fill();
  c.lineWidth = 4.5; c.strokeStyle = INK; c.stroke();
  c.lineWidth = 2.4; c.beginPath();
  for (const y of [8, 16]) { c.moveTo(10, y); c.quadraticCurveTo(48, y + 3, 86, y); }
  c.stroke(); c.restore();
}
function teardrop(c, x, y, r, ox, oy) { // tail points toward (ox,oy)
  const a = Math.atan2(oy - y, ox - x);
  c.moveTo(x + Math.cos(a) * r * 2.5, y + Math.sin(a) * r * 2.5);
  c.arc(x, y, r, a + Math.PI / 2, a + Math.PI * 1.5, false); c.closePath();
}
function heart(c, x, y, s) {
  c.moveTo(x, y + s * 0.9);
  c.bezierCurveTo(x - s * 1.6, y - s * 0.1, x - s * 0.8, y - s * 1.3, x, y - s * 0.45);
  c.bezierCurveTo(x + s * 0.8, y - s * 1.3, x + s * 1.6, y - s * 0.1, x, y + s * 0.9); c.closePath();
}
function blob(c, pts) {
  const n = pts.length, mid = i => [(pts[i][0] + pts[(i + 1) % n][0]) / 2, (pts[i][1] + pts[(i + 1) % n][1]) / 2];
  let m = mid(n - 1); c.moveTo(m[0], m[1]);
  for (let i = 0; i < n; i++) { m = mid(i); c.quadraticCurveTo(pts[i][0], pts[i][1], m[0], m[1]); }
  c.closePath();
}
function makeDrips(r, n, base, minL, maxL) {
  const span = 100 / n, out = [];
  for (let i = 0; i < n; i++) {
    const w = 9 + r() * 6;
    out.push({ cx: -2 + span * (i + 0.5) + (r() - 0.5) * span * 0.35, w, L: minL + r() * (maxL - minL) });
  }
  out.forEach(d => d.L = Math.min(d.L, 164 - base - d.w * 0.6));
  return out;
}
function collar(c, base, drips) {
  c.moveTo(4, 18); c.lineTo(92, 18);
  c.quadraticCurveTo(100, 22, 99, base - 4); c.quadraticCurveTo(99, base, 95, base);
  for (const d of [...drips].sort((a, b) => b.cx - a.cx)) {
    const r = d.w / 2;
    c.lineTo(d.cx + r + 4, base); c.quadraticCurveTo(d.cx + r, base, d.cx + r, base + 5);
    c.lineTo(d.cx + r * 0.8, base + d.L);
    c.arc(d.cx, base + d.L, r * 1.12, 0, Math.PI, false);
    c.lineTo(d.cx - r, base + 5); c.quadraticCurveTo(d.cx - r, base, d.cx - r - 4, base);
  }
  c.lineTo(1, base); c.quadraticCurveTo(-3, base, -3, base - 4); c.quadraticCurveTo(-4, 22, 4, 18); c.closePath();
}

/* Each jar gets one of six "overflow" looks, with its own random details. */
const STYLE_NAMES = ["drips", "puddle", "foam", "geyser", "splash", "hearts"];
function jarParams(idx) {
  const r = rng(idx * 7919 + 101);
  const row = Math.floor(idx / COLS), style = (idx % COLS + row * 3) % 6;
  const side = r() < 0.5 ? -1 : 1;
  const P = { style, phase: r() * 6.28, r };
  if (style === 0) { P.base = 40 + r() * 8; P.drips = makeDrips(r, 4 + (r() < 0.5 ? 1 : 0), P.base, 8, 125); }
  if (style === 1) {
    P.base = 40; P.drips = makeDrips(r, 3, P.base, 30, 90); P.drips[Math.floor(r() * 3)].L = 999;
    P.drips.forEach(d => d.L = Math.min(d.L, 164 - P.base - d.w * 0.6));
    const pts = [], rx = 64 + r() * 10, ry = 10 + r() * 3;
    for (let i = 0; i < 14; i++) { const a = i / 14 * Math.PI * 2, k = 0.86 + r() * 0.24; pts.push([48 + Math.cos(a) * rx * k, 170 + Math.sin(a) * ry * k]); }
    P.puddle = pts;
  }
  if (style === 2) {
    P.base = 38; P.drips = makeDrips(r, 3, P.base, 6, 45);
    P.foam = [];
    for (let i = 0; i < 14; i++) { const x = 48 + (r() - 0.5) * 88; P.foam.push([x, 28 - (1 - Math.abs(x - 48) / 46) * 34 - r() * 6, 7 + r() * 8]); }
    P.lid = { dx: side * (14 + r() * 8), dy: -24, rot: side * (0.2 + r() * 0.12) };
  }
  if (style === 3) {
    P.base = 40; P.drips = makeDrips(r, 4, P.base, 6, 70);
    P.drops = [[2 + r() * 8, -26, 4], [-10, -4 + r() * 6, 3.5], [-15, 20 + r() * 8, 3], [92 + r() * 6, -24, 4], [106, -2 + r() * 6, 3.5], [111, 22 + r() * 8, 3]];
    P.origin = [48, -20];
    P.lid = { dx: side * 36, dy: -26, rot: side * 0.6 };
  }
  if (style === 4) {
    P.base = 42; P.drips = makeDrips(r, 4, P.base, 10, 95);
    P.drops = []; P.origin = [48, 24];
    for (let i = 0; i < 6; i++) { const s = i % 2 ? 1 : -1; P.drops.push([48 + s * (60 + r() * 12), 4 + r() * 100, 2.6 + r() * 2]); }
    P.splats = [[-12 - r() * 6, 172, 7], [108 + r() * 6, 173, 6], [118, 166, 2.5], [-22, 166, 2.5]];
  }
  if (style === 5) {
    P.base = 44; P.drips = makeDrips(r, 5, P.base, 6, 105);
    P.hearts = [[14 + r() * 8, -14 - r() * 6, 7 + r() * 2], [48 + (r() - 0.5) * 10, -26, 9 + r() * 2], [80 + r() * 8, -12 - r() * 6, 6 + r() * 2]];
  }
  return P;
}

function drawJar(c, idx, level, rgb) {
  const P = jarParams(idx), r = P.r, fill = css(rgb);
  c.save(); c.lineJoin = "round"; c.lineCap = "round";

  // puddle sits under the jar
  if (level === 5 && P.puddle) {
    c.beginPath(); blob(c, P.puddle); c.lineWidth = 7; c.strokeStyle = INK; c.stroke(); c.fillStyle = fill; c.fill();
    c.beginPath(); c.ellipse(20, 172, 10, 2.5, 0, 0, 7); c.fillStyle = "rgba(255,255,255,.55)"; c.fill();
  }

  // liquid inside
  c.save(); bodyPath(c); c.fillStyle = "#fff"; c.fill(); c.clip();
  if (level > 0) {
    const top = 32, bottom = 170, frac = [0, .16, .36, .58, .8, 1][level];
    const ly = level === 5 ? 28 : bottom - (bottom - top) * frac, amp = level === 5 ? 0 : 2.2;
    const g = c.createLinearGradient(0, ly, 0, bottom); g.addColorStop(0, lighten(rgb, .12)); g.addColorStop(1, darken(rgb, .2));
    const surf = () => { for (let x = -4; x <= 100; x += 4) c.lineTo(x, ly + Math.sin(x * 0.11 + P.phase) * amp); };
    c.beginPath(); c.moveTo(-4, ly); surf(); c.lineTo(100, 180); c.lineTo(-4, 180); c.closePath(); c.fillStyle = g; c.fill();
    c.beginPath(); c.moveTo(-4, ly); surf(); c.strokeStyle = lighten(rgb, .45); c.lineWidth = 3; c.stroke();
    c.strokeStyle = css(mix(rgb, [255, 255, 255], .6), .85); c.lineWidth = 1.6;
    for (let i = 0; i < 2 + level; i++) {
      const bx = 18 + r() * 60, by = ly + 10 + r() * Math.max(0, bottom - ly - 22), br = 1.5 + r() * 2.6;
      c.beginPath(); c.arc(bx, by, br, 0, 7); c.stroke();
    }
  }
  c.fillStyle = "rgba(255,255,255,.5)"; c.beginPath(); roundRect(c, 11, 50, 6, 78, 3); roundRect(c, 11, 134, 6, 10, 3); c.fill();
  c.restore();

  // glass
  bodyPath(c); c.lineWidth = 4.5; c.strokeStyle = INK; c.stroke();
  c.lineWidth = 2.5; c.beginPath(); c.moveTo(18, 160); c.quadraticCurveTo(26, 165, 38, 164); c.moveTo(58, 164); c.quadraticCurveTo(70, 165, 78, 160); c.stroke();
  c.beginPath(); roundRect(c, 12, 20, 72, 14, 4); c.fillStyle = level === 5 ? fill : "#fff"; c.fill(); c.lineWidth = 4; c.stroke();

  // overflow!
  if (level === 5) {
    const shapes = [];
    const foamFill = lighten(rgb, .55);
    if (P.style === 3) shapes.push({ fill, path: () => {
      c.moveTo(34, 24); c.quadraticCurveTo(40, 4, 36, -8);
      c.quadraticCurveTo(26, -20, 38, -24); c.quadraticCurveTo(44, -36, 52, -25);
      c.quadraticCurveTo(60, -34, 64, -21); c.quadraticCurveTo(72, -14, 60, -8);
      c.quadraticCurveTo(56, 4, 62, 24); c.closePath(); } });
    shapes.push({ fill, path: () => collar(c, P.base, P.drips) });
    if (P.foam) for (const [x, y, rad] of P.foam) shapes.push({ fill: foamFill, path: () => c.arc(x, y, rad, 0, 7) });
    if (P.drops) for (const [x, y, rad] of P.drops) shapes.push({ fill, path: () => teardrop(c, x, y, rad, P.origin[0], P.origin[1]) });
    if (P.splats) for (const [x, y, rad] of P.splats) shapes.push({ fill, path: () => c.ellipse(x, y, rad, rad * 0.4, 0, 0, 7) });
    if (P.hearts) for (const [x, y, s] of P.hearts) shapes.push({ fill, path: () => heart(c, x, y, s) });

    c.lineWidth = 7; c.strokeStyle = INK;
    for (const s of shapes) { c.beginPath(); s.path(); c.stroke(); }
    for (const s of shapes) { c.beginPath(); s.p
</body>
</html>
