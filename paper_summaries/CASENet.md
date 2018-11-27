# CASENet:Deep Category-Aware Semantic Edge Detection (Yu 2017)
## Summary
Yu et al creates a model for category-aware semantic edge detection. They modify the HED architecture into not doing side classification for all layers, but only the last one before concatenation. The previous layers output one single channel feature map each which is replicated into a shared convolution, on which a K-grouped convolution is made into a K channel multi-label output. They get new SOTA on the SBD dataset and also evaluate on the Cityscapes dataset.
## Link
[CASENet:Deep Category-Aware Semantic Edge Detection (Yu 2017)](https://arxiv.org/abs/1705.09759)
