## Guided Curriculum Model Adaptation and Uncertainty-Aware Evaluation for Semantic Nighttime Image Segmentation

#### Research Question
How to adapt daytime semantic segmentation models to unlabeled nighttime images and address the uncertainty on invalid regions in nighttime images?

(Method + Evaluation)

#### Motivation
1. Inspired by adding intermediate domain between the source and target because of the continuous changing environment illumination, extend this idea to add shared content which can provide as the guidance to help the knowledge transfer from a favorable condition to an adverse condition.
2. Because the adverse condition in nighttime images, there are some regions are hard to determine even by human vision, to make model roubust, it should have the ability to predict invalid regions with high uncertainty while being confident in determining valid regions. However, the invalid regions determination is excluded in existing methods.

#### Framework

- **Overall Goal**

  **Source domain:** in daytime

  **Intermediate domain:** in twilight time (an intermediate level of darkness between source and target)

  **Target domain:** in nighttime
  
  **Goal:** adapt daytime models to nighttime without nighttime annotations and evaluate the substantial uncertainty of semantics in nighttime images.

- **Framework**


- **HighLight**

#### Good Expression
1. since having the vision system declare a prediction as invalid can help the downstream driving system avoid the fatal consequences of this prediction being false
