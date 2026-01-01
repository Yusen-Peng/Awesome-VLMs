# Efficiency

- [x] CVPR 2024: [Cluster Masking](https://arxiv.org/abs/2405.08815)
  - contribution: mask **random clusters** of visually similar image patches when training contrastive vision-language models
    - Choosing clusters: instead of using K-means, they simply randomly select **anchor patches** from the image, calculate the pairwise distances among all patches, in which clusters formed within a distance threshold are masked out.
    - ![alt text](/figures/cluster_masking.png)

- [x] CVPR 2023: [FLIP](https://arxiv.org/abs/2212.00794)
  - motivation: efficiency speedup during contrastive pretraining
  - contribution: simply mask many image tokens
    - ![alt text](/figures/FLIP.png)

- [x] ICML 2023: [BLIP-2](https://arxiv.org/abs/2301.12597)
  - motivation: vision-language alignment is challenging if LLM is frozen
  - contribution:
    - first stage
      - Q-Former consists of **two transformer submodules** that share the same self-attention layers
      - have **queries** (i.e., a set of learnable embeddings) to extract visual representation most relevant to the text
      - ![alt text](/figures/Q_former_first_stage.png)
    - second stage
      - FC (i.e., projector) to project query embeddings *Z* into the same dimension as the text embedding of the LLM
      - decoder-based LLMs (e.g. caption) encoder-decoder-based LLMs (soft visual prompts + prefix text)
      - ![alt text](/figures/Q_former_second_stage.png)

- [x] ACL findings 2023: [EfficientVLM](https://aclanthology.org/2023.findings-acl.873/)
  - contribution: distilling then pruning
    - distilling: 
      - vision language pre-training loss (L-VLM): contrastive loss + matching loss + masked language modeling loss + bounding box prediction loss
      - distillation loss: L-VLM + MSE of (attention distill + hidden states distill + logits distill)
    - modal-adaptive pruning with a random binary variable **z**: 
      - a differentiable approximation of **L0** regularization to measure the effective size of the pruned model
    - ![alt text](/figures/EfficientVLM.png)

- [x] ECCV 2022: [Tip-Adapter](https://arxiv.org/abs/2111.03930)
  - motivation: inherits CLIP’s training-free advantage
  - contribution:
    - construct a KV cache to serve as "few-shot knowledge"
    - combine CLIP original zero-shot **text classifier** with **domain-specific** cache logits
    - ![alt text](/figures/tip_adapter.png)
