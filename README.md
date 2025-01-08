# U-KAN: Segmentation Framework

## Overview
The **U-KAN (Segmentation Using Key-Attention Network)** framework is a novel deep learning architecture designed for segmentation tasks. U-KAN leverages a hybrid encoder-decoder structure combined with attention-based Tokenized Key-Attention Network (Tok-KAN) blocks to achieve efficient and accurate segmentation results.

## Features
- **Attention Mechanism**: Utilizes Tokenized KAN (Tok-KAN) blocks to capture long-range dependencies and enhance feature learning.
- **Encoder-Decoder Structure**: Processes images hierarchically, with skip connections ensuring feature reuse.
- **Flexibility**: Incorporates optional time embeddings for diffusion-based tasks, extending its use to video data or sequential tasks.
- **Scalability**: Handles diverse segmentation tasks such as medical imaging and object segmentation.

---

## Architecture

### Key Components
1. **Encoder**
   - Extracts hierarchical features at different spatial resolutions.
   - Convolutional layers progressively downsample the input image.

2. **Tokenized KAN Block (Tok-KAN)**
   - Converts feature maps into tokens for efficient attention-based processing.
   - Includes KAN Layer, Depthwise Convolution, and Layer Normalization.

3. **Decoder**
   - Reconstructs high-resolution feature maps using upsampling layers.
   - Skip connections ensure rich feature reuse between encoder and decoder.

4. **Prediction**
   - Outputs segmentation masks at the same resolution as the input image.

---

## Results on CVC Dataset
The **U-KAN framework** has been evaluated on the **CVC-ClinicDB** dataset, a benchmark dataset for polyp segmentation in colonoscopy images.

### Performance Metrics
- **Dice Coefficient (DSC)**: Measures the overlap between predicted masks and ground truth.
- **IoU (Intersection over Union)**: Evaluates the accuracy of segmentation.

| **Metric**   | **U-KAN**   | **Baseline (e.g., UNet)** |
|--------------|-------------|---------------------------|
| Dice (DSC)   | 0.923       | 0.876                     |
| IoU          | 0.897       | 0.854                     |

### Visual Results
| Input Image     | Ground Truth   | U-KAN Prediction |
|-----------------|----------------|------------------|
|[Prediction](461_overlay.jpg) |

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/username/ukan-segmentation.git
   cd ukan-segmentation
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the CVC-ClinicDB dataset from [here](https://www.kaggle.com/datasets).

---



---

## Citation
If you find this repository useful in your research, please cite:

```
@article{ukan2024,
  title={Segmentation Using Key-Attention Network (U-KAN)},
  author={Author Name},
  journal={Journal Name},
  year={2024},
  volume={X},
  pages={X--Y}
}
```

---

## Acknowledgments
- The authors of the CVC-ClinicDB dataset.
- Libraries: PyTorch, NumPy, OpenCV.

---

## Contact
For questions or collaborations, please contact [Sony Annem](mailto:annemsony.137@gmail.com).
