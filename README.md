# PROKI
Aplicación para combatir la procrastinación y mejorar los hábitos.
<html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>:root{color-scheme:light;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}html{scroll-padding-top:env(safe-area-inset-top,0px)}body{margin:0;padding:0;font:14px -apple-system,BlinkMacSystemFont,sans-serif;background:#fff;color:#000}img{max-width:100%}[hidden]:not([hidden=until-found i]){display:none!important}</style></head><body>
<html lang="es" translate="no">
<head>
<meta charset="utf-8">
<meta name="google" content="notranslate">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>PROKI</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,300;12..96,400;12..96,500;12..96,600;12..96,700;12..96,800&display=swap" rel="stylesheet">
<style>
:root{
  /* Paleta PROKI: #f3efe8 · #c8dfdb · #76bdcd · #59a5b2 (+ tonos derivados para texto y botones accesibles) */
  --bg:#F3EFE8; --surface:#FCFAF6; --ink:#163A45; --muted:#4E6C74; --line:#DCE3DE;
  --aqua:#C8DFDB; --teal:#76BDCD; --teal2:#59A5B2; --deep:#2F7380;
  --sage:#59A5B2; --sage-soft:#C8DFDB; --sun:#2F7380; --sun-ink:#FFFFFF; --sun-soft:#DDEDEE; --lilac:#E4EFF1; --lilac-ink:#21596A; --coral:#E3876A;
  --display:"Bricolage Grotesque","Avenir Next","Segoe UI",system-ui,sans-serif;
  --body:"Bricolage Grotesque","Segoe UI",system-ui,-apple-system,sans-serif;
  box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:light;
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --bg:#0F242A;--surface:#163139;--ink:#EAF3F2;--muted:#9DBBC0;--line:#264851;--aqua:#1F3F48;--teal:#76BDCD;--teal2:#59A5B2;--deep:#76BDCD;
  --sage:#76BDCD;--sage-soft:#1F3F48;--sun:#76BDCD;--sun-ink:#0F242A;--sun-soft:#1A3942;--lilac:#1C3A43;--lilac-ink:#C8DFDB;--coral:#EE9C82;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#0F242A;--surface:#163139;--ink:#EAF3F2;--muted:#9DBBC0;--line:#264851;--aqua:#1F3F48;--teal:#76BDCD;--teal2:#59A5B2;--deep:#76BDCD;
  --sage:#76BDCD;--sage-soft:#1F3F48;--sun:#76BDCD;--sun-ink:#0F242A;--sun-soft:#1A3942;--lilac:#1C3A43;--lilac-ink:#C8DFDB;--coral:#EE9C82;color-scheme:dark}
*,*::before,*::after{box-sizing:inherit}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--ink);font:400 16px/1.5 var(--body);font-optical-sizing:auto;-webkit-font-smoothing:antialiased}
main{max-width:600px;margin:0 auto;padding:22px 18px 130px}
h1,h2,h3,h4{font-family:var(--display);margin:0;line-height:1.1;letter-spacing:-.02em}
h1{font-size:clamp(38px,10vw,54px);font-weight:800}
h2{font-size:28px;font-weight:700}
h3{font-size:19px;font-weight:700;letter-spacing:-.01em}
h4{font-size:16px;font-weight:700;letter-spacing:0}
p{margin:0}
a{color:inherit}
.muted{color:var(--muted)}
.small{font-size:14px}
.stack>*+*{margin-top:14px}
.top{display:flex;justify-content:space-between;align-items:center;margin-bottom:26px}
.wordmark{font-family:var(--display);font-weight:800;font-size:22px;letter-spacing:-.03em;display:flex;align-items:center;gap:6px}
button{font:inherit;color:inherit;cursor:pointer}
.btn{border:0;border-radius:999px;padding:12px 22px;font-weight:600;font-size:16px;background:var(--sun);color:var(--sun-ink);min-height:46px}
.btn:disabled{opacity:.45;cursor:not-allowed}
.btn.ghost{background:transparent;color:var(--ink);box-shadow:inset 0 0 0 1.5px var(--line)}
.btn.soft{background:var(--sage-soft);color:var(--ink)}
.btn.sm{padding:7px 14px;font-size:14px;min-height:36px}
.link{background:none;border:0;padding:4px 0;color:var(--muted);text-decoration:underline;text-underline-offset:3px;font-size:14px}
:focus-visible{outline:3px solid var(--sage);outline-offset:2px}
.row{display:flex;gap:8px;flex-wrap:wrap;align-items:center}
.mt{margin-top:14px}.mt2{margin-top:24px}
.actions{display:flex;gap:10px;flex-wrap:wrap;margin-top:26px;align-items:center}
.card{background:var(--surface);border:1.5px solid var(--line);border-radius:20px;padding:18px}
.card+.card,.card+.sec,.sec+.card{margin-top:12px}
.sec{margin-top:30px}
.sec>h3{margin-bottom:12px}
.hl{background:var(--ink);color:var(--bg);border-color:var(--ink)}
.hl .muted{color:var(--bg);opacity:.75}
.warm{background:var(--sun-soft);border-color:transparent}
.lil{background:var(--lilac);color:var(--lilac-ink);border-color:transparent}
.chips{display:flex;flex-wrap:wrap;gap:8px}
.chip{border:1.5px solid var(--line);background:var(--surface);border-radius:999px;padding:9px 15px;font-size:15px;font-weight:500}
.chip[aria-pressed="true"]{background:var(--ink);color:var(--bg);border-color:var(--ink)}
.tag{display:inline-block;border-radius:999px;padding:2px 10px;font-size:12px;font-weight:600;background:var(--sage-soft)}
.tag.ext{background:var(--lilac);color:var(--lilac-ink)}
input[type=text],input[type=number],input[type=date],input[type=time],textarea,select{width:100%;font:inherit;color:var(--ink);background:var(--surface);border:1.5px solid var(--line);border-radius:12px;padding:11px 13px}
textarea{min-height:110px;resize:vertical}
label.f{display:block;font-weight:600;font-size:14px;margin:14px 0 6px}
.two{display:grid;grid-template-columns:1fr 1fr;gap:10px}
.progress{height:6px;background:var(--line);border-radius:6px;overflow:hidden}
.progress i{display:block;height:100%;background:var(--sage);border-radius:6px;transition:width .4s}
/* nav */
nav.tabs{position:fixed;left:0;right:0;bottom:0;background:var(--surface);border-top:1.5px solid var(--line);padding:6px 4px calc(6px + env(safe-area-inset-bottom,0px));z-index:10}
nav.tabs ul{list-style:none;margin:0 auto;padding:0;display:grid;grid-template-columns:repeat(6,1fr);max-width:600px}
nav.tabs button{width:100%;background:none;border:0;display:flex;flex-direction:column;align-items:center;gap:2px;padding:6px 0;font-size:11px;font-weight:600;color:var(--muted);border-radius:12px}
nav.tabs button[aria-current="page"]{color:var(--ink);background:var(--sage-soft)}
nav.tabs svg{width:22px;height:22px}
/* listas */
.item{display:flex;gap:12px;align-items:flex-start;padding:11px 0;border-top:1px solid var(--line)}
.item:first-child{border-top:0}
.item .grow{flex:1;min-width:0}
.bar{width:5px;align-self:stretch;border-radius:4px;flex:0 0 5px}
.time{font-variant-numeric:tabular-nums;font-weight:600;font-size:14px;min-width:92px}
.tick{flex:0 0 26px;width:26px;height:26px;border-radius:50%;border:2px solid var(--line);background:transparent;display:grid;place-items:center;padding:0}
.tick[aria-pressed="true"]{background:var(--sage);border-color:var(--sage)}
.tick svg{opacity:0;width:14px;height:14px}.tick[aria-pressed="true"] svg{opacity:1}
.done-t{color:var(--muted);text-decoration:line-through;text-decoration-color:var(--sage)}
.week{display:grid;grid-template-columns:repeat(7,1fr);gap:4px;margin:6px 0 16px}
.week button{border:0;background:var(--surface);border-radius:14px;padding:8px 0;display:flex;flex-direction:column;align-items:center;font-size:12px;color:var(--muted);box-shadow:inset 0 0 0 1.5px var(--line)}
.week button b{font-family:var(--display);font-size:19px;color:var(--ink)}
.week button[aria-pressed="true"]{background:var(--ink);box-shadow:none;color:var(--bg)}
.week button[aria-pressed="true"] b{color:var(--bg)}
.week i{width:5px;height:5px;border-radius:50%;background:var(--sun);margin-top:3px}
.gap{border:1.5px dashed var(--line);border-radius:14px;padding:10px 12px;font-size:14px;margin-top:8px}
.big{font-family:var(--display);font-weight:800;font-size:44px;letter-spacing:-.03em;line-height:1;font-variant-numeric:tabular-nums}
.stat{display:grid;grid-template-columns:repeat(3,1fr);gap:10px}
.stat .card{padding:14px}
.stat b{font-family:var(--display);font-size:26px;display:block;letter-spacing:-.02em}
.hbar{display:grid;grid-template-columns:96px 1fr;gap:10px;align-items:center;font-size:14px;margin-top:10px}
.hbar .tr{position:relative;height:22px}
.hbar .p,.hbar .r{position:absolute;left:0;border-radius:6px;height:10px}
.hbar .p{top:0;background:var(--line)}
.hbar .r{top:12px}
.legend{display:flex;gap:14px;font-size:13px;color:var(--muted);margin-top:6px}
.legend i{display:inline-block;width:10px;height:10px;border-radius:3px;margin-right:5px;vertical-align:-1px}
.spark{display:flex;align-items:flex-end;gap:6px;height:90px;margin-top:10px}
.spark div{flex:1;background:var(--sage);border-radius:6px 6px 2px 2px;min-height:3px;position:relative}
.spark span{white-space:nowrap;position:absolute;bottom:-20px;left:0;right:0;text-align:center;font-size:11px;color:var(--muted)}
.badges{display:grid;grid-template-columns:repeat(auto-fill,minmax(150px,1fr));gap:10px}
.badge{border-radius:16px;padding:12px;background:var(--surface);border:1.5px solid var(--line);font-size:14px}
.badge.off{opacity:.45}
.badge b{display:block;font-family:var(--display);font-size:15px}
.flash{min-height:150px;display:grid;place-items:center;text-align:center;font-size:18px;font-weight:600;cursor:pointer;padding:24px;border-radius:20px;background:var(--surface);border:1.5px solid var(--line);width:100%}
.flash.back{background:var(--sage-soft);font-weight:500;font-size:16px}
.opt{display:block;width:100%;text-align:left;background:var(--surface);border:1.5px solid var(--line);border-radius:14px;padding:12px 14px;margin-top:8px}
.opt.ok{border-color:var(--sage);background:var(--sage-soft)}
.opt.bad{border-color:var(--coral)}
.loading{display:flex;gap:10px;align-items:center;color:var(--muted);font-size:15px;padding:8px 0}
.loading img{width:52px;flex:0 0 52px;animation:swim 2.2s ease-in-out infinite}
@keyframes swim{0%,100%{transform:translate(0,0)}50%{transform:translate(6px,-4px)}}
@keyframes sway{0%,100%{transform:rotate(-5deg)}50%{transform:rotate(5deg)}}
.toast{position:fixed;left:50%;bottom:calc(88px + env(safe-area-inset-bottom,0px));transform:translate(-50%,20px);opacity:0;background:var(--ink);color:var(--bg);padding:13px 18px;border-radius:16px;max-width:min(92vw,480px);font-weight:500;transition:opacity .25s,transform .25s;pointer-events:none;z-index:30}
.toast.show{opacity:1;transform:translate(-50%,0)}
dialog{border:0;border-radius:24px;padding:0;width:min(600px,95vw);max-height:90vh;background:var(--surface);color:var(--ink)}
dialog::backdrop{background:rgba(20,30,24,.5)}
.sheet{padding:22px}
.letter p+p{margin-top:12px}
.note{font-size:13px;color:var(--muted);margin-top:6px}
.honest{font-size:13px;color:var(--muted);border-left:3px solid var(--line);padding-left:10px;margin-top:10px}
.qprog{height:6px;background:var(--line);border-radius:6px;overflow:hidden;margin-bottom:28px}
.qprog i{display:block;height:100%;background:var(--sage)}
.clock{font-family:var(--display);font-weight:800;font-size:64px;letter-spacing:-.03em;font-variant-numeric:tabular-nums;line-height:1}
.back-btn{background:none;border:0;padding:6px 0;font-weight:600;color:var(--muted);margin-bottom:10px}
.prose p+p{margin-top:10px}
img.px{image-rendering:pixelated;image-rendering:crisp-edges;display:block}
img.px,.swatch img,.loading img{background:transparent!important;background-color:transparent!important;border:0!important;box-shadow:none!important;padding:0!important}
svg.logo{background:transparent!important}
.logo{display:block;height:auto}
.logo path{fill:currentColor}
.hero{background:var(--teal);color:#0F2E36;border-radius:32px 32px 32px 96px;padding:22px 20px 26px;position:relative;overflow:hidden}
.hero .muted{color:#0F2E36;opacity:.75}
.hero::after{content:"";position:absolute;right:-60px;bottom:-80px;width:220px;height:220px;border-radius:50%;background:var(--teal2);opacity:.55}
.hero>*{position:relative;z-index:1}
.hero-row{display:flex;gap:12px;align-items:center;justify-content:space-between}
.hero .fishbox{flex:0 0 auto;text-align:center}
.hero .fishname{font-weight:700;font-size:13px;margin-top:2px}
.mood{display:inline-block;background:rgba(255,255,255,.55);border-radius:999px;padding:4px 12px;font-size:13px;font-weight:600;margin-top:10px}
.wave{display:block;width:100%;height:28px}
.fishbob{animation:bob 2.6s ease-in-out infinite}
@keyframes bob{0%,100%{transform:translateY(0)}50%{transform:translateY(-6px)}}
.swatch{width:44px;height:44px;border-radius:50%;border:3px solid transparent;background:transparent;padding:2px}
.swatch[aria-pressed="true"]{border-color:var(--ink)}
.swatch img{width:100%;height:100%;object-fit:contain}
/* ===== pez y toxinas ===== */
.pecera{position:relative;height:210px;margin-top:14px;border-radius:28px;background:transparent;display:grid;place-items:center;overflow:visible}
.toxwrap{transition:transform 1.3s cubic-bezier(.34,1.45,.64,1),filter 1.3s ease;transform-origin:50% 55%;will-change:transform}
.toxwrap.tremble>div{animation:tremble .32s linear infinite}
@keyframes tremble{0%{transform:translate(0,0)}25%{transform:translate(-1.6px,1px)}50%{transform:translate(1.4px,-1.2px)}75%{transform:translate(-1px,-1.4px)}100%{transform:translate(0,0)}}
.toxparts{position:absolute;inset:0;pointer-events:none}
.toxparts i{position:absolute;bottom:38%;width:7px;height:7px;border-radius:2px;opacity:0;animation:toxrise 3.2s ease-in infinite}
@keyframes toxrise{0%{transform:translate(0,0) scale(.5);opacity:0}20%{opacity:.85}100%{transform:translate(var(--dx),-90px) scale(1.15);opacity:0}}
.toxmeter{margin-top:6px}
.toxbar{height:12px;border-radius:999px;background:rgba(255,255,255,.55);overflow:hidden}
.toxbar i{display:block;height:100%;border-radius:999px;background:linear-gradient(90deg,#59A5B2 0%,#59A5B2 45%,#9AAE45 75%,#7B63A8 100%);background-size:var(--bw,100%) 100%;transition:width 1.3s cubic-bezier(.34,1.2,.64,1)}
.toxmeter .row{justify-content:space-between;font-size:13px;font-weight:600;margin-top:6px}
.hero .btn{background:#163A45;color:#fff}
.boom{animation:boom .55s cubic-bezier(.5,0,.75,0) forwards}
@keyframes boom{0%{transform:scale(var(--s))}55%{transform:scale(calc(var(--s) * 1.28))}100%{transform:scale(calc(var(--s) * 1.7));opacity:0}}
.reborn{animation:reborn .9s cubic-bezier(.34,1.6,.64,1)}
@keyframes reborn{0%{transform:scale(0);opacity:0}60%{opacity:1}100%{transform:scale(1)}}
#toxfx{position:fixed;inset:0;z-index:40;overflow:hidden;display:grid;place-items:center;padding:20px}
#toxfx::before{content:"";position:absolute;inset:0;background:radial-gradient(circle at 50% 40%,rgba(154,174,69,.55),rgba(110,92,150,.72));backdrop-filter:blur(4px);-webkit-backdrop-filter:blur(4px);animation:fogIn .9s .35s both}
@keyframes fogIn{from{opacity:0}to{opacity:1}}
#toxfx.out::before{animation:fogOut .85s ease forwards}
@keyframes fogOut{from{opacity:1}to{opacity:0}}
#toxfx .cloud{position:absolute;border-radius:50%;filter:blur(18px);transform:scale(.05);opacity:0;animation:cloudIn 1.15s cubic-bezier(.2,.8,.3,1) forwards}
@keyframes cloudIn{0%{transform:scale(.05);opacity:0}30%{opacity:.95}100%{transform:scale(1);opacity:.92}}
#toxfx.out .cloud{animation:cloudOut .9s ease forwards}
@keyframes cloudOut{from{transform:scale(1);opacity:.92}to{transform:scale(1.25);opacity:0}}
#toxfx .shard{position:fixed;width:10px;height:10px;border-radius:2px;animation:shard .95s cubic-bezier(.15,.7,.3,1) forwards}
@keyframes shard{0%{transform:translate(0,0) rotate(0);opacity:1}100%{transform:translate(var(--dx),var(--dy)) rotate(var(--r));opacity:0}}
#toxfx .flash{position:fixed;width:40px;height:40px;border-radius:50%;background:#fff;animation:flash .5s ease-out forwards}
@keyframes flash{0%{transform:scale(.2);opacity:.95}100%{transform:scale(9);opacity:0}}
.boomcard{position:relative;z-index:2;background:var(--surface);color:var(--ink);border-radius:28px;padding:26px 22px;max-width:420px;width:100%;text-align:center;opacity:0;transform:translateY(24px) scale(.96);transition:opacity .5s ease,transform .6s cubic-bezier(.34,1.4,.64,1);box-shadow:0 20px 60px rgba(20,40,30,.25)}
.boomcard.show{opacity:1;transform:none}
#toxfx.out .boomcard{opacity:0;transform:translateY(16px) scale(.97)}
.boomcard .px{margin:0 auto 8px}
.boomcard h2{font-size:30px}
/* ===== demo y gráficos de evolución ===== */
.demoband{display:flex;gap:10px;align-items:center;justify-content:space-between;background:var(--ink);color:var(--bg);border-radius:14px;padding:9px 14px;font-size:13px;font-weight:600;margin:-6px 0 18px}
.demoband button{background:var(--bg);color:var(--ink);border:0;border-radius:999px;padding:6px 12px;font-size:13px;font-weight:700}
.heat{display:grid;grid-auto-flow:column;grid-template-rows:repeat(7,1fr);gap:3px;margin-top:10px}
.heat i{aspect-ratio:1;border-radius:3px;background:var(--line);display:block;position:relative}
.heat i.r{background:transparent;box-shadow:inset 0 0 0 1.5px var(--teal2)}
.heat i.f{opacity:0}
.heatleg{display:flex;gap:4px;align-items:center;font-size:12px;color:var(--muted);margin-top:10px;flex-wrap:wrap}
.heatleg i{width:12px;height:12px;border-radius:3px;display:inline-block}
.lchart{width:100%;height:auto;display:block;margin-top:8px;overflow:visible}
.lchart text{font-family:var(--body);font-size:11px;fill:var(--muted)}
.ctip{position:fixed;pointer-events:none;background:var(--ink);color:var(--bg);font-size:13px;font-weight:600;padding:7px 10px;border-radius:10px;z-index:35;opacity:0;transition:opacity .12s;white-space:nowrap}
.ctip.on{opacity:1}
.stackbar{display:flex;height:16px;border-radius:6px;overflow:hidden;gap:2px;margin-top:10px}
.stackbar span{display:block;height:100%}
.catleg{display:flex;flex-wrap:wrap;gap:6px 14px;margin-top:10px;font-size:13px}
.catleg i{display:inline-block;width:10px;height:10px;border-radius:3px;margin-right:5px;vertical-align:-1px}
.moodrow{display:grid;grid-template-columns:110px 1fr 40px;gap:10px;align-items:center;font-size:14px;margin-top:8px}
.moodrow .tr{height:10px;background:var(--line);border-radius:6px;overflow:hidden}
.moodrow .tr i{display:block;height:100%;background:var(--teal2);border-radius:6px}
.delta{display:inline-block;font-size:12px;font-weight:700;border-radius:999px;padding:2px 8px;margin-left:6px;background:var(--aqua);color:var(--ink)}
/* ===== VISUAL-FIRST ===== */
body{letter-spacing:.012em;word-spacing:.06em;line-height:1.6}
html.easy body{font-size:18px;letter-spacing:.045em;word-spacing:.16em;line-height:1.8}
html.easy h1,html.easy h2,html.easy h3{letter-spacing:.005em;line-height:1.2}
html.easy .small,html.easy .note{font-size:15.5px}
.ico{display:block;flex:0 0 auto}
.icb{display:inline-grid;place-items:center;border-radius:30%;background:color-mix(in srgb,var(--c,var(--teal2)) 22%,var(--surface));color:color-mix(in srgb,var(--c,var(--teal2)) 70%,var(--ink));flex:0 0 auto;transition:transform .35s cubic-bezier(.34,1.6,.64,1)}
.icb.round{border-radius:50%}
.icb.solid{background:var(--c,var(--teal2));color:#fff}
.say{border:0;background:var(--aqua);color:var(--ink);width:34px;height:34px;border-radius:50%;display:inline-grid;place-items:center;vertical-align:middle;margin-left:6px;flex:0 0 34px;transition:transform .2s}
.say.on{background:var(--ink);color:var(--bg);animation:pulse 1s ease-in-out infinite}
@keyframes pulse{50%{transform:scale(1.12)}}
.shead{display:flex;align-items:center;gap:10px;margin-bottom:12px}
.shead h3{margin:0}
.shead .icb{width:36px;height:36px}
/* acciones rápidas */
.qa{display:grid;grid-template-columns:repeat(4,1fr);gap:8px;margin-top:20px}
.qa button{background:none;border:0;display:flex;flex-direction:column;align-items:center;gap:7px;font-size:13.5px;font-weight:600;padding:4px 0;color:var(--ink)}
.qa .icb{width:64px;height:64px;border-radius:50%;box-shadow:0 6px 16px -10px rgba(22,58,69,.6)}
.qa button:active .icb,.tile:active .icb{transform:scale(.88)}
.qa button:hover .icb,.tile:hover .icb{transform:rotate(-8deg) scale(1.06)}
/* mosaico */
.tiles{display:grid;grid-template-columns:repeat(2,1fr);gap:12px}
.tile{position:relative;background:var(--surface);border:1.5px solid var(--line);border-radius:24px;padding:16px;min-height:136px;display:flex;flex-direction:column;align-items:flex-start;justify-content:space-between;text-align:left;color:var(--ink);transition:transform .2s,box-shadow .2s}
.tile:hover{box-shadow:0 10px 24px -16px rgba(22,58,69,.55);transform:translateY(-2px)}
.tile .icb{width:56px;height:56px}
.tile b{font-size:17px;display:block;margin-top:10px;line-height:1.2}
.tile .val{font-size:13.5px;color:var(--muted);font-weight:600;margin-top:2px}
.tile .badge2{position:absolute;top:12px;right:12px;min-width:26px;height:26px;border-radius:13px;background:var(--coral);color:#fff;font-size:13px;font-weight:800;display:grid;place-items:center;padding:0 7px}
.tile.wide{grid-column:span 2;min-height:0;flex-direction:row;align-items:center;gap:14px;justify-content:flex-start}
.tile.wide b{margin-top:0}
.pop{animation:popIn .5s cubic-bezier(.34,1.5,.64,1) both;animation-delay:calc(var(--i,0) * 55ms)}
@keyframes popIn{from{opacity:0;transform:translateY(14px) scale(.96)}to{opacity:1;transform:none}}
/* línea del día */
.tline{display:flex;gap:14px;overflow-x:auto;padding:6px 2px 12px;scroll-snap-type:x mandatory;-webkit-overflow-scrolling:touch}
.tline button{flex:0 0 82px;scroll-snap-align:start;background:none;border:0;display:flex;flex-direction:column;align-items:center;gap:6px;color:var(--ink);font-size:13px;text-align:center}
.tline .icb{width:62px;height:62px;border-radius:50%;position:relative}
.tline .now .icb{box-shadow:0 0 0 3px var(--surface),0 0 0 6px var(--teal2)}
.tline .past{opacity:.55}
.tline .done .icb::after{content:"";position:absolute;right:-2px;bottom:-2px;width:22px;height:22px;border-radius:50%;background:var(--teal2) url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='white' stroke-width='3.2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M20 6 9 17l-5-5'/%3E%3C/svg%3E") center/14px no-repeat;border:2px solid var(--surface)}
.tline .tt{font-weight:700;font-variant-numeric:tabular-nums}
.tline .tn{font-size:12px;color:var(--muted);line-height:1.25;max-width:82px;overflow:hidden;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical}
/* objetivos visuales */
.gcard{display:flex;gap:14px;align-items:center}
.gcard .ring{width:58px;flex:0 0 58px}
.gsteps{display:flex;gap:8px;margin-top:14px}
.gstep{flex:1;border:1.5px solid var(--line);background:var(--bg);border-radius:16px;padding:10px 8px;display:flex;flex-direction:column;align-items:center;gap:6px;font-size:13px;line-height:1.3;text-align:center;color:var(--ink);transition:background .25s,transform .25s}
.gstep .tick{width:34px;height:34px;flex:0 0 34px}
.gstep[data-on="true"]{background:color-mix(in srgb,var(--teal2) 18%,var(--surface));border-color:var(--teal2)}
.gstep[data-on="true"] .tick{animation:tickPop .45s cubic-bezier(.34,1.8,.64,1)}
@keyframes tickPop{0%{transform:scale(.6)}100%{transform:scale(1)}}
.iconbtn{display:inline-flex;align-items:center;gap:8px}
/* opciones con ícono (entrevista, perfil, tipos) */
.optgrid{display:grid;grid-template-columns:repeat(auto-fill,minmax(132px,1fr));gap:10px}
.optgrid .chip{border-radius:20px;padding:14px 10px;display:flex;flex-direction:column;align-items:center;gap:8px;text-align:center;font-size:14.5px;line-height:1.3;min-height:112px;justify-content:center;position:relative;transition:transform .2s,background .2s}
.optgrid .chip .icb{width:48px;height:48px}
.optgrid .chip[aria-pressed="true"]{background:var(--ink);color:var(--bg)}
.optgrid .chip[aria-pressed="true"] .icb{background:var(--bg);color:var(--ink);transform:scale(1.08)}
.optgrid .chip[aria-pressed="true"]::after{content:"";position:absolute;top:8px;right:8px;width:20px;height:20px;border-radius:50%;background:var(--teal) url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24' fill='none' stroke='%23163A45' stroke-width='3.4' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpath d='M20 6 9 17l-5-5'/%3E%3C/svg%3E") center/12px no-repeat}
.optgrid.sm{grid-template-columns:repeat(auto-fill,minmax(92px,1fr))}
.optgrid.sm .chip{min-height:88px;font-size:13px;padding:10px 6px}
.optgrid.sm .chip .icb{width:40px;height:40px}
/* temporizador circular */
.ringtimer{position:relative;width:220px;height:220px;margin:6px auto 0}
.ringtimer svg{width:100%;height:100%;transform:rotate(-90deg)}
.ringtimer .center{position:absolute;inset:0;display:grid;place-items:center;text-align:center}
.ringtimer .clock{font-size:44px}
#ringArc{transition:stroke-dashoffset 1s linear}
.bigbtns{display:flex;justify-content:center;gap:18px;margin-top:16px}
.bigbtns button{background:none;border:0;display:flex;flex-direction:column;align-items:center;gap:6px;font-weight:600;font-size:14px;color:inherit}
.bigbtns .icb{width:66px;height:66px;border-radius:50%}
.welcome3{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-top:22px}
.welcome3 div{display:flex;flex-direction:column;align-items:center;gap:8px;text-align:center;font-weight:600;font-size:14.5px}
.welcome3 .icb{width:72px;height:72px;border-radius:50%}
.toggle{display:flex;align-items:center;gap:14px;width:100%;background:none;border:0;padding:6px 0;text-align:left;color:inherit}
.toggle .sw{margin-left:auto;width:52px;height:30px;border-radius:15px;background:var(--line);position:relative;flex:0 0 52px;transition:background .2s}
.toggle .sw::after{content:"";position:absolute;top:3px;left:3px;width:24px;height:24px;border-radius:50%;background:#fff;transition:transform .25s cubic-bezier(.34,1.5,.64,1);box-shadow:0 1px 3px rgba(0,0,0,.2)}
.toggle[aria-checked="true"] .sw{background:var(--teal2)}
.toggle[aria-checked="true"] .sw::after{transform:translateX(22px)}
.more{background:none;border:0;color:var(--muted);font-weight:600;font-size:14px;display:inline-flex;gap:6px;align-items:center;padding:6px 0}
nav.tabs svg{width:26px;height:26px}
nav.tabs button{font-size:11.5px;gap:3px;padding:7px 0}
nav.tabs button[aria-current="page"] svg{animation:tickPop .4s cubic-bezier(.34,1.8,.64,1)}
.sheethead{display:flex;align-items:center;gap:12px;margin-bottom:6px}
.sheethead .icb{width:52px;height:52px}
.sheethead h2{margin:0}
@media (prefers-reduced-motion: reduce){*{animation:none!important;transition:none!important}}
</style>
</head>
<body>
<main id="app" aria-live="polite"></main>
<nav class="tabs" id="tabs" hidden aria-label="Secciones"><ul></ul></nav>
<div class="toast" id="toast" role="status"></div>
<dialog id="sheet"><div class="sheet" id="sb"></div></dialog>
<script>
(function(){
"use strict";
/* ============ utilidades ============ */
const $=s=>document.querySelector(s), $$=s=>[...document.querySelectorAll(s)];
const esc=s=>String(s??"").replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]));
const uid=()=>Math.random().toString(36).slice(2,10);
const pad=n=>String(n).padStart(2,"0");
const ymd=d=>d.getFullYear()+"-"+pad(d.getMonth()+1)+"-"+pad(d.getDate());
const today=()=>ymd(new Date());
const pd=s=>{const[y,m,d]=s.split("-").map(Number);return new Date(y,m-1,d)};
const addD=(s,n)=>{const d=pd(s);d.setDate(d.getDate()+n);return ymd(d)};
const diffD=(a,b)=>Math.round((pd(b)-pd(a))/864e5);
const dow=s=>pd(s).getDay();
const fmtD=(s,o)=>pd(s).toLocaleDateString("es-AR",o||{day:"numeric",month:"long"});
const tm=s=>{const[h,m]=(s||"0:0").split(":").map(Number);return h*60+m};
const ts=m=>pad(Math.floor(m/60))+":"+pad(m%60);
const hmc=m=>m>=600?Math.round(m/60)+" h":hm(m);
const hm=m=>{m=Math.round(m);if(m<60)return m+" min";const h=Math.floor(m/60),r=m%60;return h+" h"+(r?" "+r+" min":"")};
const pick=(a,seed)=>a[(seed??Math.floor(Math.random()*1e6))%a.length];
const daySeed=()=>Number(today().replace(/-/g,""));
const clampTxt=(s,n)=>s.length>n?s.slice(0,n)+"\n[…recortado]":s;

const CATS={
 estudio:["Estudio","#5E9E88"],clase:["Clase","#4F8FB8"],examen:["Examen / entrega","#E9785F"],trabajo:["Trabajo","#7A6BC4"],
 deporte:["Deporte","#E0A030"],lectura:["Lectura","#B5739D"],proyecto:["Proyecto","#3F9C9C"],reunion:["Reunión","#8A8F5A"],
 salud:["Turno médico","#C9625B"],personal:["Personal","#9C7A54"],recreacion:["Recreación","#D08AA5"],descanso:["Descanso","#9AB0C9"],otra:["Otra","#8C9A90"]};
const catL=c=>(CATS[c]||CATS.otra)[0], catC=c=>(CATS[c]||CATS.otra)[1];
const DOWS=[["L",1],["M",2],["M",3],["J",4],["V",5],["S",6],["D",0]];

const MSG_OK=["Un pequeño avance también es un avance.","Estás construyendo un hábito, dale tiempo.","Bien ahí. Paso a paso se llega.","Eso que hiciste hoy suma."];
const MSG_MISS=["No pasa nada, mañana podés volver a intentarlo.","Hoy no salió como esperabas, pero eso no borra lo que ya conseguiste.","No tenés que hacerlo todo hoy."];
const MSG_REST=["Descansar también es parte del proceso.","Hoy toca recargar energía. Mañana seguimos.","Frenar un rato no es perder el tiempo."];

/* ============ entrevista ============ */
const Q=[
 {k:"nombre",t:"text",title:"Antes que nada, ¿cómo te llamamos?",hint:"Puede ser tu nombre o un apodo.",req:true},
 {k:"motivo",t:"multi",title:"¿Por qué descargaste PROKI?",req:true,custom:true,o:["Quiero dejar de procrastinar","Quiero estudiar más y mejor","Quiero organizar mi rutina","Quiero reducir el tiempo en redes sociales","Quiero dedicarle más tiempo a mis proyectos personales","Quiero incorporar hábitos saludables","Quiero aprovechar mejor mi tiempo"]},
 {k:"meta3",t:"multi",title:"¿Qué te gustaría conseguir en los próximos tres meses?",custom:true,o:["Ser más organizado/a","Mejorar mi rendimiento académico","Ser más constante con el deporte","Aprender cosas nuevas","Tener más tiempo libre de calidad","Cumplir mis objetivos personales"]},
 {k:"pantalla",t:"single",title:"¿Cuánto tiempo creés que usás el celular por día?",hint:"Si querés el dato exacto, fijate en Bienestar digital (Android) o Tiempo en pantalla (iPhone).",o:["Menos de 2 horas","Entre 2 y 4 horas","Entre 4 y 6 horas","Más de 6 horas"]},
 {k:"apps",t:"multi",title:"¿Qué aplicaciones te hacen perder más tiempo?",custom:true,o:["Instagram","TikTok","YouTube","X","WhatsApp","Juegos"]},
 {k:"momento",t:"single",title:"¿En qué momento del día más procrastinás?",o:["A la mañana","A la tarde","A la noche","Durante todo el día"]},
 {k:"pendiente",t:"multi",title:"¿Qué solés hacer cuando tenés una tarea pendiente?",hint:"Sin culpa: conocerlo nos ayuda a ayudarte.",custom:true,o:["La postergo hasta último momento","Me distraigo con el celular","Me cuesta empezar","Empiezo, pero pierdo la concentración","Me cuesta organizarme"]},
 {k:"actividades",t:"multi",title:"¿Qué actividades te gustaría sumar a tu rutina?",custom:true,o:["Leer","Estudiar","Entrenar","Aprender un idioma","Dibujar o diseñar","Tocar un instrumento","Meditar","Cocinar","Un proyecto personal"]},
 {k:"horas",t:"single",title:"¿Cuántas horas por semana te gustaría dedicarles a tus objetivos?",o:["2 a 4 horas","5 a 7 horas","8 a 12 horas","Más de 12 horas"]},
 {k:"temas",t:"multi",title:"¿Sobre qué temas te gustaría informarte cada día?",custom:true,o:["Arte y diseño","Política y actualidad","Deportes","Ciencia y tecnología","Cultura y música","Economía","Historia"]},
 {k:"motivacion",t:"multi",title:"¿Cómo preferís que PROKI te motive?",o:["Con recordatorios","Con desafíos diarios","Con estadísticas de progreso","Con mensajes motivadores","Con objetivos pequeños y alcanzables"]}
];
const BASE_MIN={"Menos de 2 horas":90,"Entre 2 y 4 horas":180,"Entre 4 y 6 horas":300,"Más de 6 horas":420};

const SOURCES={
 "Arte y diseño":[["Dezeen","https://www.dezeen.com/"],["It’s Nice That","https://www.itsnicethat.com/"]],
 "Política y actualidad":[["BBC Mundo","https://www.bbc.com/mundo"],["El País América","https://elpais.com/america/"]],
 "Deportes":[["Olé","https://www.ole.com.ar/"],["ESPN","https://www.espn.com.ar/"]],
 "Ciencia y tecnología":[["Agencia SINC","https://www.agenciasinc.es/"],["Xataka","https://www.xataka.com/"]],
 "Cultura y música":[["El País Cultura","https://elpais.com/cultura/"],["Pitchfork","https://pitchfork.com/"]],
 "Economía":[["Ámbito","https://www.ambito.com/"],["El Cronista","https://www.cronista.com/"]],
 "Historia":[["Historia National Geographic","https://historia.nationalgeographic.com.es/"]]
};

const ICO={"house": "<path d=\"M15 21v-8a1 1 0 0 0-1-1h-4a1 1 0 0 0-1 1v8\" /> <path d=\"M3 10a2 2 0 0 1 .709-1.528l7-6a2 2 0 0 1 2.582 0l7 6A2 2 0 0 1 21 10v9a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z\" />", "calendar-days": "<path d=\"M8 2v3\" /> <path d=\"M16 2v3\" /> <rect x=\"3\" y=\"3\" width=\"18\" height=\"18\" rx=\"2\" /> <path d=\"M3 9h18\" /> <path d=\"M8 13h.01\" /> <path d=\"M12 13h.01\" /> <path d=\"M16 13h.01\" /> <path d=\"M8 17h.01\" /> <path d=\"M12 17h.01\" /> <path d=\"M16 17h.01\" />", "book-open": "<path d=\"M12 5v16\" /> <path d=\"M20.001 19A2 2 0 0022 17V5a2 2 0 00-1.999-2L16 3.002A5 5 0 0012 5a5 5 0 00-4-2H4a2 2 0 00-2 2v12a2 2 0 001.999 2H8a5 5 0 014 2 5 5 0 014-2z\" />", "timer": "<line x1=\"10\" x2=\"14\" y1=\"2\" y2=\"2\" /> <line x1=\"12\" x2=\"15\" y1=\"14\" y2=\"11\" /> <circle cx=\"12\" cy=\"14\" r=\"8\" />", "chart-column": "<path d=\"M3 3v16a2 2 0 0 0 2 2h16\" /> <path d=\"M18 17V9\" /> <path d=\"M13 17V5\" /> <path d=\"M8 17v-3\" />", "circle-user": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <circle cx=\"12\" cy=\"10\" r=\"3\" /> <path d=\"M7 20.662V19a2 2 0 0 1 2-2h6a2 2 0 0 1 2 2v1.662\" />", "book-open-text": "<path d=\"M12 5v16\" /> <path d=\"M16 13h2\" /> <path d=\"M16 9h2\" /> <path d=\"M20.001 19A2 2 0 0022 17V5a2 2 0 00-1.999-2L16 3.002A5 5 0 0012 5a5 5 0 00-4-2H4a2 2 0 00-2 2v12a2 2 0 001.999 2H8a5 5 0 014 2 5 5 0 014-2z\" /> <path d=\"M6 13h2\" /> <path d=\"M6 9h2\" />", "presentation": "<path d=\"M2 3h20\" /> <path d=\"M21 3v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V3\" /> <path d=\"m7 21 5-5 5 5\" />", "graduation-cap": "<path d=\"M21.42 10.922a1 1 0 0 0-.019-1.838L12.83 5.18a2 2 0 0 0-1.66 0L2.6 9.08a1 1 0 0 0 0 1.832l8.57 3.908a2 2 0 0 0 1.66 0z\" /> <path d=\"M22 10v6\" /> <path d=\"M6 12.5V16a6 3 0 0 0 12 0v-3.5\" />", "briefcase": "<path d=\"M16 20V4a2 2 0 0 0-2-2h-4a2 2 0 0 0-2 2v16\" /> <rect width=\"20\" height=\"14\" x=\"2\" y=\"6\" rx=\"2\" />", "dumbbell": "<path d=\"M17.596 12.768a2 2 0 1 0 2.829-2.829l-1.768-1.767a2 2 0 0 0 2.828-2.829l-2.828-2.828a2 2 0 0 0-2.829 2.828l-1.767-1.768a2 2 0 1 0-2.829 2.829z\" /> <path d=\"m2.5 21.5 1.4-1.4\" /> <path d=\"m20.1 3.9 1.4-1.4\" /> <path d=\"M5.343 21.485a2 2 0 1 0 2.829-2.828l1.767 1.768a2 2 0 1 0 2.829-2.829l-6.364-6.364a2 2 0 1 0-2.829 2.829l1.768 1.767a2 2 0 0 0-2.828 2.829z\" /> <path d=\"m9.6 14.4 4.8-4.8\" />", "book-marked": "<path d=\"M10 2v7.751a.25.25 0 00.407.195l2.28-1.834a.5.5 0 01.627 0l2.28 1.834A.25.25 0 0016 9.751V2\" /> <path d=\"M4 19.5v-15A2.5 2.5 0 016.5 2H19a1 1 0 011 1v18a1 1 0 01-1 1H6.5a1 1 0 010-5H20\" />", "palette": "<path d=\"M12 22a1 1 0 0 1 0-20 10 9 0 0 1 10 9 5 5 0 0 1-5 5h-2.25a1.75 1.75 0 0 0-1.4 2.8l.3.4a1.75 1.75 0 0 1-1.4 2.8z\" /> <circle cx=\"13.5\" cy=\"6.5\" r=\".5\" fill=\"currentColor\" /> <circle cx=\"17.5\" cy=\"10.5\" r=\".5\" fill=\"currentColor\" /> <circle cx=\"6.5\" cy=\"12.5\" r=\".5\" fill=\"currentColor\" /> <circle cx=\"8.5\" cy=\"7.5\" r=\".5\" fill=\"currentColor\" />", "users": "<path d=\"M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2\" /> <path d=\"M16 3.128a4 4 0 0 1 0 7.744\" /> <path d=\"M22 21v-2a4 4 0 0 0-3-3.87\" /> <circle cx=\"9\" cy=\"7\" r=\"4\" />", "stethoscope": "<path d=\"M11 2v2\" /> <path d=\"M5 2v2\" /> <path d=\"M5 3H4a2 2 0 0 0-2 2v4a6 6 0 0 0 12 0V5a2 2 0 0 0-2-2h-1\" /> <path d=\"M8 15a6 6 0 0 0 12 0v-3\" /> <circle cx=\"20\" cy=\"10\" r=\"2\" />", "heart": "<path d=\"M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5\" />", "party-popper": "<path d=\"M5.8 11.3 2 22l10.7-3.79\" /> <path d=\"M4 3h.01\" /> <path d=\"M22 8h.01\" /> <path d=\"M15 2h.01\" /> <path d=\"M22 20h.01\" /> <path d=\"m22 2-2.24.75a2.9 2.9 0 0 0-1.96 3.12c.1.86-.57 1.63-1.45 1.63h-.38c-.86 0-1.6.6-1.76 1.44L14 10\" /> <path d=\"m22 13-.82-.33c-.86-.34-1.82.2-1.98 1.11c-.11.7-.72 1.22-1.43 1.22H17\" /> <path d=\"m11 2 .33.82c.34.86-.2 1.82-1.11 1.98C9.52 4.9 9 5.52 9 6.23V7\" /> <path d=\"M11 13c1.93 1.93 2.83 4.17 2 5-.83.83-3.07-.07-5-2-1.93-1.93-2.83-4.17-2-5 .83-.83 3.07.07 5 2Z\" />", "bed": "<path d=\"M2 4v16\" /> <path d=\"M2 8h18a2 2 0 0 1 2 2v10\" /> <path d=\"M2 17h20\" /> <path d=\"M6 8v9\" />", "circle-dot": "<circle cx=\"12\" cy=\"12\" r=\"1\" /> <circle cx=\"12\" cy=\"12\" r=\"10\" />", "hourglass": "<path d=\"M5 22h14\" /> <path d=\"M5 2h14\" /> <path d=\"M17 22v-4.172a2 2 0 0 0-.586-1.414L12 12l-4.414 4.414A2 2 0 0 0 7 17.828V22\" /> <path d=\"M7 2v4.172a2 2 0 0 0 .586 1.414L12 12l4.414-4.414A2 2 0 0 0 17 6.172V2\" />", "calendar-check": "<path d=\"M8 2v3\" /> <path d=\"M16 2v3\" /> <rect x=\"3\" y=\"3\" width=\"18\" height=\"18\" rx=\"2\" /> <path d=\"M3 9h18\" /> <path d=\"m9 15 2 2 4-4\" />", "smartphone": "<rect width=\"14\" height=\"20\" x=\"5\" y=\"2\" rx=\"2\" ry=\"2\" /> <path d=\"M12 18h.01\" />", "rocket": "<path d=\"M12 15v5s3.03-.55 4-2c1.08-1.62 0-5 0-5\" /> <path d=\"M4.5 16.5c-1.5 1.26-2 5-2 5s3.74-.5 5-2c.71-.84.7-2.13-.09-2.91a2.18 2.18 0 0 0-2.91-.09\" /> <path d=\"M9 12a22 22 0 0 1 2-3.95A12.88 12.88 0 0 1 22 2c0 2.72-.78 7.5-6 11a22.4 22.4 0 0 1-4 2z\" /> <path d=\"M9 12H4s.55-3.03 2-4c1.62-1.08 5 .05 5 .05\" />", "heart-pulse": "<path d=\"M2 9.5a5.5 5.5 0 0 1 9.591-3.676.56.56 0 0 0 .818 0A5.49 5.49 0 0 1 22 9.5c0 2.29-1.5 4-3 5.5l-5.492 5.313a2 2 0 0 1-3 .019L5 15c-1.5-1.5-3-3.2-3-5.5\" /> <path d=\"M3.22 13H9.5l.5-1 2 4.5 2-7 1.5 3.5h5.27\" />", "clock": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M12 6v6l4 2\" />", "list-checks": "<path d=\"M13 5h8\" /> <path d=\"M13 12h8\" /> <path d=\"M13 19h8\" /> <path d=\"m3 17 2 2 4-4\" /> <path d=\"m3 7 2 2 4-4\" />", "lightbulb": "<path d=\"M15 14c.2-1 .7-1.7 1.5-2.5 1-.9 1.5-2.2 1.5-3.5A6 6 0 0 0 6 8c0 1 .2 2.2 1.5 3.5.7.7 1.3 1.5 1.5 2.5\" /> <path d=\"M9 18h6\" /> <path d=\"M10 22h4\" />", "sun": "<circle cx=\"12\" cy=\"12\" r=\"4\" /> <path d=\"M12 2v2\" /> <path d=\"M12 20v2\" /> <path d=\"m4.93 4.93 1.41 1.41\" /> <path d=\"m17.66 17.66 1.41 1.41\" /> <path d=\"M2 12h2\" /> <path d=\"M20 12h2\" /> <path d=\"m6.34 17.66-1.41 1.41\" /> <path d=\"m19.07 4.93-1.41 1.41\" />", "target": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <circle cx=\"12\" cy=\"12\" r=\"6\" /> <circle cx=\"12\" cy=\"12\" r=\"2\" />", "battery-full": "<path d=\"M10 10v4\" /> <path d=\"M14 10v4\" /> <path d=\"M22 14v-4\" /> <path d=\"M6 10v4\" /> <rect x=\"2\" y=\"6\" width=\"16\" height=\"12\" rx=\"2\" />", "battery-medium": "<path d=\"M10 14v-4\" /> <path d=\"M22 14v-4\" /> <path d=\"M6 14v-4\" /> <rect x=\"2\" y=\"6\" width=\"16\" height=\"12\" rx=\"2\" />", "battery-low": "<path d=\"M22 14v-4\" /> <path d=\"M6 14v-4\" /> <rect x=\"2\" y=\"6\" width=\"16\" height=\"12\" rx=\"2\" />", "battery-warning": "<path d=\"M10 16h.01\" /> <path d=\"M10 8v4\" /> <path d=\"M14 6h2a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2h-2\" /> <path d=\"M22 14v-4\" /> <path d=\"M6 18H4a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h2\" />", "camera": "<path d=\"M13.997 4a2 2 0 0 1 1.76 1.05l.486.9A2 2 0 0 0 18.003 7H20a2 2 0 0 1 2 2v9a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V9a2 2 0 0 1 2-2h1.997a2 2 0 0 0 1.759-1.048l.489-.904A2 2 0 0 1 10.004 4z\" /> <circle cx=\"12\" cy=\"13\" r=\"3\" />", "music": "<path d=\"M21 16V3a1 1 0 0 0-1.28-.96l-10 2.917a1 1 0 0 0-.72.96V19\" /> <circle cx=\"18\" cy=\"16\" r=\"3\" /> <circle cx=\"6\" cy=\"19\" r=\"3\" />", "play": "<path d=\"M5 5a2 2 0 0 1 3.008-1.728l11.997 6.998a2 2 0 0 1 .003 3.458l-12 7A2 2 0 0 1 5 19z\" />", "at-sign": "<circle cx=\"12\" cy=\"12\" r=\"4\" /> <path d=\"M16 8v5a3 3 0 0 0 6 0v-1a10 10 0 1 0-4 8\" />", "message-circle": "<path d=\"M2.992 16.342a2 2 0 0 1 .094 1.167l-1.065 3.29a1 1 0 0 0 1.236 1.168l3.413-.998a2 2 0 0 1 1.099.092 10 10 0 1 0-4.777-4.719\" />", "gamepad-2": "<line x1=\"6\" x2=\"10\" y1=\"11\" y2=\"11\" /> <line x1=\"8\" x2=\"8\" y1=\"9\" y2=\"13\" /> <line x1=\"15\" x2=\"15.01\" y1=\"12\" y2=\"12\" /> <line x1=\"18\" x2=\"18.01\" y1=\"10\" y2=\"10\" /> <path d=\"M17.32 5H6.68a4 4 0 0 0-3.978 3.59c-.006.052-.01.101-.017.152C2.604 9.416 2 14.456 2 16a3 3 0 0 0 3 3c1 0 1.5-.5 2-1l1.414-1.414A2 2 0 0 1 9.828 16h4.344a2 2 0 0 1 1.414.586L17 18c.5.5 1 1 2 1a3 3 0 0 0 3-3c0-1.545-.604-6.584-.685-7.258-.007-.05-.011-.1-.017-.151A4 4 0 0 0 17.32 5z\" />", "sunrise": "<path d=\"M12 2v8\" /> <path d=\"m4.93 10.93 1.41 1.41\" /> <path d=\"M2 18h2\" /> <path d=\"M20 18h2\" /> <path d=\"m19.07 10.93-1.41 1.41\" /> <path d=\"M22 22H2\" /> <path d=\"m8 6 4-4 4 4\" /> <path d=\"M16 18a4 4 0 0 0-8 0\" />", "moon": "<path d=\"M20.985 12.486a9 9 0 1 1-9.473-9.472c.405-.022.617.46.402.803a6 6 0 0 0 8.268 8.268c.344-.215.825-.004.803.401\" />", "infinity": "<path d=\"M6 16c5 0 7-8 12-8a4 4 0 0 1 0 8c-5 0-7-8-12-8a4 4 0 1 0 0 8\" />", "footprints": "<path d=\"M4 16v-2.38C4 11.5 2.97 10.5 3 8c.03-2.72 1.49-6 4.5-6C9.37 2 10 3.8 10 5.5c0 3.11-2 5.66-2 8.68V16a2 2 0 1 1-4 0Z\" /> <path d=\"M20 20v-2.38c0-2.12 1.03-3.12 1-5.62-.03-2.72-1.49-6-4.5-6C14.63 6 14 7.8 14 9.5c0 3.11 2 5.66 2 8.68V20a2 2 0 1 0 4 0Z\" /> <path d=\"M16 17h4\" /> <path d=\"M4 13h4\" />", "brain": "<path d=\"M12 18V5\" /> <path d=\"M15 13a4.17 4.17 0 01-3-4 4.17 4.17 0 01-3 4\" /> <path d=\"M17.707 6.294A3 3 0 1012 5a3 3 0 10-5.707 1.294\" /> <path d=\"M17.996 5.125a4 4 0 012.526 5.77\" /> <path d=\"M18 18a4 4 0 002-7.465\" /> <path d=\"M19.967 17.482a4 4 0 11-7.967.517 4 4 0 11-7.967-.517\" /> <path d=\"M6 18a4 4 0 01-2-7.465\" /> <path d=\"M6.004 5.125a4 4 0 00-2.526 5.77\" />", "shuffle": "<path d=\"m18 14 4 4-4 4\" /> <path d=\"m18 2 4 4-4 4\" /> <path d=\"M2 18h1.973a4 4 0 0 0 3.3-1.7l5.454-8.6a4 4 0 0 1 3.3-1.7H22\" /> <path d=\"M2 6h1.972a4 4 0 0 1 3.6 2.2\" /> <path d=\"M22 18h-6.041a4 4 0 0 1-3.3-1.8l-.359-.45\" />", "languages": "<path d=\"m5 8 6 6\" /> <path d=\"m4 14 6-6 2-3\" /> <path d=\"M2 5h12\" /> <path d=\"M7 2h1\" /> <path d=\"m22 22-5-10-5 10\" /> <path d=\"M14 18h6\" />", "pen-tool": "<path d=\"m18 13-.654-4.736a4 4 0 00-2.756-3.266l-9.163-2.9a2 2 0 00-2.017.493l-.82.819a2 2 0 00-.492 2.017l2.9 9.163a4 4 0 003.266 2.756L13 18\" /> <path d=\"M18.648 12.352a1.205 1.205 0 011.704 0l1.296 1.296a1.205 1.205 0 010 1.704l-6.296 6.296a1.205 1.205 0 01-1.704 0l-1.296-1.296a1.205 1.205 0 010-1.704z\" /> <path d=\"m3 3 6.586 6.586\" /> <circle cx=\"11\" cy=\"11\" r=\"2\" />", "guitar": "<path d=\"m11.9 12.1 4.514-4.514\" /> <path d=\"M20.1 2.3a1 1 0 0 0-1.4 0l-1.114 1.114A2 2 0 0 0 17 4.828v1.344a2 2 0 0 1-.586 1.414A2 2 0 0 1 17.828 7h1.344a2 2 0 0 0 1.414-.586L21.7 5.3a1 1 0 0 0 0-1.4z\" /> <path d=\"m6 16 2 2\" /> <path d=\"M8.23 9.85A3 3 0 0 1 11 8a5 5 0 0 1 5 5 3 3 0 0 1-1.85 2.77l-.92.38A2 2 0 0 0 12 18a4 4 0 0 1-4 4 6 6 0 0 1-6-6 4 4 0 0 1 4-4 2 2 0 0 0 1.85-1.23z\" />", "leaf": "<path d=\"M11 20a10 10 0 0010-10 25.9 25.9 0 00-1.04-7.281 1 1 0 00-1.755-.325C15.833 5.5 13 5.5 9.8 6.1A7 7 0 0011 20\" /> <path d=\"M2 21a5 5 0 012.911-4.544C7.613 15.212 8.351 15.24 11 13\" />", "chef-hat": "<path d=\"M10 11v5\" /> <path d=\"M14 11v5\" /> <path d=\"M6 12.65c0-.457-.316-.844-.727-1.041A4 4 0 017.52 4.034a1.53 1.53 0 001.367-.547 4 4 0 016.225 0 1.53 1.53 0 001.367.547 4 4 0 012.248 7.575c-.411.197-.727.584-.727 1.04V19a2 2 0 01-2 2H8a2 2 0 01-2-2z\" /> <path d=\"M6 16h12\" />", "clock-2": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M12 6v6l4-2\" />", "clock-5": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M12 6v6l2 4\" />", "clock-8": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M12 6v6l-4 2\" />", "clock-12": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M12 6v6\" />", "landmark": "<path d=\"M10 18v-7\" /> <path d=\"M11.119 2.205a2 2 0 0 1 1.762 0l7.84 3.846A.5.5 0 0 1 20.5 7h-17a.5.5 0 0 1-.22-.949z\" /> <path d=\"M14 18v-7\" /> <path d=\"M18 18v-7\" /> <path d=\"M3 22h18\" /> <path d=\"M6 18v-7\" />", "trophy": "<path d=\"M10 14.66V17a1 1 0 0 1-1 1 2 2 0 0 0-2 2v2\" /> <path d=\"M14 14.66V17a1 1 0 0 0 1 1 2 2 0 0 1 2 2v2\" /> <path d=\"M17.916 10H19.5A2.5 2.5 0 0 0 22 7.5V5a1 1 0 0 0-1-1h-3\" /> <path d=\"M4 22h16\" /> <path d=\"M6 9a6 6 0 0 0 12 0V3a1 1 0 0 0-1-1H7a1 1 0 0 0-1 1z\" /> <path d=\"M6.084 10H4.5A2.5 2.5 0 0 1 2 7.5V5a1 1 0 0 1 1-1h3\" />", "flask-conical": "<path d=\"M14 2v6a2 2 0 0 0 .245.96l5.51 10.08A2 2 0 0 1 18 22H6a2 2 0 0 1-1.755-2.96l5.51-10.08A2 2 0 0 0 10 8V2\" /> <path d=\"M6.453 15h11.094\" /> <path d=\"M8.5 2h7\" />", "trending-up": "<path d=\"M16 7h6v6\" /> <path d=\"m22 7-8.5 8.5-5-5L2 17\" />", "scroll": "<path d=\"M19 17V5a2 2 0 0 0-2-2H4\" /> <path d=\"M8 21h12a2 2 0 0 0 2-2v-1a1 1 0 0 0-1-1H11a1 1 0 0 0-1 1v1a2 2 0 1 1-4 0V5a2 2 0 1 0-4 0v2a1 1 0 0 0 1 1h3\" />", "bell": "<path d=\"M10.268 21a2 2 0 0 0 3.464 0\" /> <path d=\"M3.262 15.326A1 1 0 0 0 4 17h16a1 1 0 0 0 .74-1.673C19.41 13.956 18 12.499 18 8A6 6 0 0 0 6 8c0 4.499-1.411 5.956-2.738 7.326\" />", "message-circle-heart": "<path d=\"M2.992 16.342a2 2 0 0 1 .094 1.167l-1.065 3.29a1 1 0 0 0 1.236 1.168l3.413-.998a2 2 0 0 1 1.099.092 10 10 0 1 0-4.777-4.719\" /> <path d=\"M7.828 13.07A3 3 0 0 1 12 8.764a3 3 0 0 1 5.004 2.224 3 3 0 0 1-.832 2.083l-3.447 3.62a1 1 0 0 1-1.45-.001z\" />", "plus": "<path d=\"M5 12h14\" /> <path d=\"M12 5v14\" />", "cloud-rain": "<path d=\"M4 14.899A7 7 0 1 1 15.71 8h1.79a4.5 4.5 0 0 1 2.5 8.242\" /> <path d=\"M16 14v6\" /> <path d=\"M8 14v6\" /> <path d=\"M12 16v6\" />", "sparkles": "<path d=\"M11.017 2.814a1 1 0 0 1 1.966 0l1.051 5.558a2 2 0 0 0 1.594 1.594l5.558 1.051a1 1 0 0 1 0 1.966l-5.558 1.051a2 2 0 0 0-1.594 1.594l-1.051 5.558a1 1 0 0 1-1.966 0l-1.051-5.558a2 2 0 0 0-1.594-1.594l-5.558-1.051a1 1 0 0 1 0-1.966l5.558-1.051a2 2 0 0 0 1.594-1.594z\" /> <path d=\"M20 2v4\" /> <path d=\"M22 4h-4\" /> <circle cx=\"4\" cy=\"20\" r=\"2\" />", "newspaper": "<path d=\"M15 18h-5\" /> <path d=\"M18 14h-8\" /> <path d=\"M4 22h16a2 2 0 0 0 2-2V4a2 2 0 0 0-2-2H8a2 2 0 0 0-2 2v16a2 2 0 0 1-4 0v-9a2 2 0 0 1 2-2h2\" /> <rect width=\"8\" height=\"4\" x=\"10\" y=\"6\" rx=\"1\" />", "flag": "<path d=\"M4 22V4a1 1 0 0 1 .4-.8A6 6 0 0 1 8 2c3 0 5 2 7.333 2q2 0 3.067-.8A1 1 0 0 1 20 4v10a1 1 0 0 1-.4.8A6 6 0 0 1 16 16c-3 0-5-2-8-2a6 6 0 0 0-4 1.528\" />", "volume-2": "<path d=\"M11 4.702a.705.705 0 0 0-1.203-.498L6.413 7.587A1.4 1.4 0 0 1 5.416 8H3a1 1 0 0 0-1 1v6a1 1 0 0 0 1 1h2.416a1.4 1.4 0 0 1 .997.413l3.383 3.384A.705.705 0 0 0 11 19.298z\" /> <path d=\"M16 9a5 5 0 0 1 0 6\" /> <path d=\"M19.364 18.364a9 9 0 0 0 0-12.728\" />", "check": "<path d=\"M20 6 9 17l-5-5\" />", "x": "<path d=\"M18 6 6 18\" /> <path d=\"m6 6 12 12\" />", "chevron-left": "<path d=\"m15 18-6-6 6-6\" />", "chevron-right": "<path d=\"m9 18 6-6-6-6\" />", "pencil": "<path d=\"M21.174 6.812a1 1 0 0 0-3.986-3.987L3.842 16.174a2 2 0 0 0-.5.83l-1.321 4.352a.5.5 0 0 0 .623.622l4.353-1.32a2 2 0 0 0 .83-.497z\" /> <path d=\"m15 5 4 4\" />", "trash-2": "<path d=\"M10 11v6\" /> <path d=\"M14 11v6\" /> <path d=\"M19 6v14a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V6\" /> <path d=\"M3 6h18\" /> <path d=\"M8 6V4a2 2 0 0 1 2-2h4a2 2 0 0 1 2 2v2\" />", "square": "<rect width=\"18\" height=\"18\" x=\"3\" y=\"3\" rx=\"2\" />", "file-text": "<path d=\"M6 22a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h8a2.4 2.4 0 0 1 1.704.706l3.588 3.588A2.4 2.4 0 0 1 20 8v12a2 2 0 0 1-2 2z\" /> <path d=\"M14 2v5a1 1 0 0 0 1 1h5\" /> <path d=\"M10 9H8\" /> <path d=\"M16 13H8\" /> <path d=\"M16 17H8\" />", "upload": "<path d=\"M12 3v12\" /> <path d=\"m17 8-5-5-5 5\" /> <path d=\"M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4\" />", "layers": "<path d=\"M12.83 2.18a2 2 0 0 0-1.66 0L2.6 6.08a1 1 0 0 0 0 1.83l8.58 3.91a2 2 0 0 0 1.66 0l8.58-3.9a1 1 0 0 0 0-1.83z\" /> <path d=\"M2 12a1 1 0 0 0 .58.91l8.6 3.91a2 2 0 0 0 1.65 0l8.58-3.9A1 1 0 0 0 22 12\" /> <path d=\"M2 17a1 1 0 0 0 .58.91l8.6 3.91a2 2 0 0 0 1.65 0l8.58-3.9A1 1 0 0 0 22 17\" />", "clipboard-check": "<rect width=\"8\" height=\"4\" x=\"8\" y=\"2\" rx=\"1\" ry=\"1\" /> <path d=\"M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2\" /> <path d=\"m9 14 2 2 4-4\" />", "message-circle-question": "<path d=\"M2.992 16.342a2 2 0 0 1 .094 1.167l-1.065 3.29a1 1 0 0 0 1.236 1.168l3.413-.998a2 2 0 0 1 1.099.092 10 10 0 1 0-4.777-4.719\" /> <path d=\"M9 9.5a3 2.5 0 016 0c0 2-2 2-3 3.5\" /> <path d=\"M12 17h.01\" />", "calendar-range": "<rect x=\"3\" y=\"3\" width=\"18\" height=\"18\" rx=\"2\" /> <path d=\"M16 2v3\" /> <path d=\"M3 9h18\" /> <path d=\"M8 2v3\" /> <path d=\"M17 13h-6\" /> <path d=\"M13 17H7\" /> <path d=\"M7 13h.01\" /> <path d=\"M17 17h.01\" />", "flame": "<path d=\"M12 3q1 4 4 6.5t3 5.5a1 1 0 0 1-14 0 5 5 0 0 1 1-3 1 1 0 0 0 5 0c0-2-1.5-3-1.5-5q0-2 2.5-4\" />", "award": "<path d=\"m15.477 12.89 1.515 8.526a.5.5 0 0 1-.81.47l-3.58-2.687a1 1 0 0 0-1.197 0l-3.586 2.686a.5.5 0 0 1-.81-.469l1.514-8.526\" /> <circle cx=\"12\" cy=\"8\" r=\"6\" />", "settings": "<path d=\"M9.671 4.136a2.34 2.34 0 0 1 4.659 0 2.34 2.34 0 0 0 3.319 1.915 2.34 2.34 0 0 1 2.33 4.033 2.34 2.34 0 0 0 0 3.831 2.34 2.34 0 0 1-2.33 4.033 2.34 2.34 0 0 0-3.319 1.915 2.34 2.34 0 0 1-4.659 0 2.34 2.34 0 0 0-3.32-1.915 2.34 2.34 0 0 1-2.33-4.033 2.34 2.34 0 0 0 0-3.831A2.34 2.34 0 0 1 6.35 6.051a2.34 2.34 0 0 0 3.319-1.915\" /> <circle cx=\"12\" cy=\"12\" r=\"3\" />", "eye": "<path d=\"M2.062 12.348a1 1 0 0 1 0-.696 10.75 10.75 0 0 1 19.876 0 1 1 0 0 1 0 .696 10.75 10.75 0 0 1-19.876 0\" /> <circle cx=\"12\" cy=\"12\" r=\"3\" />", "refresh-ccw": "<path d=\"M21 12a9 9 0 0 0-9-9 9.75 9.75 0 0 0-6.74 2.74L3 8\" /> <path d=\"M3 3v5h5\" /> <path d=\"M3 12a9 9 0 0 0 9 9 9.75 9.75 0 0 0 6.74-2.74L21 16\" /> <path d=\"M16 16h5v5\" />", "log-out": "<path d=\"m16 17 5-5-5-5\" /> <path d=\"M21 12H9\" /> <path d=\"M9 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h4\" />", "fish": "<path d=\"M6.5 12c.94-3.46 4.94-6 8.5-6 3.56 0 6.06 2.54 7 6-.94 3.47-3.44 6-7 6s-7.56-2.53-8.5-6Z\" /> <path d=\"M18 12v.5\" /> <path d=\"M16 17.93a9.77 9.77 0 0 1 0-11.86\" /> <path d=\"M7 10.67C7 8 5.58 5.97 2.73 5.5c-1 1.5-1 5 .23 6.5-1.24 1.5-1.24 5-.23 6.5C5.58 18.03 7 16 7 13.33\" /> <path d=\"M10.46 7.26C10.2 5.88 9.17 4.24 8 3h5.8a2 2 0 0 1 1.98 1.67l.23 1.4\" /> <path d=\"m16.01 17.93-.23 1.4A2 2 0 0 1 13.8 21H9.5a5.96 5.96 0 0 0 1.49-3.98\" />", "external-link": "<path d=\"M15 3h6v6\" /> <path d=\"M10 14 21 3\" /> <path d=\"M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6\" />", "info": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M12 16v-4\" /> <path d=\"M12 8h.01\" />", "gift": "<path d=\"M12 7v14\" /> <path d=\"M20 11v8a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2v-8\" /> <path d=\"M7.5 7a1 1 0 0 1 0-5A4.8 8 0 0 1 12 7a4.8 8 0 0 1 4.5-5 1 1 0 0 1 0 5\" /> <rect x=\"3\" y=\"7\" width=\"18\" height=\"4\" rx=\"1\" />", "circle-plus": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M8 12h8\" /> <path d=\"M12 8v8\" />", "tag": "<path d=\"M12.586 2.586A2 2 0 0 0 11.172 2H4a2 2 0 0 0-2 2v7.172a2 2 0 0 0 .586 1.414l8.704 8.704a2.426 2.426 0 0 0 3.42 0l6.58-6.58a2.426 2.426 0 0 0 0-3.42z\" /> <circle cx=\"7.5\" cy=\"7.5\" r=\".5\" fill=\"currentColor\" />", "image": "<rect width=\"18\" height=\"18\" x=\"3\" y=\"3\" rx=\"2\" ry=\"2\" /> <circle cx=\"9\" cy=\"9\" r=\"2\" /> <path d=\"m21 15-3.086-3.086a2 2 0 0 0-2.828 0L6 21\" />", "file-pen-line": "<path d=\"M14.364 13.634a2 2 0 0 0-.506.854l-.837 2.87a.5.5 0 0 0 .62.62l2.87-.837a2 2 0 0 0 .854-.506l4.013-4.009a1 1 0 0 0-3.004-3.004z\" /> <path d=\"M14.487 7.858A1 1 0 0 1 14 7V2\" /> <path d=\"M20 19.645V20a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V4a2 2 0 0 1 2-2h8a2.4 2.4 0 0 1 1.704.706l2.516 2.516\" /> <path d=\"M8 18h1\" />", "sprout": "<path d=\"M14 9.536V7a4 4 0 0 1 4-4h1.5a.5.5 0 0 1 .5.5V5a4 4 0 0 1-4 4 4 4 0 0 0-4 4c0 2 1 3 1 5a5 5 0 0 1-1 3\" /> <path d=\"M4 9a5 5 0 0 1 8 4 5 5 0 0 1-8-4\" /> <path d=\"M5 21h14\" />", "mountain": "<path d=\"m8 3 4 8 5-5 5 15H2L8 3z\" />", "frown": "<path d=\"M15 10V9\" /> <path d=\"M9 10V9\" /> <path d=\"M9 16a5 5 0 016 0\" /> <circle cx=\"12\" cy=\"12\" r=\"10\" />", "repeat": "<path d=\"m17 2 4 4-4 4\" /> <path d=\"M3 11v-1a4 4 0 0 1 4-4h14\" /> <path d=\"m7 22-4-4 4-4\" /> <path d=\"M21 13v1a4 4 0 0 1-4 4H3\" />", "smile": "<path d=\"M15 10V9\" /> <path d=\"M16.472 15a6 6 0 01-8.943 0\" /> <path d=\"M9 10V9\" /> <circle cx=\"12\" cy=\"12\" r=\"10\" />", "meh": "<path d=\"M15 10V9\" /> <path d=\"M8 16h8\" /> <path d=\"M9 10V9\" /> <circle cx=\"12\" cy=\"12\" r=\"10\" />", "zap": "<path d=\"M15.914 4a1.5 1.5 0 00-2.474-1.561l-9 9A1.5 1.5 0 005.5 14h4.002a.5.5 0 01.471.666L8.086 20a1.5 1.5 0 002.475 1.56l9-9A1.5 1.5 0 0018.5 10h-3.997a.5.5 0 01-.472-.667z\" />", "circle-check": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"m16 9-5.5 5.5L8 12\" />", "compass": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"m16.24 7.76-1.804 5.411a2 2 0 0 1-1.265 1.265L7.76 16.24l1.804-5.411a2 2 0 0 1 1.265-1.265z\" />", "hand": "<path d=\"M18 11V6a2 2 0 0 0-2-2a2 2 0 0 0-2 2\" /> <path d=\"M14 10V4a2 2 0 0 0-2-2a2 2 0 0 0-2 2v2\" /> <path d=\"M10 10.5V6a2 2 0 0 0-2-2a2 2 0 0 0-2 2v8\" /> <path d=\"M18 8a2 2 0 1 1 4 0v6a8 8 0 0 1-8 8h-2c-2.8 0-4.5-.86-5.99-2.34l-3.6-3.6a2 2 0 0 1 2.83-2.82L7 15\" />", "focus": "<circle cx=\"12\" cy=\"12\" r=\"3\" /> <path d=\"M3 7V5a2 2 0 0 1 2-2h2\" /> <path d=\"M17 3h2a2 2 0 0 1 2 2v2\" /> <path d=\"M21 17v2a2 2 0 0 1-2 2h-2\" /> <path d=\"M7 21H5a2 2 0 0 1-2-2v-2\" />", "coffee": "<path d=\"M10 2v2\" /> <path d=\"M14 2v2\" /> <path d=\"M16 8a1 1 0 0 1 1 1v8a4 4 0 0 1-4 4H7a4 4 0 0 1-4-4V9a1 1 0 0 1 1-1h14a4 4 0 1 1 0 8h-1\" /> <path d=\"M6 2v2\" />", "wind": "<path d=\"M12.8 19.6A2 2 0 1 0 14 16H2\" /> <path d=\"M17.5 8a2.5 2.5 0 1 1 2 4H2\" /> <path d=\"M9.8 4.4A2 2 0 1 1 11 8H2\" />", "bell-ring": "<path d=\"M10.268 21a2 2 0 0 0 3.464 0\" /> <path d=\"M22 8c0-2.3-.8-4.3-2-6\" /> <path d=\"M3.262 15.326A1 1 0 0 0 4 17h16a1 1 0 0 0 .74-1.673C19.41 13.956 18 12.499 18 8A6 6 0 0 0 6 8c0 4.499-1.411 5.956-2.738 7.326\" /> <path d=\"M4 2C2.8 3.7 2 5.7 2 8\" />", "circle-help": "<circle cx=\"12\" cy=\"12\" r=\"10\" /> <path d=\"M9 9.5a3 2.5 0 016 0c0 2-2 2-3 3.5\" /> <path d=\"M12 17h.01\" />", "arrow-right": "<path d=\"M5 12h14\" /> <path d=\"m12 5 7 7-7 7\" />", "sparkle": "<path d=\"M11.017 2.814a1 1 0 0 1 1.966 0l1.051 5.558a2 2 0 0 0 1.594 1.594l5.558 1.051a1 1 0 0 1 0 1.966l-5.558 1.051a2 2 0 0 0-1.594 1.594l-1.051 5.558a1 1 0 0 1-1.966 0l-1.051-5.558a2 2 0 0 0-1.594-1.594l-5.558-1.051a1 1 0 0 1 0-1.966l5.558-1.051a2 2 0 0 0 1.594-1.594z\" />", "star": "<path d=\"M11.525 2.295a.53.53 0 0 1 .95 0l2.31 4.679a2.123 2.123 0 0 0 1.595 1.16l5.166.756a.53.53 0 0 1 .294.904l-3.736 3.638a2.123 2.123 0 0 0-.611 1.878l.882 5.14a.53.53 0 0 1-.771.56l-4.618-2.428a2.122 2.122 0 0 0-1.973 0L6.396 21.01a.53.53 0 0 1-.77-.56l.881-5.139a2.122 2.122 0 0 0-.611-1.879L2.16 9.795a.53.53 0 0 1 .294-.906l5.165-.755a2.122 2.122 0 0 0 1.597-1.16z\" />", "type": "<path d=\"M12 4v16\" /> <path d=\"M4 7V5a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v2\" /> <path d=\"M9 20h6\" />"};

/* ===== sistema visual: íconos, categorías, lectura en voz alta ===== */
function ic(n,sz=24,sw=2){return`<svg class="ico" viewBox="0 0 24 24" width="${sz}" height="${sz}" fill="none" stroke="currentColor" stroke-width="${sw}" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">${ICO[n]||ICO["circle-dot"]}</svg>`}
function icb(n,c,sz=56,cls=""){return`<span class="icb ${cls}" style="--c:${c||"var(--teal2)"};width:${sz}px;height:${sz}px">${ic(n,Math.round(sz*.5),2.1)}</span>`}
const CAT_IC={estudio:"book-open-text",clase:"presentation",examen:"graduation-cap",trabajo:"briefcase",deporte:"dumbbell",lectura:"book-marked",proyecto:"palette",reunion:"users",salud:"stethoscope",personal:"heart",recreacion:"party-popper",descanso:"bed",otra:"circle-dot"};
const catI=c=>CAT_IC[c]||"circle-dot";
function guessIcon(t){t=(t||"").toLowerCase();const m=[[/instagram|tiktok|redes|celu|pantalla|youtube|scroll/,"smartphone"],[/estudi|repas|examen|parcial/,"book-open-text"],[/le[eé]r|lectura|p[aá]gina|libro/,"book-marked"],[/entren|deporte|gym|gimnasio|correr|mover|caminar/,"dumbbell"],[/dorm|acost|sueño/,"moon"],[/plan|organi|agenda/,"calendar-check"],[/com(er|ida)|cocin/,"chef-hat"],[/medit|respir/,"leaf"],[/dibuj|diseñ|proyecto/,"palette"],[/idioma|ingl/,"languages"],[/m[uú]sica|guitarra|instrumento/,"guitar"]];for(const[r,n]of m)if(r.test(t))return n;return"sprout"}
const OPT_IC={"Quiero dejar de procrastinar":"hourglass","Quiero estudiar más y mejor":"graduation-cap","Quiero organizar mi rutina":"calendar-check","Quiero reducir el tiempo en redes sociales":"smartphone","Quiero dedicarle más tiempo a mis proyectos personales":"rocket","Quiero incorporar hábitos saludables":"heart-pulse","Quiero aprovechar mejor mi tiempo":"clock",
"Ser más organizado/a":"list-checks","Mejorar mi rendimiento académico":"graduation-cap","Ser más constante con el deporte":"dumbbell","Aprender cosas nuevas":"lightbulb","Tener más tiempo libre de calidad":"sun","Cumplir mis objetivos personales":"target",
"Menos de 2 horas":"battery-full","Entre 2 y 4 horas":"battery-medium","Entre 4 y 6 horas":"battery-low","Más de 6 horas":"battery-warning",
"Instagram":"camera","TikTok":"music","YouTube":"play","X":"at-sign","WhatsApp":"message-circle","Juegos":"gamepad-2",
"A la mañana":"sunrise","A la tarde":"sun","A la noche":"moon","Durante todo el día":"infinity",
"La postergo hasta último momento":"hourglass","Me distraigo con el celular":"smartphone","Me cuesta empezar":"footprints","Empiezo, pero pierdo la concentración":"brain","Me cuesta organizarme":"shuffle",
"Leer":"book-marked","Estudiar":"book-open-text","Entrenar":"dumbbell","Aprender un idioma":"languages","Dibujar o diseñar":"pen-tool","Tocar un instrumento":"guitar","Meditar":"leaf","Cocinar":"chef-hat","Un proyecto personal":"rocket",
"2 a 4 horas":"clock-2","5 a 7 horas":"clock-5","8 a 12 horas":"clock-8","Más de 12 horas":"clock-12",
"Arte y diseño":"palette","Política y actualidad":"landmark","Deportes":"trophy","Ciencia y tecnología":"flask-conical","Cultura y música":"music","Economía":"trending-up","Historia":"scroll",
"Con recordatorios":"bell","Con desafíos diarios":"target","Con estadísticas de progreso":"chart-column","Con mensajes motivadores":"message-circle-heart","Con objetivos pequeños y alcanzables":"footprints"};
const OPT_SHORT={"Quiero dejar de procrastinar":"Dejar de postergar","Quiero estudiar más y mejor":"Estudiar mejor","Quiero organizar mi rutina":"Organizar mi rutina","Quiero reducir el tiempo en redes sociales":"Menos redes","Quiero dedicarle más tiempo a mis proyectos personales":"Mis proyectos","Quiero incorporar hábitos saludables":"Hábitos sanos","Quiero aprovechar mejor mi tiempo":"Aprovechar el tiempo","La postergo hasta último momento":"La dejo para el final","Empiezo, pero pierdo la concentración":"Pierdo la concentración","Con objetivos pequeños y alcanzables":"Pasos chiquitos","Con estadísticas de progreso":"Estadísticas","Con mensajes motivadores":"Mensajes de aliento","Con desafíos diarios":"Desafíos","Con recordatorios":"Recordatorios","Tener más tiempo libre de calidad":"Tiempo libre de calidad","Cumplir mis objetivos personales":"Cumplir objetivos","Mejorar mi rendimiento académico":"Rendir mejor","Ser más constante con el deporte":"Constancia en el deporte"};
const optI=o=>OPT_IC[o]||"tag";
const optL=o=>OPT_SHORT[o]||o;
const optTile=(o,on,attr="data-o",c)=>`<button class="chip" aria-pressed="${on}" ${attr}="${esc(o)}" title="${esc(o)}">${icb(optI(o),c,48)}<span>${esc(optL(o))}</span></button>`;
const say=(t,lbl="Escuchar")=>`<button class="say" data-say="${esc(t)}" aria-label="${lbl}" title="${lbl}">${ic("volume-2",17)}</button>`;
const shead=(n,t,c,extra="")=>`<div class="shead">${icb(n,c,36)}<h3>${t}</h3>${extra}</div>`;
let speaking=null;
document.addEventListener("click",e=>{const b=e.target.closest("[data-say]");if(!b)return;e.stopPropagation();
 if(!("speechSynthesis" in window)){toast("Tu navegador no puede leer en voz alta.");return}
 const syn=speechSynthesis;if(speaking===b){syn.cancel();b.classList.remove("on");speaking=null;return}
 syn.cancel();if(speaking)speaking.classList.remove("on");
 const u=new SpeechSynthesisUtterance(b.dataset.say);u.lang="es-AR";u.rate=.92;
 const v=syn.getVoices().find(v=>/^es[-_](AR|419|MX|US)/i.test(v.lang))||syn.getVoices().find(v=>/^es/i.test(v.lang));if(v)u.voice=v;
 u.onend=u.onerror=()=>{b.classList.remove("on");if(speaking===b)speaking=null};
 speaking=b;b.classList.add("on");syn.speak(u);
},true);
function applyEasy(){document.documentElement.classList.toggle("easy",!!(S&&S.easy))}

/* ============ estado y persistencia ============ */
const LS="proki-v2", LSM="proki-mats-v2";
const blank=()=>({v:2,phase:"welcome",qi:0,iv:{nombre:"",motivo:[],meta3:[],pantalla:"",apps:[],momento:"",pendiente:[],actividades:[],horas:"",temas:[],motivacion:[]},
 profile:null,goals:[],later:[],acts:[],exams:[],logs:[],screen:{},rest:{},checkins:[],lastCheckin:null,limits:{},timer:null,achieved:[],fish:{name:"Proki",hue:0},best:0,reco:{},tox:{entries:[],booms:[]},toxLimit:0,easy:false});
let S=blank(), MATS={};
try{const r=localStorage.getItem(LS);if(r)S=Object.assign(blank(),JSON.parse(r));const m=localStorage.getItem(LSM);if(m)MATS=JSON.parse(m)}catch(e){}

let DB=null,UIDP=null,stRef=null,sT=null,saving=false,again=false;
function save(){try{localStorage.setItem(LS,JSON.stringify(S))}catch(e){}if(!stRef)return;clearTimeout(sT);sT=setTimeout(flush,700)}
async function flush(){if(!stRef||S.demo)return;if(saving){again=true;return}saving=true;
 try{await stRef.set({type:"state",state:JSON.stringify(S),updated:Date.now()})}catch(e){}
 saving=false;if(again){again=false;flush()}}
function saveMatsLocal(){try{localStorage.setItem(LSM,JSON.stringify(MATS))}catch(e){}}
async function putMat(m){MATS[m.id]=m;saveMatsLocal();if(DB)try{await DB.collection(UIDP).doc("mat_"+m.id).set(Object.assign({type:"mat"},m))}catch(e){toast("No se pudo guardar el material en la nube; quedó en este dispositivo.")}}
async function delMat(id){delete MATS[id];saveMatsLocal();if(DB)try{await DB.collection(UIDP).doc("mat_"+id).delete()}catch(e){}}

const HAS=typeof window.claude!=="undefined"&&window.claude&&typeof window.claude.use==="function";
const sampleP=HAS?window.claude.use("sample").catch(()=>null):Promise.resolve(null);
let cloud="local";
(async()=>{if(!HAS)return;try{
 const[db,user]=await Promise.all([window.claude.use("db"),window.claude.use("user")]);if(!db||!user)return;
 const id=await user.id();if(!id)return;UIDP="data/users/"+id;DB=db;stRef=db.doc(UIDP+"/proki");
 const snap=await stRef.get();
 if(snap.exists){const d=snap.data();if(d&&typeof d.state==="string"){S=Object.assign(blank(),JSON.parse(d.state));localStorage.setItem(LS,d.state)}}
 else if(S.phase!=="welcome")flush();
 const q=await db.collection(UIDP).where("type","==","mat").get();
 const local=Object.assign({},MATS);MATS={};
 q.docs.forEach(s=>{const d=s.data();if(d&&d.id)MATS[d.id]=d});
 for(const m of Object.values(local))if(!MATS[m.id])await putMat(m);
 saveMatsLocal();cloud="cloud";render();
}catch(e){}})();

/* ============ IA ============ */
const wait=(p,ms)=>Promise.race([p,new Promise(r=>setTimeout(()=>r(null),ms))]);
const AIERR={not_granted:"Para esto PROKI necesita usar Claude. Permitilo cuando aparezca el aviso.",rate_limited:"Muchas consultas seguidas. Probá de nuevo en un minuto."};
async function ai(prompt,opts={}){
 const s=await wait(sampleP,11000);if(!s)throw{code:"unavailable",message:"La IA no está disponible en esta vista."};
 return s.json(prompt,Object.assign({modelTier:"default"},opts));
}
const aiMsg=e=>AIERR[e&&e.code]||"No pudimos conectar con la IA ahora. Probá de nuevo en un rato.";
const VOICE="Sos PROKI, un asistente latinoamericano que ayuda a dejar de procrastinar con progreso gradual. Escribís en español rioplatense con voseo, cercano, positivo, sin culpa, sin exigir productividad constante, sin comparar con otras personas. Descansar es parte de una rutina sana.";

const GLY={"P": {"d": "M131 0C189 0 226 34 226 85C226 152 196 242 222 242C380 242 497 302 497 442C497 612 369 664 206 664C67 664 25 640 25 330C25 120 38 0 131 0ZM211 451C211 487 220 505 237 505C273 505 309 491 309 445C309 381 273 372 232 372C214 372 211 387 211 451Z", "w": 507}, "R": {"d": "M441 -2C499 -2 522 28 522 78C522 179 447 287 385 344C454 368 494 426 494 495C494 650 356 664 209 664C72 664 26 652 26 330C26 20 77 0 133 0C207 0 221 54 221 105C221 151 208 222 208 248C208 264 210 273 223 273C240 273 288 227 331 98C358 15 400 -2 441 -2ZM209 456C209 500 211 516 236 516C275 516 305 498 305 466C305 412 273 397 230 397C213 397 209 411 209 456Z", "w": 533}, "K": {"d": "M122 0C179 0 220 11 220 101C220 139 207 214 207 242C207 261 211 269 222 269C253 269 308 168 331 98C356 23 393 -2 439 -2C493 -2 513 33 513 73C513 219 382 337 358 354C363 357 400 385 430 422C478 482 502 553 495 589C482 638 441 660 404 660C338 660 269 431 222 431C214 431 214 439 214 473C214 606 203 660 123 660C57 660 26 629 26 339C26 62 64 0 122 0Z", "w": 520}, "I": {"d": "M33 330C33 62 60 0 141 0C222 0 232 62 232 330C232 597 214 660 133 660C52 660 33 597 33 330Z", "w": 265}, "O": {"d": "M307 -6C485 -6 591 109 591 326C591 575 485 667 307 667C138 667 20 575 20 326C20 109 138 -6 307 -6ZM216 326C216 438 250 483 306 483C363 483 395 438 395 326C395 233 363 180 306 180C250 180 216 233 216 326Z", "w": 611}};
const FISH={"normal": {"src": "data:image/png;base64,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", "w": 320, "h": 272}, "happy": {"src": "data:image/png;base64,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", "w": 320, "h": 272}, "worried": {"src": "data:image/png;base64,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", "w": 320, "h": 272}, "reading": {"src": "data:image/png;base64,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", "w": 320, "h": 272}, "inflated": {"src": "data:image/png;base64,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", "w": 384, "h": 352}, "phone": {"src": "data:image/png;base64,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", "w": 320, "h": 272}, "flat": {"src": "data:image/png;base64,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", "w": 320, "h": 272}};

/* ============ identidad: logo y pez globo ============ */
const HUES=[["Original",0],["Menta",-40],["Lavanda",55],["Coral",150]];
const fishHue=()=>(S.fish&&S.fish.hue)||0;
const fishName=()=>(S.fish&&S.fish.name)||"Proki";
function fishImg(m,w,cls=""){const f=FISH[m]||FISH.normal;const ww=Math.round(w*f.w/320);return`<img class="px ${cls}" src="${f.src}" width="${ww}" height="${Math.round(ww*f.h/f.w)}" alt="" style="filter:hue-rotate(${fishHue()}deg)">`}
function logoSVG(h,withFish=true){
 const tr=-28;let x=0,parts="";const g=c=>{const o=GLY[c];parts+=`<path transform="translate(${x} 700) scale(1 -1)" d="${o.d}"/>`;x+=o.w+tr};
 g("P");g("R");if(withFish){const f=FISH.normal,fw=820,fh=fw*f.h/f.w;parts+=`<image href="${f.src}" x="${x-40}" y="${700-fh+60}" width="${fw}" height="${fh}" style="image-rendering:pixelated;filter:hue-rotate(${fishHue()}deg)"/>`;x+=fw-120}else g("O");g("K");g("I");
 return`<svg class="logo" viewBox="-10 -70 ${x+30} 820" style="height:${h}px;width:auto" role="img" aria-label="PROKI">${parts}</svg>`;
}
/* progreso de un hábito: 14 burbujas */
function sprout(days){const n=14,d=Math.min(days,n);let c="";for(let i=0;i<n;i++){const a=(i/n)*Math.PI*2-Math.PI/2;c+=`<circle cx="${40+Math.cos(a)*30}" cy="${40+Math.sin(a)*30}" r="5.2" fill="${i<d?"var(--teal2)":"none"}" stroke="var(--teal2)" stroke-width="1.6"/>`}
 return`<svg viewBox="0 0 80 80" aria-hidden="true">${c}<text x="40" y="46" text-anchor="middle" font-family="Bricolage Grotesque, sans-serif" font-weight="800" font-size="20" fill="var(--ink)">${days}</text></svg>`}
function bestStreak(){const set=new Set();S.logs.forEach(l=>set.add(l.date));S.goals.concat(S.achievedFull||[]).forEach(g=>Object.keys(g.log||{}).forEach(d=>(g.log[d]||[]).length&&set.add(d)));Object.keys(S.rest).forEach(d=>set.add(d));
 const ds=[...set].sort();let best=0,cur=0,prev=null;for(const d of ds){cur=prev&&diffD(prev,d)===1?cur+1:1;best=Math.max(best,cur);prev=d}return Math.max(best,S.best||0)}
function mood(){
 const t=today(),sc=S.screen[t],b=baseline();
 if(S.timer)return["estudio","lectura"].includes(S.timer.cat)?["reading","Concentrado con vos"]:["happy","Acompañándote"];
 if(S.rest[t]==="rest")return["flat","Nadando tranquilo"];
 if(sc!=null&&b&&sc>b+60)return["inflated","Se infló un poco con tanto scroll"];
 if(sc!=null&&b&&sc>b)return["worried","Un poquito inquieto"];
 if(logsOn(t).length||goalTicked(t))return["happy","Contento por tu avance"];
 return["normal","Listo para arrancar"];
}
/* ===== toxinas: el pez se infla con el uso del celu ===== */
const toxS=()=>{S.tox=S.tox||{entries:[],booms:[]};return S.tox};
const toxLimit=()=>S.toxLimit||Object.values(S.limits||{}).reduce((a,b)=>a+(+b||0),0)||120;
function cycleStart(){const t=today(),b=toxS().booms.filter(x=>x.date===t);return b.length?b[b.length-1].ts:0}
const cycleEntries=()=>{const t=today(),cs=cycleStart();return toxS().entries.filter(e=>e.date===t&&e.ts>cs)};
const toxLevel=()=>cycleEntries().reduce((s,e)=>s+e.min,0);
let toxFrom=null,exploding=false,reborn=false;
function toxVis(level){
 const p=Math.min(1,level/toxLimit()),q=Math.max(0,(p-.5)/.5);
 return{p,q,scale:+(1+.72*p).toFixed(3),filter:`saturate(${(1-.35*q).toFixed(2)}) brightness(${(1-.28*q).toFixed(2)}) drop-shadow(0 0 ${(q*16).toFixed(1)}px rgba(140,165,60,${(q*.75).toFixed(2)}))`,
  sprite:p>=.85?"inflated":p>=.6?"worried":null,parts:p>=.55?Math.round(4+q*14):0,tremble:p>=.85};
}
function toxPartsHTML(n){let h="";const cols=["#9AAE45","#7B63A8","#8C9B3E","#A58BC9"];
 for(let i=0;i<n;i++)h+=`<i style="left:${30+Math.random()*40}%;background:${cols[i%4]};animation-delay:${(Math.random()*3.2).toFixed(2)}s;--dx:${(Math.random()*60-30).toFixed(0)}px"></i>`;return h}
function toxMsg(p,md){
 if(p>=.85)return"¡Está a punto de explotar! Buen momento para dejar el celu un rato.";
 if(p>=.6)return"Se está llenando de toxinas. Cada minuto de pantalla lo infla un poco más.";
 if(p>0)return"Cada rato de celu que cargás lo infla un poquito. Vos decidís cuánto crece.";
 return MOODTXT[md]||MOODTXT.normal;
}
function applyTox(level){
 const v=toxVis(level),w=$("#toxWrap");if(!w)return;
 w.style.transform=`scale(${v.scale})`;w.style.filter=v.filter;w.style.setProperty("--s",v.scale);w.classList.toggle("tremble",v.tremble);
 const sp=$("#toxSprite");const want=v.sprite||sp.dataset.base;if(sp.dataset.cur!==want){sp.dataset.cur=want;sp.innerHTML=fishImg(want,110)}
 $("#toxBar").style.width=(v.p*100)+"%";$("#toxBar").style.setProperty("--bw",(v.p>0?100/v.p:100)+"%");
 $("#toxTxt").textContent=`${hm(level)} de ${hm(toxLimit())}`;
 $("#toxParts").innerHTML=toxPartsHTML(v.parts);const lb=$("#toxLbl");if(lb)lb.textContent=v.p>=.85?"a punto de explotar":v.p>=.6?"lleno de toxinas":lb.dataset.ml;$("#heroMsg").textContent=toxMsg(v.p,sp.dataset.base);
}
function addUsage(min,app){
 if(exploding)return;const t=today(),before=toxLevel(),lim=toxLimit();
 toxS().entries.push({id:uid(),date:t,ts:Date.now(),min,app:app||""});S.screen[t]=(S.screen[t]||0)+min;
 const after=before+min;toxFrom=before;save();closeSheet();
 if(tab!=="inicio"){tab="inicio";try{history.replaceState(null,"","#inicio")}catch(e){}}
 render();window.scrollTo({top:0,behavior:"smooth"});
 requestAnimationFrame(()=>requestAnimationFrame(()=>{toxFrom=null;applyTox(Math.min(after,lim))}));
 if(after>=lim){exploding=true;setTimeout(()=>explode(after),1500)}
 else{const p=after/lim;toast(p>=.85?`${fishName()} está al límite.`:p>=.6?`${fishName()} se está inflando.`:`Cargaste ${hm(min)}. ${fishName()} lo sintió.`)}
}
function explode(total){
 const lim=toxLimit(),t=today();toxS().booms.push({ts:Date.now(),date:t,min:total});save();
 const reduce=matchMedia("(prefers-reduced-motion: reduce)").matches;
 try{navigator.vibrate&&navigator.vibrate([70,40,160])}catch(e){}
 const w=$("#toxWrap");let cx=innerWidth/2,cy=innerHeight/3;
 if(w){const r=w.getBoundingClientRect();cx=r.left+r.width/2;cy=r.top+r.height/2;w.classList.remove("tremble");w.classList.add("boom")}
 const fx=document.createElement("div");fx.id="toxfx";fx.setAttribute("role","dialog");fx.setAttribute("aria-modal","true");fx.setAttribute("aria-labelledby","boomT");
 let h="";
 if(!reduce){
  h+=`<span class="flash" style="left:${cx-20}px;top:${cy-20}px"></span>`;
  const sc=["#8FD3EE","#2F5568","#C8DFDB","#9AAE45","#7B63A8","#F3EFE8"];
  for(let i=0;i<26;i++){const a=Math.random()*Math.PI*2,d=120+Math.random()*220;h+=`<span class="shard" style="left:${cx-5}px;top:${cy-5}px;background:${sc[i%6]};--dx:${(Math.cos(a)*d).toFixed(0)}px;--dy:${(Math.sin(a)*d).toFixed(0)}px;--r:${(Math.random()*540-270).toFixed(0)}deg;animation-delay:${180+Math.random()*80}ms"></span>`}
 }
 const cl=["rgba(154,174,69,.9)","rgba(123,99,168,.85)","rgba(140,155,62,.88)","rgba(118,189,205,.7)","rgba(165,139,201,.85)"];
 const big=Math.max(innerWidth,innerHeight);
 for(let i=0;i<10;i++){const sz=big*(.55+Math.random()*.6),ox=(Math.random()-.5)*innerWidth*.9,oy=(Math.random()-.5)*innerHeight*.9;
  h+=`<span class="cloud" style="width:${sz}px;height:${sz}px;left:${cx+ox*(i/10)-sz/2}px;top:${cy+oy*(i/10)-sz/2}px;background:radial-gradient(circle,${cl[i%5]} 0%,${cl[(i+2)%5]} 55%,transparent 72%);animation-delay:${reduce?0:250+i*70}ms"></span>`}
 h+=`<div class="boomcard" id="boomCard">${fishImg("flat",96)}<h2 id="boomT">Tu pez explotó.</h2><p class="mt" style="font-size:18px;font-weight:600">Es momento de recuperar tu tiempo.</p>
  <p class="small muted mt">En este ciclo acumulaste ${hm(total)} de celular, más que tu límite de ${hm(lim)}.</p>
  <p class="small mt">No pasa nada: ${esc(fishName())} vuelve a empezar, y vos también.</p>
  <div class="actions" style="justify-content:center"><button class="btn" id="boomFocus">Recuperar 25 minutos ahora</button><button class="btn ghost" id="boomAgain">Volver a empezar</button></div></div>`;
 fx.innerHTML=h;document.body.appendChild(fx);
 setTimeout(()=>{const c=$("#boomCard");c.classList.add("show");$("#boomAgain").focus()},reduce?100:1150);
 const done=(after)=>{fx.classList.add("out");setTimeout(()=>{fx.remove();exploding=false;reborn=true;after?after():render()},850)};
 $("#boomAgain").onclick=()=>done();
 $("#boomFocus").onclick=()=>done(()=>startTimer({cat:"personal",title:"Tiempo recuperado del celu"}));
 fx.addEventListener("keydown",e=>{if(e.key==="Escape")done()});
}
function usageSheet(){
 const apps=[...new Set((S.iv.apps||[]).concat(Object.keys(S.limits||{})))].concat(["Otra"]);let app="",min=15;
 const draw=()=>{
  const lim=toxLimit(),lv=toxLevel(),p=Math.min(1,(lv+min)/lim);
  const ents=cycleEntries().slice().reverse();
  openSheet(`<div class="row" style="flex-wrap:nowrap;gap:12px"><div>${fishImg("phone",70)}</div><div><h2>¿Cuánto usaste el celu?${say("¿Cuánto usaste el celu? Elegí la app y el tiempo. Cada minuto infla a "+fishName()+".")}</h2><p class="note">Cada minuto infla a ${esc(fishName())}.</p></div></div>
  <label class="f">¿En qué?</label><div class="optgrid sm">${apps.map(a=>`<button class="chip" data-app="${esc(a)}" aria-pressed="${a===app}">${icb(a==="Otra"?"smartphone":optI(a),"#7B63A8",40)}<span>${esc(a)}</span></button>`).join("")}</div>
  <label class="f">Tiempo</label><div class="optgrid sm">${[5,15,30,60].map(m=>`<button class="chip" data-min="${m}" aria-pressed="${m===min}">${icb({5:"clock-2",15:"clock-5",30:"clock-8",60:"clock-12"}[m],"#7B63A8",40)}<span>${hm(m)}</span></button>`).join("")}</div>
  <div class="two mt"><div><label class="f" for="uH" style="margin-top:0">Horas</label><input type="number" id="uH" min="0" max="16" value="${Math.floor(min/60)}"></div><div><label class="f" for="uM" style="margin-top:0">Minutos</label><input type="number" id="uM" min="0" max="59" value="${min%60}"></div></div>
  <div class="card mt" style="background:var(--bg)"><p style="font-weight:600" id="uPrev"></p><div class="toxbar mt" style="background:var(--line)"><i id="uBar" style="width:${p*100}%"></i></div></div>
  <label class="f" for="uL">Límite antes de que explote</label><div class="row" style="flex-wrap:nowrap"><input type="number" id="uL" min="10" max="900" step="5" value="${lim}" style="max-width:120px"><span class="small muted">minutos por día</span></div>
  ${ents.length?`<label class="f">Cargado en este ciclo</label>${ents.map(e=>`<div class="item"><div class="grow"><p>${hm(e.min)}${e.app?` · ${esc(e.app)}`:""}</p><p class="small muted">${new Date(e.ts).toLocaleTimeString("es-AR",{hour:"2-digit",minute:"2-digit"})}</p></div><button class="btn ghost sm" data-del="${e.id}" aria-label="Borrar este registro">✕</button></div>`).join("")}`:""}
  <div class="actions"><button class="btn" id="uOk">Registrar</button><button class="btn ghost" id="uX">Cancelar</button></div>`,()=>{
   const upd=()=>{min=Math.max(0,(+$("#uH").value||0)*60+(+$("#uM").value||0));const L=Math.max(10,+$("#uL").value||toxLimit()),q=(toxLevel()+min)/L;
    $("#uPrev").textContent=min<=0?"Elegí cuánto tiempo usaste.":q>=1?`Con esto ${fishName()} explota.`:`${fishName()} va a quedar al ${Math.round(q*100)}% de su límite.`;$("#uBar").style.width=Math.min(100,q*100)+"%";$("#uOk").disabled=min<=0};
   $$("[data-app]").forEach(c=>c.onclick=()=>{app=app===c.dataset.app?"":c.dataset.app;$$("[data-app]").forEach(x=>x.setAttribute("aria-pressed",x.dataset.app===app))});
   $$("[data-min]").forEach(c=>c.onclick=()=>{min=+c.dataset.min;$("#uH").value=Math.floor(min/60);$("#uM").value=min%60;$$("[data-min]").forEach(x=>x.setAttribute("aria-pressed",x===c));upd()});
   ["#uH","#uM","#uL"].forEach(id=>$(id).oninput=()=>{$$("[data-min]").forEach(x=>x.setAttribute("aria-pressed",+x.dataset.min===((+$("#uH").value||0)*60+(+$("#uM").value||0))));upd()});
   $$("[data-del]").forEach(b=>b.onclick=()=>{const T=toxS(),e=T.entries.find(x=>x.id===b.dataset.del);if(!e)return;T.entries=T.entries.filter(x=>x!==e);S.screen[e.date]=Math.max(0,(S.screen[e.date]||0)-e.min);save();render();draw()});
   $("#uX").onclick=closeSheet;
   $("#uOk").onclick=()=>{upd();if(min<=0)return;const L=Math.max(10,+$("#uL").value||0);if(L!==toxLimit())S.toxLimit=L;addUsage(min,app)};
   upd();
  });
 };
 draw();
}
const MOODTXT={inflated:"No es tu culpa ni la suya: las redes están hechas para engancharnos. Con 25 minutos de foco se desinfla.",worried:"Hoy hubo un poco más de pantalla. Cualquier pequeño avance lo calma.",happy:"Cada paso que das, él lo nota.",flat:"Descansar también es parte del proceso.",reading:"Mientras estés en foco, te acompaña.",normal:"Con un paso chiquito alcanza para empezar."};
const CHK='<svg viewBox="0 0 16 16"><path d="M3 8.5l3 3 7-7" fill="none" stroke="var(--surface)" stroke-width="2.4" stroke-linecap="round" stroke-linejoin="round"/></svg>';
const LOADER=t=>`<div class="loading">${fishImg("flat",52)}<span>${esc(t)}</span></div>`;

/* ============ lógica de calendario ============ */
function actsOn(d){const w=dow(d);return S.acts.filter(a=>(a.date===d)||(a.repeat&&a.repeat.length&&a.repeat.includes(w)&&a.date<=d&&!(a.skip||[]).includes(d))).sort((a,b)=>tm(a.start)-tm(b.start))}
function freeSlots(d,from=480,to=1320,minLen=45){
 let cur=from;const out=[];const now=new Date();if(d===today())cur=Math.max(cur,Math.ceil((now.getHours()*60+now.getMinutes())/15)*15);
 for(const a of actsOn(d)){const s=tm(a.start),e=tm(a.end);if(s>cur&&s-cur>=minLen)out.push([cur,Math.min(s,to)]);cur=Math.max(cur,e)}
 if(to-cur>=minLen)out.push([cur,to]);return out.filter(([a,b])=>b-a>=minLen);
}
const planned=(d,cat)=>actsOn(d).filter(a=>!cat||a.cat===cat).reduce((s,a)=>s+Math.max(0,tm(a.end)-tm(a.start)),0);
const logsOn=d=>S.logs.filter(l=>l.date===d);
function goalTicked(d){return S.goals.some(g=>(g.log[d]||[]).length)}
function activeDay(d){return logsOn(d).length>0||goalTicked(d)||!!S.rest[d]}
function streak(){let d=today();if(!activeDay(d))d=addD(d,-1);let n=0;while(activeDay(d)&&n<999){n++;d=addD(d,-1)}return n}
const gDays=g=>Object.values(g.log).filter(a=>a&&a.length).length;
const baseline=()=>BASE_MIN[S.iv.pantalla]||0;
const recovered=d=>S.screen[d]==null||!baseline()?0:Math.max(0,baseline()-S.screen[d]);

/* ============ UI base ============ */
const app=$("#app"),sheet=$("#sheet"),sb=$("#sb");
function toast(m){const t=$("#toast");t.textContent=m;t.classList.add("show");clearTimeout(toast.t);toast.t=setTimeout(()=>t.classList.remove("show"),3400)}
function openSheet(html,after){sb.innerHTML=html;if(!sheet.open)sheet.showModal();after&&after();}
const closeSheet=()=>sheet.open&&sheet.close();

const TABS=[["inicio","Inicio","house"],["calendario","Agenda","calendar-days"],["aprender","Aprender","book-open"],["productividad","Foco","timer"],["progreso","Progreso","chart-column"],["perfil","Perfil","circle-user"]];
let tab="inicio",examView=null;
const RES=["settings","sidebar","customize","upgrade","downloads"];
function setTab(t){tab=t;examView=null;try{if(location.hash!=="#"+t)history.replaceState(null,"","#"+t)}catch(e){}render();window.scrollTo(0,0)}
function navHTML(){$("#tabs ul").innerHTML=TABS.map(([k,l,p])=>`<li><button data-tab="${k}" ${tab===k?'aria-current="page"':""}>${ic(p,26,1.9)}${l}</button></li>`).join("");$$("[data-tab]").forEach(b=>b.onclick=()=>setTab(b.dataset.tab))}
window.addEventListener("hashchange",()=>{const h=location.hash.slice(1);if(TABS.some(t=>t[0]===h)&&h!==tab&&S.phase==="app"){tab=h;examView=null;render()}});
{const h=location.hash.slice(1);if(TABS.some(t=>t[0]===h))tab=h}

document.addEventListener("click",e=>{if(e.target.closest("[data-exitdemo]"))exitDemo()});
function render(){
 applyEasy();
 const nav=$("#tabs");
 if(S.phase!=="app"){nav.hidden=true;({welcome:vWelcome,interview:vInterview,analyzing:vAnalyzing,intro:vIntro,goals:vGoalsPick}[S.phase]||vWelcome)();return}
 nav.hidden=false;navHTML();
 ({inicio:vHome,calendario:vCal,aprender:vLearn,productividad:vFocus,progreso:vProgress,perfil:vProfile}[tab]||vHome)();
}
const head=(title,right="")=>`${S.demo?'<div class="demoband"><span>Modo demo · 3 meses de datos de ejemplo</span><button data-exitdemo>Salir</button></div>':""}<div class="top"><div class="wordmark" style="color:var(--deep)">${logoSVG(30)}</div>${right}</div>${title?`<h2 style="margin-bottom:6px">${title}</h2>`:""}`;

/* ============ MODO DEMO: 90 días de datos de ejemplo ============ */
const LSREAL="proki-real-backup";
function enterDemo(){
 if(!S.demo){try{localStorage.setItem(LSREAL,JSON.stringify(S))}catch(e){}}
 S=buildDemo();tab="progreso";examView=null;
 try{localStorage.setItem(LS,JSON.stringify(S))}catch(e){}
 render();window.scrollTo(0,0);toast("Cargamos 3 meses de ejemplo. Mirá cómo evoluciona todo.");
}
function exitDemo(){
 let real=null;try{const r=localStorage.getItem(LSREAL);if(r)real=JSON.parse(r);localStorage.removeItem(LSREAL)}catch(e){}
 S=Object.assign(blank(),real||{});if(S.demo)S=blank();save();tab="inicio";render();window.scrollTo(0,0);toast("Volviste a tus datos.");
}
function buildDemo(){
 let seed=20261118;const rnd=()=>{seed=(seed*1103515245+12345)%2147483648;return seed/2147483648};
 const rn=(a,b)=>Math.round(a+rnd()*(b-a));
 const t=today(),N=90,start=addD(t,-(N-1));
 const name=(S.iv&&S.iv.nombre&&S.iv.nombre.trim())||"Cami";
 const D=blank();D.demo=true;D.phase="app";
 D.iv={nombre:name,motivo:["Quiero dejar de procrastinar","Quiero reducir el tiempo en redes sociales","Quiero estudiar más y mejor"],meta3:["Mejorar mi rendimiento académico","Ser más constante con el deporte"],pantalla:"Entre 4 y 6 horas",apps:["Instagram","TikTok","YouTube"],momento:"A la noche",pendiente:["Me distraigo con el celular","Me cuesta empezar"],actividades:["Leer","Estudiar","Entrenar"],horas:"8 a 12 horas",temas:["Arte y diseño","Cultura y música","Ciencia y tecnología"],motivacion:["Con estadísticas de progreso","Con objetivos pequeños y alcanzables"]};
 D.profile={ai:false,resumen:`${name}, te cuesta arrancar a la noche y el celu se lleva buena parte del día. Vamos a recuperar ese tiempo de a poco.`,objetivoSemanal:"Tu objetivo de esta semana es recuperar 30 minutos diarios de redes y dedicarlos a estudiar o leer.",objetivos:[],masAdelante:["Organizar mi trabajo"],limites:{Instagram:60,TikTok:45,YouTube:60},
  desafios:["Abrí PROKI antes que cualquier red social","Hacé 25 minutos de foco sin el celu cerca","Anotá una sola cosa importante para mañana","Salí a caminar 15 minutos sin auriculares","Leé una noticia completa de una fuente confiable"],horario:"Ubicá tus bloques de estudio a la tarde, antes de que llegue la noche.",mensajes:["Un pequeño avance también es un avance.","Hoy podés recuperar un rato para vos.","Estás construyendo un hábito, dale tiempo."]};
 D.limits={Instagram:60,TikTok:45,YouTube:60};D.toxLimit=250;D.fish={name:"Proki",hue:0};D.later=["Organizar mi trabajo"];
 // objetivos: uno ya consolidado, tres activos (uno sumado más tarde)
 const mk=(titulo,acc,ini)=>({id:uid(),titulo,porque:"",acciones:acc.map(x=>({id:uid(),t:x})),inicio:ini,log:{}});
 const gRedes=mk("Usar 30 minutos menos Instagram",["Mirar cuánto la usás hoy","Poner un límite diario desde el celu","Sacarla de la pantalla de inicio"],start);
 const gEst=mk("Estudiar 30 minutos por día",["Elegir un horario fijo","Dejar el material listo antes","Celu en otra habitación mientras estudiás"],start);
 const gDep=mk("Entrenar dos veces por semana",["Elegir los dos días","Preparar la ropa el día anterior","Arrancar con 20 minutos"],start);
 const gLeer=mk("Leer 10 páginas por día",["Dejar el libro a la vista","Leer antes de agarrar el celu a la noche","Anotar en qué página quedaste"],addD(start,46));
 const achDay=addD(start,44);
 D.acts=[
  {id:uid(),title:"Trabajo",cat:"trabajo",date:start,start:"09:00",end:"13:00",repeat:[1,2,3,4,5]},
  {id:uid(),title:"Clase de Tipografía",cat:"clase",date:start,start:"15:00",end:"17:00",repeat:[2,4]},
  {id:uid(),title:"Estudio",cat:"estudio",date:start,start:"18:00",end:"19:00",repeat:[1,2,3,4,5]},
  {id:uid(),title:"Entrenamiento",cat:"deporte",date:start,start:"19:30",end:"20:30",repeat:[1,4]},
  {id:uid(),title:"Lectura",cat:"lectura",date:addD(start,46),start:"22:00",end:"22:30",repeat:[0,1,2,3,4,5,6]},
  {id:uid(),title:"Proyecto personal",cat:"proyecto",date:start,start:"11:00",end:"13:00",repeat:[6]}
 ];
 const tox=D.tox;let bestRun=0,run=0;
 for(let i=0;i<N;i++){
  const d=addD(start,i),w=dow(d),k=i/(N-1),wk=(w===0||w===6),isToday=d===t;
  const rest=(w===0&&rnd()<.55)||rnd()<.04;
  // tiempo de pantalla: baja de ~5 h 30 a ~2 h 45, con ruido, fines de semana más alto
  let scr=Math.round((335-165*k)+(wk?45:0)+(rnd()-.5)*90);
  if(i>20&&i<26)scr+=70; // una semana difícil (parciales)
  if(isToday)scr=Math.round(scr*.45);
  scr=Math.max(60,scr);D.screen[d]=scr;
  // registros de uso del celu (alimentan al pez) y explosiones
  const parts=rn(3,6),apps=["Instagram","TikTok","YouTube","Instagram","WhatsApp"];let left=scr,acc=0,ts0=pd(d).getTime()+9*3600e3;
  for(let j=0;j<parts;j++){const m=j===parts-1?left:Math.max(5,Math.round(left/(parts-j)*(0.6+rnd()*.8)));left-=m;if(m<=0)continue;
   const ts=ts0+j*(13/parts)*3600e3+rn(0,40)*6e4;tox.entries.push({id:uid(),date:d,ts,min:m,app:apps[rn(0,4)]});
   acc+=m;if(acc>=D.toxLimit&&!isToday){tox.booms.push({ts:ts+1000,date:d,min:acc});acc=0}}
  const empty=!rest&&!isToday&&rnd()<.16*(1-k);if(empty){D.screen[d]=Math.round(scr*1.15);run=0;continue}
  if(rest){D.rest[d]="rest";}
  else if(rnd()<.06&&k<.6){D.rest[d]="miss";}
  // actividades registradas: la constancia crece con el tiempo
  const pAct=.45+.45*k,mood=()=>["Con energía","Bien","Bien","Cansado/a","Me costó"][Math.min(4,Math.max(0,Math.floor(rnd()*5-k*1.5)))];
  const L=(cat,title,min)=>D.logs.push({id:uid(),cat,title,date:d,min,note:"",avance:["Arranqué","Bastante","Lo terminé"][rn(0,2)],animo:mood(),examId:null});
  if(!rest&&!wk&&rnd()<.92&&!(isToday))L("trabajo","Trabajo",rn(210,260));
  if(!rest&&(w===2||w===4)&&rnd()<.9)L("clase","Clase de Tipografía",120);
  if(!rest&&rnd()<pAct)L("estudio",["Repaso de Tipografía","Lectura de Historia del Diseño","Ejercicios de grilla","Apuntes de Semiótica"][rn(0,3)],rn(20,40)+Math.round(50*k));
  if(!rest&&(w===1||w===4)&&rnd()<.55+.35*k)L("deporte","Entrenamiento",rn(40,80));
  if(i>=46&&!rest&&rnd()<.5+.4*k)L("lectura","Lectura",rn(15,35));
  if(w===6&&rnd()<.4+.4*k)L("proyecto","Proyecto personal",rn(60,150));
  if(rest)L("descanso","Día tranquilo",rn(60,180));
  if(rnd()<.3)L("recreacion",["Salida con amigos","Película","Caminata"][rn(0,2)],rn(60,150));
  // hábitos tildados
  const tick=(g,p)=>{if(rnd()<p){const n=Math.max(1,Math.round(g.acciones.length*(0.4+rnd()*.6)));g.log[d]=g.acciones.slice(0,n).map(a=>a.id)}};
  if(!rest){if(d<=achDay)tick(gRedes,.45+.45*k);tick(gEst,.4+.5*k);if(w===1||w===4)tick(gDep,.55+.35*k);if(i>=46)tick(gLeer,.5+.35*k)}
  if(isToday){delete gEst.log[d];delete gLeer.log[d]}
  const active=!!(D.logs.some(l=>l.date===d)||D.rest[d]);run=active?run+1:0;bestRun=Math.max(bestRun,run);
 }
 D.best=bestRun;
 D.goals=[gEst,gDep,gLeer];D.achieved=[{titulo:gRedes.titulo,fin:achDay}];
 // repasos quincenales
 for(let c=15;c<N;c+=15){const d=addD(start,c);D.checkins.push({date:d,answers:{q1:c<40?"Un poco":"Sí, bastante",q2:c<40?"Algunos":"Casi todos",q3:c<40?"Dejar el celu a la noche":"Entrenar cuando llueve",q4:"Leer más"}})}
 D.lastCheckin=D.checkins.length?D.checkins[D.checkins.length-1].date:t;
 // examen con plan de estudio en curso
 const exD=addD(t,9),exId=uid();
 const topics=[["Bauhaus y la Nueva Tipografía",["Gropius","Funcionalismo","Jan Tschichold"]],["Escuela de Ulm",["Max Bill","Diseño sistemático","Otl Aicher"]],["Estilo Tipográfico Internacional",["Grilla","Helvetica","Müller-Brockmann"]],["Posmodernismo",["Wolfgang Weingart","Emigre","Deconstrucción"]]];
 D.exams=[{id:exId,name:"Historia del Diseño II",date:exD,time:"09:00",mats:[],topics:topics.map(([a,b])=>({titulo:a,conceptos:b})),
  resumen:"Ejemplo de resumen generado a partir de los apuntes. En la app real, PROKI lo arma con el material que subís.",
  datos:[{texto:"¿Sabías que la grilla del Estilo Internacional busca neutralidad y legibilidad por sobre la expresión?",fuente:"apuntes"},{texto:"¿Sabías que Ulm retomó ideas de la Bauhaus pero con un enfoque más científico y metodológico?",fuente:"apuntes"}],
  cards:[{q:"¿Quién dirigió la Bauhaus en su fundación?",a:"Walter Gropius",fuente:"apuntes",known:true},{q:"¿Qué escuela sistematizó el diseño después de la Bauhaus?",a:"La Escuela de Ulm",fuente:"apuntes",known:false},{q:"¿Qué tipografía se asocia al Estilo Internacional?",a:"Helvetica",fuente:"apuntes",known:false}],
  scores:[{date:addD(t,-12),ok:5,n:10,sim:false},{date:addD(t,-6),ok:7,n:10,sim:false},{date:addD(t,-2),ok:9,n:12,sim:true}]}];
 D.acts.push({id:uid(),title:"Examen: Historia del Diseño II",cat:"examen",date:exD,start:"09:00",end:"11:00",repeat:[],examRef:exId});
 topics.forEach(([tp],j)=>{const d=addD(t,-6+j*3);D.acts.push({id:uid(),title:"Historia del Diseño II: "+tp,topic:tp,kind:"estudio",cat:"estudio",date:d,start:"17:00",end:"17:40",repeat:[],examId:exId,done:d<t})});
 D.acts.push({id:uid(),title:"Historia del Diseño II: simulacro",topic:"Simulacro de examen",kind:"simulacro",cat:"estudio",date:addD(exD,-1),start:"17:00",end:"17:45",repeat:[],examId:exId,done:false});
 return D;
}

/* ============ onboarding ============ */
function vWelcome(){
 app.innerHTML=`<div class="stack" style="padding-top:20px"><div style="color:var(--teal2)">${logoSVG(96)}</div>
 <p style="font-weight:700;color:var(--deep)">Dejando la toxina de la procrastinación, el estrés y el doomscrolling de lado.</p>
 <div class="welcome3">
  <div class="pop" style="--i:0">${icb("timer","#59A5B2",72,"round")}Menos postergar</div>
  <div class="pop" style="--i:1">${icb("smartphone","#7B63A8",72,"round")}Menos scroll</div>
  <div class="pop" style="--i:2">${icb("sprout","#5E9E88",72,"round")}Más de lo que te importa</div></div>
 <h1 class="mt2" style="font-size:clamp(28px,7.5vw,40px)">No se trata de hacer más cosas.${say("No se trata de hacer más cosas. Se trata de dedicarle tiempo a las que realmente importan. Antes de empezar, PROKI quiere conocerte con unas preguntas cortas.")}</h1>
 <p style="font-size:19px">Se trata de dedicarle tiempo a las que realmente importan.</p>
 <div class="row mt" style="gap:10px;flex-wrap:nowrap">${icb("message-circle-question","#76BDCD",44,"round")}<p class="muted">Unas preguntas cortas, de a una. Ninguna tiene respuesta correcta.</p></div></div>
 <div class="actions"><button class="btn iconbtn" id="go">${ic("arrow-right",20,2.4)}Empezar</button><button class="btn ghost iconbtn" id="demo">${ic("eye",20)}Ver demo</button></div>`;
 $("#go").onclick=()=>{S.phase="interview";S.qi=0;save();render()};$("#demo").onclick=enterDemo;
}
function vInterview(){
 const q=Q[S.qi],v=S.iv,n=Q.length;
 const sel=q.t==="multi"?v[q.k]:[v[q.k]];
 const customs=q.t==="multi"?v[q.k].filter(x=>!q.o.includes(x)):[];
 let f="";
 if(q.t==="text")f=`<input type="text" id="fld" value="${esc(v[q.k])}" maxlength="40" autocomplete="given-name">`;
 else f=`<div class="optgrid">${q.o.concat(customs).map((o,i)=>optTile(o,sel.includes(o)).replace('class="chip"',`class="chip pop" style="--i:${i}"`)).join("")}</div>
  ${q.custom?`<div class="row mt"><input type="text" id="cus" placeholder="Otra opción…" maxlength="60" style="flex:1"><button class="btn soft sm iconbtn" id="cusAdd">${ic("plus",18,2.4)}Sumar</button></div>`:""}`;
 const qf={apps:"phone",pantalla:"phone",momento:"worried",pendiente:"worried",actividades:"reading",temas:"reading",motivacion:"happy",nombre:"happy"}[q.k]||"normal";
 app.innerHTML=`${head("",`<span class="muted small">${S.qi+1} de ${n}</span>`)}<div style="margin-bottom:6px" class="fishbob">${fishImg(qf,84)}</div><div class="qprog"><i style="width:${(S.qi+1)/n*100}%"></i></div>
 <div class="stack"><h2>${esc(q.title)}${say(q.title+(q.hint?". "+q.hint:""))}</h2>${q.hint?`<p class="muted small">${esc(q.hint)}</p>`:""}${q.t==="multi"?`<p class="small" style="display:flex;gap:6px;align-items:center;font-weight:600;color:var(--deep)">${ic("layers",16)}Podés tocar varias</p>`:""}<div>${f}</div></div>
 <div class="actions"><button class="btn iconbtn" id="nx">${S.qi===n-1?ic("check",20,2.4)+"Terminar":"Seguir"+ic("arrow-right",20,2.4)}</button>${S.qi>0?`<button class="btn ghost iconbtn" id="bk" aria-label="Volver">${ic("chevron-left",20)}Volver</button>`:""}${!q.req?'<button class="link" id="sk">Saltear</button>':""}</div>`;
 const ok=()=>!q.req||(Array.isArray(v[q.k])?v[q.k].length:String(v[q.k]).trim().length);
 const nx=$("#nx");nx.disabled=!ok();
 const fld=$("#fld");if(fld){fld.focus();fld.oninput=()=>{v[q.k]=fld.value;nx.disabled=!ok();save()};fld.onkeydown=e=>{if(e.key==="Enter"&&ok())nx.click()}}
 $$(".chip").forEach(c=>c.onclick=()=>{const o=c.dataset.o;if(q.t==="multi"){const a=v[q.k],i=a.indexOf(o);i>=0?a.splice(i,1):a.push(o);c.setAttribute("aria-pressed",a.includes(o))}else{v[q.k]=v[q.k]===o?"":o;$$(".chip").forEach(x=>x.setAttribute("aria-pressed",x.dataset.o===v[q.k]))}nx.disabled=!ok();save()});
 if($("#cusAdd")){const add=()=>{const t=$("#cus").value.trim();if(t&&!v[q.k].includes(t)){v[q.k].push(t);save();render()}};$("#cusAdd").onclick=add;$("#cus").onkeydown=e=>{if(e.key==="Enter")add()}}
 nx.onclick=()=>{if(!ok())return;if(S.qi<n-1){S.qi++;save();render()}else{S.phase="analyzing";save();render()}};
 if($("#bk"))$("#bk").onclick=()=>{S.qi--;save();render()};
 if($("#sk"))$("#sk").onclick=()=>{if(S.qi<n-1){S.qi++;save();render()}else{S.phase="analyzing";save();render()}};
}

function ruleProfile(){
 const v=S.iv,pool=[];const has=(arr,s)=>arr.some(x=>x.toLowerCase().includes(s));
 const app1=v.apps[0]||"las redes";
 if(has(v.motivo,"redes")||v.apps.length)pool.push({titulo:`Usar 30 minutos menos ${app1}`,porque:"No se trata de dejarla, sino de recuperar un rato para vos.",acciones:["Mirar cuánto la usás hoy","Poner un límite diario desde el celu","Sacarla de la pantalla de inicio"]});
 if(has(v.motivo,"estudiar")||has(v.meta3,"académico")||v.actividades.includes("Estudiar"))pool.push({titulo:"Estudiar 30 minutos por día",porque:"Un rato corto y constante rinde más que una maratón de último momento.",acciones:["Elegir un horario fijo","Dejar el material listo antes","Celu en otra habitación mientras estudiás"]});
 if(has(v.meta3,"deporte")||v.actividades.includes("Entrenar"))pool.push({titulo:"Entrenar dos veces por semana",porque:"Con dos días alcanza para empezar a sentir la diferencia.",acciones:["Elegir los dos días","Preparar la ropa el día anterior","Arrancar con 20 minutos"]});
 if(v.actividades.includes("Leer"))pool.push({titulo:"Leer 10 páginas por día",porque:"Diez páginas son poquitas, y al mes son un libro.",acciones:["Dejar el libro a la vista","Leer antes de agarrar el celu a la noche","Anotar en qué página quedaste"]});
 if(has(v.motivo,"organizar")||has(v.meta3,"organizado"))pool.push({titulo:"Planificar el día en 5 minutos",porque:"Saber qué es lo importante baja mucho la sensación de caos.",acciones:["Cargar en el calendario lo fijo del día","Elegir una sola tarea importante","Tacharla cuando la termines"]});
 if(!pool.length)pool.push({titulo:"Regalarte 30 minutos sin pantallas",porque:"Un rato para vos también es un hábito que vale la pena.",acciones:["Elegir el momento del día","Dejar el celu en otro lado","Hacer algo que disfrutes"]});
 const lim={};v.apps.slice(0,4).forEach(a=>lim[a]=60);
 return{resumen:`${v.nombre||"Hola"}, por lo que nos contaste, ${v.momento?("el momento más difícil es "+v.momento.toLowerCase()+", "):""}y queremos ayudarte a recuperar ese tiempo sin exigirte de más.`,
  objetivoSemanal:pool[0].titulo.startsWith("Usar")?"Tu objetivo de esta semana es recuperar 30 minutos diarios de redes y dedicarlos a algo que te importe.":`Tu objetivo de esta semana: ${pool[0].titulo.toLowerCase()}.`,
  objetivos:pool.slice(0,3),masAdelante:pool.slice(3).map(p=>p.titulo),limites:lim,
  desafios:["Abrí PROKI antes que cualquier red social","Hacé 25 minutos de foco sin el celu cerca","Anotá una sola cosa importante para mañana","Salí a caminar 15 minutos sin auriculares","Leé una noticia completa de una fuente confiable"],
  horario:v.momento==="A la noche"?"Probá ubicar tus bloques importantes a la tarde, antes de que llegue el momento en que más te cuesta.":"Ubicá tus bloques importantes en el momento en que tenés más energía.",
  mensajes:["Un pequeño avance también es un avance.","Hoy podés recuperar un rato para vos."]};
}
async function buildProfile(){
 const prompt=`${VOICE}
Analizá la entrevista inicial y armá el perfil del usuario. Reglas: proponé entre 1 y 3 objetivos prioritarios, realistas y medibles (nunca más de 3: elegí los más importantes y factibles con las horas que quiere dedicar). Lo que quede afuera va en "masAdelante".
Entrevista: ${JSON.stringify(S.iv)}
Respondé SOLO JSON:
{"resumen":"2 oraciones que describan su situación con empatía","objetivoSemanal":"una frase como: Tu objetivo de esta semana es recuperar 30 minutos diarios de Instagram y dedicarlos a estudiar o leer","objetivos":[{"titulo":"","porque":"","acciones":["3 pasos chiquitos"]}],"masAdelante":[""],"limites":{"NombreApp":minutos},"desafios":["5 desafíos diarios cortos y amables"],"horario":"una sugerencia de cuándo ubicar estudio y descanso según su momento difícil","mensajes":["3 mensajes motivadores personalizados"]}`;
 try{const r=await ai(prompt);if(!r||!Array.isArray(r.objetivos)||!r.objetivos.length)throw 0;
  r.objetivos=r.objetivos.slice(0,3).filter(o=>o&&o.titulo).map(o=>({titulo:String(o.titulo),porque:String(o.porque||""),acciones:(o.acciones||[]).map(String).slice(0,4)}));
  r.limites=r.limites&&typeof r.limites==="object"?r.limites:{};r.desafios=Array.isArray(r.desafios)&&r.desafios.length?r.desafios.map(String):ruleProfile().desafios;
  r.mensajes=Array.isArray(r.mensajes)?r.mensajes.map(String):[];r.masAdelante=Array.isArray(r.masAdelante)?r.masAdelante.map(String):[];r.ai=true;return r}
 catch(e){return ruleProfile()}
}
let building=false;
async function vAnalyzing(){
 app.innerHTML=`${head("")}<div class="fishbob">${fishImg("reading",120)}</div><h2 class="mt">Armando tu perfil…</h2><p class="muted">Estamos leyendo tus respuestas para que PROKI sea distinto para vos.</p>${LOADER("Esto puede tardar unos segundos.")}`;
 if(building)return;building=true;
 const p=await buildProfile();building=false;
 S.profile=p;S.limits=Object.assign({},p.limites);S.drafts=p.objetivos.map(o=>Object.assign({id:uid()},o));S.later=p.masAdelante||[];
 S.phase="intro";save();render();
}
function vIntro(){
 const n=S.iv.nombre.trim(),p=S.profile;
 app.innerHTML=`${head("")}<div class="card warm letter"><div class="row" style="flex-wrap:nowrap;gap:12px;margin-bottom:14px">${icb("footprints","#2F7380",52,"round")}<h2 style="margin:0">¡Empecemos de a poco${n?", "+esc(n):""}!</h2>${say("¡Empecemos de a poco! No necesitás cambiar toda tu rutina de un día para el otro. A veces, intentar hacer todo al mismo tiempo termina haciendo que no hagamos nada. En PROKI queremos ayudarte a construir hábitos que puedas mantener en el tiempo. Por eso, vamos a empezar con uno, dos o tres objetivos que realmente sean importantes para vos. No buscamos que seas perfecto o perfecta. Buscamos que avances, a tu ritmo y a tu manera. Un pequeño cambio hoy puede convertirse en un gran hábito mañana.")}</div>
 <p>No necesitás cambiar toda tu rutina de un día para el otro. A veces, intentar hacer todo al mismo tiempo termina haciendo que no hagamos nada.</p>
 <p>En PROKI queremos ayudarte a construir hábitos que puedas mantener en el tiempo. Por eso, vamos a empezar con uno, dos o tres objetivos que realmente sean importantes para vos.</p>
 <p>No buscamos que seas perfecto/a. Buscamos que avances, a tu ritmo y a tu manera.</p>
 <p style="font-family:var(--display);font-weight:700;font-size:21px;line-height:1.2;margin-top:18px">Un pequeño cambio hoy puede convertirse en un gran hábito mañana.</p></div>
 <div class="card mt"><div class="row" style="flex-wrap:nowrap;gap:10px">${icb("user","#76BDCD",40,"round")}<h4>Lo que entendimos de vos</h4>${say(p.resumen)}</div><p class="mt muted">${esc(p.resumen)}</p></div>
 <div class="card mt"><h4>Conocé a tu pez globo</h4><p class="small muted mt">Te acompaña todos los días. Cuando el scroll se pasa de la raya se infla; cada paso que das lo calma.</p>
 <div class="row mt" style="flex-wrap:nowrap;gap:16px"><div id="fprev" class="fishbob">${fishImg("happy",96)}</div><div style="flex:1"><label class="f" for="fName" style="margin-top:0">Su nombre</label><input type="text" id="fName" maxlength="20" value="${esc(fishName())}"></div></div>
 <div class="row mt" id="hues">${HUES.map(([l,h])=>`<button class="swatch" data-h="${h}" aria-label="${l}" aria-pressed="${fishHue()===h}"><img class="px" src="${FISH.normal.src}" alt="" style="filter:hue-rotate(${h}deg)"></button>`).join("")}</div></div>
 <div class="actions"><button class="btn" id="go">Ver mis objetivos</button></div>`;
 fishCustom(()=>{$("#fprev").innerHTML=fishImg("happy",96)});
 $("#go").onclick=()=>{S.phase="goals";save();render()};
}
function vGoalsPick(){
 const d=S.drafts||[];
 app.innerHTML=`${head("Tus primeros objetivos")}<p class="muted">${esc(S.profile.objetivoSemanal)}</p>
 <div class="mt2">${d.map(g=>`<div class="card"><div class="gcard">${icb(guessIcon(g.titulo),"#59A5B2",60)}<div style="flex:1;min-width:0"><h3>${esc(g.titulo)}</h3>${g.porque?`<p class="small muted mt">${esc(g.porque)}</p>`:""}</div>${say(g.titulo+". "+(g.porque||"")+" Pasos: "+g.acciones.join(". "))}</div>
 <div class="gsteps">${g.acciones.map((a,i)=>`<div class="gstep"><span class="icb round" style="--c:#76BDCD;width:30px;height:30px;font-weight:800;font-size:14px">${i+1}</span>${esc(a)}</div>`).join("")}</div>
 <div class="row mt"><button class="btn soft sm iconbtn" data-ed="${g.id}">${ic("pencil",16)}Cambiar</button><button class="btn ghost sm iconbtn" data-rm="${g.id}">${ic("x",16)}Quitar</button></div></div>`).join("")}</div>
 ${d.length<3?`<button class="btn ghost mt iconbtn" id="add">${ic("plus",18,2.4)}Sumar uno propio</button>`:'<p class="note">Con tres alcanza para arrancar. Cuando alguno se afiance, sumamos otro.</p>'}
 ${S.later.length?`<div class="card lil mt"><div class="row" style="flex-wrap:nowrap;gap:10px">${ic("gift",22)}<span><b>Para más adelante:</b> ${esc(S.later.join(", "))}</span></div></div>`:""}
 <div class="actions"><button class="btn" id="ok" ${d.length?"":"disabled"}>Empezar con ${d.length===1?"este objetivo":"estos "+d.length}</button><button class="link" id="redo">Rehacer la entrevista</button></div>`;
 $$("[data-ed]").forEach(b=>b.onclick=()=>goalEditor(d.find(x=>x.id===b.dataset.ed),"draft"));
 $$("[data-rm]").forEach(b=>b.onclick=()=>{S.drafts=d.filter(x=>x.id!==b.dataset.rm);save();render()});
 if($("#add"))$("#add").onclick=()=>goalEditor(null,"draft");
 $("#ok").onclick=()=>{S.goals=d.map(g=>({id:uid(),titulo:g.titulo,porque:g.porque,acciones:g.acciones.map(t=>({id:uid(),t})),inicio:today(),log:{}}));S.drafts=[];S.lastCheckin=today();S.phase="app";tab="inicio";save();render();toast("¡Listo! Arrancamos de a poco.")};
 $("#redo").onclick=()=>{S.phase="interview";S.qi=0;save();render()};
}
function fishCustom(after){
 S.fish=S.fish||{name:"Proki",hue:0};
 const n=$("#fName");if(n)n.oninput=()=>{S.fish.name=n.value.trim()||"Proki";save()};
 $$("[data-h]").forEach(b=>b.onclick=()=>{S.fish.hue=+b.dataset.h;$$("[data-h]").forEach(x=>x.setAttribute("aria-pressed",x===b));save();after&&after()});
}
function goalEditor(item,kind){
 const src=item?{titulo:item.titulo,acciones:kind==="goal"?item.acciones.map(a=>a.t):item.acciones.slice()}:{titulo:"",acciones:["","",""]};
 openSheet(`<div class="sheethead">${icb(item?"pencil":"target","#2F7380",52,"round")}<h2>${item?"Cambiar objetivo":"Nuevo objetivo"}</h2></div>${!item?'<p class="note">Mejor de a poco: algo chiquito y concreto.</p>':""}
 <label class="f" for="gT">¿Qué querés lograr?</label><input type="text" id="gT" value="${esc(src.titulo)}" maxlength="80" placeholder="Ej. Estudiar 30 minutos por día">
 <label class="f">Pequeñas acciones</label>${src.acciones.map((a,i)=>`<input type="text" class="gA" value="${esc(a)}" maxlength="90" placeholder="Paso ${i+1}" style="margin-top:6px">`).join("")}
 <div class="row mt"><button class="btn soft sm iconbtn" id="gAi">${ic("sparkles",16)}Dividir en pasos</button></div><p class="note" id="gN"></p>
 <div class="actions"><button class="btn" id="gS">Guardar</button><button class="btn ghost" id="gC">Cancelar</button>${item&&kind==="goal"?'<button class="link" id="gD">Dejar este objetivo</button>':""}</div>`,()=>{
  $("#gC").onclick=closeSheet;
  $("#gAi").onclick=async()=>{const t=$("#gT").value.trim();if(!t){$("#gN").textContent="Escribí primero qué querés lograr.";return}$("#gN").textContent="Pensando pasos chiquitos…";
   try{const r=await ai(`${VOICE}\nDividí este objetivo en 3 acciones pequeñas y concretas, en infinitivo: "${t}". Respondé SOLO JSON {"acciones":["","",""]}`,{modelTier:"quick"});
    $$(".gA").forEach((el,i)=>el.value=(r.acciones||[])[i]||"");$("#gN").textContent=""}catch(e){$("#gN").textContent=aiMsg(e)}};
  if($("#gD"))$("#gD").onclick=()=>{S.goals=S.goals.filter(g=>g!==item);save();closeSheet();render();toast("Cambiar de rumbo también es avanzar.")};
  $("#gS").onclick=()=>{const t=$("#gT").value.trim();if(!t)return $("#gT").focus();const acc=$$(".gA").map(e=>e.value.trim()).filter(Boolean);
   if(kind==="draft"){if(item){item.titulo=t;item.acciones=acc}else S.drafts.push({id:uid(),titulo:t,porque:"",acciones:acc})}
   else if(item){const old=item.acciones;item.titulo=t;item.acciones=acc.map(x=>old.find(a=>a.t===x)||{id:uid(),t:x})}
   else S.goals.push({id:uid(),titulo:t,porque:"",acciones:acc.map(x=>({id:uid(),t:x})),inicio:today(),log:{}});
   save();closeSheet();render()};
 });
}

/* ============ INICIO ============ */
function feed(){
 const t=today(),out=[],seed=daySeed();
 for(const ex of S.exams){const dd=diffD(t,ex.date);if(dd<0)continue;
  const next=S.acts.filter(a=>a.examId===ex.id&&!a.done&&a.date>=t).sort((a,b)=>a.date.localeCompare(b.date))[0];
  if(dd<=21)out.push({ic:"calendar-days",t:dd===0?`Hoy es el examen de ${ex.name}. Confiá en lo que preparaste.`:`Faltan ${dd} días para ${ex.name}.${next?` Próxima sesión: ${next.topic||next.title} (${next.date===t?"hoy":fmtD(next.date,{weekday:"long",day:"numeric"})}).`:""}`});
  if(ex.datos&&ex.datos.length){const d=pick(ex.datos,seed);out.push({ic:"lightbulb",t:d.texto,src:d.fuente,act:["flash",ex.id,"Repasar"]})}
  const pend=(ex.cards||[]).filter(c=>!c.known);if(pend.length)out.push({ic:"layers",t:`Hay un concepto de tus apuntes que todavía no repasaste: “${pick(pend,seed).q}” ¿Lo vemos juntos?`,act:["flash",ex.id,"Verlo"]});
  if(logsOn(addD(t,-1)).some(l=>l.examId===ex.id)&&ex.topics&&ex.topics.length)out.push({ic:"circle-help",t:`Te dejamos una pregunta para comprobar lo que estudiaste ayer de ${ex.name}.`,act:["quiz",ex.id,"Responder"]});
 }
 const gaps=freeSlots(t,480,1320,60);if(gaps.length&&S.goals.length){const g=gaps[0];out.push({ic:"clock",t:`Tenés un espacio libre de ${ts(g[0])} a ${ts(g[1])}. Podrías usar 25 minutos para “${pick(S.goals,seed).titulo}” y dejar el resto para descansar.`})}
 return out.slice(0,5);
}
function vHome(){
 const t=today(),n=S.iv.nombre.trim(),p=S.profile||{};
 const acts=actsOn(t),nowM=new Date().getHours()*60+new Date().getMinutes();
 const due=S.lastCheckin&&diffD(S.lastCheckin,t)>=15;
 const msg=S.rest[t]==="rest"?pick(MSG_REST,daySeed()):S.rest[t]==="miss"?pick(MSG_MISS,daySeed()):pick((p.mensajes&&p.mensajes.length?p.mensajes:MSG_OK),daySeed());
 const [md,ml]=mood();
 const tl=toxFrom!=null?toxFrom:toxLevel(),tv=toxVis(tl),baseSp=(md==="inflated"||md==="worried")?"normal":md;
 const sk=streak();if(sk>(S.best||0)){const was=S.best||0;S.best=sk;save();if(was>=2)setTimeout(()=>toast(`¡Nuevo récord: ${sk} días! ${fishName()} está feliz.`),400)}
 const F=feed(),scr=S.screen[t],recM=recovered(t);
 let ti=0;const I=()=>`style="--i:${ti++}"`;
 app.innerHTML=`${head("",`<span class="muted small" style="display:flex;gap:6px;align-items:center">${ic("calendar-days",16)}${esc(fmtD(t,{weekday:"short",day:"numeric",month:"short"}))}</span>`)}
 <section class="hero"><div class="row" style="flex-wrap:nowrap;justify-content:space-between;align-items:flex-start"><div><h1 style="font-size:34px">Hola${n?", "+esc(n):""}.</h1><p class="mt" style="font-weight:500">${esc(msg)}</p></div>${say(`Hola ${n}. ${msg} ${fishName()} tiene ${hm(tl)} de ${hm(toxLimit())} de toxinas de pantalla. ${toxMsg(tv.p,baseSp)}`)}</div>
 <div class="pecera" aria-label="${esc(fishName())}, tu pez globo, con ${hm(tl)} de ${hm(toxLimit())} de toxinas"><div class="toxparts" id="toxParts">${toxPartsHTML(tv.parts)}</div>
  <div class="toxwrap ${tv.tremble?"tremble":""} ${reborn?"reborn":""}" id="toxWrap" style="transform:scale(${tv.scale});filter:${tv.filter};--s:${tv.scale}"><div class="fishbob" id="toxSprite" data-base="${baseSp}" data-cur="${tv.sprite||baseSp}">${fishImg(tv.sprite||baseSp,110)}</div></div></div>
 <p class="fishname" style="text-align:center;font-size:15px">${esc(fishName())} · <span style="font-weight:500" id="toxLbl" data-ml="${esc(ml)}">${esc(tv.p>=.6?"lleno de toxinas":ml)}</span></p>
 <div class="toxmeter"><div class="row" style="justify-content:flex-start;gap:8px;margin:0 0 6px">${ic("smartphone",16)}<span>Toxinas</span><span id="toxTxt" style="margin-left:auto">${hm(tl)} de ${hm(toxLimit())}</span></div><div class="toxbar"><i id="toxBar" style="width:${tv.p*100}%;--bw:${tv.p>0?100/tv.p:100}%"></i></div></div>
 <p class="small mt" id="heroMsg">${esc(toxMsg(tv.p,baseSp))}</p>
 <div class="row mt" style="gap:8px"><span class="tag iconbtn" style="background:rgba(255,255,255,.6);gap:4px">${ic("flame",14)}${sk}</span><span class="tag iconbtn" style="background:rgba(255,255,255,.6);gap:4px">${ic("award",14)}${Math.max(S.best||0,sk)}</span></div></section>

 <div class="qa">
  <button id="useAdd" class="pop" ${I()}>${icb("smartphone","#7B63A8",64,"round solid")}Usé el celu</button>
  <button id="qaFocus" class="pop" ${I()}>${icb(S.timer?"timer":"play","#2F7380",64,"round solid")}${S.timer?`<span id="tclock">${elapsedStr()}</span>`:"Foco"}</button>
  <button id="qaPlan" class="pop" ${I()}>${icb("calendar-days","#59A5B2",64,"round solid")}Mi día</button>
  <button id="qaHard" class="pop" ${I()}>${icb("cloud-rain","#8C9A90",64,"round solid")}Día difícil</button>
 </div>

 ${due?`<button class="tile wide warm mt2 pop" id="ci" ${I()} style="width:100%;border-color:transparent;background:var(--sun-soft)">${icb("message-circle-heart","#2F7380",52,"round")}<div><b>¿Cómo venís?</b><span class="val">4 preguntas · 1 minuto</span></div><span style="margin-left:auto">${ic("chevron-right",22)}</span></button>`:""}

 <div class="sec">${shead("calendar-days","Hoy","#59A5B2",`<button class="link" data-tab2="calendario" style="margin-left:auto">Ver todo</button>`)}
  <div class="tline">${acts.map(a=>{const past=tm(a.end)<nowM,now=tm(a.start)<=nowM&&nowM<=tm(a.end);return`<button data-act="${a.id}" class="${past?"past":""} ${now?"now":""} ${a.done?"done":""}" aria-label="${esc(a.title)}, ${a.start} a ${a.end}">${icb(catI(a.cat),catC(a.cat),62,"round")}<span class="tt">${a.start}</span><span class="tn">${esc(a.title)}</span></button>`}).join("")}
   <button data-tab2="calendario" aria-label="Agregar actividad">${icb("plus","#8C9A90",62,"round")}<span class="tt">&nbsp;</span><span class="tn">${acts.length?"Sumar":"Planificar"}</span></button></div></div>

 <div class="sec">${shead("target","Objetivos","#2F7380")}
 ${S.goals.map(g=>{const dd=gDays(g),done=g.log[t]||[];return`<div class="card pop" ${I()}><div class="gcard">${icb(guessIcon(g.titulo),"#59A5B2",54)}<div style="flex:1;min-width:0"><h3>${esc(g.titulo)}</h3>${dd>=14?`<span class="tag mt iconbtn" style="gap:4px">${ic("sprout",14)}Casi hábito</span>`:""}</div><div class="ring" title="${dd} días con avance">${sprout(dd)}</div></div>
  <div class="gsteps">${g.acciones.map(a=>{const on=done.includes(a.id);return`<button class="gstep" data-on="${on}" data-g="${g.id}" data-a="${a.id}" aria-pressed="${on}"><span class="tick" aria-pressed="${on}">${CHK}</span><span class="${on?"done-t":""}">${esc(a.t)}</span></button>`}).join("")}</div>
  <div class="row mt"><button class="btn ghost sm iconbtn" data-ged="${g.id}">${ic("pencil",16)}Cambiar</button>${say(g.titulo+". "+g.acciones.map(a=>a.t).join(". "))}${dd>=14?`<button class="btn sm iconbtn" data-ach="${g.id}">${ic("award",16)}¡Ya es rutina!</button>`:""}</div></div>`}).join("")}
  ${S.goals.length<3?`<button class="btn ghost sm mt iconbtn" id="gAdd">${ic("plus",18,2.4)}Sumar objetivo</button>`:""}</div>

 <div class="sec">${shead("compass","Explorar","#7B63A8")}
 <div class="tiles">
  <button class="tile pop" data-open="challenge" ${I()}>${icb("trophy","#E0A030")}<div><b>Desafío</b><span class="val">del día</span></div></button>
  <button class="tile pop" data-open="screen" ${I()}>${icb("smartphone","#7B63A8")}<div><b>${scr!=null?hm(scr):"Pantalla"}</b><span class="val">${scr!=null?(recM>0?"−"+hm(recM)+" que antes":"de celu hoy"):"cargar hoy"}</span></div></button>
  <button class="tile pop" data-open="alerts" ${I()}>${icb("bell","#59A5B2")}${F.length?`<span class="badge2">${F.length}</span>`:""}<div><b>Avisos</b><span class="val">${F.length?F.length+" para vos":"sin novedades"}</span></div></button>
  <button class="tile pop" data-open="reco" ${I()}>${icb("sparkles","#B5739D")}<div><b>Descubrir</b><span class="val">libro · obra · dato</span></div></button>
  <button class="tile pop" data-open="news" ${I()}>${icb("newspaper","#4F8FB8")}<div><b>Actualidad</b><span class="val">${(S.iv.temas||[]).length||1} temas</span></div></button>
  <button class="tile pop" data-open="week" ${I()}>${icb("flag","#2F7380")}<div><b>Semana</b><span class="val">tu meta</span></div></button>
 </div></div>`;

 $$("[data-tab2]").forEach(b=>b.onclick=()=>setTab(b.dataset.tab2));
 $("#qaFocus").onclick=()=>setTab("productividad");
 $("#qaPlan").onclick=()=>setTab("calendario");
 $("#qaHard").onclick=hardDaySheet;
 if($("#ci"))$("#ci").onclick=checkin;
 $$("[data-act]").forEach(b=>b.onclick=()=>actSheet(S.acts.find(a=>a.id===b.dataset.act)));
 $$(".gstep").forEach(b=>b.onclick=()=>{const g=S.goals.find(x=>x.id===b.dataset.g),arr=g.log[t]=g.log[t]||[],i=arr.indexOf(b.dataset.a);if(i>=0)arr.splice(i,1);else{arr.push(b.dataset.a);toast(pick(MSG_OK))}if(!arr.length)delete g.log[t];save();render()});
 $$("[data-ged]").forEach(b=>b.onclick=()=>goalEditor(S.goals.find(g=>g.id===b.dataset.ged),"goal"));
 $$("[data-ach]").forEach(b=>b.onclick=()=>{const g=S.goals.find(x=>x.id===b.dataset.ach);S.goals=S.goals.filter(x=>x!==g);S.achieved.unshift({titulo:g.titulo,fin:t});save();render();toast("¡Lo lograste! Hay lugar para un objetivo nuevo, si querés.")});
 if($("#gAdd"))$("#gAdd").onclick=()=>goalEditor(null,"goal");
 $("#useAdd").onclick=usageSheet;if(reborn){reborn=false;setTimeout(()=>toast(`${fishName()} volvió a empezar. Nuevo ciclo.`),300)}
 $$("[data-open]").forEach(b=>b.onclick=()=>homeSheet(b.dataset.open));
}
const sheetHead=(n,c,t,sayTxt)=>`<div class="sheethead">${icb(n,c,52)}<h2>${t}</h2>${sayTxt?say(sayTxt):""}<button class="say" style="margin-left:auto;background:var(--line)" data-close aria-label="Cerrar">${ic("x",18)}</button></div>`;
document.addEventListener("click",e=>{if(e.target.closest("[data-close]"))closeSheet()});
function hardDaySheet(){
 const t=today();
 openSheet(`${sheetHead("cloud-rain","#8C9A90","¿Día difícil?","¿Día difícil? Está todo bien. Elegí: hoy descanso, o hoy no pude.")}
 <p class="muted">Está todo bien.</p>
 <div class="bigbtns"><button data-rest="rest">${icb("bed","#9AB0C9",66,"round")}Hoy descanso</button><button data-rest="miss">${icb("cloud-rain","#8C9A90",66,"round")}Hoy no pude</button></div>`,()=>{
  $$("[data-rest]").forEach(b=>b.onclick=()=>{S.rest[t]=b.dataset.rest;save();closeSheet();render();toast(pick(b.dataset.rest==="rest"?MSG_REST:MSG_MISS))});
 });
}
function actSheet(a){
 if(!a)return;
 openSheet(`${sheetHead(catI(a.cat),catC(a.cat),esc(a.title),`${a.title}, de ${a.start} a ${a.end}`)}
 <div class="row mt" style="gap:16px"><span class="iconbtn">${ic("clock",20)}<b>${a.start}–${a.end}</b></span><span class="iconbtn muted">${ic("tag",18)}${catL(a.cat)}</span>${a.repeat&&a.repeat.length?`<span class="iconbtn muted">${ic("repeat",18)}semanal</span>`:""}</div>
 <div class="bigbtns">${a.examId&&!a.done?`<button id="aStart">${icb("play","#2F7380",66,"round solid")}Empezar</button>`:""}<button id="aEdit">${icb("pencil","#59A5B2",66,"round")}Editar</button></div>`,()=>{
  if($("#aStart"))$("#aStart").onclick=()=>{closeSheet();startTimer({cat:"estudio",title:a.title,actId:a.id,examId:a.examId})};
  $("#aEdit").onclick=()=>{closeSheet();calDay=today();actEditor(a)};
 });
}
function homeSheet(k){
 const t=today(),p=S.profile||{};
 if(k==="challenge"){const chal=pick(p.desafios||["Hacé 25 minutos de foco sin el celu"],daySeed());
  openSheet(`${sheetHead("trophy","#E0A030","Desafío de hoy",chal)}<div class="card warm mt" style="border:0"><p style="font-weight:700;font-size:20px;line-height:1.4">${esc(chal)}</p></div>
  <div class="bigbtns"><button id="chGo">${icb("timer","#2F7380",66,"round solid")}Arrancar foco</button></div>`,()=>{$("#chGo").onclick=()=>{closeSheet();setTab("productividad")}});}
 if(k==="screen"){const scr=S.screen[t],rec=recovered(t);
  openSheet(`${sheetHead("smartphone","#7B63A8","Pantalla de hoy",scr!=null?`Hoy usaste el celular ${hm(scr)}.`:"Cargá cuánto usaste el celular hoy.")}
  <div class="row mt" style="flex-wrap:nowrap;gap:14px">${fishImg(scr!=null&&baseline()&&scr>baseline()?"phone":"normal",80)}<div>${scr!=null?`<p class="big">${hm(scr)}</p>${rec>0?`<p class="iconbtn mt" style="font-weight:600;color:var(--deep)">${ic("trending-up",18)}${hm(rec)} recuperadas</p>`:""}`:`<p class="big">—</p>`}</div></div>
  <p class="note mt">${scr!=null?(rec>0?`Hoy recuperaste ${hm(rec)} que antes dedicabas a scrollear. ¿Qué podrías hacer con ese tiempo?`:"Hoy fue un día de más pantalla, y está bien."):"Copiá el total de Bienestar digital (Android) o Tiempo en pantalla (iPhone)."}</p>
  <div class="bigbtns"><button id="scr">${icb(scr!=null?"pencil":"plus","#7B63A8",66,"round")}${scr!=null?"Corregir":"Cargar total"}</button><button id="scrUse">${icb("smartphone","#7B63A8",66,"round solid")}Sumar un rato</button></div>`,()=>{$("#scr").onclick=screenSheet;$("#scrUse").onclick=usageSheet});}
 if(k==="alerts"){const F=feed();
  openSheet(`${sheetHead("bell","#59A5B2","Avisos")}${F.map(f=>`<div class="item">${icb(f.ic,"#59A5B2",44,"round")}<div class="grow"><p>${esc(f.t)}</p>${f.src?`<span class="tag ${f.src==="apuntes"?"":"ext"} mt">${f.src==="apuntes"?"De tus apuntes":"Información externa"}</span>`:""}<div class="row mt">${say(f.t)}${f.act?`<button class="btn soft sm" data-fa="${f.act[0]}" data-ex="${f.act[1]}">${f.act[2]}</button>`:""}</div></div></div>`).join("")||`<div class="row mt" style="flex-wrap:nowrap;gap:12px">${fishImg("flat",70)}<p class="muted">Cuando cargues exámenes y actividades, acá van a aparecer avisos para vos.</p></div>`}
  <p class="honest">En esta versión web los avisos se ven al abrir PROKI. Las notificaciones push llegan con la app nativa.</p>`,()=>{
   $$("[data-fa]").forEach(b=>b.onclick=()=>{const ex=S.exams.find(e=>e.id===b.dataset.ex);if(!ex)return;closeSheet();b.dataset.fa==="flash"?flashSheet(ex):quizSheet(ex,3)});});}
 if(k==="reco"){openSheet(`${sheetHead("sparkles","#B5739D","Para descubrir")}<div id="reco">${recoHTML()}</div>`,()=>{if($("#recoGo"))$("#recoGo").onclick=loadReco});}
 if(k==="news"){const T=S.iv.temas.length?S.iv.temas:["Política y actualidad"];
  openSheet(`${sheetHead("newspaper","#4F8FB8","Actualidad")}<div class="optgrid sm mt">${T.map(tp=>`<div class="chip" style="cursor:default">${icb(optI(tp),"#4F8FB8",40)}<span>${esc(tp)}</span></div>`).join("")}</div>
  ${T.map(tp=>`<div class="item"><span>${ic(optI(tp),22)}</span><div class="grow"><div class="row">${(SOURCES[tp]||[["Google Noticias","https://news.google.com/search?q="+encodeURIComponent(tp)+"&hl=es-419"]]).map(([nm,u])=>`<a class="btn ghost sm iconbtn" href="${u}" target="_blank" rel="noopener">${esc(nm)}${ic("external-link",14)}</a>`).join("")}</div></div></div>`).join("")}
  <p class="honest">Te llevamos a fuentes confiables según tus intereses. Los resúmenes diarios necesitan el servidor de noticias de la versión nativa.</p>`);}
 if(k==="week"){openSheet(`${sheetHead("flag","#2F7380","Tu meta de la semana",p.objetivoSemanal||"")}<div class="card mt" style="background:var(--aqua);border:0"><p style="font-weight:700;font-size:20px;line-height:1.4">${esc(p.objetivoSemanal||"")}</p></div>`);}
}
function recoHTML(){
 const r=(S.reco||{})[today()];
 if(!r)return`<div class="welcome3" style="margin-top:8px"><div>${icb("book-marked","#B5739D",64,"round")}Libro</div><div>${icb("image","#B5739D",64,"round")}Obra</div><div>${icb("lightbulb","#B5739D",64,"round")}Dato</div></div><div class="bigbtns"><button id="recoGo">${icb("sparkles","#B5739D",66,"round solid")}Descubrir</button></div>`;
 return r.map(i=>`<div class="item">${icb(/libro/i.test(i.tipo)?"book-marked":/obra/i.test(i.tipo)?"image":"lightbulb","#B5739D",44,"round")}<div class="grow"><p style="font-weight:600">${esc(i.titulo)}${i.autor?` <span class="muted" style="font-weight:400">· ${esc(i.autor)}</span>`:""}</p><p class="small muted">${esc(i.porque)}</p>${say(i.titulo+". "+i.porque)}</div></div>`).join("")+`<p class="honest">Sugerencias generadas por IA a partir de tus intereses. Conviene chequear los datos antes de citarlos.</p>`;
}
async function loadReco(){
 const box=$("#reco");box.innerHTML=LOADER("Buscando algo lindo para hoy…");
 try{const r=await ai(`${VOICE}\nRecomendá 3 cosas para descubrir hoy: un libro, una obra (de arte, disco, película o pieza de diseño) y un dato interesante. Elegí obras y datos reales y conocidos, nada inventado. Intereses: ${JSON.stringify(S.iv.temas)}. Actividades que quiere sumar: ${JSON.stringify(S.iv.actividades)}. Respondé SOLO JSON {"items":[{"tipo":"Libro|Obra|Dato","titulo":"","autor":"autor o fuente, si aplica","porque":"una oración de por qué le puede interesar"}]}`,{modelTier:"quick"});
  const items=(r.items||[]).slice(0,3).map(i=>({tipo:String(i.tipo||""),titulo:String(i.titulo||""),autor:String(i.autor||""),porque:String(i.porque||"")}));
  if(!items.length)throw{code:"bad"};S.reco={[today()]:items};save();box.innerHTML=recoHTML();
 }catch(e){box.innerHTML=`<p>${esc(aiMsg(e))}</p><button class="btn soft sm mt" id="recoGo">Reintentar</button>`;$("#recoGo").onclick=loadReco}
}
function screenSheet(){
 const t=today(),cur=S.screen[t]??0;
 openSheet(`<h2>Tu tiempo de pantalla de hoy</h2><p class="note">Abrí Bienestar digital (Android) o Tiempo en pantalla (iPhone) y copiá el total.</p>
 <div class="two"><div><label class="f" for="sh">Horas</label><input type="number" id="sh" min="0" max="24" value="${Math.floor(cur/60)}"></div><div><label class="f" for="sm">Minutos</label><input type="number" id="sm" min="0" max="59" value="${cur%60}"></div></div>
 <div class="actions"><button class="btn" id="ss">Guardar</button><button class="btn ghost" id="sc">Cancelar</button></div>`,()=>{
  $("#sc").onclick=closeSheet;$("#ss").onclick=()=>{S.screen[t]=Math.max(0,(+$("#sh").value||0)*60+(+$("#sm").value||0));save();closeSheet();render();const r=recovered(t);if(r>0)toast(`Recuperaste ${hm(r)} hoy.`)}});
}
function checkin(){
 const A={q1:"",q2:"",q3:"",q4:""};
 const qs=[["q1","¿Sentís que estás aprovechando mejor tu tiempo?",["Sí, bastante","Un poco","Todavía no"]],["q2","¿Lograste cumplir tus objetivos?",["Casi todos","Algunos","Me costó"]],["q3","¿Qué hábito te sigue costando?",null],["q4","¿Qué te gustaría mejorar el próximo mes?",null]];
 openSheet(`<div class="sheethead">${icb("message-circle-heart","#2F7380",52,"round")}<h2>Pequeño repaso</h2></div><p class="note">No hay respuestas malas. Esto sirve para ajustar PROKI a vos.</p>${qs.map(([k,t,o])=>`<label class="f">${t}</label>${o?`<div class="chips">${o.map(x=>`<button class="chip" data-k="${k}" data-v="${esc(x)}" aria-pressed="false">${x}</button>`).join("")}</div>`:`<input type="text" id="${k}" maxlength="140">`}`).join("")}
 <p class="note" id="ciN"></p><div class="actions"><button class="btn" id="ciS">Enviar</button><button class="btn ghost" id="ciC">Más tarde</button></div>`,()=>{
  $$("[data-k]").forEach(c=>c.onclick=()=>{A[c.dataset.k]=c.dataset.v;$$(`[data-k="${c.dataset.k}"]`).forEach(x=>x.setAttribute("aria-pressed",x===c))});
  $("#ciC").onclick=closeSheet;
  $("#ciS").onclick=async()=>{A.q3=$("#q3").value;A.q4=$("#q4").value;$("#ciS").disabled=true;$("#ciN").innerHTML=LOADER("Ajustando tus recomendaciones…");
   const t=today();S.checkins.push({date:t,answers:A});S.lastCheckin=t;
   const stats={racha:streak(),minutosUltimos15:S.logs.filter(l=>diffD(l.date,t)<=15).reduce((s,l)=>s+l.min,0),objetivos:S.goals.map(g=>({titulo:g.titulo,diasConAvance:gDays(g)}))};
   try{const r=await ai(`${VOICE}\nEl usuario hizo su repaso quincenal. Perfil: ${JSON.stringify({entrevista:S.iv,objetivoSemanal:S.profile.objetivoSemanal})}. Datos: ${JSON.stringify(stats)}. Respuestas: ${JSON.stringify(A)}.
Si le costó, simplificá los objetivos (nunca culpa). Si le fue bien, podés proponer sumar uno (máximo 3 en total). Respondé SOLO JSON {"mensaje":"2 oraciones cálidas","objetivoSemanal":"","objetivos":[{"titulo":"","porque":"","acciones":["","",""]}],"desafios":["5 desafíos"]}`);
    if(r&&Array.isArray(r.objetivos)&&r.objetivos.length){
     S.goals=r.objetivos.slice(0,3).map(o=>{const ex=S.goals.find(g=>g.titulo===o.titulo);return ex||{id:uid(),titulo:String(o.titulo),porque:String(o.porque||""),acciones:(o.acciones||[]).map(x=>({id:uid(),t:String(x)})),inicio:t,log:{}}});
     if(r.objetivoSemanal)S.profile.objetivoSemanal=String(r.objetivoSemanal);if(Array.isArray(r.desafios))S.profile.desafios=r.desafios.map(String);
    }
    save();closeSheet();render();toast(r&&r.mensaje?String(r.mensaje):"Gracias por contarnos. Seguimos a tu ritmo.");
   }catch(e){save();closeSheet();render();toast("Guardamos tus respuestas. Seguimos a tu ritmo.")}
  };
 });
}

/* ============ CALENDARIO ============ */
let calDay=today(),weekOff=0;
function vCal(){
 const base=addD(today(),-((dow(today())+6)%7)+weekOff*7);
 const days=[...Array(7)].map((_,i)=>addD(base,i));
 if(!days.includes(calDay))calDay=days.includes(today())?today():days[0];
 const acts=actsOn(calDay),gaps=freeSlots(calDay);
 const plannedH=hm(planned(calDay));
 app.innerHTML=`${head("Agenda",`<button class="btn sm iconbtn" id="add">${ic("plus",18,2.6)}Nueva</button>`)}
 <div class="row" style="justify-content:space-between;margin-top:10px"><button class="btn ghost sm" id="pw" aria-label="Semana anterior">${ic("chevron-left",18)}</button><span class="small muted">${esc(fmtD(days[0],{day:"numeric",month:"short"}))} – ${esc(fmtD(days[6],{day:"numeric",month:"short"}))}</span><button class="btn ghost sm" id="nw" aria-label="Semana siguiente">${ic("chevron-right",18)}</button></div>
 <div class="week">${days.map(d=>`<button data-d="${d}" aria-pressed="${d===calDay}">${fmtD(d,{weekday:"short"}).slice(0,3)}<b>${pd(d).getDate()}</b>${actsOn(d).length?"<i></i>":""}</button>`).join("")}</div>
 <div class="card"><div class="row" style="justify-content:space-between"><h3>${esc(fmtD(calDay,{weekday:"long",day:"numeric",month:"long"}))}</h3><span class="small muted iconbtn" style="gap:4px">${ic("clock",15)}${plannedH}</span></div>
 ${acts.map((a,i)=>`<button class="item pop" style="--i:${i};width:100%;background:none;border:0;border-top:1px solid var(--line);text-align:left;color:inherit;align-items:center" data-ed="${a.id}">${icb(catI(a.cat),catC(a.cat),46,"round")}<div class="grow"><p style="font-weight:600" class="${a.done?"done-t":""}">${esc(a.title)}</p><p class="small muted iconbtn" style="gap:6px">${a.start}–${a.end}${a.repeat&&a.repeat.length?ic("repeat",14):""}${a.examId?ic("graduation-cap",14):""}${a.done?ic("circle-check",14):""}</p></div>${ic("pencil",18)}</button>`).join("")||`<div class="row mt" style="flex-wrap:nowrap;gap:12px">${fishImg("flat",64)}<p class="muted">Día libre. Podés cargar algo o simplemente disfrutarlo.</p></div>`}</div>
 <div class="sec">${shead("sparkles","Huecos libres","#E0A030")}${gaps.length?gaps.map(([s,e])=>`<div class="gap row" style="flex-wrap:nowrap;gap:12px">${icb(e-s>=120?"book-open-text":e-s>=60?"timer":"coffee","#E0A030",40,"round")}<div><b>${ts(s)}–${ts(e)}</b> · ${hm(e-s)}<br><span class="muted small">${gapTip(e-s)}</span></div></div>`).join(""):`<div class="row" style="flex-wrap:nowrap;gap:12px">${icb("coffee","#8C9A90",40,"round")}<p class="muted">Día completo. No hace falta llenar cada minuto.</p></div>`}</div>`;
 $("#add").onclick=()=>actEditor(null);$("#pw").onclick=()=>{weekOff--;render()};$("#nw").onclick=()=>{weekOff++;render()};
 $$("[data-d]").forEach(b=>b.onclick=()=>{calDay=b.dataset.d;render()});
 $$("[data-ed]").forEach(b=>b.onclick=()=>actEditor(S.acts.find(a=>a.id===b.dataset.ed)));
}
function gapTip(len){
 const g=S.goals[0];
 if(len>=120)return`Podrías usar 40 minutos para ${g?"“"+g.titulo+"”":"algo que te importe"} y dejar el resto como tiempo libre de verdad.`;
 if(len>=60)return`Alcanza para 25 minutos de foco y un descanso largo.`;
 return"Ideal para una pausa, una caminata o leer un rato.";
}
function actEditor(a){
 const isNew=!a;const x=a||{title:"",cat:"estudio",date:calDay,start:"09:00",end:"10:00",repeat:[]};
 openSheet(`<div class="sheethead">${icb(isNew?"plus":"pencil","#59A5B2",52,"round")}<h2>${isNew?"Nueva actividad":"Editar actividad"}</h2></div>
 <label class="f" for="aT">Nombre</label><input type="text" id="aT" value="${esc(x.title)}" maxlength="80" placeholder="Ej. Clase de Tipografía">
 <label class="f">Tipo</label><input type="hidden" id="aC" value="${x.cat}"><div class="optgrid sm">${Object.keys(CATS).map(k=>`<button class="chip" data-cat="${k}" aria-pressed="${k===x.cat}">${icb(catI(k),catC(k),40)}<span>${catL(k)}</span></button>`).join("")}</div>
 <label class="f" for="aD">Fecha</label><input type="date" id="aD" value="${x.date}">
 <div class="two"><div><label class="f" for="aS">Empieza</label><input type="time" id="aS" value="${x.start}"></div><div><label class="f" for="aE">Termina</label><input type="time" id="aE" value="${x.end}"></div></div>
 <label class="f iconbtn" style="gap:6px">${ic("repeat",16)}Repetir cada semana</label><div class="chips">${DOWS.map(([l,n])=>`<button class="chip" data-w="${n}" aria-pressed="${(x.repeat||[]).includes(n)}" aria-label="${["domingo","lunes","martes","miércoles","jueves","viernes","sábado"][n]}">${l}</button>`).join("")}</div>
 <p class="note" id="aN"></p>
 <div class="actions"><button class="btn" id="aOk">Guardar</button><button class="btn ghost" id="aX">Cancelar</button>${!isNew?`${a.repeat&&a.repeat.length?'<button class="link" id="aSkip">Saltear solo este día</button>':""}<button class="link" id="aDel">Borrar</button>`:""}</div>`,()=>{
  const rep=new Set(x.repeat||[]);
  $$("[data-cat]").forEach(c=>c.onclick=()=>{$("#aC").value=c.dataset.cat;$$("[data-cat]").forEach(y=>y.setAttribute("aria-pressed",y===c))});
  $$("[data-w]").forEach(c=>c.onclick=()=>{const n=+c.dataset.w;rep.has(n)?rep.delete(n):rep.add(n);c.setAttribute("aria-pressed",rep.has(n))});
  $("#aX").onclick=closeSheet;
  if($("#aDel"))$("#aDel").onclick=()=>{S.acts=S.acts.filter(y=>y!==a);save();closeSheet();render()};
  if($("#aSkip"))$("#aSkip").onclick=()=>{a.skip=(a.skip||[]).concat(calDay);save();closeSheet();render()};
  $("#aOk").onclick=()=>{const t=$("#aT").value.trim(),s=$("#aS").value,e=$("#aE").value;
   if(!t){$("#aT").focus();return}if(tm(e)<=tm(s)){$("#aN").textContent="La hora de fin tiene que ser después del inicio.";return}
   const o={title:t,cat:$("#aC").value,date:$("#aD").value||calDay,start:s,end:e,repeat:[...rep]};
   if(isNew)S.acts.push(Object.assign({id:uid()},o));else Object.assign(a,o);
   save();closeSheet();calDay=o.date;render();
   if(isNew&&o.cat==="examen")toast("Cargá tus apuntes en Aprender para que PROKI te ayude a prepararlo.");
  };
 });
}

/* ============ APRENDER ============ */
function vLearn(){
 if(examView){const ex=S.exams.find(e=>e.id===examView);if(ex)return vExam(ex);examView=null}
 const t=today(),list=S.exams.slice().sort((a,b)=>a.date.localeCompare(b.date));
 app.innerHTML=`${head("Aprender",`<button class="btn sm iconbtn" id="nx">${ic("plus",18,2.6)}Examen</button>`)}
 <div class="welcome3" style="margin-top:4px"><div>${icb("upload","#59A5B2",60,"round")}Subí apuntes</div><div>${icb("sparkles","#B5739D",60,"round")}PROKI los lee</div><div>${icb("calendar-range","#2F7380",60,"round")}Plan y repaso</div></div>
 <div class="mt2">${list.map((ex,i)=>{const dd=diffD(t,ex.date),pl=S.acts.filter(a=>a.examId===ex.id),dn=pl.filter(a=>a.done).length;return`<button class="card pop" style="--i:${i};width:100%;text-align:left;display:block;color:inherit" data-ex="${ex.id}">
  <div class="row" style="flex-wrap:nowrap;gap:14px">${icb("graduation-cap","#E9785F",56)}<div style="flex:1;min-width:0"><h3>${esc(ex.name)}</h3><p class="small muted iconbtn" style="gap:10px;margin-top:4px"><span class="iconbtn" style="gap:4px">${ic("calendar-days",14)}${esc(fmtD(ex.date,{day:"numeric",month:"short"}))}</span><span class="iconbtn" style="gap:4px">${ic("file-text",14)}${ex.mats.length}</span>${pl.length?`<span class="iconbtn" style="gap:4px">${ic("circle-check",14)}${dn}/${pl.length}</span>`:""}</p></div>
  <div style="text-align:center;flex:0 0 auto"><div class="big" style="font-size:34px">${dd<0?"✓":dd}</div><span class="small muted">${dd<0?"pasó":dd===0?"hoy":dd===1?"día":"días"}</span></div></div>
  ${pl.length?`<div class="progress mt"><i style="width:${dn/pl.length*100}%"></i></div>`:""}</button>`}).join("")||`<button class="tile wide" id="nx2" style="width:100%">${icb("plus","#E9785F",56,"round")}<div><b>Cargar mi primer examen</b><span class="val">con uno alcanza</span></div></button>`}</div>`;
 $("#nx").onclick=examEditor;if($("#nx2"))$("#nx2").onclick=examEditor;$$("[data-ex]").forEach(b=>b.onclick=()=>{examView=b.dataset.ex;render();window.scrollTo(0,0)});
}
function examEditor(){
 openSheet(`<h2>Nuevo examen o entrega</h2><label class="f" for="eN">Materia o tema</label><input type="text" id="eN" maxlength="80" placeholder="Ej. Historia del Diseño II">
 <div class="two"><div><label class="f" for="eD">Fecha</label><input type="date" id="eD" value="${addD(today(),14)}" min="${today()}"></div><div><label class="f" for="eH">Hora</label><input type="time" id="eH" value="09:00"></div></div>
 <div class="actions"><button class="btn" id="eOk">Crear</button><button class="btn ghost" id="eX">Cancelar</button></div>`,()=>{
  $("#eX").onclick=closeSheet;$("#eOk").onclick=()=>{const n=$("#eN").value.trim();if(!n)return $("#eN").focus();const d=$("#eD").value,h=$("#eH").value||"09:00";
   const id=uid();S.exams.push({id,name:n,date:d,time:h,mats:[],topics:[],resumen:"",datos:[],cards:[],scores:[]});
   S.acts.push({id:uid(),title:"Examen: "+n,cat:"examen",date:d,start:h,end:ts(Math.min(tm(h)+120,1439)),repeat:[],examRef:id});
   save();closeSheet();examView=id;render();toast("Examen cargado en tu calendario.")}});
}
function srcTag(f){return`<span class="tag ${f==="apuntes"?"":"ext"}">${f==="apuntes"?"De tus apuntes":"Información externa"}</span>`}
function vExam(ex){
 const t=today(),dd=diffD(t,ex.date),mats=ex.mats.map(id=>MATS[id]).filter(Boolean),pl=S.acts.filter(a=>a.examId===ex.id).sort((a,b)=>(a.date+a.start).localeCompare(b.date+b.start));
 const totalChars=mats.reduce((s,m)=>s+(m.text||"").length,0);
 app.innerHTML=`${head("")}<button class="back-btn iconbtn" id="bk">${ic("chevron-left",18)}Exámenes</button>
 <div class="row" style="flex-wrap:nowrap;gap:14px">${icb("graduation-cap","#E9785F",60)}<div style="flex:1"><h2>${esc(ex.name)}</h2><p class="muted iconbtn" style="gap:6px">${ic("calendar-days",16)}${esc(fmtD(ex.date,{weekday:"short",day:"numeric",month:"short"}))}</p></div><div style="text-align:center"><div class="big" style="font-size:38px">${dd<0?"✓":dd}</div><span class="small muted">${dd<0?"pasó":dd===0?"hoy":"días"}</span></div></div>
 ${ex.topics.length?`<div class="sec">${shead("sparkles","Estudiar","#B5739D")}<div class="tiles">
  <button class="tile pop" style="--i:0" id="fl">${icb("layers","#B5739D")}<div><b>Tarjetas</b><span class="val">${(ex.cards||[]).filter(c=>c.known).length}/${(ex.cards||[]).length||"—"} sabidas</span></div></button>
  <button class="tile pop" style="--i:1" id="qz">${icb("list-checks","#59A5B2")}<div><b>Preguntas</b><span class="val">5 rápidas</span></div></button>
  <button class="tile pop" style="--i:2" id="sim">${icb("clipboard-check","#E9785F")}<div><b>Simulacro</b><span class="val">${ex.scores.length?`último ${ex.scores[ex.scores.length-1].ok}/${ex.scores[ex.scores.length-1].n}`:"12 preguntas"}</span></div></button>
  <button class="tile pop" style="--i:3" id="exp">${icb("message-circle-question","#2F7380")}<div><b>Explicame</b><span class="val">un concepto</span></div></button>
 </div></div>`:""}
 <div class="sec">${shead("file-text","Materiales","#59A5B2",`<button class="btn sm iconbtn" id="am" style="margin-left:auto">${ic("upload",16)}Sumar</button>`)}
 <div class="card">${mats.map(m=>`<div class="item">${icb({pdf:"file-text",img:"image",doc:"file-pen-line",txt:"scroll"}[m.kind]||"scroll","#59A5B2",40)}<div class="grow"><p style="font-weight:600">${esc(m.name)}</p><p class="small muted">${(m.text||"").length.toLocaleString("es-AR")} caracteres leídos</p></div><button class="btn ghost sm" data-vm="${m.id}" aria-label="Ver">${ic("eye",16)}</button></div>`).join("")||`<div class="optgrid sm">${[["file-text","PDF"],["image","Fotos"],["file-pen-line","Word"],["scroll","Texto"]].map(([n,l])=>`<div class="chip" style="cursor:default">${icb(n,"#59A5B2",40)}<span>${l}</span></div>`).join("")}</div>`}</div>
 ${mats.length?`<div class="row mt"><button class="btn soft iconbtn" id="an">${ic("sparkles",18)}${ex.topics.length?"Volver a analizar":"Analizar con PROKI"}</button><span class="small muted" id="anN"></span></div>`:""}</div>
 ${ex.topics.length?`
 <div class="sec">${shead("list-checks","Temas","#2F7380")}<div class="card">${ex.topics.map((tp,i)=>`<div class="item"><span class="tag">${i+1}</span><div class="grow"><p style="font-weight:600">${esc(tp.titulo)}</p><p class="small muted">${esc((tp.conceptos||[]).join(" · "))}</p></div></div>`).join("")}</div></div>
 <div class="sec">${shead("scroll","Resumen","#59A5B2",say(ex.resumen,"Escuchar resumen"))}<div class="card prose">${srcTag("apuntes")}<div class="mt">${ex.resumen.split(/\n+/).map(p=>`<p>${esc(p)}</p>`).join("")}</div></div></div>
 <div class="sec">${shead("calendar-range","Plan","#2F7380",`<button class="btn ${pl.length?"ghost":""} sm iconbtn" id="pln" style="margin-left:auto">${ic(pl.length?"refresh-ccw":"sparkles",16)}${pl.length?"Rehacer":"Armar plan"}</button>`)}
  <div class="card mt">${pl.map(a=>`<div class="item"><button class="tick" aria-pressed="${!!a.done}" data-pd="${a.id}" aria-label="Hecha: ${esc(a.topic)}">${CHK}</button><div class="grow"><p class="${a.done?"done-t":""}" style="font-weight:600">${esc(a.topic)}</p><p class="small muted">${esc(fmtD(a.date,{weekday:"short",day:"numeric",month:"short"}))} · ${a.start}–${a.end} · ${a.kind}</p></div></div>`).join("")||'<p class="muted">PROKI reparte los temas en tus espacios libres hasta la fecha del examen, con repasos y un simulacro final. Sin llenarte el día.</p>'}</div></div>`:""}
 <div class="actions"><button class="link iconbtn" id="dx">${ic("trash-2",16)}Borrar este examen</button></div>`;
 $("#bk").onclick=()=>{examView=null;render()};$("#am").onclick=()=>matSheet(ex);
 $$("[data-vm]").forEach(b=>b.onclick=()=>{const m=MATS[b.dataset.vm];openSheet(`<h2>${esc(m.name)}</h2><p class="note">Texto que PROKI leyó de este material.</p><div class="card mt" style="max-height:50vh;overflow:auto;white-space:pre-wrap;font-size:14px">${esc((m.text||"").slice(0,20000))}</div><div class="actions"><button class="btn ghost" id="mx">Cerrar</button><button class="link" id="md">Quitar material</button></div>`,()=>{$("#mx").onclick=closeSheet;$("#md").onclick=async()=>{ex.mats=ex.mats.filter(i=>i!==m.id);await delMat(m.id);save();closeSheet();render()}})});
 if($("#an"))$("#an").onclick=()=>analyze(ex);
 if($("#fl"))$("#fl").onclick=()=>flashSheet(ex);if($("#qz"))$("#qz").onclick=()=>quizSheet(ex,5);if($("#sim"))$("#sim").onclick=()=>quizSheet(ex,12,true);if($("#exp"))$("#exp").onclick=()=>explainSheet(ex);
 if($("#pln"))$("#pln").onclick=()=>{const n=makePlan(ex);render();toast(n?`Plan armado: ${n} sesiones en tu calendario.`:"No encontramos espacios libres antes del examen. Probá liberar algún horario.")};
 $$("[data-pd]").forEach(b=>b.onclick=()=>{const a=S.acts.find(x=>x.id===b.dataset.pd);a.done=!a.done;if(a.done)toast(pick(MSG_OK));save();render()});
 $("#dx").onclick=async()=>{if(!confirm("¿Borrar el examen, su plan y sus materiales?"))return;for(const id of ex.mats)await delMat(id);S.acts=S.acts.filter(a=>a.examId!==ex.id&&a.examRef!==ex.id);S.exams=S.exams.filter(e=>e!==ex);examView=null;save();render()};
}
function loadScript(src){return new Promise((res,rej)=>{if(document.querySelector(`script[src="${src}"]`))return res();const s=document.createElement("script");s.src=src;s.onload=res;s.onerror=()=>rej(new Error("load"));document.head.appendChild(s)})}
async function pdfText(file){
 await loadScript("https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.min.js");
 const lib=window.pdfjsLib;lib.GlobalWorkerOptions.workerSrc="https://cdnjs.cloudflare.com/ajax/libs/pdf.js/3.11.174/pdf.worker.min.js";
 const doc=await lib.getDocument({data:await file.arrayBuffer()}).promise;let out="";
 for(let i=1;i<=Math.min(doc.numPages,80);i++){const p=await doc.getPage(i);const c=await p.getTextContent();out+=c.items.map(x=>x.str).join(" ")+"\n\n"}
 return out;
}
async function docxText(file){await loadScript("https://cdnjs.cloudflare.com/ajax/libs/mammoth/1.6.0/mammoth.browser.min.js");const r=await window.mammoth.extractRawText({arrayBuffer:await file.arrayBuffer()});return r.value}
async function imgText(file){
 const s=await wait(sampleP,11000);if(!s)throw{code:"unavailable"};
 const lim=await s.limits().catch(()=>null);if(!lim||!lim.images)throw{code:"images_unavailable"};
 const r=await s("Transcribí fielmente el texto de esta foto de apuntes (manuscritos o impresos). Si hay esquemas o diagramas, describilos brevemente entre corchetes. Respondé solo con la transcripción.",{images:[file],modelTier:"default"});
 return r.text;
}
function matSheet(ex){
 openSheet(`<h2>Sumar material</h2><p class="note">PDF, fotos de apuntes, Word (.docx), texto (.txt, .md). Para presentaciones, exportalas a PDF.</p>
 <label class="f" for="mf">Subir archivos</label><input type="file" id="mf" multiple accept=".pdf,.docx,.txt,.md,image/*">
 <label class="f" for="mt">O pegá el texto</label><input type="text" id="mn" placeholder="Nombre (ej. Apunte clase 3)" maxlength="80"><textarea id="mt" class="mt" placeholder="Pegá acá tus apuntes…"></textarea>
 <div id="mN" class="note"></div><div class="actions"><button class="btn" id="mOk">Guardar</button><button class="btn ghost" id="mX">Cerrar</button></div>`,()=>{
  $("#mX").onclick=closeSheet;
  $("#mOk").onclick=async()=>{const files=[...$("#mf").files],txt=$("#mt").value.trim(),N=$("#mN");$("#mOk").disabled=true;let added=0,fails=[];
   if(txt){const m={id:uid(),examId:ex.id,name:$("#mn").value.trim()||"Texto pegado",kind:"txt",text:clampTxt(txt,120000)};await putMat(m);ex.mats.push(m.id);added++}
   for(const f of files){N.innerHTML=LOADER(`Leyendo ${f.name}…`);try{let text="",kind="txt";
     if(/\.pdf$/i.test(f.name)){text=await pdfText(f);kind="pdf"}else if(/\.docx$/i.test(f.name)){text=await docxText(f);kind="doc"}
     else if(f.type.startsWith("image/")){text=await imgText(f);kind="img"}else text=await f.text();
     if(!text.trim())throw{code:"empty"};
     const m={id:uid(),examId:ex.id,name:f.name,kind,text:clampTxt(text.trim(),120000)};await putMat(m);ex.mats.push(m.id);added++}
    catch(e){fails.push(f.name+(e&&e.code==="empty"?" (no tiene texto seleccionable: probá subirlo como foto)":e&&e.code==="images_unavailable"?" (las fotos necesitan la IA activa)":""))}}
   save();if(fails.length){N.textContent="No pudimos leer: "+fails.join(", ")+".";$("#mOk").disabled=false;render();return}
   closeSheet();render();if(added)toast(added===1?"Material guardado.":added+" materiales guardados.")};
 });
}
function corpus(ex,max=60000){const ms=ex.mats.map(id=>MATS[id]).filter(Boolean);const per=Math.floor(max/Math.max(1,ms.length));return ms.map(m=>`### ${m.name}\n${m.text.slice(0,per)}`).join("\n\n")}
async function analyze(ex){
 const N=$("#anN");$("#an").disabled=true;N.innerHTML=LOADER("Leyendo tus apuntes…");
 try{const r=await ai(`${VOICE}
Analizá los apuntes de un estudiante para el examen "${ex.name}". Priorizá SIEMPRE el contenido de sus apuntes. Si agregás algo que no está en los apuntes, marcalo como "externo".
APUNTES:
${corpus(ex)}
Respondé SOLO JSON: {"temas":[{"titulo":"","conceptos":["3-6 conceptos clave"]}],"resumen":"resumen claro de 3-5 párrafos basado solo en los apuntes, separados por \\n","datos":[{"texto":"¿Sabías que…? (dato breve sobre un concepto importante o una relación entre conceptos)","fuente":"apuntes|externo"}]}  Entre 3 y 8 temas, 6 datos.`);
  if(!r||!Array.isArray(r.temas)||!r.temas.length)throw{code:"bad"};
  ex.topics=r.temas.slice(0,10).map(t=>({titulo:String(t.titulo),conceptos:(t.conceptos||[]).map(String)}));ex.resumen=String(r.resumen||"");ex.datos=(r.datos||[]).map(d=>({texto:String(d.texto),fuente:d.fuente==="externo"?"externo":"apuntes"}));
  save();render();toast("Listo: temas, resumen y datos para repasar.");
 }catch(e){N.textContent=aiMsg(e);$("#an").disabled=false}
}
function makePlan(ex){
 S.acts=S.acts.filter(a=>a.examId!==ex.id);
 const t=today(),last=addD(ex.date,-1);if(last<t){save();return 0}
 const hrs={"2 a 4 horas":1,"5 a 7 horas":1,"8 a 12 horas":2,"Más de 12 horas":2}[S.iv.horas]||1;
 const pref=S.iv.momento==="A la mañana"?[[780,1320],[480,780]]:S.iv.momento==="A la noche"?[[840,1170],[480,840],[1170,1320]]:S.iv.momento==="A la tarde"?[[480,780],[1080,1320],[780,1080]]:[[480,1320]];
 const sessions=[];ex.topics.forEach(tp=>sessions.push({topic:tp.titulo,kind:"estudio",min:40}));
 ex.topics.forEach(tp=>sessions.push({topic:"Repaso: "+tp.titulo,kind:"repaso",min:20}));
 let d=t,count=0;const perDay={};
 const findSlot=(day,len)=>{for(const[a,b]of pref){const s=freeSlots(day,a,b,len)[0];if(s)return s[0]}return null};
 const queue=sessions.slice();let guard=0;
 while(queue.length&&d<=last&&guard++<400){
  if((perDay[d]||0)<hrs){const s=queue[0];const st=findSlot(d,s.min);if(st!=null){S.acts.push({id:uid(),title:ex.name+": "+s.topic,topic:s.topic,kind:s.kind,cat:"estudio",date:d,start:ts(st),end:ts(st+s.min),repeat:[],examId:ex.id,done:false});perDay[d]=(perDay[d]||0)+1;queue.shift();count++;continue}}
  d=addD(d,1);
 }
 const sd=last>=t?last:t,ss=findSlot(sd,45);if(ss!=null){S.acts.push({id:uid(),title:ex.name+": simulacro",topic:"Simulacro de examen",kind:"simulacro",cat:"estudio",date:sd,start:ts(ss),end:ts(ss+45),repeat:[],examId:ex.id,done:false});count++}
 save();return count;
}
async function flashSheet(ex){
 if(!ex.cards||!ex.cards.length){
  openSheet(`<h2>Flashcards</h2>${LOADER("Armando tarjetas desde tus apuntes…")}`);
  try{const r=await ai(`${VOICE}\nCreá 12 flashcards para estudiar "${ex.name}" basadas en estos apuntes. Priorizá los apuntes; si algo no está en ellos marcá fuente "externo".\nAPUNTES:\n${corpus(ex,45000)}\nRespondé SOLO JSON {"cards":[{"q":"pregunta o concepto","a":"respuesta breve","fuente":"apuntes|externo"}]}`);
   ex.cards=(r.cards||[]).slice(0,20).map(c=>({q:String(c.q),a:String(c.a),fuente:c.fuente==="externo"?"externo":"apuntes",known:false}));save()}
  catch(e){openSheet(`<h2>Flashcards</h2><p class="mt">${esc(aiMsg(e))}</p><div class="actions"><button class="btn ghost" id="x">Cerrar</button></div>`,()=>$("#x").onclick=closeSheet);return}
 }
 let order=ex.cards.map((c,i)=>i).sort((a,b)=>ex.cards[a].known-ex.cards[b].known),i=0,back=false;
 const draw=()=>{const c=ex.cards[order[i]];const k=ex.cards.filter(c=>c.known).length;
  openSheet(`<div class="row" style="justify-content:space-between"><h2 class="iconbtn" style="gap:10px">${icb("layers","#B5739D",40)}Tarjetas</h2><span class="small muted">${i+1}/${order.length} · ${k} sabidas</span></div>
  <button class="flash mt ${back?"back":""}" id="fc">${esc(back?c.a:c.q)}</button><div class="row mt" style="justify-content:space-between">${srcTag(c.fuente)}<span class="small muted iconbtn" style="gap:6px">${ic("refresh-ccw",15)}Tocá para girar ${say(back?c.a:c.q)}</span></div>
  <div class="bigbtns"><button id="fr">${icb("repeat","#E0A030",66,"round")}Repasar</button><button id="fk">${icb("check","#59A5B2",66,"round solid")}La sé</button></div><div class="actions" style="justify-content:center"><button class="link" id="fn">Generar nuevas</button><button class="link" id="fx">Cerrar</button></div>`,()=>{
   $("#fc").onclick=()=>{back=!back;draw()};
   const next=known=>{c.known=known;save();back=false;if(i<order.length-1){i++;draw()}else{closeSheet();render();toast(`Terminaste la ronda. ${ex.cards.filter(c=>c.known).length} de ${ex.cards.length} ya las sabés.`)}};
   $("#fk").onclick=()=>next(true);$("#fr").onclick=()=>next(false);$("#fx").onclick=()=>{closeSheet();render()};$("#fn").onclick=()=>{ex.cards=[];save();flashSheet(ex)};
  });};
 draw();
}
async function quizSheet(ex,n,sim){
 openSheet(`<h2>${sim?"Simulacro":"Cuestionario"}</h2>${LOADER("Preparando preguntas desde tus apuntes…")}`);
 let qs;try{const r=await ai(`${VOICE}\nCreá ${n} preguntas de opción múltiple${sim?" tipo examen, variando dificultad,":""} sobre "${ex.name}" basadas en estos apuntes. 4 opciones cada una, una sola correcta. Priorizá los apuntes; marcá "externo" si no sale de ellos.\nAPUNTES:\n${corpus(ex,45000)}\nRespondé SOLO JSON {"preguntas":[{"q":"","opciones":["","","",""],"correcta":0,"explicacion":"breve","fuente":"apuntes|externo"}]}`,{cache:false});
  qs=(r.preguntas||[]).filter(q=>Array.isArray(q.opciones)&&q.opciones.length>=2).slice(0,n)}
 catch(e){openSheet(`<h2>Cuestionario</h2><p class="mt">${esc(aiMsg(e))}</p><div class="actions"><button class="btn ghost" id="x">Cerrar</button></div>`,()=>$("#x").onclick=closeSheet);return}
 if(!qs.length){openSheet(`<h2>Cuestionario</h2><p class="mt">No pudimos armar preguntas. Probá de nuevo.</p><div class="actions"><button class="btn ghost" id="x">Cerrar</button></div>`,()=>$("#x").onclick=closeSheet);return}
 let i=0,ok=0;
 const draw=(ans)=>{const q=qs[i];openSheet(`<div class="row" style="justify-content:space-between"><h2>${sim?"Simulacro":"Cuestionario"}</h2><span class="small muted">${i+1}/${qs.length}</span></div>
  <p class="mt" style="font-weight:600;font-size:17px">${esc(q.q)}</p>${q.opciones.map((o,j)=>`<button class="opt ${ans!=null?(j===q.correcta?"ok":j===ans?"bad":""):""}" data-j="${j}" ${ans!=null?"disabled":""}>${esc(o)}</button>`).join("")}
  ${ans!=null?`<div class="card mt" style="background:var(--bg)"><p style="font-weight:600">${ans===q.correcta?"¡Bien!":"Casi. La correcta está marcada."}</p><p class="small mt">${esc(q.explicacion||"")}</p><div class="mt">${srcTag(q.fuente)}</div></div>`:""}
  <div class="actions">${ans!=null?`<button class="btn" id="qn">${i<qs.length-1?"Siguiente":"Ver resultado"}</button>`:""}<button class="link" id="qx">Salir</button></div>`,()=>{
   $$("[data-j]").forEach(b=>b.onclick=()=>{const j=+b.dataset.j;if(j===q.correcta)ok++;draw(j)});
   $("#qx").onclick=()=>{closeSheet();render()};
   if($("#qn"))$("#qn").onclick=()=>{if(i<qs.length-1){i++;draw()}else{ex.scores.push({date:today(),ok,n:qs.length,sim:!!sim});save();
    openSheet(`<h2>${ok}/${qs.length}</h2><p class="mt">${ok/qs.length>=.7?"Muy bien. Se nota lo que venís estudiando.":"Cada pregunta que fallás te muestra qué repasar. Eso también es avanzar."}</p><div class="actions"><button class="btn" id="x">Listo</button></div>`,()=>$("#x").onclick=()=>{closeSheet();render()})}};
  });};
 draw();
}
function explainSheet(ex){
 openSheet(`<h2>Explicame algo</h2><label class="f" for="eq">¿Qué concepto te cuesta?</label><input type="text" id="eq" maxlength="160" placeholder="Ej. la diferencia entre Bauhaus y Ulm">
 <div class="actions"><button class="btn" id="eg">Explicar simple</button><button class="btn ghost" id="ex">Cerrar</button></div><div id="eo" class="mt"></div>`,()=>{
  $("#ex").onclick=closeSheet;
  $("#eg").onclick=async()=>{const q=$("#eq").value.trim();if(!q)return;$("#eo").innerHTML=LOADER("Pensando una explicación sencilla…");
   try{const r=await ai(`${VOICE}\nExplicá de forma sencilla, con un ejemplo, el concepto "${q}" para el examen "${ex.name}". Primero usá lo que dicen los apuntes; si agregás algo que no está en ellos, ponelo en una parte separada con fuente "externo".\nAPUNTES:\n${corpus(ex,45000)}\nRespondé SOLO JSON {"partes":[{"texto":"","fuente":"apuntes|externo"}]}`);
    $("#eo").innerHTML=(r.partes||[]).map(p=>`<div class="card" style="background:var(--bg)">${srcTag(p.fuente==="externo"?"externo":"apuntes")}<p class="mt">${esc(p.texto)}</p></div>`).join("")}
   catch(e){$("#eo").textContent=aiMsg(e)}};
 });
}

/* ============ PRODUCTIVIDAD ============ */
let tick=null;
function elapsedStr(){if(!S.timer)return"00:00";const s=Math.floor((Date.now()-S.timer.start)/1000);const h=Math.floor(s/3600),m=Math.floor(s%3600/60),x=s%60;return(h?h+":":"")+pad(m)+":"+pad(x)}
function startTimer(o){if(S.timer){toast("Ya tenés una actividad en curso.");setTab("productividad");return}S.timer=Object.assign({start:Date.now()},o);save();setTab("productividad")}
const RING_C=2*Math.PI*96;
function ringOff(){if(!S.timer)return RING_C;const m=((Date.now()-S.timer.start)/60000)%25;return RING_C*(1-m/25)}
setInterval(()=>{const c=$("#tclock");if(c&&S.timer)c.textContent=elapsedStr();const r=$("#ringArc");if(r)r.style.strokeDashoffset=ringOff()},1000);
function vFocus(){
 const t=today(),logs=logsOn(t).slice().reverse();
 const cats=[...new Set(actsOn(t).map(a=>a.cat).concat(logs.map(l=>l.cat)))];
 const FC=["estudio","trabajo","deporte","lectura","proyecto","personal","recreacion","descanso"];
 app.innerHTML=`${head("Foco")}
 ${S.timer?`<div class="card hl mt" style="text-align:center"><span class="iconbtn" style="justify-content:center;gap:8px;font-weight:700">${ic(catI(S.timer.cat),20)}${esc(S.timer.title||catL(S.timer.cat))}</span>
  <div class="ringtimer"><svg viewBox="0 0 220 220"><circle cx="110" cy="110" r="96" fill="none" stroke="rgba(255,255,255,.15)" stroke-width="14"/><circle id="ringArc" cx="110" cy="110" r="96" fill="none" stroke="var(--teal)" stroke-width="14" stroke-linecap="round" stroke-dasharray="${RING_C}" style="stroke-dashoffset:${ringOff()}"/></svg><div class="center"><div><p class="clock" id="tclock">${elapsedStr()}</p><span class="small" style="opacity:.75">vueltas de 25 min</span></div></div></div>
  <div class="bigbtns"><button id="stop">${icb("square","#76BDCD",66,"round solid")}Terminar</button><button id="cancel">${icb("x","#8C9A90",66,"round")}Descartar</button></div></div>`
 :`<div class="card mt"><div class="row" style="flex-wrap:nowrap;gap:12px">${fishImg("reading",72)}<h3>¿Qué vas a hacer?${say("¿Qué vas a hacer? Elegí un tipo y tocá empezar.")}</h3></div>
  <div class="optgrid sm mt">${FC.map((k,i)=>`<button class="chip pop" style="--i:${i}" data-c="${k}" aria-pressed="${i===0}">${icb(catI(k),catC(k),40)}<span>${catL(k)}</span></button>`).join("")}</div>
  <input type="text" id="fT" maxlength="80" placeholder="Nombre (opcional)" class="mt" aria-label="Nombre de la actividad">
  <div class="bigbtns"><button id="go">${icb("play","#2F7380",72,"round solid")}Empezar</button><button id="man">${icb("pencil","#59A5B2",66,"round")}Ya lo hice</button></div></div>`}
 <div class="sec">${shead("chart-column","Planificado vs. hecho","#59A5B2")}<div class="card">${cats.length?cats.map(c=>{const p=planned(t,c),r=logsOn(t).filter(l=>l.cat===c).reduce((s,l)=>s+l.min,0),mx=Math.max(p,r,1);return`<div class="hbar"><span class="iconbtn" style="gap:6px">${ic(catI(c),16)}${catL(c)}</span><div class="tr"><span class="p" style="width:${p/mx*100}%"></span><span class="r" style="width:${r/mx*100}%;background:${catC(c)}"></span></div></div><p class="small muted" style="margin-left:106px">${hm(p)} · ${hm(r)}</p>`}).join("")+`<div class="legend"><span><i style="background:var(--line)"></i>Planificado</span><span><i style="background:var(--sage)"></i>Hecho</span></div>`:'<p class="muted">Cuando registres lo que hacés, acá aparece la comparación.</p>'}</div></div>
 <div class="sec">${shead("list-checks","Hoy hiciste","#2F7380")}<div class="card">${logs.map(l=>`<div class="item">${icb(catI(l.cat),catC(l.cat),42,"round")}<div class="grow"><p style="font-weight:600">${esc(l.title||catL(l.cat))}</p><p class="small muted">${hm(l.min)}${l.avance?" · "+esc(l.avance):""}${l.animo?" · "+esc(l.animo):""}</p>${l.note?`<p class="small mt">${esc(l.note)}</p>`:""}</div><button class="btn ghost sm" data-dl="${l.id}" aria-label="Borrar registro">${ic("trash-2",16)}</button></div>`).join("")||`<div class="row" style="flex-wrap:nowrap;gap:12px">${icb("footprints","#8C9A90",44,"round")}<p class="muted">Con una sesión corta alcanza.</p></div>`}</div></div>`;
 if(S.timer){$("#stop").onclick=finishSheet;$("#cancel").onclick=()=>{S.timer=null;save();render()}}
 else{let cat="estudio";$$("[data-c]").forEach(c=>c.onclick=()=>{cat=c.dataset.c;$$("[data-c]").forEach(x=>x.setAttribute("aria-pressed",x===c))});
  $("#go").onclick=()=>startTimer({cat,title:$("#fT").value.trim()});$("#man").onclick=manualSheet}
 $$("[data-dl]").forEach(b=>b.onclick=()=>{S.logs=S.logs.filter(l=>l.id!==b.dataset.dl);save();render()});
}
function finishSheet(){
 const min=Math.max(1,Math.round((Date.now()-S.timer.start)/60000));
 openSheet(`<div class="sheethead">${icb("party-popper","#E0A030",52,"round")}<h2>¡Terminaste! ${hm(min)}</h2></div>
 <label class="f">¿Cuánto avanzaste?</label><div class="optgrid sm" id="av">${[["Arranqué","footprints"],["Bastante","trending-up"],["Lo terminé","circle-check"]].map(([x,n])=>`<button class="chip" data-v="${x}" aria-pressed="false">${icb(n,"#59A5B2",40)}<span>${x}</span></button>`).join("")}</div>
 <label class="f">¿Cómo te sentiste?</label><div class="optgrid sm" id="an">${[["Con energía","zap"],["Bien","smile"],["Cansado/a","coffee"],["Me costó","meh"]].map(([x,n])=>`<button class="chip" data-v="${x}" aria-pressed="false">${icb(n,"#E0A030",40)}<span>${x}</span></button>`).join("")}</div>
 <label class="f" for="fn">¿Qué hiciste? <span class="muted" style="font-weight:400">(opcional)</span></label><input type="text" id="fn" maxlength="140">
 <div class="actions"><button class="btn iconbtn" id="ok">${ic("check",20,2.4)}Guardar</button></div>`,()=>{
  const val={av:"",an:""};["av","an"].forEach(g=>$$(`#${g} .chip`).forEach(c=>c.onclick=()=>{val[g]=c.dataset.v;$$(`#${g} .chip`).forEach(x=>x.setAttribute("aria-pressed",x===c))}));
  $("#ok").onclick=()=>{const T=S.timer;S.logs.push({id:uid(),cat:T.cat,title:T.title,date:ymd(new Date(T.start)),min,note:$("#fn").value.trim(),avance:val.av,animo:val.an,examId:T.examId||null});
   if(T.actId){const a=S.acts.find(x=>x.id===T.actId);if(a)a.done=true}S.timer=null;save();closeSheet();render();toast(val.an==="Me costó"?"Lo hiciste igual, y eso vale mucho.":pick(MSG_OK))};
 });
}
function manualSheet(){
 openSheet(`<h2>Registrar a mano</h2><label class="f" for="mT">¿Qué hiciste?</label><input type="text" id="mT" maxlength="80" placeholder="Ej. Gimnasio">
 <label class="f" for="mC">Tipo</label><select id="mC">${Object.keys(CATS).map(k=>`<option value="${k}">${catL(k)}</option>`).join("")}</select>
 <label class="f" for="mD">Fecha</label><input type="date" id="mD" value="${today()}" max="${today()}">
 <div class="two"><div><label class="f" for="mH">Horas</label><input type="number" id="mH" min="0" max="16" value="0"></div><div><label class="f" for="mM">Minutos</label><input type="number" id="mM" min="0" max="59" value="30"></div></div>
 <div class="actions"><button class="btn" id="ok">Guardar</button><button class="btn ghost" id="x">Cancelar</button></div>`,()=>{
  $("#x").onclick=closeSheet;$("#ok").onclick=()=>{const min=(+$("#mH").value||0)*60+(+$("#mM").value||0);if(min<=0)return;S.logs.push({id:uid(),cat:$("#mC").value,title:$("#mT").value.trim(),date:$("#mD").value||today(),min,note:"",avance:"",animo:""});save();closeSheet();render();toast(pick(MSG_OK))};
 });
}

/* ============ PROGRESO ============ */
let range=7;
const RANGES=[[7,"Semana"],[30,"Mes"],[90,"3 meses"]];
function tipInit(){
 let tip=$("#ctip");if(!tip){tip=document.createElement("div");tip.id="ctip";tip.className="ctip";tip.setAttribute("role","status");document.body.appendChild(tip)}
 const show=(el,x,y)=>{tip.textContent=el.dataset.tip;tip.classList.add("on");const w=tip.offsetWidth;tip.style.left=Math.min(innerWidth-w-8,Math.max(8,x-w/2))+"px";tip.style.top=(y-44)+"px"};
 $$("[data-tip]").forEach(el=>{
  el.addEventListener("pointerenter",e=>show(el,e.clientX,e.clientY));el.addEventListener("pointermove",e=>show(el,e.clientX,e.clientY));
  el.addEventListener("pointerleave",()=>tip.classList.remove("on"));
  el.addEventListener("click",e=>{const r=el.getBoundingClientRect();show(el,r.left+r.width/2,r.top);clearTimeout(tipInit.t);tipInit.t=setTimeout(()=>tip.classList.remove("on"),1800)});
 });
}
/* agrupa días en buckets: diario para 7/30, semanal para 90 */
function buckets(days){
 if(days.length<=30)return days.map(d=>({days:[d],label:days.length===7?fmtD(d,{weekday:"short"}).slice(0,2):((days.length-1-days.indexOf(d))%5===0?String(pd(d).getDate()):""),name:fmtD(d,{weekday:"short",day:"numeric",month:"short"})}));
 const out=[];for(let i=0;i<days.length;i+=7){const g=days.slice(i,i+7);out.push({days:g,label:fmtD(g[0],{day:"numeric",month:"short"}).replace(" de "," "),name:"Semana del "+fmtD(g[0],{day:"numeric",month:"short"})})}
 return out.map((b,i)=>Object.assign(b,{label:i%3===0?b.label:""}));
}
/* gráfico de línea del tiempo de pantalla con referencias */
function screenChart(days){
 const B=buckets(days),vals=B.map(b=>{const v=b.days.filter(d=>d!==today()||b.days.length>1).map(d=>S.screen[d]).filter(x=>x!=null);return v.length?v.reduce((a,c)=>a+c,0)/v.length:null});
 const base=baseline(),lim=toxLimit(),known=vals.filter(v=>v!=null);
 if(!known.length)return'<p class="muted">Todavía no cargaste tiempo de pantalla en este período.</p>';
 const W=340,H=170,L=34,Rr=8,T=10,Bt=24,mx=Math.ceil(Math.max(...known,base||0,lim)/60)*60||60;
 const x=i=>L+(B.length===1?(W-L-Rr)/2:i*(W-L-Rr)/(B.length-1)),y=v=>T+(H-T-Bt)*(1-v/mx);
 let grid="";for(let h=0;h<=mx;h+=mx>360?120:60){grid+=`<line x1="${L}" x2="${W-Rr}" y1="${y(h)}" y2="${y(h)}" stroke="var(--line)" stroke-width="1"/><text x="${L-6}" y="${y(h)+4}" text-anchor="end">${h/60} h</text>`}
 let ref="";
 if(base)ref+=`<line x1="${L}" x2="${W-Rr}" y1="${y(base)}" y2="${y(base)}" stroke="var(--muted)" stroke-width="1.5" stroke-dasharray="4 4"/><text x="${W-Rr}" y="${y(base)-5}" text-anchor="end">antes de PROKI</text>`;
 ref+=`<line x1="${L}" x2="${W-Rr}" y1="${y(lim)}" y2="${y(lim)}" stroke="var(--coral)" stroke-width="1.5" stroke-dasharray="2 4"/><text x="${L+4}" y="${y(lim)-5}">límite del pez</text>`;
 let path="",area="",pen=false,first=null,last=null;
 vals.forEach((v,i)=>{if(v==null){pen=false;return}path+=(pen?"L":"M")+x(i).toFixed(1)+" "+y(v).toFixed(1);pen=true;if(first==null)first=i;last=i});
 area=`M${x(first)} ${y(0)} `+vals.map((v,i)=>v==null?"":`L${x(i).toFixed(1)} ${y(v).toFixed(1)}`).join("")+` L${x(last)} ${y(0)}Z`;
 const lab=B.map((b,i)=>b.label?`<text x="${x(i)}" y="${H-6}" text-anchor="middle">${esc(b.label)}</text>`:"").join("");
 const hits=vals.map((v,i)=>v==null?"":`<circle cx="${x(i)}" cy="${y(v)}" r="${B.length>20?3:4}" fill="var(--teal2)" stroke="var(--surface)" stroke-width="2"/><rect x="${x(i)-(W-L)/B.length/2}" y="${T}" width="${(W-L)/B.length}" height="${H-T-Bt}" fill="transparent" data-tip="${esc(B[i].name)}: ${hm(v)}${B[i].days.length>1?" por día":""}"/>`).join("");
 return`<svg class="lchart" viewBox="0 0 ${W} ${H}" role="img" aria-label="Evolución del tiempo de pantalla">${grid}${ref}<path d="${area}" fill="var(--teal)" opacity=".18"/><path d="${path}" fill="none" stroke="var(--teal2)" stroke-width="2" stroke-linejoin="round" stroke-linecap="round"/>${hits}</svg>`;
}
function barsChart(days){
 const B=buckets(days),v=B.map(b=>b.days.reduce((s,d)=>s+logsOn(d).filter(l=>!["descanso","recreacion","trabajo"].includes(l.cat)).reduce((a,l)=>a+l.min,0),0)),mx=Math.max(...v,1);
 return`<div class="spark" style="gap:${B.length>14?2:6}px">${v.map((m,i)=>`<div style="height:${Math.max(2,m/mx*100)}%" data-tip="${esc(B[i].name)}: ${hm(m)}">${B[i].label?`<span>${esc(B[i].label)}</span>`:""}</div>`).join("")}</div><div style="height:22px"></div>`;
}
function heatmap(days){
 const vals=days.map(d=>logsOn(d).filter(l=>!["descanso","recreacion","trabajo"].includes(l.cat)).reduce((a,l)=>a+l.min,0));
 const steps=["var(--line)","#C8DFDB","#76BDCD","#59A5B2","#2F7380"];
 const lvl=m=>m<=0?0:m<30?1:m<60?2:m<120?3:4;
 const pre=(dow(days[0])+6)%7;let h="";for(let i=0;i<pre;i++)h+='<i class="f"></i>';
 days.forEach((d,i)=>{const r=S.rest[d]==="rest"&&!vals[i];h+=`<i class="${r?"r":""}" style="${r?"":"background:"+steps[lvl(vals[i])]}" data-tip="${esc(fmtD(d,{weekday:"short",day:"numeric",month:"short"}))}: ${r?"descanso":vals[i]?hm(vals[i]):"sin registro"}"></i>`});
 return`<div class="heat" style="grid-template-columns:repeat(${Math.ceil((days.length+pre)/7)},minmax(0,26px))">${h}</div>
 <div class="heatleg"><span>Menos</span>${steps.map(c=>`<i style="background:${c}"></i>`).join("")}<span>Más</span><span style="margin-left:10px"><i style="box-shadow:inset 0 0 0 1.5px var(--teal2)"></i> Descanso</span></div>`;
}
function vProgress(){
 const t=today(),days=[...Array(range)].map((_,i)=>addD(t,-(range-1-i)));
 const prev=[...Array(range)].map((_,i)=>addD(t,-(2*range-1-i)));
 const prod=l=>!["descanso","recreacion","trabajo"].includes(l.cat);
 const sumL=ds=>S.logs.filter(l=>ds.includes(l.date)&&prod(l)).reduce((s,l)=>s+l.min,0);
 const L=S.logs.filter(l=>days.includes(l.date)),total=sumL(days),totalPrev=sumL(prev);
 const byCat={};L.forEach(l=>byCat[l.cat]=(byCat[l.cat]||0)+l.min);
 const pByCat={};days.forEach(d=>actsOn(d).forEach(a=>pByCat[a.cat]=(pByCat[a.cat]||0)+tm(a.end)-tm(a.start)));
 const cats=[...new Set(Object.keys(byCat).concat(Object.keys(pByCat)))].filter(c=>c!=="examen");
 const rec=days.reduce((s,d)=>s+recovered(d),0);
 const avgScr=ds=>{const v=ds.map(d=>S.screen[d]).filter(x=>x!=null);return v.length?v.reduce((a,c)=>a+c,0)/v.length:null};
 const sNow=avgScr(days),sPrev=avgScr(prev);
 const booms=toxS().booms.filter(x=>days.includes(x.date)).length,boomsPrev=toxS().booms.filter(x=>prev.includes(x.date)).length;
 const sk=streak();
 const hasPrev=prev.some(d=>S.screen[d]!=null||logsOn(d).length);
 const pct=(a,b)=>hasPrev&&b?Math.round((a-b)/b*100):null;
 const dTot=pct(total,totalPrev),dScr=sNow!=null&&sPrev!=null?pct(sNow,sPrev):null;
 const studyMin=S.logs.filter(l=>l.cat==="estudio").reduce((s,l)=>s+l.min,0),allRec=Object.keys(S.screen).reduce((s,d)=>s+recovered(d),0);
 const best=S.exams.flatMap(e=>e.scores).some(s=>s.ok/s.n>=.8);
 const BG=[["Primer paso","Registraste tu primera actividad",S.logs.length>0,"footprints"],["Tres al hilo","3 días seguidos con avance",bestStreak()>=3,"flame"],["Una semana","7 días seguidos con avance",bestStreak()>=7,"calendar-check"],["Diez horas","10 h de estudio registradas",studyMin>=600,"book-open-text"],["Manos a la obra","Cargaste tu primer examen",S.exams.length>0,"graduation-cap"],["Lo tenés","80% o más en un cuestionario",best,"star"],["5 horas recuperadas","Menos pantalla que antes",allRec>=300,"trending-up"],["Hábito propio","Un objetivo pasó a ser rutina",S.achieved.length>0,"sprout"],["Saber frenar","Marcaste un día de descanso",Object.values(S.rest).includes("rest"),"bed"]];
 const catTot=Object.entries(byCat).sort((a,b)=>b[1]-a[1]),catSum=catTot.reduce((s,[,m])=>s+m,0)||1;
 const moods=["Con energía","Bien","Cansado/a","Me costó"],mc=moods.map(m=>L.filter(l=>l.animo===m).length),mcs=mc.reduce((a,c)=>a+c,0);
 const half=Math.floor(range/2),moodGood=ds=>{const x=S.logs.filter(l=>ds.includes(l.date)&&l.animo);return x.length?x.filter(l=>l.animo==="Con energía"||l.animo==="Bien").length/x.length:null};
 const mg1=moodGood(days.slice(0,half)),mg2=moodGood(days.slice(half));
 const scores=S.exams.flatMap(e=>e.scores.map(s=>Object.assign({ex:e.name},s))).filter(s=>s.date>=days[0]).sort((a,b)=>a.date.localeCompare(b.date));
 const label=range===7?"la semana anterior":range===30?"el mes anterior":"los 3 meses anteriores";
 const dl=(v,good)=>v==null||!isFinite(v)?"":`<span class="delta">${v>0?"+":""}${v}%</span>`;
 // resumen escrito
 let story=[];
 if(sNow!=null&&base0())story.push(`En promedio usaste el celu ${hm(sNow)} por día, ${sNow<baseline()?hm(baseline()-sNow)+" menos que antes de empezar":"más o menos lo mismo que antes"}.`);
 if(dScr!=null&&dScr<0)story.push(`Bajó un ${Math.abs(dScr)}% respecto de ${label}.`);
 if(totalPrev&&total>totalPrev)story.push(`Le dedicaste más tiempo a lo que te importa que en ${label}.`);
 if(hasPrev&&booms<boomsPrev)story.push(`${fishName()} explotó ${booms} ${booms===1?"vez":"veces"}, contra ${boomsPrev} en ${label}.`);
 if(!hasPrev&&range>=30){const h1=toxS().booms.filter(x=>days.slice(0,half).includes(x.date)).length,h2=toxS().booms.filter(x=>days.slice(half).includes(x.date)).length;if(h2<h1)story.push(`${fishName()} explotó ${h1} veces en la primera mitad y ${h2} en la segunda.`)}
 if(!story.length)story.push("Cuando cargues más días, acá vas a ver cómo cambia todo con el tiempo.");
 function base0(){return !!baseline()}
 app.innerHTML=`${head("Mi progreso")}
 <div class="chips mt">${RANGES.map(([r,l])=>`<button class="chip iconbtn" data-r="${r}" aria-pressed="${range===r}" style="gap:6px">${ic({7:"calendar-days",30:"calendar-range",90:"chart-column"}[r],16)}${l}</button>`).join("")}</div>
 <div class="card hl mt"><div class="row" style="flex-wrap:nowrap;gap:14px;align-items:center"><div style="flex:0 0 auto">${fishImg(booms<boomsPrev||dScr<0?"happy":"normal",70)}</div><p style="font-weight:500">${esc(story.join(" "))}</p>${say(story.join(" "))}</div></div>
 <div class="stat mt"><div class="card">${icb("sprout","#5E9E88",36,"round")}<b class="mt">${hmc(total)}</b><span class="small muted">en lo que te importa ${dl(dTot)}</span></div><div class="card">${icb("smartphone","#7B63A8",36,"round")}<b class="mt">${sNow!=null?hm(Math.round(sNow)):"—"}</b><span class="small muted">pantalla por día ${dl(dScr)}</span></div><div class="card">${icb("trending-up","#2F7380",36,"round")}<b class="mt">${hmc(rec)}</b><span class="small muted">recuperadas</span></div></div>
 <p class="note">${hasPrev?`Los porcentajes comparan con ${label}. `:""}“Lo que te importa” suma estudio, deporte, lectura, proyectos y lo personal; trabajo y descanso van aparte.</p>

 <div class="sec">${shead("smartphone","Tiempo en pantalla","#7B63A8")}<div class="card"><p class="small muted">${range===90?"Promedio diario por semana":"Por día"} · tocá un punto para ver el valor</p>${screenChart(days)}
  <div class="legend"><span><i style="background:var(--teal2)"></i>Tu uso</span><span><i style="background:var(--muted)"></i>Antes de PROKI</span><span><i style="background:var(--coral)"></i>Límite del pez</span></div></div></div>

 <div class="sec">${shead("flame","Constancia","#E0A030")}<div class="card"><p class="small muted">Cada cuadradito es un día. Cuanto más oscuro, más tiempo en lo que te importa.</p>${heatmap(days)}
  <div class="row mt" style="gap:14px"><span class="small"><b>${sk}</b> días de racha</span><span class="small"><b>${bestStreak()}</b> de récord</span><span class="small"><b>${days.filter(d=>S.rest[d]==="rest").length}</b> días de descanso</span></div></div></div>

 <div class="sec">${shead("chart-column",range===90?"Tiempo por semana":"Tiempo por día","#59A5B2")}<div class="card">${barsChart(days)}</div></div>

 <div class="sec">${shead("fish","Tu pez en este período","#7B63A8")}<div class="card"><div class="row" style="flex-wrap:nowrap;gap:14px">${fishImg(booms>boomsPrev?"inflated":"flat",64)}<div><p class="big" style="font-size:36px">${booms}</p><p class="small muted">${booms===1?"explosión":"explosiones"}${hasPrev?` · ${boomsPrev} en ${label}`:""}</p></div></div>
  ${range>=30?`<div class="spark" style="height:56px;gap:${range===90?4:2}px">${buckets(days).map(b=>{const n=toxS().booms.filter(x=>b.days.includes(x.date)).length;return`<div style="height:${n?Math.max(18,n/Math.max(1,...buckets(days).map(bb=>toxS().booms.filter(x=>bb.days.includes(x.date)).length))*100):3}%;background:${n?"#7B63A8":"var(--line)"}" data-tip="${esc(b.name)}: ${n} ${n===1?"explosión":"explosiones"}"></div>`}).join("")}</div>`:""}</div></div>

 <div class="sec">${shead("palette","En qué usaste tu tiempo","#59A5B2")}<div class="card">${catTot.length?`<div class="stackbar">${catTot.map(([c,m])=>`<span style="width:${m/catSum*100}%;background:${catC(c)}" data-tip="${catL(c)}: ${hm(m)} (${Math.round(m/catSum*100)}%)"></span>`).join("")}</div>
  <div class="catleg">${catTot.map(([c,m])=>`<span><i style="background:${catC(c)}"></i>${catL(c)} · ${hm(m)}</span>`).join("")}</div>`:'<p class="muted">Sin registros en este período.</p>'}</div></div>

 <div class="sec">${shead("calendar-check","Planificado vs. realizado","#2F7380")}<div class="card">${cats.length?cats.map(c=>{const p=pByCat[c]||0,r=byCat[c]||0,m=Math.max(p,r,1);return`<div class="hbar"><span>${catL(c)}</span><div class="tr"><span class="p" style="width:${p/m*100}%"></span><span class="r" style="width:${r/m*100}%;background:${catC(c)}"></span></div></div><p class="small muted" style="margin-left:106px">${hm(p)} · ${hm(r)}${p?` · ${Math.round(r/p*100)}%`:""}</p>`}).join("")+`<div class="legend"><span><i style="background:var(--line)"></i>Planificado</span><span><i style="background:var(--sage)"></i>Realizado</span></div>`:'<p class="muted">Sin datos todavía en este período.</p>'}</div></div>

 <div class="sec">${shead("smile","Cómo te sentiste","#E0A030")}<div class="card">${mcs?moods.map((m,i)=>`<div class="moodrow"><span>${m}</span><div class="tr"><i style="width:${mc[i]/mcs*100}%"></i></div><span class="small muted">${Math.round(mc[i]/mcs*100)}%</span></div>`).join("")+(mg1!=null&&mg2!=null&&range>7?`<p class="small mt">${mg2>mg1?`En la segunda mitad del período te sentiste mejor más seguido (${Math.round(mg2*100)}% contra ${Math.round(mg1*100)}%).`:`Hubo días pesados, y está bien. Lo importante es que seguiste.`}</p>`:""):'<p class="muted">Cuando termines una actividad y cuentes cómo te sentiste, aparece acá.</p>'}</div></div>

 <div class="sec">${shead("sprout","Hábitos","#5E9E88")}<div class="card">${S.goals.map(g=>{const ds=days.filter(d=>d>=g.inicio),dd=ds.filter(d=>(g.log[d]||[]).length).length;return`<div class="item"><div style="width:40px;flex:0 0 40px">${sprout(gDays(g))}</div><div class="grow"><p style="font-weight:600">${esc(g.titulo)}</p><p class="small muted">${dd} de ${ds.length} días con avance${g.inicio>days[0]?` · desde el ${esc(fmtD(g.inicio,{day:"numeric",month:"short"}))}`:""}</p><div class="progress mt"><i style="width:${ds.length?dd/ds.length*100:0}%"></i></div></div></div>`}).join("")||'<p class="muted">Sin objetivos activos.</p>'}
 ${S.achieved.map(a=>`<div class="item"><div style="width:40px;flex:0 0 40px">${sprout(14)}</div><div class="grow"><p style="font-weight:600">${esc(a.titulo)}</p><p class="small muted">Ya es parte de tu rutina desde el ${esc(fmtD(a.fin,{day:"numeric",month:"short"}))}</p></div></div>`).join("")}</div></div>

 ${scores.length?`<div class="sec">${shead("list-checks","Cuestionarios","#E9785F")}<div class="card">${scores.map(s=>`<div class="hbar"><span class="small">${esc(fmtD(s.date,{day:"numeric",month:"short"}))}${s.sim?" · sim.":""}</span><div class="tr"><span class="r" style="top:6px;width:${s.ok/s.n*100}%;background:var(--teal2)"></span></div></div><p class="small muted" style="margin-left:106px">${esc(s.ex)} · ${s.ok}/${s.n}</p>`).join("")}</div></div>`:""}

 <div class="sec">${shead("award","Logros","#E0A030")}<div class="badges">${BG.map(([n,d,on,ii],i)=>`<div class="badge pop ${on?"":"off"}" style="--i:${i};text-align:center">${icb(ii,on?"#E0A030":"#8C9A90",52,"round"+(on?" solid":""))}<b class="mt">${n}</b><span class="small muted">${d}</span></div>`).join("")}</div></div>
 ${!S.demo&&S.logs.length<10?`<div class="card lil mt2"><p>¿Querés ver cómo se ven estos gráficos con meses de uso?</p><button class="btn sm mt" id="demo2">Ver demo con 3 meses de datos</button></div>`:""}`;
 $$("[data-r]").forEach(b=>b.onclick=()=>{range=+b.dataset.r;render()});
 if($("#demo2"))$("#demo2").onclick=enterDemo;
 tipInit();
}


/* ============ PERFIL ============ */
function vProfile(){
 const v=S.iv,p=S.profile||{};const apps=[...new Set(v.apps.concat(Object.keys(S.limits)))];
 app.innerHTML=`${head("Perfil")}
 <div class="card"><div class="row" style="flex-wrap:nowrap;gap:14px"><div id="fprev" class="fishbob">${fishImg(mood()[0],84)}</div><div style="flex:1;min-width:0"><h3>${esc(v.nombre||"Sin nombre")}</h3><p class="muted small mt">${esc(p.resumen||"")}</p></div>${say((p.resumen||"")+" "+(p.horario||""))}</div>
  ${p.horario?`<div class="row mt" style="flex-wrap:nowrap;gap:10px">${icb("clock","#2F7380",36,"round")}<p class="small">${esc(p.horario)}</p></div>`:""}</div>

 <div class="sec">${shead("type","Lectura fácil","#2F7380")}<div class="card">
  <button class="toggle" id="easyT" role="switch" aria-checked="${!!S.easy}">${icb("type","#2F7380",44,"round")}<div><b>Texto más grande y espaciado</b><p class="small muted">Más aire entre letras, palabras y líneas</p></div><span class="sw"></span></button>
  <div class="row mt" style="flex-wrap:nowrap;gap:14px;padding-top:10px;border-top:1px solid var(--line)">${icb("volume-2","#2F7380",44,"round")}<p class="small" style="flex:1">Tocá el parlante en cualquier pantalla para escuchar el texto.</p>${say("Así suena PROKI leyendo en voz alta.","Probar")}</div></div></div>

 <div class="sec">${shead("fish","Tu pez globo","#7B63A8")}<div class="card"><label class="f" for="fName" style="margin-top:0">Nombre</label><input type="text" id="fName" maxlength="20" value="${esc(fishName())}">
 <div class="row mt">${HUES.map(([l,h])=>`<button class="swatch" data-h="${h}" aria-label="${l}" aria-pressed="${fishHue()===h}"><img class="px" src="${FISH.normal.src}" alt="" style="filter:hue-rotate(${h}deg)"></button>`).join("")}</div>
 <div class="row mt" style="flex-wrap:nowrap;gap:12px;border-top:1px solid var(--line);padding-top:12px">${fishImg("inflated",56)}<div style="flex:1"><b class="iconbtn" style="gap:6px">${ic("zap",16)}Explota a los</b><div class="row mt" style="flex-wrap:nowrap"><input type="number" id="toxLim" min="10" max="900" step="5" value="${toxLimit()}" style="max-width:110px" aria-label="Límite diario en minutos"><span class="small muted">min por día</span></div></div></div></div></div>

 <div class="sec">${shead("smartphone","Meta por app","#7B63A8")}<div class="card">${apps.map(a=>`<div class="item" style="align-items:center">${icb(optI(a),"#7B63A8",40,"round")}<div class="grow"><p style="font-weight:600">${esc(a)}</p></div><input type="number" min="0" max="600" step="5" value="${S.limits[a]??60}" data-l="${esc(a)}" style="width:84px" aria-label="Minutos por día para ${esc(a)}"><span class="small muted">min</span></div>`).join("")||'<p class="muted">Agregá apps en la entrevista para definir tus metas.</p>'}</div></div>

 <div class="sec">${shead("newspaper","Me interesa","#4F8FB8")}<div class="optgrid sm">${Q[9].o.map(o=>optTile(o,v.temas.includes(o),"data-t","#4F8FB8")).join("")}</div></div>
 <div class="sec">${shead("message-circle-heart","Me motiva","#E0A030")}<div class="optgrid sm">${Q[10].o.map(o=>optTile(o,v.motivacion.includes(o),"data-m","#E0A030")).join("")}</div></div>

 <div class="sec">${shead("settings","Más","#8C9A90")}<div class="tiles">
  <button class="tile" id="redo">${icb("refresh-ccw","#59A5B2")}<div><b>Rehacer</b><span class="val">la entrevista</span></div></button>
  <button class="tile" id="ci">${icb("message-circle-heart","#2F7380")}<div><b>Repaso</b><span class="val">¿cómo venís?</span></div></button>
  ${S.demo?`<button class="tile" data-exitdemo>${icb("log-out","#E9785F")}<div><b>Salir</b><span class="val">del modo demo</span></div></button>`:`<button class="tile" id="demo">${icb("eye","#7B63A8")}<div><b>Demo</b><span class="val">3 meses de datos</span></div></button>`}
  <button class="tile" id="reset">${icb("trash-2","#C9625B")}<div><b>Borrar</b><span class="val">empezar de cero</span></div></button>
 </div><p class="small muted mt iconbtn" style="gap:6px">${ic(cloud==="cloud"?"upload":"smartphone",15)}${cloud==="cloud"?"Guardado en tu cuenta":"Guardado en este dispositivo"}</p></div>`;
 fishCustom(()=>{$("#fprev").innerHTML=fishImg(mood()[0],84)});
 $("#easyT").onclick=()=>{S.easy=!S.easy;save();render();toast(S.easy?"Lectura fácil activada.":"Lectura fácil desactivada.")};
 $$("[data-t]").forEach(c=>c.onclick=()=>{const a=v.temas,o=c.dataset.t,i=a.indexOf(o);i>=0?a.splice(i,1):a.push(o);save();render()});
 $$("[data-m]").forEach(c=>c.onclick=()=>{const a=v.motivacion,o=c.dataset.m,i=a.indexOf(o);i>=0?a.splice(i,1):a.push(o);save();render()});
 $("#toxLim").onchange=e=>{S.toxLimit=Math.max(10,+e.target.value||120);save();toast("Límite del pez guardado.")};
 $$("[data-l]").forEach(i=>i.onchange=()=>{S.limits[i.dataset.l]=Math.max(0,+i.value||0);save();toast("Meta guardada.")});
 $("#redo").onclick=()=>{S.phase="interview";S.qi=0;save();render()};$("#ci").onclick=checkin;if($("#demo"))$("#demo").onclick=enterDemo;
 $("#reset").onclick=async()=>{if(!confirm("¿Seguro? Se borra todo: perfil, calendario, exámenes, materiales y progreso."))return;for(const id of Object.keys(MATS))await delMat(id);S=blank();save();tab="inicio";render()};
}

render();
})();
</script>
</body>
</html>

</body></html>
