---
title: "On-chip semidense representation map for dense visual features driven by attention processes"
authors:
- Sara Granados
- admin
- Sonia Mota
- Javier Díaz
- Eduardo Ros
author_notes:
- ""
date: "2014-09-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2020-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Journal of Real-Time Image Processing*"
publication_short: ""

abstract: We describe an intelligent scheme to condense dense vision features, efficiently reducing the size of representation maps and keeping relevant information for further processing during subsequent stages. We have integrated our condensation algorithm in a low-level-vision system that obtains several vision-features in real-time working on an FPGA. Within this framework, our condensation algorithm allows for the transfer of information from the FPGA device (or processing chip) to any co-processor (from embedded ones to external PCs or DSPs) under technological constraints (such as bandwidth, memory and performance ones). Our condensation core processes 1024 × 1024 resolution images at up to 90 fps. Hence, our condensation module performs this process introducing an insignificant delay in the vision system. A hardware implementation usually implies a simplified version of the vision-feature extractor. Therefore, our condensation process inherently regularizes low-level-vision features, effectively reducing discontinuities and errors. The semidense representation obtained is compatible with mid-/high-level-vision modules, usually implemented as software components. In addition, our versatile semidense map is ready to receive feedback from attention processes, integrating task-driven attention (i.e. top-down information) in real time. Thus, the main advantages of this core are real-time throughput, versatility, inherent regularization, scalability and feedback from other stages.

# Summary. An optional shortened abstract.
summary: ""

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://link.springer.com/article/10.1007/s11554-012-0320-3
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides:
---

