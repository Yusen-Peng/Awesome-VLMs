# Vision-Language Understanding

- [x] [CLIP](https://arxiv.org/abs/2103.00020)
- [x] [SigLIP](https://arxiv.org/abs/2303.15343) - sigmoid loss without global normalization from Softmax


- [x] [ImageBind](https://arxiv.org/abs/2305.05665)
  - motivation: 
    - embeddings are usually limited to the pairs of modalities used for training
    - "just aligning each modality’s embedding to image embeddings leads to an emergent alignment across all of the modalities"
  - contribution:
    - from natural alignment to emergent alignment across images, videos, text, audio, depth, thermal, and IMU
    - ![alt text](/figures/ImageBind.png)
- [x] [VideoCLIP](https://arxiv.org/abs/2109.14084)
  - motivation: granularity about **sequence length** and **semantics** (apple/banana v.s. apple/car) can be hard
  - contribution:
    - for positive pairs: use video and text clips that are **loosely temporarily overlapping** instead of enforcing strict boundaries
      - underlying rationale: strict temporal alignment ≠ semantic alignment!
    - for negative pairs: retrieve a cluster of videos that are similar to each other
      - underlying rationable: "mining clips from other videos can provide much more challenging negatives"
    - ![alt text](/figures/VideoCLIP.png)
