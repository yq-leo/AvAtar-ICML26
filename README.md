# AvAtar: Learning to Align via Active Optimal Transport

<div align="center">
    <a href="">
    <img src="https://img.shields.io/static/v1?label=ICML'26&message=Paper&color=red"></a>
    <!-- <a href="https://github.com/yq-leo/PlanetAlign/blob/main/LICENSE.txt"><img src="https://badgen.net/github/license/yq-leo/PlanetAlign?color=green"></a> -->
    <a href="https://github.com/yq-leo/AvAtar-ICML26/blob/main/LICENSE.txt"><img src="https://img.shields.io/badge/License-MIT-green.svg"></a>
    <a href="https://github.com/yq-leo/PlanetAlign"><img src="https://img.shields.io/badge/PRs-Welcome-blue.svg"></a>
</div>

Welcome to the offical repository of AvAtar, an active learning framework for optimal-transport-based alignment algorithms.

---

## Results
### 🚀 SOTA effectiveness across 3 different alignment tasks

<div style="display: flex; gap: 16px; width: 100%; align-items: stretch;">
  <div style="flex: 1; display: flex;">
    <img src="figs/bench_na.png"
         alt="bench_na.png"
         style="width: 100%; object-fit: contain;">
  </div>
  <div style="flex: 1; display: flex; flex-direction: column; gap: 16px;">
    <img src="figs/bench_itr.png"
         alt="bench_itr.png"
         style="width: 100%; flex: 1; object-fit: cover;">
    <img src="figs/bench_itg.png"
         alt="bench_itg.png"
         style="width: 100%; flex: 1; object-fit: cover;">
  </div>
</div>

### ⚖️ Good balance between effectivness and efficieny

<div style="display: flex; gap: 5px; width: 100%; align-items: flex-start;">

  <!-- First image: 50% -->
  <div style="flex: 2;">
    <img src="figs/efficiency.png"
         alt="efficiency.png"
         style="width: 100%; object-fit: contain;">
  </div>

  <!-- Second image: 25% -->
  <div style="flex: 1;">
    <img src="figs/conv1.png"
         alt="conv1.png"
         style="width: 100%; object-fit: contain;">
  </div>

  <!-- Third image: 25% -->
  <div style="flex: 1;">
    <img src="figs/conv2.png"
         alt="conv2.png"
         style="width: 100%; object-fit: contain;">
  </div>

</div>

---

## How to use

### Environment Setup
1. Create a new conda environment using the provided `environment.yml` file:
   ```bash
   conda env create --file environment.yml
   ```

2. Activate the environment:
   ```bash
   conda activate avatar
   ```

### Task1: Network Alignment (NA)

We leverage the [PlanetAlign](https://arxiv.org/abs/2505.21366) library for conducting active learning on network alignment tasks, which features a rich collections of built-in datasets and OT-based methods for NA. Please refer to the [code repository](https://github.com/yq-leo/PlanetAlign) and [documentation](https://planetalign.readthedocs.io/en/latest/) of PlanetAlign for detailed installation and usage guides.

After setting up the PlanetAlign environment, you can run the AvAtar for network alignment using the following command:

```bash
python source/active_na.py
```

### Task2 Image-Text Retrieval (ITR)
We use the [CIFAR10-C](https://zenodo.org/records/2535967) and [ImageNet-C](https://zenodo.org/records/2235448) datasets for image-text retrieval tasks. Please download the datasets and place them under the `data/` directory before running the code.

For the OT-based alignment algorithms, we use the GOT method proposed in [Graph Optimal Transport for Cross-Domain Alignment](https://arxiv.org/pdf/2006.14744). The code for GOT is available at the [official repository](https://github.com/LiqunChen0606/Graph-Optimal-Transport).

After setting up the datasets and the GOT method, you can run the AvAtar for image-text retrieval using the following command:

```bash
python source/active_itr.py
```

### Task3 Image-Text Grounding (ITG)
We use the [COCO](https://cocodataset.org/#home) and [Flickr30K Entities](https://bryanplummer.com/Flickr30kEntities/) datasets for image-text grounding tasks. Please download the datasets and place them under the `data/` directory before running the code.

Similar to the image-text retrieval task, for the OT-based alignment algorithms, we use the GOT method proposed in [Graph Optimal Transport for Cross-Domain Alignment](https://arxiv.org/pdf/2006.14744). The code for GOT is available at the [official repository](https://github.com/LiqunChen0606/Graph-Optimal-Transport).

After setting up the datasets and the GOT method, you can run the AvAtar for image-text grounding using the following command:

```bash
python source/active_itg.py
```

---

## Citation
If you find our work useful for your research, please consider citing AvAtar with the following bibtex:

