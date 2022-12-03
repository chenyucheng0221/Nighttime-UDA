## Refign: Align and Refine for Adaptation of Semantic Segmentation to Adverse Conditions

#### Research Question
How to leverage intermediate domain as a reference to improve the predictions of the target domain images?


#### Motivation
1. There a large body of reseach keen on the unsupervised domain adaptation to adapte the labeled source domain to different unlabeled target domain. Our work is the extension of UDA methods to enhance the performance of current approaches.
2. There is an issue of noisy propagation in previous UDA methods, which results in a drift in pseudo-labels. The issue could lead an overfitting problem in large neural networks so that the generalization performance would be degraded. This is issue would be tackled in this work.

#### Methodology

- **Overall Goal**
  **Source domain:** CityScapes
  
  **Intermediate domain (Reference):** normal-condition images of ACDC (share the content and region characteristic with target domain, share the weather and time with source domain)
  
  **Target domain:** adverse-condition images of ACDC
  
  **Goal:** Leverage normal-condition images overlapped with source and target domain as reference to imporove the predictions of target domain images.
  
  *TN: This method highly relies on the reference image and the accuracy of the predicted pseudo-labels, but the reference image is synthesized by combining the scenes from target domain and illumination style from source domain, such combination may not completely simulate the real-world scenes.*

- **Framework**

  The framework consists of two modules: the alignment module and the refinement module
  
  ![image](../Image/Refign-Framework.png)

- **HighLight**

  **Alignment Module:**
  
  Spatial alignment of the target image and intermediate image is the preliminary condition for the latter refinement. Here introducing a warp component to achieve it.
  
  **Refinement Module:**
  
  The refinement module refines the pseudo-labels to mitigate the confirmation bias issue. The input of refinement module comes from the output of the alignment module: aligned reference class probabilities and the mactching confidence map.
  
#### Experiment

#### Acceptance Reason


#### Inspiration
In our work, the content and illumination gap should be considered at the same time, and the multi-step DA method would be exploited. During the multi-step process, the refinement mechanism can be considered.
