---
title: BRAINAV - BRAIn-inspired visual processing for real-time
energy-efficient autonomous NAVigation 
summary: BRAINAV builds on the integration of visual processing pipelines for energy-efficient edge processing using neuromorphic strategies, for the application of autonomous navigation. First, visual processing is crucial in perception system components and specifically, for scene awareness in navigation applications. Robotic agents require understanding their context to plan and make decisions accordingly. This is even more relevant in applications such as robotics. However, computer vision is a very demanding task in terms of resources, and effective navigation requires low latencies to close perception-action loops in real-time. Second, regarding 3D perception and scene understanding, state-of-the-art solutions are focused on accuracy performance but other qualities such as energy consumption must be also taken into account. 

tags:
- Neuromorphic
- Real-time systems
- Autonomous navigation
- Drones
- Machine Learning
- Computer vision

date: "2021-12-20T00:00:00Z"

authors:
- Francisco Barranco

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: ""
  focal_point: Smart

links:
- icon: github
  icon_pack: fab
  name: Visit
  url: https://github.com/DaniDeniz/IndoorActionDataset
url_code: ""
url_pdf: "https://doi.org/10.3390/electronics13234786"
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#  slides: example
---

* This work was supported by the National Project PID2022-141466OB-I00 funded by MICIU/AEI/10.13039/501100011033 and by ERDF/EU.
{{< figure src="aei_logo.png" id="AEI_logo" >}}

## Summary
BRAINAV aims at developing bio-inspired pipelines for real-time energy-efficient visual navigation that operates in the real-world in optimized platforms embedded onboard mobile robots. First, we need the development of a new paradigm for computer vision that allows us to effectively work with asynchronous neuromorphic sensors that imitate visual retinas and the development of high-performance architectures for reaching real-time performance with them. Then, we also require efficient ML networks for reaching low-energy inference and eventually, to propose new bio-inspired components to solve mapping, localization, and path planning for exploration. We are committed to prove the potential of our energy-efficient vision pipelines and therefore, we propose the use case of autonomous navigation using mobile robots.

Video processing is crucial in perception due for environment understanding. However, computer vision is a very demanding task and in robotics it requires to close perception-action loops in real-time. Moreover, distributed local mobile nodes need low-energy operation since they run on batteries. Power consumption vs. performance is a challenging trade-off, especially in distributed environments, given the number of sensors, the heterogeneity of the system, their autonomy or their need of high performance. Our hypothesis is that biologically-inspired strategies will help us achieve energy-efficient solutions that reach good levels of accuracy while operating in real-time in real
scenarios.


## Objectives

The main general objective of BRAINAV is the development of a bio-inspired pipeline for real-time
energy-efficient visual navigation that operates in the real-world in optimized platforms embedded in
mobile robots. First, we need the development of a new paradigm for computer vision that allows us
to effectively work with these asynchronous neuromorphic sensors and the development of high-
performance architectures for reaching real-time performance. Then, we also require efficient ML
networks for reaching low-energy inference and eventually, to propose new bio-inspired components
to solve mapping, localization, and path planning for exploration. Finally, we also propose to prove
the potential of our energy-efficient vision pipelines for autonomous navigation using mobile robots.

Our specific objectives (SO) are detailed next:

*SO1. To develop of event-driven perception for navigation tasks.*
As mentioned before in the state of the art, some works have addressed the task previously with event-
based sensors [BAR14a, BAR21, VID18]. However, their results are still very poor, reaching only low
performance. In our previous work, we have thoroughly studied alternative knowledge-based methods
for 3D perception, mainly image motion and 3D motion estimation. In BRAINAV, we
propose to study new methods based on Machine Learning solutions [DEN23, ISE23] to achieve
better accuracy performance. Also, most of the previous methods build images out of accumulation of
events for prefixed time intervals and apply classic methods to these artificial images. This severely
harms the performance and does not take advantage of the main feature of neuromorphic sensors, their
high-temporal resolution or low latency. We propose the development and evaluation of event-driven
methods for motion and 3D geometry estimation [BAR21]. Lastly, the accuracy of our solution will be
evaluated using novel benchmarks and datasets that integrate both events and images using the motion
capture system available in our lab. Moreover, we are committed to the Open Science principles and
will release the datasets for the community. This is crucial for the adv ancement of neuromorphic
engineering, due the current lack of datasets and their relevance for Machine Learning techniques.

*SO2. To optimize for real-time energy-efficient processing engines.*
In an effort to reduce the computational complexity of the prop osed solutions, we will explore
different mechanisms for low-energy computation. First, we propose the use of optimization
techniques on ANNs such as: model quantization [LIA21] shortening bit widths for inference to reduce
computational complexity; pruning [VAD22], that removes connections with smaller values in
networks; and distillation [DEN23], that allows transferring knowledge from teacher complex models
to student simpler ones. Second, we are also interested in exploring new techniques based on Spiking
Neural Networks. These are biologically-plausible neural architectures do take into account energy
consumption [DAV21] doing learning with sparse data. We also propose the exploration of brain-like
structures to build new navigation methods that imitate their functionalities. 

*SO3. To implement real-time processing on embedded platforms with neuromorphic sensors.*
Dealing with a real-world application imposes restrictions such as real-time performance for closing
our perception-action loops for autonomous navigation. We will consider different hardware
accelerators such as GPUs or FPGAs, using the latest advancements for the development of fine-
tuning pipelines (e.g. DeepStream) and for optimized hardware datapaths (e.g. Vitis AI). The selected
hardware accelerator will impose different non-functional requirements on the implementations
developed for SO1 and functionally optimized for SO2, for performance, latency and power
consumption. This objective also pursues the effective integration of the asynchrono us sensors into
von Neumann architectures which is by itself, an additional challenge.

