
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0a0a0a">
  <meta name="description" content="Akash S. — Content Creator, Video Editor and Visual Designer. Explore cinematic videos and creative poster designs.">

  <title>Akash S. | Creative Portfolio</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Space+Grotesk:wght@400;500;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #0a0a0a;
      --panel: #141414;
      --text: #f5f5f5;
      --muted: #999999;
      --accent: #c7ff65;
      --border: #292929;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 90px;
    }

    body {
      background: var(--bg);
      color: var(--text);
      font-family: 'DM Sans', sans-serif;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      display: block;
      width: 100%;
    }

    button {
      font: inherit;
    }

    .container {
      width: min(1120px, 90%);
      margin: auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(10, 10, 10, 0.88);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid var(--border);
    }

    nav {
      min-height: 76px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 24px;
    }

    .logo {
      font: 700 21px 'Space Grotesk', sans-serif;
      letter-spacing: -1px;
    }

    .logo span {
      color: var(--accent);
    }

    .nav-links {
      display: flex;
      gap: 28px;
      color: #c4c4c4;
      font-size: 13px;
    }

    .nav-links a:hover,
    .text-link:hover {
      color: var(--accent);
    }

    .hero {
      min-height: 590px;
      display: flex;
      align-items: center;
      padding: 100px 0 90px;
    }

    .eyebrow {
      color: var(--accent);
      text-transform: uppercase;
      font-size: 11px;
      letter-spacing: 3px;
      font-weight: 700;
      margin-bottom: 22px;
    }

    h1, h2, h3 {
      font-family: 'Space Grotesk', sans-serif;
      line-height: 1.08;
    }

    h1 {
      font-size: clamp(48px, 8vw, 94px);
      letter-spacing: -5px;
      max-width: 850px;
    }

    h1 span {
      color: var(--accent);
    }

    .hero-description {
      color: var(--muted);
      max-width: 520px;
      margin: 25px 0 32px;
      font-size: 16px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 13px 21px;
      border: 1px solid var(--border);
      border-radius: 4px;
      font-size: 13px;
      font-weight: 600;
      transition: 0.25s;
      cursor: pointer;
    }

    .button.primary {
      background: var(--accent);
      color: #111;
      border-color: var(--accent);
    }

    .button:hover {
      transform: translateY(-3px);
    }

    section {
      padding: 85px 0;
      border-top: 1px solid var(--border);
    }

    .section-heading {
      display: flex;
      justify-content: space-between;
      align-items: end;
      gap: 20px;
      margin-bottom: 35px;
    }

    h2 {
      font-size: clamp(32px, 5vw, 48px);
      letter-spacing: -2px;
    }

    .section-note {
      color: var(--muted);
      font-size: 13px;
    }

    .filters {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-bottom: 30px;
    }

    .filter {
      border: 1px solid var(--border);
      background: transparent;
      color: var(--muted);
      border-radius: 30px;
      padding: 9px 17px;
      cursor: pointer;
      font-size: 12px;
    }

    .filter.active,
    .filter:hover {
      background: var(--accent);
      color: #111;
      border-color: var(--accent);
    }

    .project-grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 28px;
    }

    .project {
      min-width: 0;
    }

    .project[hidden] {
      display: none;
    }

    .project-image {
      position: relative;
      aspect-ratio: 16 / 9;
      overflow: hidden;
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 5px;
    }

    .project-image img {
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s;
    }

    .project:hover .project-image img {
      transform: scale(1.04);
    }

    .project-image.poster {
      aspect-ratio: 4 / 5;
      max-width: 440px;
    }

    .project-image.poster img {
      object-fit: contain;
    }

    .project-image .placeholder {
      height: 100%;
      display: grid;
      place-items: center;
      color: #777;
      font-size: 12px;
      text-align: center;
      padding: 20px;
    }

    .project-info {
      display: flex;
      justify-content: space-between;
      align-items: start;
      gap: 15px;
      padding-top: 16px;
    }

    .project-info h3 {
      font-size: 19px;
      margin-bottom: 5px;
      letter-spacing: -0.4px;
    }

    .project-info p,
    .project-type {
      font-size: 12px;
      color: var(--muted);
    }

    .project-type {
      white-space: nowrap;
      color: var(--accent);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 70px;
      align-items: start;
    }

    .about-copy {
      color: var(--muted);
      font-size: 15px;
      margin-top: 20px;
    }

    .skills {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 24px;
    }

    .skill {
      border: 1px solid var(--border);
      padding: 9px 13px;
      border-radius: 3px;
      font-size: 12px;
    }

    .contact-panel {
      background: var(--panel);
      border: 1px solid var(--border);
      border-radius: 6px;
      padding: clamp(25px, 5vw, 55px);
    }

    .contact-panel h2 {
      max-width: 650px;
      margin-bottom: 20px;
    }

    .contact-panel p {
      color: var(--muted);
      margin-bottom: 25px;
    }

    footer {
      padding: 28px 0;
      color: var(--muted);
      font-size: 12px;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 15px;
      flex-wrap: wrap;
    }

    .text-link {
      color: var(--text);
    }

    .modal {
      position: fixed;
      inset: 0;
      z-index: 100;
      background: rgba(0, 0, 0, 0.94);
      display: none;
      place-items: center;
      padding: 25px;
    }

    .modal.open {
      display: grid;
    }

    .modal-content {
      width: min(100%, 1000px);
      position: relative;
    }

    .modal-content img {
      max-height: 85vh;
      object-fit: contain;
    }

    .modal-content iframe,
    .modal-content video {
      width: 100%;
      aspect-ratio: 16 / 9;
      border: 0;
      background: #000;
    }

    .modal-close {
      position: absolute;
      right: 0;
      bottom: calc(100% + 10px);
      background: transparent;
      color: white;
      border: 1px solid #555;
      padding: 7px 14px;
      cursor: pointer;
    }

    @media (max-width: 650px) {
      nav {
        min-height: 65px;
        align-items: flex-start;
        flex-direction: column;
        justify-content: center;
        gap: 8px;
        padding: 12px 0;
      }

      .nav-links {
        gap: 17px;
        font-size: 11px;
        flex-wrap: wrap;
      }

      .hero {
        min-height: 470px;
        padding: 75px 0;
      }

      h1 {
        letter-spacing: -2.5px;
      }

      section {
        padding: 60px 0;
      }

      .section-heading {
        align-items: start;
        flex-direction: column;
      }

      .project-grid {
        grid-template-columns: 1fr;
        gap: 32px;
      }

      .about-grid {
        grid-template-columns: 1fr;
        gap: 30px;
      }

      .project-info h3 {
        font-size: 17px;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after {
        scroll-behavior: auto !important;
        transition: none !important;
      }
    }
  </style>
</head>

<body>

<header>
  <nav class="container">
    <a class="logo" href="#home">AKASH<span>.</span></a>
    <div class="nav-links">
      <a href="#home">Home</a>
      <a href="#work">My Work</a>
      <a href="#about">About</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>
</header>

<main>
  <section class="hero" id="home" style="border-top:0">
    <div class="container">
      <p class="eyebrow">Content Creator · Video Editor · Visual Designer</p>
      <h1>I turn ideas into <span>visual stories.</span></h1>
      <p class="hero-description">
        Creating videos, campaigns and designs that bring ideas to life.
        A collection of my creative work, experiments and visual stories.
      </p>
      <div class="buttons">
        <a class="button primary" href="#work">Explore My Work ↗</a>
        <a class="button" href="#contact">Get In Touch</a>
      </div>
    </div>
  </section>

  <section id="work">
    <div class="container">
      <div class="section-heading">
        <div>
          <p class="eyebrow">Selected Projects</p>
          <h2>My Work<span style="color:var(--accent)">.</span></h2>
        </div>
        <p class="section-note">Videos, campaigns & visual design</p>
      </div>

      <div class="filters">
        <button class="filter active" data-filter="all">All Work</button>
        <button class="filter" data-filter="video">Video Works</button>
        <button class="filter" data-filter="poster">Poster Designs</button>
      </div>

      <div class="project-grid">

        <!-- VIDEO PROJECT 1
             Replace VIDEO_ID with your YouTube video ID.
             Replace the thumbnail URL with your own thumbnail if desired. -->
        <article class="project" data-category="video">
          <div class="project-image">
            <img src="https://placehold.co/960x540/171717/c7ff65?text=VIDEO+PROJECT+01"
                 alt="Video project 1 thumbnail" loading="lazy">
          </div>
          <div class="project-info">
            <div>
              <h3>Real Estate Film</h3>
              <p>Cinematic video · Editing · Colour grading</p>
            </div>
            <span class="project-type">VIDEO</span>
          </div>
          <button class="button" style="margin-top:14px"
                  data-video="VIDEO_ID"
                  aria-label="Watch Real Estate Film">▶ Watch Project</button>
        </article>

        <!-- VIDEO PROJECT 2 -->
        <article class="project" data-category="video">
          <div class="project-image">
            <img src="https://placehold.co/960x540/171717/c7ff65?text=VIDEO+PROJECT+02"
                 alt="Video project 2 thumbnail" loading="lazy">
          </div>
          <div class="project-info">
            <div>
              <h3>Brand Campaign</h3>
              <p>Brand storytelling · Social media</p>
            </div>
            <span class="project-type">VIDEO</span>
          </div>
          <button class="button" style="margin-top:14px"
                  data-video="VIDEO_ID"
                  aria-label="Watch Brand Campaign">▶ Watch Project</button>
        </article>

        <!-- POSTER PROJECT 1
             Replace the image URL with your poster image URL. -->
        <article class="project" data-category="poster">
          <button class="project-image poster image-open"
                  data-image="https://placehold.co/800x1000/171717/c7ff65?text=POSTER+01"
                  aria-label="View property campaign poster">
            <img src="https://placehold.co/800x1000/171717/c7ff65?text=POSTER+01"
                 alt="Property campaign poster" loading="lazy">
          </button>
          <div class="project-info">
            <div>
              <h3>Property Campaign</h3>
              <p>Creative direction · Poster design</p>
            </div>
            <span class="project-type">DESIGN</span>
          </div>
        </article>

        <!-- POSTER PROJECT 2 -->
        <article class="project" data-category="poster">
          <button class="project-image poster image-open"
                  data-image="https://placehold.co/800x1000/171717/c7ff65?text=POSTER+02"
                  aria-label="View social media poster">
            <img src="https://placehold.co/800x1000/171717/c7ff65?text=POSTER+02"
                 alt="Social media poster design" loading="lazy">
          </button>
          <div class="project-info">
            <div>
              <h3>Social Media Creative</h3>
              <p>Graphic design · Digital campaign</p>
            </div>
            <span class="project-type">DESIGN</span>
          </div>
        </article>

      </div>
    </div>
  </section>

  <section id="about">
    <div class="container about-grid">
      <div>
        <p class="eyebrow">A Little About Me</p>
        <h2>Creative thinking.<br>Visual execution.</h2>
      </div>
      <div>
        <p class="about-copy">
          I'm Akash, a content creator and visual designer based in Dubai.
          I work across video editing, photography, social media content and
          graphic design, turning ideas into visual experiences.
        </p>
        <div class="skills">
          <span class="skill">Video Editing</span>
          <span class="skill">Content Creation</span>
          <span class="skill">Graphic Design</span>
          <span class="skill">Photography</span>
          <span class="skill">Colour Grading</span>
          <span class="skill">Social Media</span>
        </div>
      </div>
    </div>
  </section>

  <section id="contact">
    <div class="container">
      <div class="contact-panel">
        <p class="eyebrow">Have a project in mind?</p>
        <h2>Let's create something worth watching.</h2>
        <p>For creative projects, collaborations and opportunities.</p>
        <div class="buttons">
          <!-- Replace with your real email address -->
          <a class="button primary"
             href="mailto:YOUR_EMAIL@example.com">Email Me ↗</a>

          <!-- Replace with your LinkedIn profile URL -->
          <a class="button" href="https://www.linkedin.com/"
             target="_blank" rel="noopener noreferrer">LinkedIn ↗</a>

          <!-- Replace with your Instagram profile URL -->
          <a class="button" href="https://www.instagram.com/"
             target="_blank" rel="noopener noreferrer">Instagram ↗</a>
        </div>
      </div>
    </div>
  </section>
</main>

<footer>
  <div class="container footer-inner">
    <span>© <span id="year"></span> Akash S. All rights reserved.</span>
    <a class="text-link" href="#home">Back to top ↑</a>
  </div>
</footer>

<!-- Popup for videos and poster images -->
<div class="modal" id="modal" role="dialog"
     aria-modal="true" aria-label="Project preview">
  <div class="modal-content">
    <button class="modal-close" id="modalClose" aria-label="Close preview">✕ Close</button>
    <div id="modalBody"></div>
  </div>
</div>

<script>
  document.getElementById('year').textContent = new Date().getFullYear();

  // Filter between all projects, videos and posters
  const filters = document.querySelectorAll('.filter');
  const projects = document.querySelectorAll('.project');

  filters.forEach(button => {
    button.addEventListener('click', () => {
      filters.forEach(item => item.classList.remove('active'));
      button.classList.add('active');

      const category = button.dataset.filter;

      projects.forEach(project => {
        project.hidden = category !== 'all' &&
                         project.dataset.category !== category;
      });
    });
  });

  // Popup preview
  const modal = document.getElementById('modal');
  const modalBody = document.getElementById('modalBody');
  const closeButton = document.getElementById('modalClose');

  function closeModal() {
    modal.classList.remove('open');
    modalBody.replaceChildren();
  }

  document.querySelectorAll('.image-open').forEach(button => {
    button.addEventListener('click', () => {
      const image = document.createElement('img');
      image.src = button.dataset.image;
      image.alt = button.getAttribute('aria-label') || 'Poster preview';
      modalBody.replaceChildren(image);
      modal.classList.add('open');
      closeButton.focus();
    });
  });

  document.querySelectorAll('[data-video]').forEach(button => {
    button.addEventListener('click', () => {
      const id = button.dataset.video.trim();

      // Avoid opening the placeholder ID before a real video is added.
      if (!id || id === 'VIDEO_ID') {
        alert('Add your YouTube video ID to this project first.');
        return;
      }

      // Only accept a standard 11-character YouTube video ID.
      if (!/^[a-zA-Z0-9_-]{11}$/.test(id)) {
        alert('Please enter a valid YouTube video ID.');
        return;
      }

      const frame = document.createElement('iframe');
      frame.src = 'https://www.youtube-nocookie.com/embed/' +
                  encodeURIComponent(id) + '?autoplay=1';
      frame.title = 'Portfolio video';
      frame.allow = 'autoplay; encrypted-media; picture-in-picture; fullscreen';
      frame.allowFullscreen = true;
      modalBody.replaceChildren(frame);
      modal.classList.add('open');
      closeButton.focus();
    });
  });

  closeButton.addEventListener('click', closeModal);

  modal.addEventListener('click', event => {
    if (event.target === modal) closeModal();
  });

  document.addEventListener('keydown', event => {
    if (event.key === 'Escape') closeModal();
  });
</script>

</body>
</html>
