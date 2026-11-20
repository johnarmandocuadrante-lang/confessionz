<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#cfe6ff">
<title>a little message 💙</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Gaegu:wght@400;700&display=swap">
<style>
:root{
  --sky1:#e6f3ff; --sky2:#bcdcff; --cloud:rgba(255,255,255,.75); --ink:#2b4a7d; --soft:#5f86bd;
  --back:#6fa8ee; --side:#a9cdf8; --side2:#8dbbf3; --bottom:#9ac4f6; --flap1:#c4defc; --flap2:#a6cbf7;
  --liner:#e3f0ff; --liner-dot:#c3dcfa; --paper:#fcfeff; --line:#d9e8fb; --margin:#f6b8c8;
  --seal1:#5b9bff; --seal2:#2f6fe0; --tape:rgba(168,205,255,.75); --overlay:rgba(34,64,112,.45);
  --shadow:rgba(36,82,150,.28);
  box-sizing:border-box; padding-top:env(safe-area-inset-top,0px); padding-bottom:env(safe-area-inset-bottom,0px);
  color-scheme:light;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --sky1:#1b2f5e; --sky2:#0d1a3a; --cloud:rgba(140,180,255,.12); --ink:#e6f0ff; --soft:#9db9e8;
    --back:#4a82d6; --side:#7aaae8; --side2:#5f93df; --bottom:#6c9fe6; --flap1:#9fc3f3; --flap2:#82aeec;
    --liner:#d6e7ff; --liner-dot:#b3d0f6; --overlay:rgba(3,10,28,.62); --shadow:rgba(0,0,0,.5); color-scheme:dark;
  }
}
:root[data-theme="dark"]{
  --sky1:#1b2f5e; --sky2:#0d1a3a; --cloud:rgba(140,180,255,.12); --ink:#e6f0ff; --soft:#9db9e8;
  --back:#4a82d6; --side:#7aaae8; --side2:#5f93df; --bottom:#6c9fe6; --flap1:#9fc3f3; --flap2:#82aeec;
  --liner:#d6e7ff; --liner-dot:#b3d0f6; --overlay:rgba(3,10,28,.62); --shadow:rgba(0,0,0,.5); color-scheme:dark;
}
*{box-sizing:border-box}
html,body{height:100%;margin:0}
body{
  background:linear-gradient(180deg,var(--sky1),var(--sky2));color:var(--ink);overflow:hidden;
  font-family:"Gaegu","Segoe Print","Comic Sans MS",cursive,sans-serif;
  display:flex;align-items:center;justify-content:center;
}
.bg{position:fixed;inset:0;pointer-events:none;overflow:hidden}
.cloud{position:absolute;width:220px;height:70px;border-radius:70px;background:var(--cloud);will-change:transform;animation:drift 38s linear infinite}
.cloud::before,.cloud::after{content:"";position:absolute;background:inherit;border-radius:50%}
.cloud::before{width:90px;height:90px;left:30px;top:-40px}
.cloud::after{width:70px;height:70px;left:100px;top:-26px}
.c1{top:12%;left:-260px}.c2{top:68%;left:-260px;animation-duration:52s;animation-delay:-20s;scale:.8}.c3{top:36%;left:-260px;animation-duration:64s;animation-delay:-44s;scale:.6}
@keyframes drift{to{transform:translateX(calc(100vw + 560px))}}
.star{position:absolute;width:14px;height:14px;opacity:0;animation:twinkle 3.4s ease-in-out infinite;fill:#fff}
@keyframes twinkle{0%,100%{opacity:0;transform:scale(.4) rotate(0)}50%{opacity:.95;transform:scale(1) rotate(25deg)}}

.stage{position:relative;display:flex;flex-direction:column;align-items:center;gap:1.4rem;padding:1rem}
.bubble{
  position:relative;margin:0;padding:.35rem 1.2rem;border-radius:999px;background:#fff;color:var(--seal2);
  font-size:1.35rem;font-weight:700;box-shadow:0 6px 14px var(--shadow);animation:bob 1.6s ease-in-out infinite;
  transition:opacity .35s,transform .35s;
}
.bubble::before{content:"";position:absolute;top:-6px;left:50%;width:12px;height:12px;background:#fff;transform:translateX(-50%) rotate(45deg);border-radius:3px}
@keyframes bob{50%{transform:translateY(-6px)}}
.opened .bubble{opacity:0;transform:scale(.8);animation:none}

.float{position:relative;margin-top:1.2rem;animation:float 4s ease-in-out infinite;will-change:transform}
.opened .float{animation:none}
@keyframes float{0%,100%{transform:translateY(-9px) rotate(-1.6deg)}50%{transform:translateY(9px) rotate(1.6deg)}}
.ground{
  width:min(60vw,240px);height:18px;border-radius:50%;background:var(--shadow);filter:blur(8px);
  margin-top:.8rem;animation:gshadow 4s ease-in-out infinite;will-change:transform,opacity;
}
.opened .ground{animation:none;opacity:.6;transition:opacity .6s}
@keyframes gshadow{0%,100%{transform:scale(1.05);opacity:.7}50%{transform:scale(.85);opacity:.4}}

.env{
  position:relative;display:block;width:min(80vw,340px,calc(44vh * 1.5));aspect-ratio:3/2;perspective:900px;
  background:none;border:0;padding:0;font:inherit;cursor:pointer;-webkit-tap-highlight-color:transparent;
}
.env:disabled{cursor:default}
.env:focus-visible{outline:3px solid var(--seal2);outline-offset:10px;border-radius:14px}
.back{position:absolute;inset:0;border-radius:10px;background:linear-gradient(180deg,var(--back),var(--side2));box-shadow:0 10px 24px var(--shadow)}
.paper{
  position:absolute;left:7%;right:7%;top:5%;bottom:5%;z-index:2;border-radius:5px;
  background:linear-gradient(var(--paper),var(--paper)) padding-box;
  box-shadow:0 1px 4px rgba(30,70,130,.25);
  background-image:repeating-linear-gradient(transparent 0 15px,var(--line) 15px 16px);background-color:var(--paper);
  transition:transform 1s cubic-bezier(.25,.9,.3,1) .6s;will-change:transform;
}
.front{position:absolute;inset:0;z-index:3;pointer-events:none}
.front i{position:absolute;inset:0;border-radius:10px}
.fl{background:linear-gradient(90deg,var(--side2),var(--side));clip-path:polygon(0 0,52% 56%,0 100%)}
.fr{background:linear-gradient(270deg,var(--side2),var(--side));clip-path:polygon(100% 0,48% 56%,100% 100%)}
.fb{background:linear-gradient(0deg,var(--bottom),var(--side));clip-path:polygon(0 100%,50% 48%,100% 100%)}
.stamp{position:absolute;right:6%;bottom:9%;z-index:3;width:11%;aspect-ratio:1;background:#fff;border-radius:3px;display:grid;place-items:center;transform:rotate(6deg);
  box-shadow:0 0 0 2px #fff,0 0 0 4px var(--side)}
.stamp svg,.seal svg{width:60%;height:60%;fill:var(--seal1)}
.flap{position:absolute;top:0;left:0;right:0;height:56%;z-index:4;transform-style:preserve-3d;transform-origin:50% 0;
  transition:transform .8s cubic-bezier(.5,0,.2,1),z-index 0s .38s;will-change:transform}
.flap i{position:absolute;inset:0;clip-path:polygon(0 0,100% 0,50% 100%);backface-visibility:hidden;-webkit-backface-visibility:hidden}
.flap .out{background:linear-gradient(180deg,var(--flap1),var(--flap2))}
.flap .in{background:radial-gradient(var(--liner-dot) 1.5px,transparent 2px) 0 0/10px 10px,var(--liner);transform:rotateX(180deg)}
.seal{
  position:absolute;left:50%;top:56%;z-index:5;width:15%;aspect-ratio:1;border-radius:50%;display:grid;place-items:center;
  background:radial-gradient(circle at 35% 30%,var(--seal1),var(--seal2));transform:translate(-50%,-50%);
  box-shadow:0 3px 6px rgba(20,50,120,.45),inset 0 -2px 3px rgba(0,30,100,.35),inset 0 2px 3px rgba(255,255,255,.4);
  transition:opacity .3s,transform .4s cubic-bezier(.5,-.6,.6,1.4);
}
.seal svg{fill:#dcebff;width:52%;height:52%}
.opened .flap{transform:rotateX(180deg);z-index:1}
.opened .paper{transform:translateY(-64%) rotate(-1.5deg)}
.opened .seal{opacity:0;transform:translate(-50%,-50%) scale(.2)}
.opened .env{pointer-events:none}

.burst{position:absolute;left:50%;top:56%;width:0;height:0;z-index:6;pointer-events:none}
.burst svg{position:absolute;left:-9px;top:-9px;width:18px;height:18px;fill:var(--seal1);opacity:0;animation:pop .95s cubic-bezier(.2,.8,.3,1) forwards}
@keyframes pop{0%{opacity:1;transform:translate(0,0) scale(.3)}100%{opacity:0;transform:translate(var(--dx),var(--dy)) scale(var(--s)) rotate(var(--r))}}

.sheet{
  position:fixed;inset:0;z-index:10;display:flex;align-items:center;justify-content:center;
  padding:max(1rem,env(safe-area-inset-top,0px)) 1rem max(1rem,env(safe-area-inset-bottom,0px));
  background:var(--overlay);backdrop-filter:blur(3px);-webkit-backdrop-filter:blur(3px);
  opacity:0;visibility:hidden;transition:opacity .6s,visibility 0s .6s;
}
.sheet.show{opacity:1;visibility:visible;transition:opacity .6s}
.card{
  position:relative;width:min(100%,540px);max-height:100%;overflow-y:auto;overscroll-behavior:contain;border-radius:8px;color:#2b4a7d;
  padding:2.2rem 1.5rem 1.4rem 3.1rem;background-color:var(--paper);
  background-image:linear-gradient(90deg,transparent 2.3rem,var(--margin) 2.3rem,var(--margin) calc(2.3rem + 1.5px),transparent calc(2.3rem + 1.5px)),
    repeating-linear-gradient(transparent 0 33px,var(--line) 33px 34px);
  background-attachment:local;
  box-shadow:0 24px 60px rgba(10,30,80,.4);
  transform:translateY(70px) scale(.8) rotate(-3deg);opacity:0;
  transition:transform .9s cubic-bezier(.2,.9,.25,1.08),opacity .5s;will-change:transform;
  scrollbar-width:thin;scrollbar-color:#a9cdf8 transparent;
}
.sheet.show .card{transform:none;opacity:1}
.card p{margin:0 0 34px;font-size:1.4rem;line-height:34px;font-weight:400}
.card p.to{font-weight:700;font-size:1.55rem}
.card .sign{margin-bottom:0;text-align:right;font-weight:700}
.sheet.show .card p{animation:rise .7s cubic-bezier(.2,.8,.3,1) both;animation-delay:calc(.55s + var(--i) * .16s)}
@keyframes rise{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:none}}
.close{
  display:block;margin:1.4rem auto 0;font:inherit;font-size:1.3rem;font-weight:700;color:#fff;
  background:linear-gradient(180deg,var(--seal1),var(--seal2));border:0;border-radius:999px;padding:.45rem 1.6rem;cursor:pointer;
  box-shadow:0 5px 12px rgba(40,90,190,.4);transition:transform .2s;
}
.close:active{transform:scale(.95)}
.close:focus-visible{outline:3px solid #a9cdf8;outline-offset:3px}

@media (hover:hover){.env:not(:disabled):hover .flap{transform:rotateX(-14deg)}.opened .env .flap{transform:rotateX(180deg)}}
@media (prefers-reduced-motion:reduce){
  .cloud,.star,.bubble,.float,.ground{animation:none}
  .paper,.flap,.card,.seal,.sheet{transition-duration:.01s;transition-delay:0s}
  .sheet.show .card p{animation:none}
  .burst{display:none}
}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute" aria-hidden="true">
  <symbol id="h" viewBox="0 0 24 24"><path d="M12 21C5 16.500 2 12.500 2 8.800 2 6.200 4 4.500 6.300 4.500c1.900 0 3.600 1 5.700 3.200 2.100-2.200 3.800-3.200 5.700-3.200C20 4.500 22 6.200 22 8.800c0 3.700-3 7.700-10 12.200z"/></symbol>
  <symbol id="s" viewBox="0 0 24 24"><path d="M12 0c.8 6.500 5.500 11.200 12 12-6.500.8-11.200 5.500-12 12-.8-6.500-5.500-11.200-12-12C6.500 11.200 11.200 6.500 12 0z"/></symbol>
</svg>

<div class="bg" aria-hidden="true">
  <div class="cloud c1"></div><div class="cloud c2"></div><div class="cloud c3"></div>
  <svg class="star" style="left:12%;top:20%"><use href="#s"/></svg>
  <svg class="star" style="left:82%;top:14%;animation-delay:-1.2s"><use href="#s"/></svg>
  <svg class="star" style="left:90%;top:56%;animation-delay:-2.2s"><use href="#s"/></svg>
  <svg class="star" style="left:7%;top:62%;animation-delay:-.6s"><use href="#s"/></svg>
  <svg class="star" style="left:70%;top:84%;animation-delay:-1.8s"><use href="#s"/></svg>
  <svg class="star" style="left:30%;top:88%;animation-delay:-2.8s"><use href="#s"/></svg>
</div>

<main class="stage" id="stage">
  <div class="float">
    <button class="env" id="env" aria-label="Open the envelope">
      <span class="back"></span>
      <span class="paper"></span>
      <span class="front"><i class="fl"></i><i class="fr"></i><i class="fb"></i></span>
      <span class="stamp"><svg><use href="#h"/></svg></span>
      <span class="flap"><i class="out"></i><i class="in"></i></span>
      <span class="seal"><svg><use href="#h"/></svg></span>
      <span class="burst" id="burst"></span>
    </button>
  </div>
  <div class="ground" aria-hidden="true"></div>
  <p class="bubble">tap me!</p>
</main>

<div class="sheet" id="sheet" role="dialog" aria-modal="true" aria-label="A message" aria-hidden="true">
  <div class="card" id="card">
    <p class="to" style="--i:0">hiii dap, good evening!</p>
    <p style="--i:1">i hope this message won’t catch you off guard, especially since hindi pa talaga tayo nakakapag-usap nang personal, pero i just wanted to speak from my heart lang sana hihi.</p>
    <p style="--i:2">ever since pinakilala ka sa’kin ni ja, you really caught my attention na talaga. hindi ’to over-exaggerating or love bombing ha, it’s just something genuine that i’ve been quietly holding onto for a while now.</p>
    <p style="--i:3">actually at first, akala ko happy crush lang siya, like “cute at pogi kasi siya and ang galing niya sa arts” kind of thing, pero as time passed, i started realizing na it’s deeper than that. you seem so kind, shy, and gentle, tapos seeing the passion and soul you put into your art made me admire you even more.</p>
    <p style="--i:4">that’s why i decided to gather the courage to send this to you. not to force anything or put any pressure on you, pero because i truly believe na someone like you deserves to know that your presence and your craft are genuinely appreciated from afar. sobrang gaan lang sa feeling na nasabi ko na ’to kwkwkwkw.</p>
    <p style="--i:5">i’m not expecting a reply, nor am i asking for anything in return. masaya na ako just knowing na nakarating ’to sa’yo. ’yun lang naman kwkwkwkw i sound so corny pero bahala na, ikaw naman na ’yan eh</p>
    <p class="sign" style="--i:6">thank you so much and take care always! 🤍</p>
    <button class="close" id="close" style="animation:rise .7s 2s both">fold it back</button>
  </div>
</div>

<script>
(function(){
  var stage=document.getElementById('stage'), env=document.getElementById('env'),
      sheet=document.getElementById('sheet'), card=document.getElementById('card'),
      burst=document.getElementById('burst'), closeBtn=document.getElementById('close'), t;
  var reduce=window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  function hearts(){
    if(reduce) return;
    var ns='http://www.w3.org/2000/svg';
    for(var i=0;i<14;i++){
      var a=(Math.PI*2*i)/14+Math.random()*.4, d=70+Math.random()*80;
      var s=document.createElementNS(ns,'svg'), u=document.createElementNS(ns,'use');
      u.setAttribute('href','#h'); s.appendChild(u);
      s.style.setProperty('--dx',Math.cos(a)*d+'px');
      s.style.setProperty('--dy',(Math.sin(a)*d-40)+'px');
      s.style.setProperty('--s',(.7+Math.random()*.9).toFixed(2));
      s.style.setProperty('--r',(Math.random()*60-30)+'deg');
      s.style.animationDelay=(Math.random()*.15)+'s';
      burst.appendChild(s);
    }
    setTimeout(function(){burst.textContent='';},1400);
  }
  function open(){
    if(stage.classList.contains('opened')) return;
    stage.classList.add('opened'); env.disabled=true; hearts();
    t=setTimeout(function(){
      sheet.classList.add('show'); sheet.setAttribute('aria-hidden','false');
      card.scrollTop=0; closeBtn.focus({preventScroll:true});
    },reduce?50:1900);
  }
  function close(){
    clearTimeout(t);
    sheet.classList.remove('show'); sheet.setAttribute('aria-hidden','true');
    setTimeout(function(){ stage.classList.remove('opened'); env.disabled=false; env.focus({preventScroll:true}); },reduce?50:650);
  }
  env.addEventListener('click',open);
  closeBtn.addEventListener('click',close);
  document.addEventListener('keydown',function(e){ if(e.key==='Escape'&&sheet.classList.contains('show')) close(); });
})();
</script>
</body>
</html>
