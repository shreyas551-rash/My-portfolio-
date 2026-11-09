<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Shreyas Rashatwar – Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  color-scheme:dark;
  --bg:#13161b; --surface:#1b1f26; --line:#2b313b; --text:#e9e7e2; --muted:#9aa3b0; --accent:#8cbcf0;
  --head:"Bricolage Grotesque","Helvetica Neue",Arial,sans-serif;
  --body:"IBM Plex Sans","Helvetica Neue",Arial,sans-serif;
  box-sizing:border-box;
  padding-top:env(safe-area-inset-top,0px);
  padding-bottom:env(safe-area-inset-bottom,0px);
}
*,*::before,*::after{box-sizing:inherit}
#bg{position:fixed;inset:0;width:100%;height:100%;z-index:-1;pointer-events:none;background:radial-gradient(60% 50% at 85% 5%,rgba(140,188,240,.14),transparent 70%),radial-gradient(50% 45% at 5% 95%,rgba(120,140,230,.12),transparent 70%)}
html{scroll-behavior:smooth;scroll-padding-top:72px}
body{margin:0;background:var(--bg);color:var(--text);font:400 1.0625rem/1.65 var(--body);-webkit-font-smoothing:antialiased}
a{color:inherit}
a:focus-visible,button:focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:4px}
.wrap{width:min(100% - 2.5rem,960px);margin-inline:auto}
h1,h2,h3{font-family:var(--head);line-height:1.1;margin:0;letter-spacing:-.02em}

/* nav */
header{position:sticky;top:env(safe-area-inset-top,0px);z-index:5;background:rgba(19,22,27,.88);backdrop-filter:blur(8px);border-bottom:1px solid var(--line)}
nav{display:flex;justify-content:space-between;align-items:center;height:60px}
.logo{font-family:var(--head);font-weight:700;text-decoration:none}
nav ul{display:flex;gap:1.5rem;list-style:none;margin:0;padding:0}
nav ul a{color:var(--muted);text-decoration:none;font-size:.95rem}
nav ul a{position:relative;padding:.3rem 0;transition:color .25s}
nav ul a::after{content:"";position:absolute;left:0;right:0;bottom:-2px;height:2px;background:var(--accent);border-radius:2px;transform:scaleX(0);transform-origin:left;transition:transform .35s ease}
nav ul a:hover{color:var(--text)}
nav ul a.active{color:var(--text)}
nav ul a.active::after{transform:scaleX(1)}
@media (prefers-reduced-motion:reduce){nav ul a,nav ul a::after{transition:none}html{scroll-behavior:auto}}

