---
title: BIO-PERCEPTION - Next generation of smart vision systems for real-time processing with bio-inspired sensors 
summary: Our goal for this project is to set up the basis for a new generation of smart autonomous agents that are able to carry out 3D perception in real-time, using biologically-inspired vision sensors. These sensors independently processed all pixels and only trigger changes in the scene (events) in the case a substantial difference in the intensity luminance happens over time for a specific location (this happens only at object contours and textures). This allows for the reduction of the transmission of redundant information and hence, the data bandwidth. 

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
  url: https://github.com/JuanIsernGhosn/Smart-Grid-Surveillance-Server
url_code: ""
url_pdf: "https://arxiv.org/abs/2011.14416"
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
#  slides: example
---

## Summary
The 3D perception of our environment such as the estimation of image motion, 3D motion, or the 3D structure of unknown scenes, are tasks that humans efficiently do. In fact, we do it in a precise manner enabling us to navigate around our environment and interact with complex dynamic scenarios in a natural way. Despite of the advances in robotics, computational capacity, and computer vision, the current state of the art cannot provide efficient solutions that are even close in performance. It is consequence of the impossibility of closing perception-action cycles. Every action performed causes a change in the environment that the perception system needs to sense, to implement the next action accordingly. The key factor for the success of the current smart vision systems is not only the perception, or the execution of the correct action; it is the capacity of performing the whole loop in real-time to allow the continuous interaction. Conventional solutions propose the increase of the computational complexity, without taking into account factors such as the energy consumption, required resources, or processing time. The most advanced high-performance architectures have problems dealing with the amount of information generated by high-resolution cameras fast enough for enabling dynamic agents to interact in the real world (for example, state- of-the-art solutions take minutes for image motion estimation). Moreover, processing has to be local in order to respond to the real-time
demands.

Our goal for this project is precisely to set up the basis for a new generation of smart autonomous agents that are able to carry out 3D perception in real-time, using biologically-inspired vision sensors. These sensors are based on the manner visual information is processed by the human eye. Rather than transmitting all the static information continuously, the retina selects the most relevant information, comprising it to be further processed in the visual cortex. In the very same way, these sensors independently processed all pixels and only trigger changes in the scene ('events') in the case a substantial difference in the intensity luminance happens over time for a specific location (this happens only at object contours and textures). This allows for the reduction of the transmission of redundant information and hence, the data bandwidth. The other key advantage is that these sensors reach very low latencies, of a few microseconds.

The current paradigm for computation with this kind of sensors is still very basic. Usually, asynchronous events are accumulated during short prefixed time intervals to create synthetic images and then, classic methods are applied to them. Unfortunately, this causes the increase of latencies and it generates redundant information that has to be processed in the same manner systems for conventional sensors do. We propose in this project a novel paradigm for event-driven computation: 1) event-wise processing, for every event that comes in, the model is updated and the event information is integrated for a specific task, taking full advantage of the high-temporal
resolution and 2) only the relevant information is transmitted.

Finally, regarding the resources we will use hardware accelerators for massively parallel processing such as GPU or FPGAs that process huge amounts of data at once, guaranteeing bounded latencies and low energy consumption. This will also enable the integration of our system via embedded platforms.

## Objectives

BIO-PERCEPTION is focused on the development of a new paradigm for vision systems that integrates neuromorphic event-based sensors. Additionally, we propose the validation of this new model by building smart vision systems for autonomous navigation, proposing drones for that. Our specific objectives (SO) are detailed next:

*SO1. Development of a new model for event-based 3D perception.*
As mentioned before in the state of the art, some works have addressed the task previously with event-based sensors [BEN12, BEN14, BAR14]. However, their results are still very poor, reaching only low performance. Moreover, most of these methods build images out of accumulation of events for prefixed time intervals and apply classic methods to these artificial images. This severely harms the performance and does not take advantage of the main feature of these sensors, their high-temporal resolution or low latency.
We propose the development and evaluation of a fully event-driven model, although it will also include the possibility of integrating conventional synchronous images to improve accuracy. The models for motion object contours will be applied here [FER01, BAR14], to estimate the image motion. Using the image motion, 3D pose and velocity can also be subsequently estimated [FER01, BAR16] and, independently moving objects (IMOs) detected in the scene. Lastly, the accuracy of our solution will be evaluated using novel benchmarks and datasets that integrate both events and images. 

*SO2. Development of a new model for event-based object segmentation.* 
Although the 3D perception module provides sparse results, object segmentation is an image-based task, which implies the need for a centralized model of the scene. In SO2, our first goal is to come up with a linking mechanism to group events and be able to distinguish different depth layers (separated by contours). Our group has already developed some models such as in [BAR15b] that could not reach real-time performance or the required accuracy. Given the popularity of Machine Learning approaches and the expertise of our Department in efficient machine learning applications, we will consider the use of Deep Learning, to develop architectures based on CNNs (Convolutional Neural Networks). These networks have proven their success in this task for images [SHE15]. After separating events from contours and events generated due to the textured regions of the objects in the scene, we will group them together in sets according to the object these events belong to. We also propose the implementation of an efficient mechanism to do that. As in SO1, we will produce new benchmarks and datasets to assess the accuracy of our models, and compare conventional and event-based approaches. 

