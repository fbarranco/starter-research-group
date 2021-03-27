+++
title = "Contour motion estimation for asynchronous event-driven cameras"
date = 2016-08-01T17:44:35+01:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Francisco Barranco", "Cornelia Fermüller", "Yiannis Aloimonos"]
    
# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "Proceedings of the IEEE"
publication_short = "Proc. of the IEEE"

# Abstract and optional shortened version.
abstract = "This paper compares image motion estimation with asynchronous event-based cameras to Computer Vision approaches using as input frame-based video sequences. Since dynamic events are triggered at significant intensity changes, which often are at the border of objects, we refer to the event-based image motion as “contour motion.” Algorithms are presented for the estimation of accurate contour motion from local spatio-temporal information for two camera models: the dynamic vision sensor (DVS), which asynchronously records temporal changes of the luminance, and a family of new sensors which combine DVS data with intensity signals. These algorithms take advantage of the high temporal resolution of the DVS and achieve robustness using a multiresolution scheme in time. It is shown that, because of the coupling of velocity and luminance information in the event distribution, the image motion estimation problem becomes much easier with the new sensors which provide both events and image intensity than with the DVS alone. Experiments on synthesized data from computer vision benchmarks show that our algorithm on combined data outperforms computer vision methods in accuracy and can achieve real-time performance, and experiments on real data confirm the feasibility of the approach. Given that current image motion (or so-called optic flow) methods cannot estimate well at object boundaries, the approach presented here could be used complementary to optic flow techniques, and can provide new avenues for computer vision motion research."
abstract_short = ""

# Featured image thumbnail (optional)
image_preview = ""

# Is this a selected publication? (true/false)
selected = true

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = [""]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []

# Links (optional).
url_pdf = ""
url_preprint = ""
url_code = ""
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""
url_custom = [{name = "Journal", url = "http://ieeexplore.ieee.org/abstract/document/6895239/" }]

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Custom Link", url = "http://example.org"}]

# Does this page contain LaTeX math? (true/false)
math = false

# Does this page require source code highlighting? (true/false)
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++

