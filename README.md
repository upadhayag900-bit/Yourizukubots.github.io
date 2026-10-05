# Yourizukubots.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Terms & Conditions — Isukobit</title>
<meta name="description" content="Terms and Conditions for using Isukobit Telegram File Store Bot.">
<style>
:root{
  --bg:#0a0e1a;
  --bg2:#0f1526;
  --card:#131b32;
  --border:#1f2a4d;
  --text:#e8ecf8;
  --muted:#93a0c2;
  --accent:#4f7cff;
  --accent2:#8b5cf6;
  --gradient:linear-gradient(135deg,#4f7cff,#8b5cf6);
}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{
  font-family:'Segoe UI',system-ui,-apple-system,sans-serif;
  background:var(--bg);
  color:var(--text);
  line-height:1.7;
  overflow-x:hidden;
}
/* ─── Animated background glow ─── */
body::before{
  content:'';position:fixed;top:-200px;left:-200px;width:600px;height:600px;
  background:radial-gradient(circle,rgba(79,124,255,.15),transparent 70%);
  pointer-events:none;z-index:0;
}
body::after{
  content:'';position:fixed;bottom:-200px;right:-200px;width:600px;height:600px;
  background:radial-gradient(circle,rgba(139,92,246,.12),transparent 70%);
  pointer-events:none;z-index:0;
}
/* ─── Scroll progress bar ─── */
#progress{
  position:fixed;top:0;left:0;height:3px;width:0%;
  background:var(--gradient);z-index:1000;
  transition:width .1s linear;
}
/* ─── Header ─── */
header{
  position:sticky;top:0;z-index:100;
  background:rgba(10,14,26,.85);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
}
.nav{
  max-width:1100px;margin:0 auto;padding:16px 24px;
  display:flex;align-items:center;justify-content:space-between;
}
.logo{
  font-size:1.3rem;font-weight:800;letter-spacing:.5px;
  background:var(--gradient);
  -webkit-background-clip:text;background-clip:text;
  -webkit-text-fill-color:transparent;
}
.logo span{-webkit-text-fill-color:var(--text);font-weight:400}
.nav a.tg{
  display:inline-flex;align-items:center;gap:8px;
  background:var(--gradient);color:#fff;text-decoration:none;
  padding:9px 18px;border-radius:50px;font-size:.9rem;font-weight:600;
  transition:transform .2s,box-shadow .2s;
}
.nav a.tg:hover{transform:translateY(-2px);box-shadow:0 8px 24px rgba(79,124,255,.4)}
/* ─── Hero ─── */
.hero{
  position:relative;z-index:1;
  max-width:1100px;margin:0 auto;
  padding:80px 24px 50px;text-align:center;
}
.hero .badge{
  display:inline-block;padding:6px 16px;border-radius:50px;
  background:rgba(79,124,255,.1);border:1px solid rgba(79,124,255,.3);
  color:var(--accent);font-size:.8rem;font-weight:600;
  letter-spacing:1px;text-transform:uppercase;
  margin-bottom:20px;animation:fadeDown .6s ease both;
}
.hero h1{
  font-size:clamp(2rem,5vw,3.2rem);font-weight:800;
  line-height:1.2;margin-bottom:16px;
  animation:fadeDown .6s .1s ease both;
}
.hero h1 em{
  font-style:normal;
  background:var(--gradient);
  -webkit-background-clip:text;background-clip:text;
  -webkit-text-fill-color:transparent;
}
.hero p{
  color:var(--muted);max-width:640px;margin:0 auto 28px;
  font-size:1.05rem;animation:fadeDown .6s .2s ease both;
}
.hero .updated{
  display:inline-block;color:var(--muted);font-size:.85rem;
  padding:8px 18px;border:1px solid var(--border);border-radius:50px;
  animation:fadeDown .6s .3s ease both;
}
@keyframes fadeDown{
  from{opacity:0;transform:translateY(-16px)}
  to{opacity:1;transform:translateY(0)}
}
/* ─── Layout ─── */
.wrap{
  position:relative;z-index:1;
  max-width:1100px;margin:0 auto;padding:20px 24px 80px;
  display:grid;grid-template-columns:260px 1fr;gap:32px;
}
/* ─── Sidebar TOC ─── */
.toc{
  position:sticky;top:90px;align-self:start;
  background:var(--card);border:1px solid var(--border);
  border-radius:16px;padding:20px;height:fit-content;
}
.toc h4{
  font-size:.75rem;text-transform:uppercase;letter-spacing:1.5px;
  color:var(--muted);margin-bottom:14px;
}
.toc a{
  display:block;color:var(--muted);text-decoration:none;
  font-size:.88rem;padding:7px 12px;border-radius:8px;
  border-left:2px solid transparent;
  transition:all .2s;
}
.toc a:hover,.toc a.active{
  color:var(--text);background:rgba(79,124,255,.08);
  border-left-color:var(--accent);
}
/* ─── Content cards ─── */
.card{
  background:var(--card);border:1px solid var(--border);
  border-radius:18px;padding:32px;margin-bottom:24px;
  opacity:0;transform:translateY(28px);
  transition:opacity .6s ease,transform .6s ease;
}
.card.visible{opacity:1;transform:translateY(0)}
.card:hover{border-color:rgba(79,124,255,.35)}
.card .num{
  display:inline-flex;align-items:center;justify-content:center;
  width:38px;height:38px;border-radius:10px;
  background:var(--gradient);color:#fff;
  font-weight:700;font-size:.95rem;margin-bottom:16px;
}
.card h2{font-size:1.35rem;margin-bottom:14px;font-weight:700}
.card h3{font-size:1.05rem;margin:20px 0 8px;color:var(--accent)}
.card p{color:#c3cbe4;margin-bottom:12px;font-size:.97rem}
.card ul,.card ol{margin:0 0 14px 22px;color:#c3cbe4}
.card li{margin-bottom:8px;font-size:.95rem}
.card li::marker{color:var(--accent)}
.card strong{color:var(--text)}
.hl{
  background:rgba(79,124,255,.12);border:1px solid rgba(79,124,255,.25);
  border-left:3px solid var(--accent);
  padding:14px 18px;border-radius:10px;
  color:#c3cbe4;font-size:.92rem;margin:14px 0;
}
.hl b{color:var(--accent)}
/* ─── Footer ─── */
footer{
  position:relative;z-index:1;
  border-top:1px solid var(--border);
  background:var(--bg2);
  padding:40px 24px;text-align:center;
}
footer .logo{font-size:1.1rem;margin-bottom:8px}
footer p{color:var(--muted);font-size:.85rem}
footer a{color:var(--accent);text-decoration:none}
/* ─── Back to top ─── */
#topBtn{
  position:fixed;bottom:24px;right:24px;z-index:500;
  width:46px;height:46px;border-radius:50%;
  background:var(--gradient);color:#fff;border:none;
  font-size:1.2rem;cursor:pointer;
  opacity:0;pointer-events:none;
  transition:opacity .3s,transform .3s;
  box-shadow:0 8px 24px rgba(79,124,255,.4);
}
#topBtn.show{opacity:1;pointer-events:auto}
#topBtn:hover{transform:translateY(-3px)}
/* ─── Mobile ─── */
@media(max-width:860px){
  .wrap{grid-template-columns:1fr}
  .toc{display:none}
  .card{padding:24px}
  .hero{padding:56px 20px 36px}
}
</style>
</head>
<body>

<div id="progress"></div>

<header>
  <div class="nav">
    <div class="logo">Isuko<span>bit</span></div>
    <a class="tg" href="https://t.me/yourisukubot" target="_blank">Open Bot</a>
  </div>
</header>

<section class="hero">
  <div class="badge">Legal</div>
  <h1>Terms &amp; <em>Conditions</em></h1>
  <p>Please read these terms carefully before using Isukobit. By using the bot, you agree to be bound by these terms.</p>
  <div class="updated">🔄 Last updated: October 2026</div>
</section>

<div class="wrap">

  <!-- Sidebar -->
  <nav class="toc" id="toc">
    <h4>📑 On this page</h4>
    <a href="#s1">1. Acceptance</a>
    <a href="#s2">2. About the Service</a>
    <a href="#s3">3. Eligibility</a>
    <a href="#s4">4. Acceptable Use</a>
    <a href="#s5">5. Your Content</a>
    <a href="#s6">6. Copyright</a>
    <a href="#s7">7. Privacy</a>
    <a href="#s8">8. Service Availability</a>
    <a href="#s9">9. Limitation of Liability</a>
    <a href="#s10">10. Termination</a>
    <a href="#s11">11. Changes to Terms</a>
    <a href="#s12">12. Contact</a>
  </nav>

  <!-- Content -->
  <main>

    <div class="card" id="s1">
      <div class="num">1</div>
      <h2>Acceptance of Terms</h2>
      <p>By accessing or using <strong>Isukobit</strong> ("the Service", "the Bot"), operated on Telegram as <strong>@yourisukubot</strong>, you agree to be bound by these Terms &amp; Conditions and our Privacy practices described herein.</p>
      <p>If you do not agree with any part of these terms, please discontinue use of the Service immediately.</p>
    </div>

    <div class="card" id="s2">
      <div class="num">2</div>
      <h2>About the Service</h2>
      <p>Isukobit is a Telegram-based utility bot that allows users to:</p>
      <ul>
        <li>Upload and organize personal files through Telegram</li>
        <li>Generate unique shareable links and codes for uploaded content</li>
        <li>Search, manage, and retrieve their own files</li>
        <li>Create grouped batches of multiple files under a single link</li>
      </ul>
      <div class="hl">⚡ The Service is provided <b>"as is"</b> and <b>"as available"</b> on the Telegram platform, and is subject to Telegram's own Terms of Service.</div>
    </div>

    <div class="card" id="s3">
      <div class="num">3</div>
      <h2>Eligibility</h2>
      <p>To use the Service you must:</p>
      <ul>
        <li>Have a valid Telegram account in good standing</li>
        <li>Be at least 13 years of age (or the minimum age of digital consent in your country)</li>
        <li>Provide accurate information when interacting with the Bot</li>
      </ul>
      <p>By using the Service, you represent that you meet these requirements.</p>
    </div>

    <div class="card" id="s4">
      <div class="num">4</div>
      <h2>Acceptable Use Policy</h2>
      <p>You agree to use the Service only for lawful purposes. You must <strong>not</strong> upload, share, or distribute:</p>
      <ul>
        <li>Content that is illegal under any applicable local, national, or international law</li>
        <li>Content that infringes the intellectual property rights of others</li>
        <li>Malware, viruses, spyware, or any harmful or destructive code</li>
        <li>Harassing, defamatory, abusive, or hateful content</li>
        <li>Adult or sexually explicit material, especially involving minors — <strong>zero tolerance</strong></li>
        <li>Spam, scams, phishing material, or misleading content</li>
        <li>Personal data of third parties without their consent</li>
      </ul>
      <div class="hl">🚫 Any violation may result in <b>immediate and permanent ban</b> from the Service without prior notice, and where required, reporting to relevant authorities.</div>
    </div>

    <div class="card" id="s5">
      <div class="num">5</div>
      <h2>Your Content &amp; Responsibility</h2>
      <p>You retain full ownership and responsibility for any content you upload or share through the Service.</p>
      <ul>
        <li>You are solely responsible for the legality, reliability, and appropriateness of your content</li>
        <li>Share links and file codes you generate should be treated like passwords — anyone with the link may access the content, subject to the Service's access controls</li>
        <li>Do not upload content you do not have the right to distribute</li>
      </ul>
      <p>We do not pre-screen user content, but reserve the right to remove any content and suspend any account that violates these terms.</p>
    </div>

    <div class="card" id="s6">
      <div class="num">6</div>
      <h2>Copyright &amp; DMCA</h2>
      <p>We respect the intellectual property rights of others and expect users to do the same.</p>
      <p>If you believe that content shared through the Service infringes your copyright, please contact us with:</p>
      <ol>
        <li>Identification of the copyrighted work claimed to be infringed</li>
        <li>The specific link or file code in question</li>
        <li>Your contact information</li>
        <li>A good-faith statement that the use is unauthorized</li>
      </ol>
      <p>Valid complaints will be processed promptly, and infringing content will be removed.</p>
    </div>

    <div class="card" id="s7">
      <div class="num">7</div>
      <h2>Privacy</h2>
      <p>The Service operates entirely within Telegram. To function, the Bot only requires the basic information Telegram provides to any bot you interact with — such as your Telegram user ID, name, and username.</p>
      <ul>
        <li>No registration beyond Telegram is required</li>
        <li>No email, phone number, or payment details are collected by the Bot</li>
        <li>Your files remain accessible only through your generated codes/links unless you choose to share them</li>
      </ul>
      <div class="hl">🔒 We never sell, rent, or trade user information to third parties.</div>
    </div>

    <div class="card" id="s8">
      <div class="num">8</div>
      <h2>Service Availability</h2>
      <p>We strive to keep the Service available 24/7, but we do not guarantee uninterrupted or error-free operation.</p>
      <ul>
        <li>The Service may be temporarily unavailable for maintenance, updates, or reasons beyond our control</li>
        <li>Since the Service depends on Telegram, any Telegram outage or policy change may affect availability</li>
        <li>Features may be added, modified, or removed at any time</li>
      </ul>
    </div>

    <div class="card" id="s9">
      <div class="num">9</div>
      <h2>Limitation of Liability</h2>
      <p>To the maximum extent permitted by law:</p>
      <ul>
        <li>The Service is provided <strong>without warranties of any kind</strong>, express or implied</li>
        <li>We are not liable for any loss of data, content, or access to your files</li>
        <li>We are not responsible for the actions, content, or conduct of any user of the Service</li>
        <li>We are not liable for any indirect, incidental, or consequential damages arising from your use of the Service</li>
        <li>You use the Service entirely at your own risk</li>
      </ul>
    </div>

    <div class="card" id="s10">
      <div class="num">10</div>
      <h2>Termination</h2>
      <p>We reserve the right to suspend or permanently terminate access to the Service for any user who:</p>
      <ul>
        <li>Violates these Terms &amp; Conditions</li>
        <li>Abuses, exploits, or attempts to disrupt the Service</li>
        <li>Uses the Service for fraudulent or illegal activities</li>
      </ul>
      <p>You may stop using the Service at any time. Termination does not limit any other rights or remedies available to us under law.</p>
    </div>

    <div class="card" id="s11">
      <div class="num">11</div>
      <h2>Changes to These Terms</h2>
      <p>We may update these Terms &amp; Conditions from time to time. When we do, we will update the "Last updated" date on this page.</p>
      <p>Continued use of the Service after changes are posted constitutes acceptance of the revised terms. We encourage you to review this page periodically.</p>
    </div>

    <div class="card" id="s12">
      <div class="num">12</div>
      <h2>Contact Us</h2>
      <p>If you have any questions, concerns, or requests regarding these Terms &amp; Conditions, you can reach us through the bot:</p>
      <div class="hl">🤖 Telegram Bot: <b>@yourisukubot</b><br>📢 Updates Channel: mention your channel here<br>📞 Support: mention your support username here</div>
      <p>We aim to respond to all inquiries as quickly as possible.</p>
    </div>

  </main>
</div>

<footer>
  <div class="logo">Isuko<span>bit</span></div>
  <p>© 2026 Isukobit — All rights reserved. · <a href="#">Terms &amp; Conditions</a></p>
</footer>

<button id="topBtn" onclick="window.scrollTo({top:0,behavior:'smooth'})" title="Back to top">↑</button>

<script>
// Scroll progress bar
window.addEventListener('scroll',()=>{
  const h=document.documentElement;
  const pct=(h.scrollTop)/(h.scrollHeight-h.clientHeight)*100;
  document.getElementById('progress').style.width=pct+'%';
  document.getElementById('topBtn').classList.toggle('show',h.scrollTop>400);
});

// Reveal cards on scroll
const obs=new IntersectionObserver((entries)=>{
  entries.forEach(e=>{if(e.isIntersecting)e.target.classList.add('visible')});
},{threshold:.12});
document.querySelectorAll('.card').forEach(c=>obs.observe(c));

// TOC active link highlight
const links=document.querySelectorAll('.toc a');
const secs=document.querySelectorAll('.card');
window.addEventListener('scroll',()=>{
  let cur='';
  secs.forEach(s=>{if(scrollY>=s.offsetTop-140)cur=s.id});
  links.forEach(l=>l.classList.toggle('active',l.getAttribute('href')==='#'+cur));
});
</script>

</body>
</html>
