# AI Photo Editing App

This project provides an app that allows users to interactively select a subject from an image, modify the subject or the background using text prompts, and swap them with new generated content. The app leverages the Segment Anything Model (SAM) to identify and mask the subject and a text-to-image diffusion model to create new content for either the subject or background based on user input.

## Table of Contents
- [Features](#features)
- [How It Works](#how-it-works)
- [Usage](#usage)
- [Setup Instructions](#setup-instructions)
- [Screenshots](#screenshots)

## Features
- **Segment Anything Model (SAM)**: Select any subject in the image by clicking on it.
- **Subject Masking**: Create and refine masks to accurately select the subject.
- **Infill Model**: Use a diffusion model to modify or replace the selected subject or background.
- **Text-to-Image Generation**: Modify backgrounds or subjects using text prompts.
- **Background and Subject Swapping**: Change the background, swap the subject, or remove objects.

## How It Works
1. **Upload an Image**: Users start by uploading an image to the app.
2. **Select a Subject**: The user clicks on the subject in the image, activating the SAM model which creates a mask around the object.
3. **Mask Refinement**: The user can refine the mask by adding additional clicks if necessary.
4. **Text Prompts**: The user inputs a prompt describing the desired new background or subject (with optional negative prompts).
5. **Generate New Content**: The model uses the text prompt to modify the background or subject.
6. **Final Output**: The app shows the final image with either the new background or subject.

## Usage

1. **Image Selection**:
    - Click on the desired subject in the uploaded image.
    - The SAM model will automatically generate a mask for the subject.

2. **Mask Refinement**:
    - Refine the selection by adding more clicks to the image until you achieve the desired mask for the subject.

3. **Prompt for Infill**:
    - Provide a text description for the new background or subject in the provided field.
    - (Optional) Add a negative prompt to prevent certain details from being generated.

4. **Subject Inversion**:
    - Select the "Infill subject instead of background" option if you wish to modify the subject and keep the background.

5. **Run Inpaint**:
    - Click the "Run Inpaint" button to generate the final image based on your selections and inputs.

## Setup Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/dinesh-bk/ai_photo_editing_app.git
   ```
2. Navigate to the project directory:
   ```bash
   cd ai_photo_editing_app
   ```
3. Install the necessary dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:
   ```bash
   python main.py
   ```

5. Access the Gradio interface. The app will automatically open in your default browser.

## Screenshots

### 1. Image Upload and Subject Selection
![Screen 1](./screen_1.jpeg)
_User selects a subject in the image using the SAM model._

### 2. Mask Refinement and Subject Infill
![Screen 2](./screen_2.jpeg)
_Mask refinement and choosing the subject to be swapped with a crocodile._


