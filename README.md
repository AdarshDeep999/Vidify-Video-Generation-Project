Vidify: AI Story-to-Video Generator
Project Overview
BradAI is an end-to-end generative AI pipeline that transforms a user's short story into a complete, narrated video. This project orchestrates multiple, distinct AI models to manage a complex creative workflow: from script analysis and scene generation to voice synthesis and final video assembly.

The core of the application is a "Creative Director" AI, powered by Google's Gemini, which uses advanced prompt engineering to ensure visual consistency and narrative coherence across all generated scenes. The result is a dynamic, high-quality video with selectable art styles, aspect ratios, and optional subtitles, created entirely from a simple text input.

This repository contains the complete, runnable Google Colab notebook demonstrating the entire pipeline.

Key Features
Multi-Stage AI Pipeline: A sophisticated workflow that integrates three separate AI services for distinct creative tasks.

Advanced Prompt Engineering: A custom-built "Creative Director" AI (Gemini) that deconstructs a narrative into a scene-by-scene visual script, maintaining character and style consistency.

Dynamic Scene Generation: Utilizes Replicate and Stability AI's SDXL model to generate high-resolution, unique images for each scene based on the Director AI's detailed prompts.

High-Quality Voice Synthesis: Integrates Microsoft Azure Cognitive Services for Speech to generate clear, natural-sounding voice narration for the story.

Automated Video Assembly: Uses MoviePy to programmatically assemble the generated images and audio into a final video file.

User-Selectable Options: The pipeline is fully configurable, allowing for:

Multiple artistic styles (Anime, Realistic, Fantasy Art, etc.).

Different video aspect ratios (16:9, 9:16, 1:1).

Optional on-screen subtitles.

Technology Stack
Script & Scene Generation: Google Gemini Pro

Image Generation: Replicate API (Stability AI - SDXL)

Voice Synthesis: Microsoft Azure Cognitive Services for Speech

Video Assembly: MoviePy

Core Language: Python

Primary Libraries: google-generativeai, replicate, azure-cognitiveservices-speech, moviepy

Development Environment: Google Colab

How to Run
This project is designed to be run as a self-contained Google Colab notebook.

Open the Notebook:
Open the bradAI_Video_Generator.ipynb file from this repository in Google Colab.

Configure API Keys:
This project requires API keys from three different services. In the Colab notebook, fill these in required cell:

GOOGLE_API_KEY: Your key from Google AI Studio.

REPLICATE_API_TOKEN: Your token from Replicate.

AZURE_SPEECH_KEY: Your key from the Azure portal.

AZURE_SPEECH_REGION: Your service region from Azure (e.g., eastus).

Run the Notebook:
Once the secrets are configured, you can run all the cells in the notebook from top to bottom (Runtime > Run all). The script will install all dependencies, configure the services, and execute the full video generation pipeline with a sample story.

Find the Output:
The final .mp4 video file will be generated and will appear in the Colab file explorer on the left sidebar, from where it can be downloaded. The process can take several minutes to complete depending on the length of the story.

Project Structure
Vidify_Video_Generator.ipynb: The main executable notebook containing the complete, documented pipeline.

README.md: This project overview file.

requirements.txt: A list of all necessary Python libraries for the project.

.gitignore: Standard Python gitignore to ensure a clean repository.
