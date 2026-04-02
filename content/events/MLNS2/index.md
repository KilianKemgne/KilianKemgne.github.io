---
title: "MLNS2 : Machine Learning Network Systems Security"

event: MLNS2
event_url: https://mlns2.org/

# location: Campus Pierre and Marie Curie, Sorbonne University
location: National Advanced School of Engineering of Yaounde
address:
  street: Pharmacie EMIA
  city: Yaounde
  region: Center
  postcode: 
  country: Cameroon

summary: "UPIPO : Unecessary Page In Page Out"
abstract: 'IO_URING based approach for double paging problem'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2026-02-16T09:00:00Z'
# date_end: '2024-11-25T17:00:00Z'
all_day: true

# Schedule page publish date (NOT talk date).
publishDate: '2026-02-16T00:00:00Z'

authors:
  - me

tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**MLNS2**](logos/irit.png)'
  focal_point: Right

links:
  # - type: code
  #   url: https://github.com
  - type: slides
    url: https://drive.google.com/file/d/1OHMIncFQLYNuVA9iVhJqAovwhwnOYDjX/view?usp=drive_link
  # - type: video
  #   url: https://youtube.com

# Markdown Slides (optional).
#   Associate this talk with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects:
  - example
---


Slides from the MLNS2 Presentation:

<!-- - **Create** slides using Hugo Blox Builder's [_Slides_](https://docs.hugoblox.com/reference/content-types/) feature and link using the `slides` parameter in the front matter of the talk file
- **Upload** an existing slide deck to this page bundle and link it using `links: [{ type: slides, url: path/to/file } ]` in front matter
- **Embed** your slides (e.g. Google Slides) or presentation video on this page using [shortcodes](https://docs.hugoblox.com/reference/markdown/).

Further event details, including [page elements](https://docs.hugoblox.com/reference/markdown/) such as image galleries, can be added to the body of this page. -->

<style>
  .slides-container {
    position: relative;
    margin-top: 1.5rem;
    margin-bottom: 2rem;
    border-radius: 12px;
    border: 1px solid #e5e7eb;
    background: #f9fafb;
    box-shadow: 0 4px 20px rgba(0,0,0,0.08);
    overflow: hidden;
  }

  .slides-toolbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0.6rem 0.9rem;
    font-size: 0.9rem;
    background: #f3f4f6;
    border-bottom: 1px solid #e5e7eb;
  }

  .slides-toolbar-title {
    font-weight: 600;
    color: #111827;
  }

  .slides-toolbar-actions {
    display: flex;
    gap: 0.5rem;
  }

  .slides-toolbar button,
  .slides-toolbar a {
    font-size: 0.8rem;
    padding: 0.25rem 0.6rem;
    border-radius: 999px;
    border: 1px solid #d1d5db;
    background: white;
    cursor: pointer;
    text-decoration: none;
    color: #111827;
  }

  .slides-toolbar button:hover,
  .slides-toolbar a:hover {
    background: #e5e7eb;
  }

  .slides-frame-wrapper {
    position: relative;
    padding-bottom: 70%; /* 4:3 au lieu de 56.25% (16:9) */
    height: 0;
  }

  .slides-frame-wrapper iframe {
    position: absolute;
    top: 0; left: 0;
    width: 100%; height: 100%;
    border: 0;
    border-radius: 0 0 12px 12px;
  }

  /* Mode plein écran dans la page */
  .slides-container.fullscreen {
    position: fixed;
    inset: 0;
    margin: 0;
    border-radius: 0;
    border: none;
    z-index: 9999;
  }

  .slides-container.fullscreen .slides-frame-wrapper {
    padding-bottom: 0;
    height: calc(100% - 44px); /* 44px ≈ hauteur toolbar */
  }

  .slides-container.fullscreen .slides-frame-wrapper iframe {
    border-radius: 0;
  }
</style>

<div class="slides-container">
  <div class="slides-toolbar">
    <span class="slides-toolbar-title">Talk Slides</span>
    <div class="slides-toolbar-actions">
      <!-- Ouvre les slides dans un nouvel onglet -->
      <a href="https://drive.google.com/file/d/1OHMIncFQLYNuVA9iVhJqAovwhwnOYDjX/view" target="_blank" rel="noopener">
        Open in new tab
      </a>
      <!-- Bouton plein écran dans la page -->
      <button type="button" onclick="toggleSlidesFullscreen(this)">
        Fullscreen
      </button>
    </div>
  </div>

  <div class="slides-frame-wrapper">
    <iframe 
      src="https://drive.google.com/file/d/1OHMIncFQLYNuVA9iVhJqAovwhwnOYDjX/preview"
      allowfullscreen="true"
      mozallowfullscreen="true"
      webkitallowfullscreen="true"
    ></iframe>
  </div>
</div>

<script>
  function toggleSlidesFullscreen(button) {
    const container = button.closest('.slides-container');
    const isFullscreen = container.classList.toggle('fullscreen');
    button.textContent = isFullscreen ? 'Exit fullscreen' : 'Fullscreen';
  }
</script>
