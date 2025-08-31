# NST
# Neural Style Transfer with VGG16
## Project Overview
This project implements Neural Style Transfer (NST), a deep learning technique to create images that combine the content of one image with the artistic style of another using a convolutional neural network (CNN). The implementation closely follows the paper by Gatys et al., utilizing the pre-trained VGG16 model and Keras backend for optimization.

## Key Features
Uses TensorFlow and Keras APIs for image manipulation.

Pre-trained VGG16 model is leveraged for feature extraction.

Style transfer is achieved by optimizing a loss function combining content, style, and total variation losses.

Scipy’s L-BFGS algorithm is used for iterative optimization.

Visualization of content, style, and generated images through Matplotlib.

## Folder Structure
images/: Contains the content and style reference images.

outputs/: Generated output images at each iteration.

notebooks/: Jupyter/Google Colab notebook with code and results.

## Installation
Clone or download the repository.

Place your content and style images into the appropriate folder.

Install the required packages:

bash
pip install numpy tensorflow keras matplotlib scipy imageio
Open and run the notebook/script in a Jupyter or Colab environment.

## Usage
Edit the paths for your content and style images at the top of the notebook/script.

By default, the generated output image combines the subject of the “content image” with the artistic style of the “style reference image.”

Run all cells to begin the optimization. Output images will be saved at each iteration for visualization.

## Methodology
Preprocessing: Content and style images are loaded and standardized for the VGG16 network.

Loss Functions: Three losses are minimized:

Content Loss: Difference in activation between content and generated images.

Style Loss: Difference in Gram matrices for style and generated images.

Total Variation Loss: Regularizes image smoothness.

Optimization: Pixels are updated iteratively to minimize the combined loss using L-BFGS.

Visualization: Matplotlib is used to display the content, style, and output images side by side for qualitative assessment.

## Customization
Change weights for content, style, or total variation losses as needed.

Experiment with different layers in VGG16 for content and style extraction.

Adjust image sizes based on available hardware; by default, images are resized to improve computational efficiency.

## References
Leon A. Gatys, Alexander S. Ecker, Matthias Bethge. "A Neural Algorithm of Artistic Style."

Example implementations: nazianafis/Neural-Style-Transfer, [Google TensorFlow Style Transfer Tutorial].

