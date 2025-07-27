<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Javitha - UI/UX Designer</title>
  <style>
    :root {
      --bg: #ffffff;
      --text: #333;
      --heading: #252D6D;
      --link: #30A3DC;
      --border: #ddd;
      --card-bg: #f9f9f9;
      --accent: #30A3DC;
      --radius: 12px;
    }

    [theme="dark"] {
      --bg: #121212;
      --text: #e0e0e0;
      --heading: #30A3DC;
      --link: #64FFDA;
      --border: #444;
      --card-bg: #1e1e1e;
      --accent: #30A3DC;
    }

    [theme="anime"] {
      --bg: linear-gradient(135deg, #fdf0f0, #e6f7ff);
      --text: #333;
      --heading: #e91e63;
      --link: #ff69b4;
      --border: #ffb6c1;
      --card-bg: rgba(255, 255, 255, 0.9);
      --accent: #e91e63;
      --radius: 20px;
    }

    [theme="gradient"] {
      --bg: linear-gradient(135deg, #ff9a9e, #a8edea, #d299c2);
      --text: #333;
      --heading: #333;
      --link: #fff;
      --border: transparent;
      --card-bg: rgba(255, 255, 255, 0.85);
      --accent: #FF416C;
      --radius: 16px;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: var(--bg);
      color: var(--text);
      margin: 0;
      padding: 30px;
      transition: all 0.4s ease;
      border-radius: var(--radius);
    }

    .container {
      max-width: 900px;
      margin: auto;
      background: var(--card-bg);
      border: 2px solid var(--border);
      border-radius: var(--radius);
      padding: 32px;
      box-shadow: 0 8px 24px rgba(0, 0, 0, 0.1);
    }

    h1, h2, h3 {
      color: var(--heading);
      margin-top: 1rem;
      transition: color 0.3s ease;
    }

    a {
      color: var(--link);
      text-decoration: none;
      font-weight: 500;
    }

    a:hover {
      text-decoration: underline;
    }

    .project-card {
      background: var(--card-bg);
      border: 1px solid var(--border);
      border-left: 4px solid var(--accent);
      padding: 16px;
      margin-bottom: 16px;
      border-radius: 10px;
      transition: transform 0.2s ease, box-shadow 0.2s ease;
    }

    .project-card:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.08);
    }

    .theme-selector {
      display: flex;
      gap: 10px;
      margin-bottom: 20px;
      flex-wrap: wrap;
    }

    .theme-btn {
      padding: 8px 14px;
      font-size: 14px;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
      transition: all 0.2s ease;
    }

    .theme-btn.dark {
      background: #121212; color: white;
    }

    .theme-btn.anime {
      background: #e91e63; color: white;
    }

    .theme-btn.gradient {
      background: linear-gradient(45deg, #FF416C, #FF4B2B); color: white;
    }

    .theme-btn.light {
      background: #666; color: white;
    }

    .theme-btn.professional {
      background: #252D6D; color: white;
    }

    .badge {
      margin: 4px;
      display: inline-block;
    }

    .stats-container {
      display: flex;
      gap: 16px;
      flex-wrap: wrap;
      margin: 20px 0;
    }

    .stats-container img {
      flex: 1;
      min-width: 300px;
      border-radius: 8px;
    }

    .fun-fact {
      font-style: italic;
      padding: 12px 16px;
      background: var(--card-bg);
      border-radius: 8px;
      border-left: 4px solid var(--accent);
    }

    .footer {
      text-align: center;
      margin-top: 40px;
      color: var(--text);
      font-size: 0.9em;
    }

    @media (prefers-color-scheme: dark) {
      body:not([theme]) {
        background: #121212;
        color: #e0e0e0;
      }
    }
  </style>
</head>
<body theme="light">
  <div class="container">

    <!-- Theme Selector -->
    <div class="theme-selector">
      <button class="theme-btn light" onclick="setTheme('light')">📘 Light</button>
      <button class="theme-btn dark" onclick="setTheme('dark')">🌙 Dark</button>
      <button class="theme-btn anime" onclick="setTheme('anime')">🎌 Anime</button>
      <button class="theme-btn gradient" onclick="setTheme('gradient')">🌈 Gradient</button>
      <button class="theme-btn professional" onclick="setTheme('professional')">💼 Pro</button>
    </div>

    <script>
      function setTheme(theme) {
        document.body.setAttribute('theme', theme);
        localStorage.setItem('theme', theme);
      }

      // Load saved theme
      const savedTheme = localStorage.getItem('theme') || 'light';
      setTheme(savedTheme);
    </script>

    <!-- Header -->
    <h1 align="center">👋 Hi, I’m <strong>Javitha</strong> ✨</h1>
    <p align="center">
      <i>🎨 UI/UX Designer | Front-End Learner | Pixel Perfectionist</i>
    </p>

    <p align="center">
      I design digital experiences that are <strong>beautiful</strong>, <strong>intuitive</strong>, and <strong>human-centered</strong>.  
      When I’m not in Figma, I’m probably sketching on paper or sipping matcha. 🍵
    </p>

    <hr style="border: 1px solid var(--border); margin: 24px 0;">

    <!-- What I Do -->
    <h2>🔍 What I Do</h2>
    <ul>
      <li>✨ Craft clean, user-friendly interfaces</li>
      <li>🧠 Turn user research into meaningful flows</li>
      <li>🖌️ Build interactive prototypes & design systems</li>
      <li>💻 Code responsive front-ends (HTML/CSS/JS)</li>
    </ul>

    <!-- Learning -->
    <h2>🌱 Currently Learning</h2>
    <ul>
      <li>Advanced Figma (Auto Layout, Variants, Dev Mode)</li>
      <li>User Testing & Accessibility Standards (WCAG)</li>
      <li>JavaScript + React for interactive UIs</li>
    </ul>

    <!-- Portfolio -->
    <h2>💼 My Design Portfolio</h2>
    <div class="project-card">
      <h3><a href="https://dribbble.com/javitha080/project1" target="_blank">📱 Mobile Banking App Redesign</a></h3>
      <p>Improved usability & visual hierarchy for a finance app. Focus on accessibility and trust.</p>
    </div>

    <div class="project-card">
      <h3><a href="https://dribbble.com/javitha080/project2" target="_blank">🌐 E-Commerce Dashboard UI</a></h3>
      <p>A clean, data-rich admin panel with intuitive navigation and real-time analytics.</p>
    </div>

    <div class="project-card">
      <h3><a href="https://dribbble.com/javitha080/project3" target="_blank">🎨 Design System: "Nova UI"</a></h3>
      <p>A modular design system with tokens, components, and dark/light mode support.</p>
    </div>

    <!-- Collaboration -->
    <h2>💞️ Open to Collaborate</h2>
    <p>I’d love to work on:</p>
    <ul>
      <li>Open-source UX improvements</li>
      <li>Design + code side projects</li>
      <li>Mentorship or design challenges</li>
    </ul>

    <!-- Contact -->
    <h2>📬 Reach Me</h2>
    <ul>
      <li>📧 <a href="mailto:javitha@example.com">javitha@example.com</a></li>
      <li>🔗 <a href="https://linkedin.com/in/javitha080">LinkedIn</a></li>
      <li>🎨 <a href="https://dribbble.com/javitha080">Dribbble</a> | <a href="https://behance.net/javitha080">Behance</a></li>
      <li>🐦 <a href="https://x.com/javitha_dev">@javitha_dev</a></li>
    </ul>

    <!-- Pronouns & Fun Fact -->
    <h2>😄 Pronouns</h2>
    <p>she/her</p>

    <h2>⚡ Fun Fact</h2>
    <p class="fun-fact">
      I’m secretly designing an <strong>anime-themed productivity app</strong> — because who says work can’t be kawaii? 🎌🌸<br>
      Also, I once redesigned a hospital app to feel <em>calm and friendly</em> — no more scary red alerts!
    </p>

    <!-- Tools -->
    <h2>🛠️ Tools & Tech</h2>
    <p>
      <img class="badge" src="https://img.shields.io/badge/Figma-F24E1E?logo=figma&logoColor=white&style=flat" alt="Figma"/>
      <img class="badge" src="https://img.shields.io/badge/Adobe_XD-470137?logo=Adobe%20XD&logoColor=#FF61F6&style=flat" alt="Adobe XD"/>
      <img class="badge" src="https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white&style=flat" alt="HTML5"/>
      <img class="badge" src="https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white&style=flat" alt="CSS3"/>
      <img class="badge" src="https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black&style=flat" alt="JavaScript"/>
      <img class="badge" src="https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white&style=flat" alt="Git"/>
    </p>

    <!-- Stats -->
    <h2>📊 GitHub Stats</h2>
    <div class="stats-container">
      <img src="https://github-readme-stats.vercel.app/api?username=Javitha080&show_icons=true&theme=radical&border_color=var(--accent)" />
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Javitha080&layout=compact&theme=radical&border_color=var(--accent)" />
    </div>

    <!-- Visitor Counter -->
    <p align="center">
      <img src="https://visitor-badge.glitch.me/badge?page_id=Javitha080.Javitha080&left_color=grey&right_color=var(--accent)" alt="visitors" />
    </p>

    <!-- Footer -->
    <div class="footer">
      Thanks for visiting my profile! ✨<br>
      Designed with love, Figma, and a lot of coffee. ☕
    </div>

  </div>
</body>
</html>

<!---
Javitha080/Javitha080 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
