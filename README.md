# MrrMonke.github.io
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Finding Meaning — Viktor Frankl Portfolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;1,300;1,400&family=Jost:wght@300;400&display=swap" rel="stylesheet">
<style>
  :root {
    --ink: #1c1814;
    --ink-soft: #3d3830;
    --ink-muted: #7a7268;
    --ink-faint: #b0a898;
    --page: #f6f1e9;
    --page-dark: #ede6d5;
    --accent: #8b4513;
    --accent-light: #f0dbc8;
    --border: rgba(80,65,45,0.15);
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--page);
    color: var(--ink);
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    line-height: 1.8;
    font-weight: 300;
  }
  nav {
    position: sticky; top: 0; z-index: 10;
    background: rgba(246,241,233,0.95);
    backdrop-filter: blur(6px);
    border-bottom: 0.5px solid var(--border);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 2.5rem; height: 52px;
  }
  .nav-title { font-style: italic; font-size: 15px; color: var(--ink-muted); }
  .nav-links { display: flex; gap: 1.75rem; list-style: none; }
  .nav-links a {
    font-family: 'Jost', sans-serif; font-size: 10px; font-weight: 400;
    letter-spacing: 0.13em; text-transform: uppercase;
    color: var(--ink-muted); text-decoration: none; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--accent); }
  .hero {
    text-align: center; padding: 5rem 2rem 4rem;
    border-bottom: 0.5px solid var(--border);
  }
  .hero-label {
    font-family: 'Jost', sans-serif; font-size: 10px; font-weight: 400;
    letter-spacing: 0.16em; text-transform: uppercase;
    color: var(--ink-faint); margin-bottom: 1.5rem;
  }
  .hero h1 { font-size: clamp(44px, 7vw, 80px); font-weight: 300; line-height: 1.1; margin-bottom: 1rem; }
  .hero h1 em { font-style: italic; color: var(--accent); }
  .hero-sub { font-size: 17px; font-style: italic; color: var(--ink-muted); max-width: 420px; margin: 0 auto; }
  .section { padding: 4rem 0; border-top: 0.5px solid var(--border); }
  .container { max-width: 720px; margin: 0 auto; padding: 0 2rem; }
  .section-label {
    font-family: 'Jost', sans-serif; font-size: 10px; font-weight: 400;
    letter-spacing: 0.14em; text-transform: uppercase;
    color: var(--ink-faint); margin-bottom: 0.75rem;
  }
  .section h2 { font-size: 30px; font-weight: 300; font-style: italic; margin-bottom: 1.75rem; color: var(--ink); }
  p.body { font-size: 18px; line-height: 1.85; color: var(--ink-soft); margin-bottom: 1.1rem; font-weight: 300; }
  .illustration { margin: 2rem 0; display: flex; justify-content: center; flex-direction: column; align-items: center; }
  .illus-caption {
    font-family: 'Jost', sans-serif; font-size: 11px; font-weight: 300;
    letter-spacing: 0.08em; color: var(--ink-faint); text-align: center; margin-top: 0.6rem;
  }
  .quote {
    margin: 2rem 0; padding: 1.75rem 2rem;
    border-left: 2px solid var(--accent); background: var(--accent-light);
  }
  .quote p { font-size: 20px; font-style: italic; line-height: 1.65; color: var(--ink); margin-bottom: 0.6rem; }
  .quote cite {
    font-family: 'Jost', sans-serif; font-size: 11px; font-weight: 300;
    letter-spacing: 0.07em; color: var(--ink-muted); font-style: normal;
  }
  .cards {
    display: grid; grid-template-columns: repeat(3, 1fr);
    gap: 1px; background: var(--border); border: 0.5px solid var(--border); margin: 1.5rem 0;
  }
  .card { background: var(--page); padding: 1.5rem 1.25rem; }
  .card-num {
    font-family: 'Jost', sans-serif; font-size: 10px; letter-spacing: 0.1em;
    text-transform: uppercase; color: var(--accent); margin-bottom: 0.5rem;
  }
  .card p { font-size: 16px; line-height: 1.6; color: var(--ink-soft); font-weight: 300; }
  .poem {
    background: var(--page-dark); border: 0.5px solid var(--border);
    padding: 3rem 2.5rem; margin: 1.5rem 0; text-align: center;
  }
  .poem-title { font-size: 22px; font-style: italic; font-weight: 300; margin-bottom: 2rem; color: var(--ink); }
  .poem-stanza { font-size: 17px; font-style: italic; line-height: 2; color: var(--ink-soft); margin-bottom: 1.5rem; }
  .poem-stanza:last-child { margin-bottom: 0; }
  .journal { background: var(--page-dark); border: 0.5px solid var(--border); padding: 2rem; margin-bottom: 1.25rem; }
  .journal h3 {
    font-family: 'Jost', sans-serif; font-size: 10px; font-weight: 400;
    letter-spacing: 0.12em; text-transform: uppercase; color: var(--ink-faint); margin-bottom: 0.75rem;
  }
  .journal .jq { font-style: italic; font-size: 17px; color: var(--accent); margin-bottom: 0.75rem; line-height: 1.5; }
  .journal p { font-size: 16px; line-height: 1.8; color: var(--ink-soft); font-weight: 300; }
  .refs { list-style: none; margin: 1rem 0; }
  .refs li {
    font-size: 16px; color: var(--ink-soft); line-height: 1.7;
    margin-bottom: 0.9rem; padding-left: 2rem; text-indent: -2rem; font-weight: 300;
  }
  footer { border-top: 0.5px solid var(--border); padding: 2.5rem 2rem; text-align: center; }
  footer p {
    font-family: 'Jost', sans-serif; font-size: 11px; font-weight: 300;
    letter-spacing: 0.08em; color: var(--ink-faint); margin-bottom: 0.3rem;
  }
  .fade { opacity: 0; transform: translateY(18px); transition: opacity 0.65s ease, transform 0.65s ease; }
  .fade.on { opacity: 1; transform: none; }
  @media (max-width: 580px) {
    .nav-links { display: none; }
    .cards { grid-template-columns: 1fr; }
    .poem { padding: 2rem 1.25rem; }
  }
