+++
title = "Pipelined architecture for real-time cost-optimized extraction of visual primitives based on FPGAs"
date = 2016-08-01T17:44:35+01:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Francisco Barranco", "Matteo Tomasi", "Javier Díaz", "Mauricio Vanegas", "Eduardo Ros"]
    
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
publication = "Digital Signal Processing"
publication_short = "Dig. Sig. Proc."

# Abstract and optional shortened version.
abstract = "This paper presents an architecture for the extraction of visual primitives on chip: energy, orientation, disparity, and optical flow. This cost-optimized architecture processes in real time high-resolution images for real-life applications. In fact, we present a versatile architecture that may be customized for different performance requirements depending on the target application. In this case, dedicated hardware and its potential on-chip implementation on FPGA devices become an efficient solution. We have developed a multi-scale approach for the computation of the gradient-based primitives. Gradient-based methods are very popular in the literature because they provide a very competitive accuracy vs. efficiency trade-off. The hardware implementation of the system is performed using superscalar fine-grain pipelines to exploit the maximum degree of parallelism provided by the FPGA. The system reaches 350 and 270 VGA frames per second (fps) for the disparity and optical flow computations respectively in their mono-scale version and up to 32 fps for the multi-scale scheme extracting all the described features in parallel. In this work we also analyze the performance in accuracy and hardware resources of the proposed implementation."
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
url_custom = [{name = "Journal", url = "https://www.sciencedirect.com/science/article/pii/S1051200412002369" }]

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

