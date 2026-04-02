---
title: "Workshop : Defis OS INRIA, Grenoble"

event: Defi OS
event_url: https://project.inria.fr/defios/files/2025/02/Defi_OS_workshop-decembre_2024-programme.pdf

location: Ensimag
address:
  street: 263 avenue du Général Leclerc
  city: Rennes
  region: BRE
  postcode: '35042'
  country: France

summary: "USM: Physical Memory Management in Userspace for Extensibility"
abstract: 'A challenge during which I presented work on integrating NUMA-awareness into USM (Userspace Memory Management), implementing a memory scheduling policy in a NUMA environment, and comparing USM with FBMM (File-Based Memory Management) (HOTOS ’23).'

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: '2024-12-12T10:00:00Z'
date_end: '2024-12-13T17:00:00Z'
all_day: false

# Schedule page publish date (NOT talk date).
publishDate: '2017-01-01T00:00:00Z'

authors:
  - me

tags: []

# Is this a featured talk? (true/false)
featured: false

image:
  caption: 'Image credit: [**Ensimag**](https://ensimag.grenoble-inp.fr/medias/photo/20140521-130548-pierre-jayet1_1705928269427-jpg)'
  focal_point: Right

links:
  # - type: code
  #   url: https://github.com
  - type: program
    url: https://project.inria.fr/defios/files/2025/02/Defi_OS_workshop-decembre_2024-programme.pdf
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

Data centers are today at the heart of all computing, from providing the computing power that supports machine learning, databases, video streaming, etc., down to providing tiny sensors with extra computing power and storage.  By centralizing computing, data centers have the potential to deliver massive computing resources while adapting the resource consumption efficiently to changing needs.  Nevertheless, data centers have not fully realized their potential of optimizing large-scale computing usage. Instead, studies have consistently shown that, even though new data centers continue to be built, existing data centers are massively underused, typically reaching a usage ratio of only 50%.

The essential problem of managing a data center is to allocate hardware resources, in an environment in which application requirements are not known a priori and are constantly changing, and where at the same time hardware capabilities are regularly evolving.  The Defi OS will attack the problem of data center underusage at the operating system level and hypervisor level, as these are the software components that interact directly with the hardware.  The Defi brings together researchers from the Whisper, WIDE, Erods (UGA), and Benagil teams and will investigate how virtual machine migration, heterogeneous architectures, rack scale computing, and custom resource management policies can be harnessed to raise the data center usage ratio toward 90%.

> [!NOTE]
> Text adapted from the [Défi OS project page](https://project.inria.fr/defios/).
<!-- 
> [!NOTE]
> Click on the **Slides** button above to download the built-in slides.

Slides of the Talk Presented at INRIA : -->

<!-- - **Create** slides using Hugo Blox Builder's [_Slides_](https://docs.hugoblox.com/reference/content-types/) feature and link using the `slides` parameter in the front matter of the talk file
- **Upload** an existing slide deck to this page bundle and link it using `links: [{ type: slides, url: path/to/file } ]` in front matter
- **Embed** your slides (e.g. Google Slides) or presentation video on this page using [shortcodes](https://docs.hugoblox.com/reference/markdown/).

Further event details, including [page elements](https://docs.hugoblox.com/reference/markdown/) such as image galleries, can be added to the body of this page. -->
