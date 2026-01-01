# Hallucination

- [x] ICML 2025: [MARINE](https://arxiv.org/abs/2402.08680)
  - motivation: combat object hallucination
  - contribution: 
    - integrates additional object detection models as toolbox to provide image-grounded guidance prompt
    - Only objects with relatively high probabilities in **both branches** could appear at top when sampling
      - why both? This strikes a balance between a better ability to follow instructions and the increased accuracy and detail in image descriptions
  - ![alt text](figures/marine.png)


- [x] EMNLP finding 2024: [V-DPO](https://aclanthology.org/2024.findings-emnlp.775/)
  - contribution:
    - curate a synthetic dataset of both **response-contrast** and **image-contrast** preference pairs
    - preference learning objective = reward - KL divergence from reference model + KL divergence from **answering WITHOUT images**
    - ![alt text](figures/V-DPO.png)