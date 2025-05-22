# Zero Ghibli: Detecting AI-Generated Studio Ghibli Artwork

This project addresses the challenge of distinguishing between authentic Studio Ghibli animation frames and AI-generated imitations through deep learning techniques. As AI-generated content becomes increasingly sophisticated, preserving artistic authenticity and protecting intellectual property becomes crucial, especially for iconic animation studios like Studio Ghibli.

## Project Overview

This repository contains:

- A Jupyter Notebook (`ghibli_analysis.ipynb`) with all data analysis code and model implementations
- Documentation of methodology and findings (`ghibli_project_documentation.pdf`)
- Dataset sources and processing techniques
- Visualization outputs and model comparison results

## Research Focus

- Comprehensive evaluation of deep learning approaches for detecting AI-generated Ghibli-style images
- Systematic comparison of seven prominent CNN architectures
- Introduction of "Ghiblinosaurus," a novel approach with specialized attention mechanisms
- Analysis of trade-offs between model accuracy, computational efficiency, and resource requirements
- Visualization techniques for model interpretability using Gradient-weighted Class Activation Mapping (Grad-CAM)

## CNN Architectures Evaluated

This project compares the performance of seven prominent convolutional neural network architectures:

1. VGG16
2. Xception
3. DenseNet121
4. MobileNetV2
5. InceptionV3
6. ResNet-50
7. EfficientNetB0

Each model brings different architectural strengths to the classification task of distinguishing authentic Ghibli frames from AI-generated imitations.

## The Ghiblinosaurus Model

We introduce "Ghiblinosaurus," a novel approach that incorporates specialized attention mechanisms designed to identify subtle artifacts and inconsistencies common in AI-generated animation. These mechanisms focus on:

- Color harmony
- Edge consistency
- Texture patterns

These features are particularly important for distinguishing authentic Ghibli artwork from synthetic imitations, as they capture the unique qualities of hand-drawn animation.

## Methodology

The analysis follows these key steps:

1. **Data Collection**: Collecting authentic Ghibli frames and AI-generated imitations
2. **Data Preprocessing**: Converting to RGB format and resizing images
3. **Data Augmentation**: Applying transformations to improve model generalization
4. **Model Development**: Implementing and training seven CNN architectures
5. **Performance Evaluation**: Comparing models across multiple performance metrics
6. **Interpretability Analysis**: Using Grad-CAM to visualize what features the models focus on

## Datasets

Our dataset comprises two distinct categories: authentic Studio Ghibli animation frames and AI-generated images that imitate the Ghibli style.

### Primary Datasets

- **Ghibli Anime Dataset**: Contains authentic frames extracted from Studio Ghibli films, representing the ground truth of genuine Ghibli artwork with its characteristic hand-drawn animation style, color palettes, and artistic techniques.
  ```python
  ghibli_dataset = load_dataset("satyamtripathii/Ghibli_Anime")
  ```

- **AI-Generated Ghibli Images Dataset**: A novel dataset **personally created and published** specifically for this research. This unique collection comprises 368 high-quality images (approximately 416 MB total) in PNG and JPG formats at various high resolutions.
  ```python
  ai_generated_dataset = load_dataset("filberthamijoyo/AI_Generated_Ghibli")
  ```

### AI-Generated Dataset Details

The AI-generated images were meticulously created by **filberthamijoyo** using multiple state-of-the-art AI generation tools:
- Midjourney
- DALL-E
- Stable Diffusion
- ChatGPT

Images were generated with prompts specifically designed to mimic the distinctive Ghibli aesthetic across diverse subjects, characters, and landscapes. This dataset represents one of the first publicly available collections specifically designed for animation-style deepfake detection, addressing a significant gap in current research resources. **The dataset has been published on Hugging Face to benefit the broader research community.**

### Data Processing

The complete dataset was processed and organized as follows:
- Images were converted to RGB format for consistency
- All images were resized to 224×224 pixels to accommodate the input requirements of the CNN architectures
- The dataset was split into training (70%), validation (15%), and testing (15%) sets, maintaining class balance in each split
- Class labels were assigned as binary categories: "real ghibli" for authentic frames and "ai generated" for synthetic images

### Data Augmentation

To improve model generalization and address the relatively limited size of the dataset, we implemented comprehensive data augmentation strategies:

**Basic Augmentations:**
- Geometric transformations: rotation (up to 40 degrees), width and height shifts (up to 30%), shearing (up to 30%), zooming (up to 30%), horizontal and vertical flips
- Color manipulations: brightness variation (±30%), channel shifting (up to 20%)

**Enhanced Augmentations (for Ghiblinosaurus model):**
- Rotation (up to 40 degrees)
- Width and height shifts (up to 40%)
- Shearing (up to 40%)
- Zooming (up to 40%)
- Brightness variation (±40%)
- Channel shifting (up to 30%)

These augmentation techniques were applied only to the training set, while validation and test sets remained unmodified to ensure accurate performance evaluation. The augmentation process was implemented using TensorFlow's ImageDataGenerator, which applies transformations in real-time during model training.

## Key Findings

Our research provides several important contributions:

- Systematic comparison of seven CNN architectures for detecting AI-generated animation
- Benchmark results across multiple performance metrics for each model
- Analysis of the trade-offs between model accuracy, computational efficiency, and resource requirements
- Insights into which visual features are most important for distinguishing authentic from AI-generated Ghibli artwork
- Demonstration of the effectiveness of specialized attention mechanisms in the Ghiblinosaurus model

For detailed findings, please refer to the Jupyter notebook and documentation.

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Required libraries: tensorflow, keras, pandas, numpy, matplotlib, seaborn, scikit-learn
- Hugging Face datasets library (`pip install datasets`)

### Installation

```bash
git clone https://github.com/filberthamijoyo/zero-ghibli.git
cd zero-ghibli
pip install -r requirements.txt
```

### Running the Analysis

Open the Jupyter notebook to explore the analysis:

```bash
jupyter notebook ghibli_analysis.ipynb
```

## Visualizations

The project includes various visualization types:

- Confusion matrices for each model's performance
- Training and validation accuracy/loss curves across architectures
- Grad-CAM visualizations highlighting regions of interest in the images
- Comparative analysis of model predictions across different types of AI-generated images
- Resource utilization metrics for each model

## Future Work

Potential extensions to this research include:

- Incorporating temporal features by analyzing frame sequences rather than isolated frames
- Developing specialized detection techniques for each AI generation tool
- Exploring ensemble methods that combine multiple architectures
- Investigating the impact of animation-specific preprocessing techniques
- Adapting the approach to other animation studios and artistic styles

## Dataset Contribution

The "AI-Generated Ghibli Images Dataset" created for this project has been made publicly available on Hugging Face by **filberthamijoyo** (the author of this project). This contribution provides a valuable resource for researchers working on animation-style deepfake detection and AI art generation analysis.

You can access and use this dataset for your own research at:
[https://huggingface.co/datasets/filberthamijoyo/AI_Generated_Ghibli](https://huggingface.co/datasets/filberthamijoyo/AI_Generated_Ghibli)

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Studio Ghibli for their incredible filmmaking and unique animation style
- Dataset creator of Ghibli Anime dataset: satyamtripathii
- The AI generation tools (Midjourney, DALL-E, Stable Diffusion, ChatGPT) for enabling this research
- The animation and deepfake detection research community for methodological inspiration 