---
title: "Pipelined architecture for real-time cost-optimized extraction of visual primitives based on FPGAs"
authors:
- admin
- Matteo Tomasi
- Javier Díaz
- Mauricio Vanegas
- Eduardo Ros
author_notes:
- ""
date: "2012-09-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2020-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Digital Signal Processing*"
publication_short: ""

abstract: This paper presents an architecture for the extraction of visual primitives on chip: energy, orientation, disparity, and optical flow. This cost-optimized architecture processes in real time high-resolution images for real-life applications. In fact, we present a versatile architecture that may be customized for different performance requirements depending on the target application. In this case, dedicated hardware and its potential on-chip implementation on FPGA devices become an efficient solution. We have developed a multi-scale approach for the computation of the gradient-based primitives. Gradient-based methods are very popular in the literature because they provide a very competitive accuracy vs. efficiency trade-off. The hardware implementation of the system is performed using superscalar fine-grain pipelines to exploit the maximum degree of parallelism provided by the FPGA. The system reaches 350 and 270 VGA frames per second (fps) for the disparity and optical flow computations respectively in their mono-scale version and up to 32 fps for the multi-scale scheme extracting all the described features in parallel. In this work we also analyze the performance in accuracy and hardware resources of the proposed implementation.

# Summary. An optional shortened abstract.
summary: ""

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://www.sciencedirect.com/science/article/pii/S1051200412002369
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

