---
title: "USM : Userspace Memory Management"
authors:
- me
- Luc Mahop
- Assane Fall
- Yves Kone
- Renaud Lachaize
- Jean-Pierre Lozi
- Alain Tchana
date: "2024-12-09T00:00:00Z"

# Schedule page publish date (NOT publication's date).
publishDate: "2017-01-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article"]

# Publication name and optional abbreviated publication name.
publication: ""
publication_short: ""

abstract: We introduce USM, a framework for rapid development of memory management (MM) policies in Linux. USM adopts a microkernel approach, allowing MM policies to run in userspace. We demonstrate the flexibility of USM by using it to implement various MM policies. Further, we evaluate USM’s performance, showing comparable or better results than Linux, with up to a 1.41 × improvement for Redis using a basic MM policy. Additionally, we compare USM with the tate-of-the-art FBMM policy and show that USM supports implementing research MM policies such as the PTEMagnet policy for virtual machines.

# Summary. An optional shortened abstract.
summary: USM is a userspace framework for rapidly developing memory-management policies in Linux. It offers kernel-like flexibility with simpler experimentation, achieving competitive performance—up to 1.41× faster than Linux on Redis—and supports advanced policies such as FBMM and PTEMagnet.

tags:
- Memory Management
- Policies implementation
- USM

featured: true

hugoblox:
  ids:
    arxiv: 1512.04133v1

links:
- type: preprint
  provider: Middleware
  id: 1512.04133v1
- type: code
  url: https://github.com/HugoBlox/hugo-blox-builder
- type: slides
  url: https://www.slideshare.net/
- type: dataset
  url: "#"
- type: poster
  url: "#"
- type: source
  url: "#"
- type: video
  url: https://youtube.com
- type: custom
  label: Custom Link
  url: http://example.org

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/s9CC2SKySJM)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
- internal-project

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---

This work is driven by the results in my [previous paper](/publications/conference-paper/) on LLMs.

> [!NOTE]
> Create your slides in Markdown - click the *Slides* button to check out the example.

Add the publication's **full text** or **supplementary notes** here. You can use rich formatting such as including [code, math, and images](https://docs.hugoblox.com/content/writing-markdown-latex/).