</style>
</head>
<body>

<nav>
  <span class="nav-title">Finding Meaning — Frankl Portfolio</span>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#quotes">Quotes</a></li>
    <li><a href="#philosophy">Philosophy</a></li>
    <li><a href="#poem">Poem</a></li>
  </ul>
</nav>

<div class="hero">
  <p class="hero-label">HZT4U — Grade 12 Philosophy &nbsp;·&nbsp; Personal Meaning Portfolio</p>
  <h1>Finding <em>Meaning</em></h1>
  <p class="hero-sub">A personal exploration of Viktor Frankl's <em>Man's Search for Meaning</em></p>
</div>

<main>

  <section class="section" id="about">
    <div class="container">
      <h2 class="fade">Who Was Viktor Frankl?</h2>
      <div class="illustration fade">
        <svg width="200" height="250" viewBox="0 0 200 250" xmlns="http://www.w3.org/2000/svg">
          <rect width="200" height="250" fill="#e8e0d0" rx="3"/>
          <!-- Jacket -->
          <ellipse cx="100" cy="218" rx="65" ry="52" fill="#2a2420"/>
          <!-- Lapels -->
          <polygon points="100,168 82,185 82,220 100,205" fill="#3a3028"/>
          <polygon points="100,168 118,185 118,220 100,205" fill="#3a3028"/>
          <!-- Shirt -->
          <rect x="93" y="168" width="14" height="40" fill="#f0ebe0"/>
          <!-- Tie -->
          <polygon points="100,172 96,178 100,215 104,178" fill="#8b4513"/>
          <!-- Neck -->
          <rect x="89" y="155" width="22" height="18" fill="#c49a70" rx="4"/>
          <!-- Head -->
          <ellipse cx="100" cy="128" rx="36" ry="42" fill="#c49a70"/>
          <!-- Hair -->
          <ellipse cx="100" cy="89" rx="36" ry="16" fill="#2a2420"/>
          <rect x="64" y="89" width="72" height="10" fill="#2a2420"/>
          <!-- Side hair -->
          <ellipse cx="66" cy="110" rx="6" ry="14" fill="#2a2420"/>
          <ellipse cx="134" cy="110" rx="6" ry="14" fill="#2a2420"/>
          <!-- Ears -->
          <ellipse cx="65" cy="128" rx="6" ry="9" fill="#b8895e"/>
          <ellipse cx="135" cy="128" rx="6" ry="9" fill="#b8895e"/>
          <!-- Eyes -->
          <ellipse cx="85" cy="120" rx="6" ry="4.5" fill="white"/>
          <ellipse cx="115" cy="120" rx="6" ry="4.5" fill="white"/>
          <circle cx="86" cy="120" r="3.5" fill="#1a1410"/>
          <circle cx="116" cy="120" r="3.5" fill="#1a1410"/>
          <circle cx="87" cy="119" r="1" fill="white"/>
          <circle cx="117" cy="119" r="1" fill="white"/>
          <!-- Eyebrows -->
          <path d="M78,111 Q85,107 92,111" stroke="#2a2420" stroke-width="2" fill="none" stroke-linecap="round"/>
          <path d="M108,111 Q115,107 122,111" stroke="#2a2420" stroke-width="2" fill="none" stroke-linecap="round"/>
          <!-- Glasses frames -->
          <circle cx="85" cy="120" r="10" fill="none" stroke="#2a2420" stroke-width="1.8"/>
          <circle cx="115" cy="120" r="10" fill="none" stroke="#2a2420" stroke-width="1.8"/>
          <line x1="95" y1="120" x2="105" y2="120" stroke="#2a2420" stroke-width="1.8"/>
          <line x1="64" y1="117" x2="75" y2="119" stroke="#2a2420" stroke-width="1.8"/>
          <line x1="125" y1="119" x2="136" y2="117" stroke="#2a2420" stroke-width="1.8"/>
          <!-- Nose -->
          <path d="M100,127 Q96,136 91,140 Q100,143 109,140 Q104,136 100,127" fill="#b8895e"/>
          <!-- Wrinkle lines (age) -->
          <path d="M78,128 Q82,130 78,132" stroke="#a07850" stroke-width="0.8" fill="none"/>
          <path d="M122,128 Q118,130 122,132" stroke="#a07850" stroke-width="0.8" fill="none"/>
          <!-- Mouth -->
          <path d="M89,150 Q100,156 111,150" stroke="#8a5a38" stroke-width="1.8" fill="none" stroke-linecap="round"/>
        </svg>
        <p class="illus-caption">Viktor Frankl (1905–1997)</p>
      </div>
      <p class="body fade">Viktor Frankl was an Austrian psychiatrist and also a Holocaust survivor whose experiences in Nazi concentration camps gave one of the most important psychological foundation of the twentieth century. He called it <em>logotherapy</em>, which is the belief that the primary human drive is not pleasure or power, but the search for meaning.</p>
      <p class="body fade">His book, <em>Man's Search for Meaning</em>, combines a story of his time in the camps with an explanation of the theory he built from those years. It has sold over 16 million copies worldwide.</p>
    </div>
  </section>

  <section class="section" id="quotes">
    <div class="container">
      <h2 class="fade">Words That Stayed With Me</h2>
      <div class="quote fade">
        <p>Everything can be taken from a man but one thing: the last of the human freedoms — to choose one's attitude in any given set of circumstances.</p>
        <cite>— Viktor Frankl, Man's Search for Meaning</cite>
      </div>
      <p class="body fade">Frankl is saying that even when everything on the outside is stripped away, the inner freedom chooses how we respond cannot be touched. This connects to Kant's idea of autonomy, that human dignity comes from our ability to reason and choose, not from our circumstances.</p>
      <div class="quote fade" style="margin-top:2rem;">
        <p>He who have a 'why' to live, can bear with almost any 'how'.</p>
        <cite>— Viktor Frankl, Man's Search for Meaning</cite>
      </div>
      <p class="body fade">Prisoners who held onto a purpose, a loved one, a goal, even a belief, were far more likely to endure and survive. This challenges utilitarian ethics: that if pleasure is what drives us, why would anyone willingly suffer for meaning? Frankl's answer is that purpose outweighs comfort every time.</p>
    </div>
  </section>

  <section class="section" id="philosophy">
    <div class="container">
      <h2 class="fade">The Ideas Behind The Book</h2>
      <div class="illustration fade">
        <svg width="480" height="120" viewBox="0 0 480 120" xmlns="http://www.w3.org/2000/svg">
          <rect width="480" height="120" fill="#ddd5c0" rx="3"/>
          <!-- Sky -->
          <rect width="480" height="65" fill="#c8c0ae" opacity="0.6"/>
          <!-- Ground -->
          <rect y="80" width="480" height="40" fill="#b4a88a" opacity="0.7"/>
          <!-- Posts -->
          <rect x="30" y="18" width="7" height="78" fill="#4a3c2a" rx="1"/>
          <rect x="140" y="18" width="7" height="78" fill="#4a3c2a" rx="1"/>
          <rect x="250" y="18" width="7" height="78" fill="#4a3c2a" rx="1"/>
          <rect x="360" y="18" width="7" height="78" fill="#4a3c2a" rx="1"/>
          <rect x="443" y="18" width="7" height="78" fill="#4a3c2a" rx="1"/>
          <!-- Post tops (pointed) -->
          <polygon points="30,18 33,10 37,18" fill="#3a2e1e"/>
          <polygon points="140,18 143,10 147,18" fill="#3a2e1e"/>
          <polygon points="250,18 253,10 257,18" fill="#3a2e1e"/>
          <polygon points="360,18 363,10 367,18" fill="#3a2e1e"/>
          <polygon points="443,18 446,10 450,18" fill="#3a2e1e"/>
          <!-- Wire strands -->
          <line x1="30" y1="33" x2="450" y2="33" stroke="#2a2218" stroke-width="1.5"/>
          <line x1="30" y1="52" x2="450" y2="52" stroke="#2a2218" stroke-width="1.5"/>
          <line x1="30" y1="70" x2="450" y2="70" stroke="#2a2218" stroke-width="1.5"/>
          <!-- Barbs top wire -->
          <g stroke="#2a2218" stroke-width="1.3" stroke-linecap="round">
            <line x1="55" y1="29" x2="60" y2="37"/><line x1="55" y1="37" x2="60" y2="29"/>
            <line x1="80" y1="29" x2="85" y2="37"/><line x1="80" y1="37" x2="85" y2="29"/>
            <line x1="108" y1="29" x2="113" y2="37"/><line x1="108" y1="37" x2="113" y2="29"/>
            <line x1="162" y1="29" x2="167" y2="37"/><line x1="162" y1="37" x2="167" y2="29"/>
            <line x1="190" y1="29" x2="195" y2="37"/><line x1="190" y1="37" x2="195" y2="29"/>
            <line x1="218" y1="29" x2="223" y2="37"/><line x1="218" y1="37" x2="223" y2="29"/>
            <line x1="272" y1="29" x2="277" y2="37"/><line x1="272" y1="37" x2="277" y2="29"/>
            <line x1="300" y1="29" x2="305" y2="37"/><line x1="300" y1="37" x2="305" y2="29"/>
            <line x1="328" y1="29" x2="333" y2="37"/><line x1="328" y1="37" x2="333" y2="29"/>
            <line x1="382" y1="29" x2="387" y2="37"/><line x1="382" y1="37" x2="387" y2="29"/>
            <line x1="410" y1="29" x2="415" y2="37"/><line x1="410" y1="37" x2="415" y2="29"/>
            <line x1="432" y1="29" x2="437" y2="37"/><line x1="432" y1="37" x2="437" y2="29"/>
          </g>
          <!-- Barbs middle wire -->
          <g stroke="#2a2218" stroke-width="1.3" stroke-linecap="round">
            <line x1="60" y1="48" x2="65" y2="56"/><line x1="60" y1="56" x2="65" y2="48"/>
            <line x1="95" y1="48" x2="100" y2="56"/><line x1="95" y1="56" x2="100" y2="48"/>
            <line x1="120" y1="48" x2="125" y2="56"/><line x1="120" y1="56" x2="125" y2="48"/>
            <line x1="170" y1="48" x2="175" y2="56"/><line x1="170" y1="56" x2="175" y2="48"/>
            <line x1="205" y1="48" x2="210" y2="56"/><line x1="205" y1="56" x2="210" y2="48"/>
            <line x1="235" y1="48" x2="240" y2="56"/><line x1="235" y1="56" x2="240" y2="48"/>
            <line x1="280" y1="48" x2="285" y2="56"/><line x1="280" y1="56" x2="285" y2="48"/>
            <line x1="315" y1="48" x2="320" y2="56"/><line x1="315" y1="56" x2="320" y2="48"/>
            <line x1="345" y1="48" x2="350" y2="56"/><line x1="345" y1="56" x2="350" y2="48"/>
            <line x1="390" y1="48" x2="395" y2="56"/><line x1="390" y1="56" x2="395" y2="48"/>
            <line x1="425" y1="48" x2="430" y2="56"/><line x1="425" y1="56" x2="430" y2="48"/>
          </g>
        </svg>
        <p class="illus-caption">The Concentration Camps Where Frankl Developed His Theory of Meaning</p>
      </div>
      <div class="cards fade">
        <div class="card">
          <p class="card-num">Pillar one</p>
          <p>Life has meaning under all circumstances, even the most miserable.</p>
        </div>
        <div class="card">
          <p class="card-num">Pillar two</p>
          <p>The will to find meaning is our most fundamental motivation.</p>
        </div>
        <div class="card">
          <p class="card-num">Pillar three</p>
          <p>We are free to choose how we respond to unavoidable suffering.</p>
        </div>
      </div>
      <p class="body fade">Frankl's logotherapy looks forward rather than backwards, asking not what shaped us, but what we are living <em>for</em>. His philosophy also follows Kant, since both argue that what makes us human is our freedom to choose, and that this freedom survives even the worst conditions.</p>
    </div>
  </section>

  <section class="section" id="poem">
    <div class="container">
      <h2 class="fade">Original poem</h2>
      <div class="poem fade">
        <p class="poem-title">The Last Freedom</p>
        <div class="poem-stanza">
          They took everything he owned,<br>
          his name, his home, his family, his time,<br>
          they stripped away the life he knew,<br>
          and left him with nothing but his mind.
        </div>
        <div class="poem-stanza">
          But somewhere in the cold and the dark,<br>
          behind the hunger and the wire and the fear,<br>
          there was something they could never touch,<br>
          a choice that still lived in him, clear.
        </div>
        <div class="poem-stanza">
          He chose how he faced every morning.<br>
          He chose what he held onto when others let go.<br>
          Not happiness, he never promised that, <br>
          but meaning, which kept him whole.
        </div>
        <div class="poem-stanza">
          And I, who have so much more than he did,<br>
          who falls apart over things that don't matter,<br>
          I carry this with me now like a lesson:<br>
          it's not about the pain, it's about what you do after.
        </div>
      </div>
    </div>
  </section>

  <section class="section">
    <div class="container">
      <h2 class="fade">How My Understanding of Meaning Changed</h2>
      <p class="body fade">When I first started reading <em>Man's Search for Meaning</em>, I expected something heavy and cold, something like a historical document about events too extreme to feel personally important. What I did not expect was how it would directly speak to my own life, and how much it would change the way I think about a word I had always taken for granted.</p>
      <p class="body fade">Before this project, I thought of meaning as something passive, a feeling that came when things were going well. I related it with happiness. Frankl broke that down completely. He showed that meaning and happiness are not the same thing. How people in the camps suffered a lot and yet, for some of them, life held intense meaning. Many people today live in comfort and feel completely empty. That reality unsettled me.</p>
      <p class="body fade">What changed most was the idea of responsibility. Frankl does not offer meaning as a gift, but rather he presents it as a task. We are responsible for finding it in whatever situation we are given. That means I cannot wait for meaning to get here. I have to go toward it. That change, from meaning as something that happens to me, to something I am responsible for, is the most important thing this project gave me.</p>
      <p class="body fade">Writing the poem forced me to bring out what actually moved me about the book. It wasn't the philosophy in the abstract, but it was the image of a man who had lost basically everything, still choosing, each morning, how to react for the day. If he could find meaning there, I have no real excuse not to find it here.</p>
      <p class="body fade">I began this project thinking about meaning as a place, or a location. I finished it understanding it as a direction, something I align myself toward through the choices I make and the way I face difficulty. Frankl didn't make that sound easy. But he made it sound possible. And right now, that feels like enough.</p>
    </div>

</main>

<footer>
  <p>HZT4U — Grade 12 Philosophy &nbsp;·&nbsp; Option D: Personal Meaning Portfolio</p>
  <p>M. Rocchetta</p>
</footer>

<script>
  const obs = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('on'); });
  }, { threshold: 0.08, rootMargin: '0px 0px -30px 0px' });
  document.querySelectorAll('.fade').forEach(el => obs.observe(el));
</script>
</body>
</html>
