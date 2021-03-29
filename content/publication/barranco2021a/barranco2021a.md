---
title: "Joint direct estimation of 3D geometry and 3D motion using spatio temporal gradients"
authors:
- admin
- Cornelia Fermuller
- Yiannis Aloimonos
- Eduardo Ros
author_notes:
- ""
date: "2021-09-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2020-01-01T00:00:00Z"

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["2"]

# Publication name and optional abbreviated publication name.
publication: "*Pattern Recognition*"
publication_short: ""

abstract: Conventional image-motion based methods for structure from motion first compute optical flow, then solve for the 3D motion parameters based on the epipolar constraint, and finally recover the 3D geometry of the scene. However, errors in optical flow due to regularization can lead to large errors in 3D motion and structure. This paper investigates whether performance and consistency can be improved by avoiding optical flow estimation in the early stages of the structure-from-motion pipeline, and it proposes a new direct method based on image gradients (normal flow) only. Our main idea lies in a reformulation of the positive-depth constraint – the basis for estimating egomotion from normal flow – as a continuous piecewise differentiable function, which allows the use of well-known minimization techniques to solve for 3D motion. 

# Summary. An optional shortened abstract.
summary: ""

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: https://www.sciencedirect.com/science/article/pii/S0031320320305628
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

