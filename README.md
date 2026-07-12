<!-- ===================================================================
     GITHUB PROFILE README — Sanyam Singla (@SAM10101010)
     Theme: Tokyo Night (cohesive dark) | Layout: Centered cards
     Enhanced with: Cursor effects, hover animations, dynamic visuals
     =================================================================== -->

<!-- =====================  CURSOR TRAIL EFFECT (SCRIPT)  ===================== -->
<script>
  // Subtle particle trail that follows cursor
  document.addEventListener('mousemove', function(e) {
    const trail = document.createElement('div');
    trail.className = 'cursor-trail';
    trail.style.left = e.pageX + 'px';
    trail.style.top = e.pageY + 'px';
    document.body.appendChild(trail);
    setTimeout(() => trail.remove(), 800);
  });

  // Custom cursor (desktop only)
  const cursor = document.createElement('div');
  cursor.className = 'custom-cursor';
  document.body.appendChild(cursor);

  document.addEventListener('mousemove', (e) => {
    cursor.style.left = e.pageX + 'px';
    cursor.style.top = e.pageY + 'px';
  });

  // Expand cursor on interactive elements
  document.querySelectorAll('a, img, button').forEach(el => {
    el.addEventListener('mouseenter', () => cursor.classList.add('cursor-hover'));
    el.addEventListener('mouseleave', () => cursor.classList.remove('cursor-hover'));
  });
</script>