/* hero: blueprint grid */
.hero{padding:7rem 0 6rem;background-image:linear-gradient(var(--line) 1px,transparent 1px),linear-gradient(90deg,var(--line) 1px,transparent 1px);background-size:48px 48px;background-position:-1px -1px;-webkit-mask-image:linear-gradient(#000 55%,transparent);mask-image:linear-gradient(#000 55%,transparent)}
.hero-in{background:none}
.hero h1{font-size:clamp(2.8rem,9vw,6rem);font-weight:700;max-width:12ch}
.hero p{font-size:clamp(1.1rem,2.4vw,1.35rem);color:var(--muted);max-width:34ch;margin:1.5rem 0 2.2rem}
.btns{display:flex;gap:.8rem;flex-wrap:wrap}
.btn{display:inline-block;padding:.75rem 1.4rem;border-radius:999px;text-decoration:none;font-weight:500;border:1px solid var(--line)}
.btn.primary{background:var(--accent);color:#0e1218;border-color:var(--accent)}
.btn:hover{border-color:var(--accent)}

section{padding:5rem 0;border-top:1px solid var(--line)}
section h2{font-size:clamp(1.8rem,4vw,2.4rem);margin-bottom:2rem}

/* about */
.about{display:grid;grid-template-columns:1.6fr 1fr;gap:3rem}
.about p{margin:0 0 1rem;max-width:60ch;color:#cfd3d9}
.facts{margin:0;padding:0;list-style:none;border-left:2px solid var(--accent);padding-left:1.2rem;align-self:start}
.facts li{padding:.45rem 0;color:var(--muted)}
.facts b{display:block;color:var(--text);font-weight:500}

/* projects */
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:1.5rem}
.card{background:var(--surface);border:1px solid var(--line);border-radius:14px;overflow:hidden;display:flex;flex-direction:column}
.card svg{display:block;width:100%;height:auto;background:#161a20;border-bottom:1px solid var(--line)}
.card div{padding:1.3rem;display:flex;flex-direction:column;gap:.6rem;flex:1}
.card h3{font-size:1.25rem}
.card p{margin:0;color:var(--muted);font-size:.98rem}
.card a{margin-top:auto;color:var(--accent);text-decoration:none;font-weight:500;padding-top:.4rem}
.card a:hover{text-decoration:underline}

/* skills */
.skills{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:2rem}
.skills h3{font-size:1.05rem;margin-bottom:.8rem}
.tags{display:flex;flex-wrap:wrap;gap:.5rem}
.tags span{border:1px solid var(--line);border-radius:999px;padding:.3rem .8rem;font-size:.92rem;color:#cfd3d9}

/* contact */
.contact p{color:var(--muted);max-width:46ch;margin:0 0 1.5rem}
.mail{font-family:var(--head);font-size:clamp(1.4rem,5vw,2.4rem);font-weight:700;text-decoration:none;border-bottom:2px solid var(--accent);overflow-wrap:anywhere}
.phone{margin-top:1.2rem;font-size:1.15rem}
.phone a{text-decoration:none;color:var(--text)}
.phone a:hover{color:var(--accent)}
.social{display:flex;gap:1.5rem;margin-top:2rem;flex-wrap:wrap}
.social a{color:var(--muted);text-decoration:none}
.social a:hover{color:var(--text)}
footer{padding:2rem 0;border-top:1px solid var(--line);color:var(--muted);font-size:.9rem}

@media (max-width:700px){
  .about{grid-template-columns:1fr;gap:2rem}
  nav ul{gap:1rem}
  .hero{padding:4.5rem 0 4rem}
  section{padding:3.5rem 0}
}
@media (max-width:420px){nav ul li:nth-child(n+4){display:none}}
</style>
</head>
<body>
<canvas id="bg" aria-hidden="true"></canvas>
<header>
  <nav class="wrap" aria-label="Main">
    <a class="logo" href="#top">Shreyas Rashatwar</a>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>

<main id="top">
  <div class="hero">
    <div class="wrap hero-in">
      <h1>Shreyas Rashatwar</h1>
      <p>Engineer who turns ideas into things that work.</p>
      <div class="btns">
        <a class="btn primary" href="#projects">See my work</a>
        <a class="btn" href="#contact">Get in touch</a>
      </div>
    </div>
  </div>

  <section id="about">
    <div class="wrap about">
      <div>
        <h2>About me</h2>
        <p>I’m an engineer who likes understanding how things work, then making them work better. I enjoy taking a problem from a rough sketch to a tested, finished result.</p>
        <p>Replace this paragraph with your story: where you study or work, what drives you, and the kind of problems you want to solve next.</p>
      </div>
      <ul class="facts">
        <li><b>Education</b>1st year, SB Jain Institute of Technology and Management</li>
        <li><b>Focus</b>Data Science</li>
        <li><b>Location</b>Nagpur</li>
      </ul>
    </div>
  </section>

  <section id="projects">
    <div class="wrap">
      <h2>Projects</h2>
      <div class="grid">
        <article class="card">
          <svg viewBox="0 0 320 180" role="img" aria-label="Gear illustration"><g fill="none" stroke="#8cbcf0" stroke-width="2" stroke-linejoin="round"><circle cx="125" cy="90" r="38"/><circle cx="125" cy="90" r="14"/><circle cx="215" cy="70" r="24"/><circle cx="215" cy="70" r="8"/><path d="M125 44v-12M125 136v12M79 90H67M171 90h12M92 57l-8-8M158 123l8 8M92 123l-8 8M158 57l8-8M215 40v-10M215 100v10M185 70h-10M245 70h10"/></g></svg>
          <div>
            <h3>Personal AI</h3>
            <p>My own AI assistant for everyday life. It understands plain-language commands, keeps my tasks organised, and talks back by voice.</p>
            <a href="https://claude.ai/artifact/4EUnQKbRGVaYZS9sUciYsA" target="_blank" rel="noopener" aria-label="View Personal AI project">View project</a>
          </div>
        </article>
        <article class="card">
          <svg viewBox="0 0 320 180" role="img" aria-label="Chart illustration"><g fill="none" stroke="#8cbcf0" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M40 30v120h250"/><path d="M60 120l55-35 50 20 60-60 50 25"/></g><g fill="#8cbcf0"><circle cx="60" cy="120" r="5"/><circle cx="115" cy="85" r="5"/><circle cx="165" cy="105" r="5"/><circle cx="225" cy="45" r="5"/><circle cx="275" cy="70" r="5"/></g></svg>
          <div>
            <h3>File analyser</h3>
            <p>Upload a file and get an AI analysis: a summary, key insights, problems, and answers to your own questions. Works with CSV, JSON, text, code, and images.</p>
            <a href="https://claude.ai/artifact/YKbu2SouiyBq3N2waaR7CM" target="_blank" rel="noopener" aria-label="View File analyser project">View project</a>
          </div>
        </article>
      </div>
    </div>
  </section>

  <section id="skills">
    <div class="wrap">
      <h2>Skills</h2>
      <div class="skills">
        <div>
          <h3>Engineering</h3>
          <div class="tags"><span>CAD</span><span>Prototyping</span><span>Systems design</span><span>Testing</span></div>
        </div>
        <div>
          <h3>Software &amp; tools</h3>
          <div class="tags"><span>Python</span><span>Web development</span><span>C/C++</span><span>Git</span></div>
        </div>
        <div>
          <h3>Working style</h3>
          <div class="tags"><span>Problem solving</span><span>Teamwork</span><span>Documentation</span></div>
        </div>
      </div>
    </div>
  </section>

  <section id="contact" class="contact">
    <div class="wrap">
      <h2>Contact</h2>
      <p>Open to internships, jobs, and projects. Send me a message and I’ll reply soon.</p>
      <a class="mail" href="mailto:shreyasrashatwar1@gmail.com">shreyasrashatwar1@gmail.com</a>
      <div class="phone"><a href="tel:+917588765984">+91 75887 65984</a></div>
      <div class="social">
        <a href="#" rel="noopener">LinkedIn</a>
        <a href="#" rel="noopener">GitHub</a>
        <a href="#" rel="noopener">Resume</a>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="wrap">© <span id="yr">2026</span> Shreyas Rashatwar</div>
</footer>
<script>
document.getElementById('yr').textContent=new Date().getFullYear();
(function(){
  var links=[].slice.call(document.querySelectorAll('nav ul a'));
  var secs=links.map(function(a){return document.querySelector(a.getAttribute('href'));});
  function update(){
    var y=window.scrollY+120,cur=-1;
    secs.forEach(function(s,i){if(s&&s.offsetTop<=y)cur=i;});
    if(window.innerHeight+window.scrollY>=document.documentElement.scrollHeight-4)cur=secs.length-1;
    links.forEach(function(a,i){
      var on=i===cur;
      a.classList.toggle('active',on);
      if(on)a.setAttribute('aria-current','true');else a.removeAttribute('aria-current');
    });
  }
  window.addEventListener('scroll',update,{passive:true});
  window.addEventListener('resize',update);
  update();
})();
</script>
<script>
(function(){
  var c=document.getElementById('bg'),x=c.getContext('2d');
  var reduce=window.matchMedia('(prefers-reduced-motion:reduce)').matches;
  var W,H,dpr,pts=[],mouse={x:-999,y:-999},raf;
  function size(){
    dpr=Math.min(window.devicePixelRatio||1,2);
    W=window.innerWidth;H=window.innerHeight;
    c.width=W*dpr;c.height=H*dpr;x.setTransform(dpr,0,0,dpr,0,0);
    var n=Math.min(80,Math.round(W*H/17000));
    pts=[];
    for(var i=0;i<n;i++)pts.push({x:Math.random()*W,y:Math.random()*H,vx:(Math.random()-.5)*.35,vy:(Math.random()-.5)*.35,r:1+Math.random()*1.6});
  }
  function draw(){
    x.clearRect(0,0,W,H);
    var L=130,i,j,p,q,dx,dy,d;
    for(i=0;i<pts.length;i++){
      p=pts[i];
      if(!reduce){
        p.x+=p.vx;p.y+=p.vy;
        if(p.x<0||p.x>W)p.vx*=-1;
        if(p.y<0||p.y>H)p.vy*=-1;
      }
      for(j=i+1;j<pts.length;j++){
        q=pts[j];dx=p.x-q.x;dy=p.y-q.y;d=Math.sqrt(dx*dx+dy*dy);
        if(d<L){x.strokeStyle='rgba(140,188,240,'+(0.22*(1-d/L)).toFixed(3)+')';x.lineWidth=1;x.beginPath();x.moveTo(p.x,p.y);x.lineTo(q.x,q.y);x.stroke();}
      }
      dx=p.x-mouse.x;dy=p.y-mouse.y;d=Math.sqrt(dx*dx+dy*dy);
      if(d<170){x.strokeStyle='rgba(140,188,240,'+(0.5*(1-d/170)).toFixed(3)+')';x.beginPath();x.moveTo(p.x,p.y);x.lineTo(mouse.x,mouse.y);x.stroke();}
      x.fillStyle='rgba(170,205,245,.65)';x.beginPath();x.arc(p.x,p.y,p.r,0,6.2832);x.fill();
    }
    if(!reduce)raf=requestAnimationFrame(draw);
  }
  window.addEventListener('mousemove',function(e){mouse.x=e.clientX;mouse.y=e.clientY;},{passive:true});
  window.addEventListener('touchmove',function(e){var t=e.touches[0];mouse.x=t.clientX;mouse.y=t.clientY;},{passive:true});
  window.addEventListener('resize',function(){size();if(reduce)draw();});
  document.addEventListener('visibilitychange',function(){
    if(reduce)return;
    if(document.hidden)cancelAnimationFrame(raf);else raf=requestAnimationFrame(draw);
  });
  size();draw();
})();
</script>
</body>
</html>
