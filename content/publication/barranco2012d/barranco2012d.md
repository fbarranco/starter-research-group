---
title: "Parallel architecture for hierarchical optical flow estimation based on FPGA"
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
publication: "*IEEE Transactions on Very Large Scale Integration (VLSI) Systems*"
publication_short: ""

abstract: In this work, we present a real-time implementation of a stereo algorithm on field-programmable gate array (FPGA). The approach is a phase-based model that allows computation with sub-pixel accuracy. The algorithm uses a robust multi-scale and multi-orientation method that optimizes the estimation extraction with respect to the local image structure support. With respect to the state of the art, our work increases the on-chip power of computation compared to previous approaches in order to obtain a good accuracy of results with a large disparity range. In addition, our approach is specially suited for unconstrained environments applications thanks to the robustness of the phase information, capable of dealing with severe illumination changes and with small affine deformation between the image pair. This work also includes the rectification images circuitry in order to exploit the epipolar constraints on the chip. The dedicated circuit can rectify and process images of VGA resolution at a frame rate of 57 fps. The implementation uses a fine pipelined method (also with superscalar units) and multiple user defined parameters that lead to a high working frequency and a good adaptability to different scenarios. In the paper, we present different results and we compare them with state of the art approaches.

# Summary. An optional shortened abstract.
summary: ""

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: http://ieeexplore.ieee.org/abstract/document/5772045/
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

