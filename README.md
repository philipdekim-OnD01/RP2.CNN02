# RP2.CNN02 Lecture Code and Data

This repository contains student materials for the On-device AI and CNN lecture.

## Student Links

- Blog lecture notes: <https://philipdekim-OnD01.github.io/obsidian-blog/ondevice-ai-00-overview.html>
- GitHub repository: <https://github.com/philipdekim-OnD01/RP2.CNN02>
- RPS image dataset: <https://github.com/philipdekim-OnD01/RP2.CNN02/tree/main/RPS_Dataset>
- RPS classification notebook: <https://github.com/philipdekim-OnD01/RP2.CNN02/blob/main/examples%28COLAB%29/03_CNN_Based_On-Device_AI/EX_03_RPS_Classification.ipynb>
- RPS augmentation notebook: <https://github.com/philipdekim-OnD01/RP2.CNN02/blob/main/examples%28COLAB%29/03_CNN_Based_On-Device_AI/EX_06_RPS_Classification_Augmentation.ipynb>
- TFLite dynamic range quantization: <https://github.com/philipdekim-OnD01/RP2.CNN02/blob/main/examples%28COLAB%29/04_Lightweighting/EX_05_PTQ_Dynamic_Range.ipynb>
- TFLite INT8 quantization: <https://github.com/philipdekim-OnD01/RP2.CNN02/blob/main/examples%28COLAB%29/04_Lightweighting/EX_06_PTQ_INT8.ipynb>
- Quantization aware training: <https://github.com/philipdekim-OnD01/RP2.CNN02/blob/main/examples%28COLAB%29/04_Lightweighting/EX_08_Quantization_Aware_Training.ipynb>

## RPS Dataset

The rock-paper-scissors dataset is stored in `RPS_Dataset`.

```text
RPS_Dataset/
  0/  scissors images
  1/  rock images
  2/  paper images
```

Class mapping:

| Folder | Label | Class |
| --- | ---: | --- |
| `0` | 0 | scissors |
| `1` | 1 | rock |
| `2` | 2 | paper |

Current image count:

| Class | Images |
| --- | ---: |
| scissors | 903 |
| rock | 907 |
| paper | 907 |
| total | 2717 |

## Recommended Student Flow

1. Open the blog overview and read the lecture map.
2. Run `EX_03_RPS_Classification.ipynb` to understand image loading, label mapping, DenseNet transfer learning, and TFLite export.
3. Run `EX_06_RPS_Classification_Augmentation.ipynb` to compare training with data augmentation.
4. Use the lightweighting notebooks in `examples(COLAB)/04_Lightweighting` to test quantization and pruning concepts.
5. Deploy the exported `.tflite` model on Raspberry Pi and measure FPS.

## Local Setup

Install the basic Python packages:

```bash
pip install -r requirements-cnn.txt
```

For Raspberry Pi inference, install OpenCV and TFLite runtime according to the OS image and Python version.
