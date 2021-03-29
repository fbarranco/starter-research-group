---
title: "Contour motion estimation for asynchronous event-driven cameras"
authors:
- Francisco Barranco
- Cornelia Fermüller
- Yiannis Aloimonos
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
publication: "*Proceedings of the IEEE*"
publication_short: ""

abstract: This paper compares image motion estimation with asynchronous event-based cameras to Computer Vision approaches using as input frame-based video sequences. Since dynamic events are triggered at significant intensity changes, which often are at the border of objects, we refer to the event-based image motion as “contour motion.” Algorithms are presented for the estimation of accurate contour motion from local spatio-temporal information for two camera models, the dynamic vision sensor (DVS), which asynchronously records temporal changes of the luminance, and a family of new sensors which combine DVS data with intensity signals. These algorithms take advantage of the high temporal resolution of the DVS and achieve robustness using a multiresolution scheme in time. It is shown that, because of the coupling of velocity and luminance information in the event distribution, the image motion estimation problem becomes much easier with the new sensors which provide both events and image intensity than with the DVS alone. Experiments on synthesized data from computer vision benchmarks show that our algorithm on combined data outperforms computer vision methods in accuracy and can achieve real-time performance, and experiments on real data confirm the feasibility of the approach. Given that current image motion (or so-called optic flow) methods cannot estimate well at object boundaries, the approach presented here could be used complementary to optic flow techniques, and can provide new avenues for computer vision motion research

# Summary. An optional shortened abstract.
summary: ""

tags:
- Source Themes
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: http://ieeexplore.ieee.org/abstract/document/6895239/
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

