## Cross-Domain Correlation Distillation for Unsupervised Domain Adaptation in Nighttime Semantic Segmentation

#### Research Question

How to reduce the gap of illumination, content and style between daytime and nighttime images by knowledge distillation method?

#### Motivation
1. Existing methods have the issue of ignoring the inherent difference between the daytime and nighttime images, which consider both of them contain the same style. However, the appearance discrenpancy has a significant impact on the effect of adaptation.
2. Inspired by knowledge distillation, if the synthetic nighttime images in source domain is created by the content from daytime images of source domain and illumination style from nighttime images of target domain. Based on this, it ensures that the degree of difference between daytime and nighttime images in source domian is consistent with that in target domain. Then the domian shift between daytime and nighttime images in both source and targe domain can be used as the knowldge to be distilled from multi-source domain to multi-target domain.

#### methodology

- **Overall Goal**

- **Framework**
