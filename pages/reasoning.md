# Reasoning

- [x] preprint 2025 [Path-Select Optimization](https://arxiv.org/abs/2512.06258)
  - motivation:
    - study reasoning path failures even though the answer is correct
  - basics: DPO versus GRPO
    - DPO: “Given two answers, push the **winner** above the loser.”
    - GRPO: “Given a group of answers, push the **above-average** ones up.”
  - contribution:
    - first stage: GRPO with format reward and answer reward
    - second stage: 
      - reasoning-aware reward: rule-based outcome reward + thinking reward
      - Negative Replay Memory (NRM): helping the model “remember its errors”
      - preference collection: online DPO
  - ![alt text](/figures/PSO.png)

- [X] Neurips-W 2025 [Think with Visual Abstract](https://arxiv.org/abs/2505.20164)
  - motivation:
    - images but often include redundant information -> potentially downgrades multimodal reasoning performance
  - contribution:
    - converts input images into into visual abstracts (e.g., contour, sketch, binarization)
    - ![alt text](/figures/VAT.png)

- [x] ICLR 2024: [Rephrase, Augment, Reason](https://arxiv.org/abs/2310.05861)
  - simple gradient-free framework: extract visual details, **augment questions**, and scoring the best answer
    - detail 1: salient question entities
    - detail 2: world knowledge and implicit reationale
    - detail 3: captions
  - ![alt text](/figures/RAR.png)
  
- [x] EMNLP 2024: [Whiteboard-of-Thought](https://aclanthology.org/2024.emnlp-main.1117/)
  - Whiteboard-of-thought prompting provides multimodal large language models with a metaphorical ‘whiteboard’ to draw out reasoning steps as images
  - ![alt text](/figures/Whiteboard-of-Thought.png)

