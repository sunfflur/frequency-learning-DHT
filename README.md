# Frequency learning based on the Hartley transform applied to texture classification

## Abstract
#### Artificial intelligence tools are becoming increasingly popular in current technologies, especially convolutional neural networks, which have shown surprising results in computer vision tasks. However, in some scenarios, it may be more intelligible to represent and analyze data in a transformed domain (e.g., frequency domain), which raises the idea of having a model whose learning and operations occur in this new domain. Therefore, this work aims to develop and analyze a frequency learning model based on the Hartley transform, given the real characteristic of the spectrum produced, exploring its convolution property in creating a processing layer that emerges as a potential alternative to convolutional layers. The proposed model is characterized by the following steps: (i) division into blocks, (ii) transformation to the frequency domain via Hartley transform, (iii) filtering and frequency grouping, and (iv) propagation of spectral attributes through dense layers until generating the output. This model was analyzed in the context of the texture classification problem, given its natural appeal to the frequency domain, using three datasets: Kylberg Texture Dataset (KTD), a database containing monochromatic images divided into 28 classes; KTH-TIPS2-b, a database divided into 11 classes and composed of RGB images that have variations in scale, position, and lighting; and ALOT, a database with 250 classes that adds variations in lighting, angles, and focus direction in RGB images. The results show that the frequency-based Hartley transform model is competitive compared to some well-established CNNs in the literature and presents a significant reduction in the number of adjustable parameters and training time, constituting a promising and relatively lightweight alternative.

## Experiments
#### Repository composed by the algorithms used to compare the frequency-domain approach and some ConvNets on 4 datasets:
  - Kylberg Texture Dataset;
  - KTH-TIPS2-b;
  - ALOT.

## Usage

In each folder, you'll find individual Python notebooks that can be executed independently. The notebooks cover various aspects of the project and can be used for different purposes. Follow the content description within each notebook to understand and utilize the code effectively. It's important to mention the following notebooks refers to the implementation of the frequency-based model on the Hartley domain.

## Content description

| [Kylberg Texture Dataset](https://kylberg.org/kylberg-texture-dataset-v-1-0/) | Description |
|-------------|-------------|
| Exp_KTD_a.pynb   | This notebook contains the implementation of the DFT frequency-based model on Kylberg dataset. It contains ablation studies in some components of the proposed approach: the number of splitting levels vary from 3 to 1 and the width vary from 1 to 4.|
| Exp_KTD_a_DHT.pynb   | This notebook contains the implementation of the DHT frequency-based model on Kylberg dataset. It considers the best scenarios of the previous notebook: number of splitting levels = 3 and width = 1.|
| Exp_KTD_EfficientNetV2S.pynb    | This notebook contains the implementation of EfficientNetV2S to classify the KTD images. Here we explore two versions of the same model: Using transfer learning - Pre-trained model; Without transfer learning - Random initialization. |
| Exp_KTD_DenseNet169.pynb    | This notebook contains the implementation of DenseNet169 to classify the KTD images. Here we explore two versions of the same model: Using transfer learning - Pre-trained model; Without transfer learning - Random initialization. |


