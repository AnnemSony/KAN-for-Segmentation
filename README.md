# U-KAN: Segmentation Framework

The **U-KAN (Segmentation Using Key-Attention Network)** framework is a novel deep learning architecture designed for segmentation tasks. U-KAN leverages a hybrid encoder-decoder structure combined with attention-based Tokenized Key-Attention Network (Tok-KAN) blocks to achieve efficient and accurate segmentation results.
### Architecture Diagram
![U-KAN Architecture](all.png)

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



## Dataset

The **MetaSA1B** dataset used in this project includes both images and corresponding masks. You can download it [https://ai.meta.com/datasets/segment-anything-downloads/](#).
Download and place dataset (images and masks) in inputs folder.

## Installation

To set up the U-KAN segmentation framework, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/AnnemSony/U-KAN-Segmentation.git
   cd U-KAN-Segmentation
   python train.py --arch UKAN --dataset cvc --input_w 256 --input_h 256 --name cvc_UKAN --data_dir ./inputs
   python val.py --name cvc_UKAN --output_dir ./outputs
   


