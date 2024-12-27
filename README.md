# 🚀 Toy Diffusion Playground

Welcome to Toy Diffusion Playground – a hands-on project designed to explore the fascinating world of diffusion models. This repository provides a simple, modular setup for experimenting with image generation, fine-tuning, and even diving into video diffusion.

## 📚 Overview

This project focuses on:

1. 🎨 **Image Generation**: Use pre-trained models like Stable Diffusion to generate high-quality images from text prompts
2. 🛠️ **Fine-Tuning**: Adapt diffusion models to specific styles or concepts using a small custom dataset
3. 🎥 **Video Diffusion** (optional): Experiment with text-to-video techniques and temporal diffusion models

Whether you're an ML practitioner, researcher, or enthusiast, this repository offers a structured approach to learning and experimenting with diffusion models.

## ⚙️ Features

- 🖼️ **Text-to-Image Generation**: Generate visually stunning images using the Hugging Face diffusers library.
- 🛠️ **Fine-Tuning Capabilities**: Train a diffusion model on your own dataset (e.g., personal images, new styles).
- 🔍 **Parameter Exploration**: Adjust hyperparameters to observe their impact on output quality.
- 🎥 **Optional Video Experiments**: Generate videos from text prompts using open-source video diffusion models.

## 🛠️ Getting Started

1. Clone the Repository

   git clone https://github.com/your-username/Toy-Diffusion-Playground.git
   cd Toy-Diffusion-Playground

2. Set Up the Environment

   Install the required dependencies:

   pip install -r requirements.txt

3. Download the Pre-trained Model

   Use Hugging Face’s stable-diffusion-v1-4 as the base model:

   from diffusers import StableDiffusionPipeline

   pipe = StableDiffusionPipeline.from_pretrained("CompVis/stable-diffusion-v1-4")
   pipe.to("cuda")  # Ensure you have GPU support

## 🖼️ How to Use

1. Generate Images

   Run the image_generation.ipynb notebook to create images from text prompts:
   - Input your text prompt.
   - Customize generation parameters (e.g., guidance scale, inference steps).
   - Save and visualize the generated image.

   Example:

   prompt = "a futuristic cityscape at sunset"
   image = pipe(prompt).images[0]
   image.save("results/cityscape.png")

2. Fine-Tune the Model

   Leverage the fine_tuning.ipynb notebook to fine-tune the diffusion model on a custom dataset:
   - Prepare a dataset of 5–10 images (e.g., /data folder).
   - Train the model using DreamBooth or similar techniques.
   - Generate images based on fine-tuned concepts.

## 📊 Results

Sample Outputs

Below are some examples generated during the experiments:

🎨 Prompt	🖼️ Generated Image
“A serene mountain landscape”	
“A robot painting a canvas”	

## 🎥 Optional: Video Diffusion

Interested in text-to-video generation? Explore this additional capability using open-source tools like ModelScope Text-to-Video.
   1. Install the required dependencies.
   2. Use the temporal diffusion pipeline to generate short videos from prompts.
   3. Save results in /results.

