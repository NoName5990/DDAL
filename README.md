 ---

<div align="center">    
 
# Domain Discrepancy Aware Active Learning for Cross-domain LiDAR Point Cloud Segmentation

[Zongyi Xu](), [Jixiao Liu](), [Shanshan Zhao](), [Zhongpeng Lang](), [Qianni Zhang](), [Weisheng Li]() and [Xinbo Gao]()


<img alt="image" src="docs/figs/pipeline.png" width="60%" />

</div>

### Highlight
- 🌈 we present a voxel-centric online active learning baseline that efficiently reduces the labeling cost of enormous point clouds and effectively facilitates learning with a limited budget.
- ⚖️ we introduce a novel label acquisition strategy, voxel confusion degree (VCD), that requires 1000× fewer annotations while reaching a close segmentation performance to that of the fully supervised counterpart. 
- 🚀 `Annotator` is generally applicable and works for different network architectures (e.g., MinkNet, SPVCNN, etc.), in distribution or out of distribution setting (i.e., AL, ASFDA, and ADA), and simulation-to-real
(SynLiDAR→SemanticKITTI/SemanticPOSS) and real-to-real (SemanticKITTI→nuScenes and nuScenes→SemanticKITTI) scenarios with consistent performance gains


## Usage
### Prerequisites
Please see [INSTALL.md](docs/INSTALL.md).

### Data Preparation
Please see [DATA.md](docs/DATA.md)

### Training and Evaluation
Please see [TRAIN_VAL.md](docs/TRAIN_VAL.md)


<!-- ## Citation
If you find this project useful in your research, please consider citing:
```latex
bib

``` -->

## Acknowledgements
This project is based on the [Annotator](https://github.com/BIT-DA/Annotator), we thank the author for making the source code publicly available.


## Contact

For help and issues associated with Annotator, or reporting a bug, please open a [[GitHub Issues](https://github.com/NoName5990/DDAL/issues/new)], or feel free to contact `S220201058@stu.cqupt.edu.cn`.
