# Hallucination

- [ ] NAACL 2025: [Image Token Attention-Guided Decoding](https://aclanthology.org/2025.naacl-long.75/)


- [x] ICML 2025: [MARINE](https://arxiv.org/abs/2402.08680)
  - motivation:  training/fine-tuning too costly, how about **training-free**?
  - contribution: 
    - integrates additional object detection models as toolbox to provide image-grounded guidance prompt
    - Only objects with relatively high probabilities in **both branches** could appear at top when sampling
      - why both? This strikes a balance between a better ability to follow instructions and the increased accuracy and detail in image descriptions
  - ![alt text](/figures/marine.png)


- [x] ACL finding 2025: [Hallucination-targeted DPO](https://arxiv.org/abs/2411.10436)
  - contribution:
    - develop three types of pairwise samples specifically targeting hallucination issues
      - Visual Distracted Hallucination: corrupt the image by pruning tokens with higher attention scores
      - Long Context Hallucination: truncate the last two sentences and **use as prefix** to **continue** generating text
      - Multimodal Conflict Hallucination: use GPT to **prepend** text that conflicts with the image **in front of** normal questions
      - ![alt text](/figures/HDPO.png)

- [x] EMNLP finding 2024: [V-DPO](https://aclanthology.org/2024.findings-emnlp.775/)
  - DPO basics:
  - ![alt text](/figures/DPO_basics.png)
  - contribution:
    - curate a synthetic dataset of both **response-contrast** and **image-contrast** preference pairs
    - preference learning objective = reward - KL divergence from reference model + KL divergence from **answering WITHOUT images**
    - ![alt text](/figures/V-DPO.png)
  
- [ ] CVPR 2024: [Hallucination Augmented Contrastive Learning](https://arxiv.org/abs/2312.06968)

