# Diffusion Playground

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)

## Overview

Welcome to the **Diffusion Playground**! This repository contains example Jupyter notebooks demonstrating the use of diffusion models for image enhancement and style transfer using **ControlNet** and **Stable Diffusion's Img2Img** pipelines.

These notebooks are designed to help you get started with applying advanced image processing techniques to your own images, leveraging state-of-the-art models like Stable Diffusion and ControlNet.

## Table of Contents

- [Diffusion Playground](#diffusion-playground)
    - [Overview](#overview)
    - [Table of Contents](#table-of-contents)
    - [Features](#features)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Notebooks](#notebooks)
        - [1. ControlNet.ipynb](#1-controlnetipynb)
        - [2. Img2Img.ipynb](#2-img2imgipynb)
    - [Usage](#usage)
        - [Running the Notebooks](#running-the-notebooks)
        - [Customizing Parameters](#customizing-parameters)
        - [Input Images](#input-images)
    - [Repository Structure](#repository-structure)
    - [License](#license)
    - [Acknowledgments](#acknowledgments)
    - [Contributing](#contributing)
    - [Contact](#contact)

## Features

- **Image Enhancement:** Improve the aesthetic quality of images while preserving content.
- **Style Transfer:** Transform images into artistic styles, such as paintings in the style of Vincent van Gogh.
- **ControlNet Integration:** Utilize ControlNet models to condition the diffusion process on specific image features.
- **Stable Diffusion Img2Img Pipeline:** Apply image-to-image transformations using Stable Diffusion.

## Prerequisites

- Python 3.8 or higher
- A CUDA-enabled GPU with at least 8 GB VRAM (recommended for optimal performance)
- [Conda](https://docs.conda.io/en/latest/) or [virtualenv](https://virtualenv.pypa.io/en/latest/) for managing virtual environments

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/jmhummel/diffusion-playground.git
   cd diffusion-playground
   ```

2. **Create a Virtual Environment**

   Using `conda`:

   ```bash
   conda create -n diffusion-playground python=3.8
   conda activate diffusion-playground
   ```

   Or using `virtualenv`:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install Required Packages**

   Install the dependencies listed in `requirements.txt`:

   ```bash
   pip install -r requirements.txt
   ```

   *Note: Ensure that you have the latest versions of `torch` and `diffusers` for compatibility with your GPU.*

## Notebooks

### 1. [ControlNet.ipynb](ControlNet.ipynb)

Demonstrates how to enhance images using ControlNet with Stable Diffusion. The notebook guides you through:

- Loading pre-trained ControlNet and Stable Diffusion models.
- Preparing input images and generating control images (e.g., edge maps).
- Configuring prompts and parameters for image generation.
- Displaying and saving the enhanced images.

### 2. [Img2Img.ipynb](Img2Img.ipynb)

Shows how to perform image enhancement and style transfer using Stable Diffusion's Img2Img pipeline. The notebook includes:

- Loading the Stable Diffusion Img2Img model.
- Processing input images for transformation.
- Defining prompts for style transfer (e.g., "A painting in the style of Vincent van Gogh").
- Adjusting parameters like denoising strength and guidance scale.
- Visualizing and saving the output images.

## Usage

### Running the Notebooks

1. **Launch Jupyter Notebook**

   ```bash
   jupyter notebook
   ```

2. **Open the Desired Notebook**

   In the Jupyter interface, navigate to the repository directory and open either `ControlNet.ipynb` or `Img2Img.ipynb`.

3. **Execute the Cells**

   Run each cell sequentially. The notebooks are structured to guide you through the entire process.

### Customizing Parameters

- **Prompts:** Modify the `prompt` and `negative_prompt` variables to influence the generated images.
- **Denoising Strength:** Adjust `denoising_strength` (for Img2Img) to control the balance between preserving the original image and applying transformations.
- **Inference Steps:** Change `num_inference_steps` to trade off between image quality and computation time.
- **Guidance Scale:** Tweak `guidance_scale` to control how strongly the model adheres to the prompt.

### Input Images

- Place your input images in the repository directory or specify the path accordingly.
- Ensure images are in RGB format and resized to 512x512 pixels for optimal results.
- Sample images are available in the `test-images/` directory:
    - `20240929_064700-EDIT.jpg`
    - `20240929_080554-EDIT.jpg`
    - `20240929_082639-EDIT.jpg`
    - `20240929_102048-EDIT.jpg`

## Repository Structure

```
diffusion-playground/
├── test-images/
│   ├── 20240929_064700-EDIT.jpg
│   ├── 20240929_080554-EDIT.jpg
│   ├── 20240929_082639-EDIT.jpg
│   └── 20240929_102048-EDIT.jpg
├── ControlNet.ipynb
├── Img2Img.ipynb
├── LICENSE
├── requirements.txt
└── README.md
```

- **test-images/**: Directory containing sample input images.
- **ControlNet.ipynb**: Notebook for image enhancement using ControlNet.
- **Img2Img.ipynb**: Notebook for image enhancement and style transfer using Img2Img.
- **LICENSE**: MIT License file.
- **requirements.txt**: List of required Python packages.
- **README.md**: This readme file.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **Stable Diffusion** by [CompVis](https://github.com/CompVis) and [Stability AI](https://stability.ai/)
- **ControlNet** by [lllyasviel](https://github.com/lllyasviel)
- **Diffusers Library** by [Hugging Face](https://huggingface.co/docs/diffusers/index)
- **Torch** by [PyTorch](https://pytorch.org/)

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or additions.

Before contributing, please:

- Ensure code is well-documented and follows the existing style.
- Update the `requirements.txt` file if new dependencies are added.
- Test your changes thoroughly.

## Contact

For questions or suggestions, feel free to open an issue on the [GitHub repository](https://github.com/jmhummel/diffusion-playground) or contact the repository owner.

---

*Happy experimenting with diffusion models!*