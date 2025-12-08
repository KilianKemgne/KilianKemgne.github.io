---
title: "GDR - RSD : Systems and Network Virtualization"

event: GDR - RSD
event_url: https://gdr-rsd.cnrs.fr/event/journee-virtualisation-des-systemes-et-des-reseaux/

# location: Campus Pierre and Marie Curie, Sorbonne University
location: Sorbonne University
address:
  street: 4 place Jussieu
  city: Paris
  region: IDF
  postcode: '75005'
  country: France

summary: "USM: Physical Memory Management in Userspace for Extensibility"
abstract: 'A challenge during which I presented work on integrating NUMA-awareness into USM (Userspace Memory Management), implementing a memory scheduling policy in a NUMA environment, and comparing USM with FBMM (File-Based Memory Management) (HOTOS ’23).'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2024-11-25T09:00:00Z'
# date_end: '2024-11-25T17:00:00Z'
all_day: true

# Schedule page publish date (NOT talk date).
publishDate: '2024-11-25T00:00:00Z'

authors:
  - me

tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Campus Pierre and Marie Curie**](https://thumbs.dreamstime.com/b/jussieu-campus-universite-pierre-marie-curie-upmc-th-arrondissement-paris-france-june-opened-et-located-latin-250028824.jpg)'
  focal_point: Right

links:
  # - type: code
  #   url: https://github.com
  - type: slides
    url: https://docs.google.com/presentation/d/1tznI6On54crYNicCbdlwipW9SbClfnzGvUwLsTQRc9c/edit?usp=sharing 
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

> [!NOTE]
> Click on the **Slides** button above to download the built-in slides.

Slides from the GDR RSD Presentation:

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
    padding-bottom: 56.25%;
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
      <a href="https://docs.google.com/presentation/d/1tznI6On54crYNicCbdlwipW9SbClfnzGvUwLsTQRc9c/present" target="_blank" rel="noopener">
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
      src="https://docs.google.com/presentation/d/1tznI6On54crYNicCbdlwipW9SbClfnzGvUwLsTQRc9c/embed?start=false&loop=false&delayms=3000"
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




