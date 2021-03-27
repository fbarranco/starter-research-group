+++
title = "Real-time architecture for a robust multi-scale stereo engine on FPGA"
date = 2016-08-01T17:44:35+01:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Matteo Tomasi", "Mauricio Vanegas", "Francisco Barranco", "Javier Díaz", "Eduardo Ros"]
    
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
publication = "IEEE Transactions on Very Large Scale Integration (VLSI) Systems"
publication_short = "IEEE Trans. on VLSI Syst."

# Abstract and optional shortened version.
abstract = "In this work, we present a real-time implementation of a stereo algorithm on field-programmable gate array (FPGA). The approach is a phase-based model that allows computation with sub-pixel accuracy. The algorithm uses a robust multi-scale and multi-orientation method that optimizes the estimation extraction with respect to the local image structure support. With respect to the state of the art, our work increases the on-chip power of computation compared to previous approaches in order to obtain a good accuracy of results with a large disparity range. In addition, our approach is specially suited for unconstrained environments applications thanks to the robustness of the phase information, capable of dealing with severe illumination changes and with small affine deformation between the image pair. This work also includes the rectification images circuitry in order to exploit the epipolar constraints on the chip. The dedicated circuit can rectify and process images of VGA resolution at a frame rate of 57 fps. The implementation uses a fine pipelined method (also with superscalar units) and multiple user defined parameters that lead to a high working frequency and a good adaptability to different scenarios. In the paper, we present different results and we compare them with state of the art approaches."
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
url_custom = [{name = "Journal", url = "http://ieeexplore.ieee.org/abstract/document/6071001/" }]

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

