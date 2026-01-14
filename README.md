

# Text to Image App with Stable Diffusion

Stable Bud is a desktop application that allows you to generate images from text prompts using the Stable Diffusion model. It features a modern dark-mode GUI built with CustomTkinter and runs locally on your machine.

## Features

* **Text-to-Image:** Type a prompt (e.g., "A cyberpunk cat") and generate unique art.
* **Dark Mode GUI:** Clean and modern interface using CustomTkinter.
* **CPU Optimized:** Configured to run on standard laptops (without dedicated GPUs) using "Low Memory" mode.

## Installation Guide

Follow these steps to set up the project on your computer.

### 1. Clone or Download the Project

Download the project files to a folder (e.g., `Stable Diff App`).

### 2. Create a Virtual Environment

It is recommended to use a virtual environment to keep dependencies organized.

**Windows:**

```bash
python -m venv stabletk

```

**Mac/Linux:**

```bash
python3 -m venv stabletk

```

### 3. Activate the Environment

You must activate the environment every time you work on the project.

**Windows:**

```bash
.\stabletk\Scripts\activate

```

**Mac/Linux:**

```bash
source stabletk/bin/activate

```

*(You will see `(stabletk)` appear at the start of your terminal line.)*

### 4. Install Dependencies

Run this command to install all required libraries (PyTorch, Diffusers, CustomTkinter, etc.):

```bash
pip install -r requirements.txt

```

## Configuration

You need to authenticate with Hugging Face to download the model.

1. Create a file named `authtoken.py` in the project folder.
2. Add the following line inside it, replacing the text with your actual token:

```python
auth_token = "hf_YourHuggingFaceTokenHere"

```

## How to Run

Ensure your virtual environment is activated (`(stabletk)`).

Run the application:

```bash
python app.py

```

**First Run:** The app will download the model (approx. 4GB). This may take 5–10 minutes. The window will appear once the download is complete.

## Important Notes for CPU Users

If you are running this on a laptop without a generic GPU (Nvidia):

* **Generation Time:** Generating one image typically takes 5 to 10 minutes.
* **"Not Responding":** When you click "Generate," the app window may freeze or say "Not Responding." This is normal. The app is working hard in the background. Check your terminal/command prompt to see the progress bar.
* **Memory Errors:** If the app crashes, ensure you have closed other heavy programs (Chrome tabs, games) to free up RAM.

## Project Structure

* `app.py`: Main application code.
* `authtoken.py`: Stores your API key.
* `requirements.txt`: List of python packages.
* `generated_image.png`: Output file where the generated image is saved.

## Credits & References
This project was inspired by and built following the tutorial by Nick.

Original Tutorial: Build Your Own Text to Image App with Stable Diffusion https://www.youtube.com/watch?v=7xc0Fs3fpCg

