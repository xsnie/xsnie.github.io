---
layout: paper
categories: papers
permalink: papers/predtoken
id: predtoken
title: "PredToken: Predicting Unknown Tokens and Beyond with Coarse-to-Fine Iterative Decoding"
feature-title: PredToken
authors: 
  - Xuesong Nie
  - Haoyuan Jin
  - Yunfeng Yan
  - Xi Chen
  - Zhihang Zhu
  - Donglian Qi
first-author: true
venue: IEEE/CVF Conference on Computer Vision and Pattern Recognition
venue-shorthand: CVPR
location: Seattle WA, USA
year: 2024
url: /papers/predtoken
pdf: https://openaccess.thecvf.com/content/CVPR2024/papers/Nie_PredToken_Predicting_Unknown_Tokens_and_Beyond_with_Coarse-to-Fine_Iterative_Decoding_CVPR_2024_paper.pdf#/
code: /papers/predtoken
type: conference
figure: /images/papers/predtoken.png
doi: 10.1016/j.patcog.2024.110470
selected: true
feature-description: PredToken can generate high-quality images and videos using a coarse-to-fine manner
image: /images/featured/predtoken.png
featured: true
feature-order: 0
coming-soon: false
bibtex: |-

    @inproceedings{nie2024predtoken,
        title={PredToken: Predicting Unknown Tokens and Beyond with Coarse-to-Fine Iterative Decoding},
        author={Xuesong Nie and Haoyuan Jin and Yunfeng Yan and Xi Chen and Zhihang Zhu and Donglian Qi},
        booktitle={IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
        year={2024}
    }
---

Predictive learning models, which aim to predict future frames based on past observations, are crucial to constructing world models. 
These models need to maintain low-level consistency and capture high-level dynamics in unannotated spatiotemporal data. 
Transitioning from frame-wise to token-wise prediction presents a viable strategy for addressing these needs. 
How to improve token representation and optimize token decoding presents significant challenges. 
This paper introduces PredToken, a novel predictive framework that addresses these issues by decoupling space-time tokens into distinct components for iterative cascaded decoding. 
Concretely, we first design a "decomposition, quantization, and reconstruction" schema based on VQGAN to improve the token representation. 
This scheme disentangles low- and high-frequency representations and employs a dimension-aware quantization model, allowing more low-level details to be preserved. 
Building on this, we present a "coarse-to-fine iterative decoding" method. It leverages dynamic soft decoding to refine coarse tokens and static soft decoding for fine tokens, enabling more high-level dynamics to be captured. 
These designs make PredToken produce high-quality predictions. Extensive experiments demonstrate the superiority of our method on various real-world spatiotemporal predictive benchmarks. 
Furthermore, PredToken can also be extended to other visual generative tasks to yield realistic outcomes.