*SO4. To demonstrate embedded autonomous navigation onboard mobile robots*
Finally, this objective aims at the validation of the proposed models and architectures considered in
the SO1-SO3, with different demonstrators for autonomous navigation tasks in real-world
environments. This application allows us to demonstrate the maximum potential of our optimized bio-
inspired pipelines and downstream processing, while ensuring the overall optimization in the
exploration task relying mainly on learning models. Our goal in SO4 is to develop a first semi-
autonomous platform to perform first localization and mapping. This prototype will have a minimum
intervention of a human pilot, and will be used to validate the mentioned tasks in unknown scenarios.
The second prototype will show the final autonomous explorer that will be enabled with additional
downstream applications such as the detection of other mobile robots in the scenario and possibly
tracking them, or finding specific targets.


## Bibliography
[BAR14a] F. Barranco, C. Fermüller, Y. Aloimonos. "Contour motion estimation for asynchronous event-driven cameras." Proceedings of the IEEE 102, no. 10 (2014): 1537-1556.
[BAR21] F. Barranco, C. Fermüller, Y. Aloimonos, E. Ros. "Joint direct estimation of 3D geometry and 3D motion using spatio temporal gradients." Pattern Recognition, 113, 2021.
[DAV21] S. Davidson, S. B. Furber. "Comparison of artificial and spiking neural networks on digital hardware." Frontiers in Neuroscience 15 (2021): 651141.
[DEN23] D. Deniz, J. Isern, J. Solanti, P. Jääskeläinen, P. Hnětynka, L. Bulej, E. Ros, F. Barranco. "Efficient reconfigurable CPS for monitoring the elderly at home via Deep Learning." Journal of Signal Processing Systems, (2023). 
[ISE23] J. Isern, G. Jimenez-Perera, L. Medina-Valdés, P. Chaves, D.Pampliega F. Ramos, F. Barranco. "A Cyber-Physical System for integrated remote control and protection of smart grid critical infrastructures.", Journal of Signal Processing Systems, 2023.
[LIA21] T. Liang, J. Glossner, L. Wang, S. Shi, X. Zhang. "Pruning and quantization for deep neural network acceleration: A survey." Neurocomputing 461 (2021): 370 -403.
[VAD22] S. Vadera, S. Ameen. "Methods for pruning deep neural networks." IEEE Access 10 (2022): 63280-63300.
[VID18] A. Vidal, H. Rebecq, T. Horstschaefer, D. Scaramuzza. "Ultimate SLAM? Combining events, images, and IMU for robust visual SLAM." IEEE Robotics and Automation 3, no. 2 (2018).

## Lists of contributions: publications, datasets, and code repositories

* [DEN24] Deniz, D., Ros, E., Ortigosa, E. M., & Barranco, F. (2024). **Optimized edge-cloud system for activity monitoring using knowledge distillation.** Electronics, 13(23), 4786, https://doi.org/10.3390/electronics13234786 [PDF](https://digibug.ugr.es/bitstream/handle/10481/97862/electronics-13-04786.pdf?sequence=1&isAllowed=y) [CODE](https://github.com/DaniDeniz/IndoorActionDataset) [DATA](https://github.com/DaniDeniz/IndoorActionDataset)
* [NOV24] Novo, A., Lobon, F., Garcia de Marina, H., Romero, S., & Barranco, F. (2024). **Neuromorphic perception and navigation for mobile robots: a review.** ACM Computing Surveys, 56(10), 1-37. https://doi.org/10.1145/3656469 [PDF](https://doi.org/10.3389/fnins.2023.1160034) 

* [NOV25] Novo, A., Fermuller, C., Rodríguez-Álvarez, M., Romero, S., & Barranco, F. (2025). **On ego-motion estimation from event-inertial-aided normal flow fields.** Neuromorphic Computing and Engineering IOP, Under Review (second)
* [DEN25] Deniz, D., Ros, E., Ortigosa, E. M., & Barranco, F. (2025). **Efficient reconfigurable system for home monitoring of the elderly via action recognition.** Engineering Applications of Artificial Intelligence, Under Review (second)
* [SAL25] Salinas, I., Deniz, D., Fermüller, C., Novo, A., & Barranco, F. (2025). **Event-based vision for online inference of fine-grained manipulation actions.** Nature Communications. Under Review
* [JIM25] Jimenez-Perera, G., Valencia-Vidal, B.,  Luque, N. R., Ros, E., & Barranco, F. (2025). **Informed federated learning to train robotic arm inverse dynamic model.** IEEE Robotics and Automation Letters, Under review


## Authors

* **Francisco Barranco** - *University of Granada*
Please report problems, bugs, or suggestions to fbarranco_at_ugr_dot_es (Replace _at_ by @ and _dot_ by .).

## Acknowledgments

* This work was supported by the National Project PID2022-141466OB-I00 funded by MICIU/AEI/10.13039/501100011033 and by ERDF/EU.
{{< figure src="aei_logo.png" id="AEI_logo" >}}

## License

Copyright (C) 2018 Francisco Barranco, 01/09/2018, University of Granada.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. 

You should have received a copy of the GNU General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>.

