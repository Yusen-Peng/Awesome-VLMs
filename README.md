# Awesome VLMs

a structured awesome list of VLMs with my notes.

## General surveys

- [ ] ["Exploring the Frontier of Vision-Language Models: A Survey of Current Methodologies and Future Directions"](https://arxiv.org/abs/2404.07214) by Ghosh et al. 2024
  - Vision-Language Understanding
  - Text Generation with Multimodal Input
  - Multimodal Output with Multimodal Input
- [ ]

## Model zoo - Vision-Language Understanding

- [x] [CLIP](https://arxiv.org/abs/2103.00020)
- [x] [AlphaCLIP](https://arxiv.org/abs/2312.03818)
  - motivation: focusing on the regions of interest matters for fine-grained understanding
  - contribution: 
    - datasets with more fine-grained region-text pairs
    - image encoder with an additional alpha channel
    - ![alt text](figures/AlphaCLIP.png)

- [x] [GLIP](https://arxiv.org/abs/2112.03857)
  - motivation: object-level (instead of image-level from CLIP) visual representations are needed
  - contribution:
    - reframe object detection as phrase grounding
    - replace the classification loss in object detection with alignment loss
      - alignment score: ![alt text](figures/alignment_loss.png)
    - ![alt text](figures/GLIP.png)
    - deep fusion: ![alt text](figures/deep_fusion.png)

- [x] [VLMo](https://arxiv.org/abs/2111.02358)
  - motivation: take advantage of both a dual encoder (effective for retrieval tasks) and a fusion encoder (superior on VL tasks)
  - contribution:
    - three stages pretraining: ![alt text](figures/3_stages.png)
    - joint pretraining on three tasks: 
      - image-text contrast
      - image-text matching
      - masked LM pretraining
    - ![alt text](figures/VLMo.png)

- [ ] [ImageBind]()
- [ ] VideoCLIP 
- [ ] VideoMAE

## Model zoo - Text generation with Multimodal Input
