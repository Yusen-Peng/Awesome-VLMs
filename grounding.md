# Grounding

- [x] CVPR 2024: [AlphaCLIP](https://arxiv.org/abs/2312.03818)
  - motivation: focusing on the regions of interest matters for fine-grained understanding
  - contribution: 
    - datasets with more fine-grained region-text pairs
    - image encoder with an additional alpha channel
    - ![alt text](figures/AlphaCLIP.png)

- [X] ICLR 2024: [KOSMOS-2](https://arxiv.org/abs/2306.14824)
  - motivation: add grounding capability to multimodal large language models
  - contribution: curate a dataset (GRIT) with referring expression - bounding box pairs
  - ![alt text](figures/GRIT.png)
  - add location tokens (to indicate bounding boxes) during training
  - ![alt text](figures/KOSMOS-2.png)

- [x] CVPR 2022: [GLIP](https://arxiv.org/abs/2112.03857)
  - motivation: object-level (instead of image-level from CLIP) visual representations are needed
  - contribution:
    - reframe object detection as phrase grounding
    - replace the classification loss in object detection with alignment loss
      - alignment score: ![alt text](figures/alignment_loss.png)
    - ![alt text](figures/GLIP.png)
    - deep fusion: ![alt text](figures/deep_fusion.png)