*SO3. Real-time processing architectures with event-based neuromorphic sensors.*
In the motivation we already stated that autonomy cannot be reached until perception-action loops are closed in real-time. This means that the visual perception processing should be fast enough to allow agents to interact with the dynamic real-world. Moreover, in order to embed the visual processing in our autonomous agents, we should consider platforms to integrate our processing architectures on. In order to do that, we propose the use of hardware accelerators. Our group has long expertise on optimized-CPU implementations, and GPUs, or FPGAs [BAR14b, NAV17]. Also, we will consider integrated solutions with the existing UAV platforms and their embedded processors. Models and implementations designed according to SO1 and SO2 will be adapted to the non-functional requirements related to performance, latency, or memory imposed by the selected architecture.

*SO4. Demonstrator: Autonomous drone platform.*
Finally, we also consider that the validation of the proposed models has to be shown in the framework of autonomous navigation tasks. This application allows us to demonstrate the maximum potential of the neuromorphic sensors, specifically regarding the high-temporal resolution and low latency, for example with high-speed maneuvers. Our goal in SO4 is to develop a first semi-autonomous platform that shows navigation with a minimum intervention of a human pilot for the first case, and that validates tasks such as selection of targets, segmentation, or detection of independently moving objects while navigating. The second prototype will show the whole system working to do tasks completely autonomously, without human intervention, while navigating avoiding obstacles.

## Bibliography
* [BAR14a] F. Barranco, C. Fermüller, Y. Aloimonos. "Contour motion estimation for asynchronous event-driven cameras." Proceedings of the IEEE 102, no. 10 (2014): 1537-1556.
* [BAR14b] F. Barranco, J. Diaz, B. Pino, E. Ros. "Real-time visual saliency architecture for FPGA with top-down attention modulation." IEEET on Ind. Informatics 10, 3, 726-1735, 2014.
* [BAR15] F. Barranco, C. Fermuller, Y. Aloimonos. "Bio-inspired motion estimation with event-driven sensors." In International Work-Conference on Artificial Neural Networks, pp. 309-321, 2015.
* [BAR16] F. Barranco, C. Fermuller, Y. Aloimonos, T. Delbruck. "A dataset for visual navigation with neuromorphic methods." Frontiers in neuroscience 10 (2016): 49.
* [BEN12] R. Benosman, S. Ieng, C. Clercq, C. Bartolozzi, M. Srinivasan. "Asynchronous frameless event-based optical flow." Neural Networks 27 (2012): 32-37.
* [BEN14] R. Benosman, C. Clercq, X. Lagorce, S. Ieng, C. Bartolozzi. "Event-based visual flow." IEEE transactions on neural networks and learning systems 25, no. 2 (2014): 407-417.
* [FER01] C. Fermüller, D. Shulman, Y. Aloimonos. "The statistics of optical flow." Computer Vision and Image Understanding 82, no. 1 (2001): 1-32.
* [NAV17] F. Naveros, J. Garrido, R. Carrillo, E. Ros, N. Luque. "Event-and time-driven techniques using parallel CPU-GPU co-processing for spiking neural networks." Front. in Neuroinf. 11 (2017): 7.
* [SHE15] W. Shen, X. Wang, Y. Wang, X. Bai, Z. Zhang. "Deepcontour: A deep convolutional feature learned by positive-sharing loss for contour detection." CVPR, pp. 3982-3991. 2015.

## Lists of contributions: publications, datasets, and code repositories

* Isern, J., F. Barranco, D. Deniz, J. Lesonen, J. Hannuksela, R. R. Carrillo. **Reconfigurable cyber-physical system for critical infrastructure protection in smart cities via smart video-surveillance.** Pattern Recognition Letters 140 (2020): 303-309. [PDF](https://arxiv.org/abs/2011.14416) [CODE](https://github.com/JuanIsernGhosn/Smart-Grid-Surveillance-Server)
* Déniz, D., G. Jimenez-Perera, R. Nolasco, J. Corral, F. Barranco. **Deep multimodal habit tracking system: A user-adaptive approach for low-power embedded systems.** Submitted (2022).
* Isern, J., G. Jimenez-Perera, L. Medina-Valdés, P. Chaves, D. Pampliega, F. Ramos, F. Barranco. **A Cyber-Physical System for integrated remote control andprotection of smart grid critical infrastructures.** Submitted (2022).

## Authors

* **Francisco Barranco** - *University of Granada*
Please report problems, bugs, or suggestions to fbarranco_at_ugr_dot_es (Replace _at_ by @ and _dot_ by .).

## Acknowledgments

* This work was supported by the AEI through the grant PID2019-109434RA-I00 / AEI / 10.13039/501100011033.

{{< figure src="aei_logo.jpeg" id="AEI_logo" >}}

## License

Copyright (C) 2018 Francisco Barranco, 01/09/2018, University of Granada.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details. 

You should have received a copy of the GNU General Public License along with this program.  If not, see <http://www.gnu.org/licenses/>.