<!-- =====================  GLOBAL STYLES (CURSOR + ANIMATIONS)  ===================== -->
<style>
  /* Custom cursor */
  .custom-cursor {
    position: fixed;
    width: 18px;
    height: 18px;
    border: 2px solid #6a4c93;
    border-radius: 50%;
    pointer-events: none;
    transform: translate(-50%, -50%);
    transition: width 0.25s ease, height 0.25s ease, background 0.25s ease, border-color 0.25s ease;
    z-index: 9999;
    mix-blend-mode: difference;
    background: rgba(106, 76, 147, 0.15);
  }
  .custom-cursor.cursor-hover {
    width: 38px;
    height: 38px;
    background: rgba(232, 141, 103, 0.4);
    border-color: #e88d67;
  }

  /* Cursor trail particle */
  .cursor-trail {
    position: absolute;
    width: 8px;
    height: 8px;
    background: radial-gradient(circle, #e88d67, transparent);
    border-radius: 50%;
    pointer-events: none;
    transform: translate(-50%, -50%);
    animation: fadeTrail 0.8s ease-out forwards;
    z-index: 9998;
  }
  @keyframes fadeTrail {
    0%   { opacity: 1; transform: translate(-50%, -50%) scale(1); }
    100% { opacity: 0; transform: translate(-50%, -50%) scale(3); }
  }

  /* Hide default cursor on interactive elements */
  a, button, .clickable { cursor: pointer; }
  a:hover { cursor: none; }

  /* Glow pulse for headings */
  .glow-heading {
    display: inline-block;
    animation: glowPulse 3s ease-in-out infinite;
  }
  @keyframes glowPulse {
    0%, 100% { text-shadow: 0 0 10px rgba(106, 76, 147, 0.5), 0 0 20px rgba(232, 141, 103, 0.3); }
    50%      { text-shadow: 0 0 20px rgba(106, 76, 147, 0.8), 0 0 40px rgba(232, 141, 103, 0.6); }
  }

  /* Floating animation */
  .float { animation: float 4s ease-in-out infinite; }
  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50%      { transform: translateY(-8px); }
  }

  /* Hover scale for cards and badges */
  .hover-scale {
    transition: transform 0.3s ease, filter 0.3s ease;
    display: inline-block;
  }
  .hover-scale:hover {
    transform: scale(1.08);
    filter: drop-shadow(0 0 12px rgba(232, 141, 103, 0.6));
  }

  /* Gradient text animation */
  .gradient-text {
    background: linear-gradient(90deg, #e88d67, #6a4c93, #1982c4, #e88d67);
    background-size: 300% 300%;
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    animation: gradientShift 6s ease infinite;
  }
  @keyframes gradientShift {
    0%   { background-position: 0% 50%; }
    50%  { background-position: 100% 50%; }
    100% { background-position: 0% 50%; }
  }

  /* Shimmer effect on dividers */
  .shimmer {
    height: 3px;
    background: linear-gradient(90deg, transparent, #6a4c93, #e88d67, #1982c4, transparent);
    background-size: 200% 100%;
    animation: shimmerSlide 3s linear infinite;
    border-radius: 2px;
  }
  @keyframes shimmerSlide {
    0%   { background-position: -200% 0; }
    100% { background-position: 200% 0; }
  }

  /* Pulse for profile views badge */
  .pulse-badge {
    animation: pulse 2s ease-in-out infinite;
  }
  @keyframes pulse {
    0%, 100% { transform: scale(1); }
    50%      { transform: scale(1.04); }
  }

  /* Spin + glow for trophies */
  .spin-slow { animation: spinSlow 20s linear infinite; }
  @keyframes spinSlow {
    0%   { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }
</style>

---

<!-- =====================  HERO BANNER  ===================== -->
<div align="center">
  <img class="hover-scale" src="https://capsule-render.vercel.app/api?type=waving&color=0:e88d67,25:6a4c93,50:1982c4,75:6a4c93,100:e88d67&height=220&section=header&text=Sanyam%20Singla&fontSize=70&fontColor=ffffff&fontAlignY=38&desc=Full-Stack%20Developer%20%7C%20AI%20Enthusiast%20%7C%20Creative%20Coder&descSize=18&descColor=e0e0e0&descAlignY=55&animation=fadeIn" width="100%" />
</div>

<br/>

<div align="center">
  <!-- Animated gradient name -->
  <h1 class="gradient-text glow-heading" style="font-size: 48px; margin: 0;">
    ✨ Sanyam Singla ✨
  </h1>
  <br/>
  <a href="https://git.io/typing-svg">
    <img class="hover-scale" src="https://readme-typing-svg.herokuapp.com/?font=Fira+Code&size=26&duration=3500&pause=800&color=6A4C93&center=true&vCenter=true&width=560&lines=Hi+There!+%F0%9F%91%8B+I'm+Sanyam;I+turn+%F0%9F%92%A1+ideas+into+code;Always+%F0%9F%8C%B1+learning+something+new;Let's+%F0%9F%91%8B+build+together" alt="Typing SVG" />
  </a>
  <br/>
  <img class="hover-scale pulse-badge" src="https://komarev.com/ghpvc/?username=SAM10101010&label=Profile%20Views&color=6a4c93&style=for-the-badge&labelColor=1a1b26" alt="Profile Views" />
  <br/><br/>
  <i class="gradient-text">“Turning curiosity into code, and code into experiences worth sharing.”</i>
</div>

<div class="shimmer"></div>

---

<!-- =====================  ABOUT ME  ===================== -->
<h3 align="center" class="glow-heading">✨ &nbsp;A&nbsp;b&nbsp;o&nbsp;u&nbsp;t&nbsp; &nbsp;M&nbsp;e&nbsp; &nbsp;✨</h3>

<table align="center">
  <tr>
    <td width="50%" valign="top">

🔭 **Currently working on** Helping individuals bring their creative ideas to life, building effective learning solutions, and solving coding challenges.

👯 **Looking to collaborate on** Innovative projects, engaging educational content, and brainstorming groundbreaking ideas.

🤝 **Looking for help with** Understanding your needs better to deliver tailored, precise assistance.

    </td>
    <td width="50%" valign="top">

🌱 **Currently learning** Advanced AI tooling and new ways to elevate the developer & user experience.

💬 **Ask me about** Coding, AI tools, productivity strategies, or just some fun trivia.

⚡ **Fun fact** I can “read,” “write,” and generate ideas in **90+ languages** — without taking a break! 😄

    </td>
  </tr>
</table>

---

<!-- =====================  TECH STACK  ===================== -->
<h3 align="center" class="glow-heading">🚀 &nbsp;T&nbsp;e&nbsp;c&nbsp;h&nbsp; &nbsp;S&nbsp;t&nbsp;a&nbsp;c&nbsp;k&nbsp; &nbsp;🚀</h3>

<div align="center">
 **💻 Programming Languages** 
<img class="hover-scale" src="https://skillicons.dev/icons?i=cpp,c,java,python,r,js,php&perline=7&theme=light" />
 **🌐 Web Development** 
<img class="hover-scale" src="https://skillicons.dev/icons?i=html,css,nodejs,nextjs,react&perline=5&theme=light" />
 **🗄️ Databases & Cloud** 
<img class="hover-scale" src="https://skillicons.dev/icons?i=mongodb&perline=5&theme=light" />
&nbsp;
<img class="hover-scale" src="https://img.shields.io/badge/Neon-00E5FF?style=for-the-badge&logo=neon&logoColor=black&labelColor=1a1b26" alt="Neon" />
&nbsp;
<img class="hover-scale" src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black&labelColor=1a1b26" alt="Firebase" />
 **🎨 Design & Creative Tools** 
<img class="hover-scale" src="https://skillicons.dev/icons?i=blender&perline=5&theme=light" />
&nbsp;
<img class="hover-scale" src="https://img.shields.io/badge/Adobe-FF0000?style=for-the-badge&logo=adobe&logoColor=white&labelColor=1a1b26" alt="Adobe" />
&nbsp;
<img class="hover-scale" src="https://img.shields.io/badge/Canva-00C4CC?style=for-the-badge&logo=canva&logoColor=white&labelColor=1a1b26" alt="Canva" />
&nbsp;
<img class="hover-scale" src="https://img.shields.io/badge/Krita-203759?style=for-the-badge&logo=krita&logoColor=EEF37B&labelColor=1a1b26" alt="Krita" />

</div>

---

<!-- =====================  FEATURED PROJECTS  ===================== -->
<h3 align="center" class="glow-heading">🏆 &nbsp;F&nbsp;e&nbsp;a&nbsp;t&nbsp;u&nbsp;r&nbsp;e&nbsp;d&nbsp; &nbsp;P&nbsp;r&nbsp;o&nbsp;j&nbsp;e&nbsp;c&nbsp;t&nbsp;s&nbsp; &nbsp;🏆</h3>

<p align="center">
  <em>A glimpse of what I've been building — sync live with my GitHub.</em>
</p>

<div align="center">
  <table>
    <tr>
      <td width="50%" align="center">
        <a href="https://github.com/SAM10101010/RBAC_SOLUTION" class="hover-scale">
          <img src="https://github-readme-stats.vercel.app/api/pin/?username=SAM10101010&repo=RBAC_SOLUTION&theme=tokyonight&hide_border=true&bg_color=1a1b26&title_color=e88d67&icon_color=6a4c93&text_color=c0caf5" alt="RBAC_SOLUTION" />
        </a>
      </td>
      <td width="50%" align="center">
        <a href="https://github.com/SAM10101010/cu_event_managers" class="hover-scale">
          <img src="https://github-readme-stats.vercel.app/api/pin/?username=SAM10101010&repo=cu_event_managers&theme=tokyonight&hide_border=true&bg_color=1a1b26&title_color=e88d67&icon_color=6a4c93&text_color=c0caf5" alt="cu_event_managers" />
        </a>
      </td>
    </tr>
    <tr>
      <td width="50%" align="center">
        <a href="https://github.com/SAM10101010/comet-browser-clone" class="hover-scale">
          <img src="https://github-readme-stats.vercel.app/api/pin/?username=SAM10101010&repo=comet-browser-clone&theme=tokyonight&hide_border=true&bg_color=1a1b26&title_color=e88d67&icon_color=6a4c93&text_color=c0caf5" alt="comet-browser-clone" />
        </a>
      </td>
      <td width="50%" align="center">
        <a href="https://github.com/SAM10101010/engineer_and_customer" class="hover
