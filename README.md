<h1 align="center"> Text-to-Speech with Hugging Face</h1>
<p align="center">Generate realistic human speech from text using <b>Hugging Face Transformers</b> and <b>TTS Models</b>.</p>

<p align="center">
  <a href="https://colab.research.google.com/drive/156QAcdh8hBxCpIrRqDuAJGY_bPRdsQYl" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab">
  </a>
  <a href="https://huggingface.co/models?pipeline_tag=text-to-speech" target="_blank">
    <img src="https://img.shields.io/badge/%20Hugging%20Face-TTS%20Models-orange?logo=huggingface">
  </a>
  <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python">
  <img src="https://img.shields.io/badge/Transformers-Enabled-yellow?logo=transformers">
  <img src="https://img.shields.io/badge/License-MIT-lightgrey.svg">
</p>

---

<p align="center">
  <img src="https://cdn.dribbble.com/userupload/13872334/file/original-29a4c899bd474b3b61d83c0cbcad9121.png?resize=1200x400&vertical=center" alt="TTS Banner" width="90%">
</p>

---

>  **Transform written text into expressive, lifelike audio speech** using Hugging Face's pretrained text-to-speech models.
> Ideal for **AI assistants, audiobooks, accessibility tools, and media automation workflows.**

---

## 🚀 Features

*  Convert text into realistic human speech in seconds
*  Supports multiple voices and languages
*  Built with Hugging Face Transformers & Datasets
*  Stream or download generated audio
*  Easy to run in Google Colab or locally

---

##  Project Overview

This notebook showcases the use of **Hugging Face text-to-speech pipelines** for generating high-quality audio directly from text prompts.
You can run it locally or on Google Colab with GPU acceleration for faster inference.

---

##  Setup

###  Clone Repository

```bash
git clone https://github.com/obinnachike/Text-to-Speech-with-HuggingFace.git
cd Text-to-Speech-with-HuggingFace
```

###  Install Dependencies

```bash
pip install transformers
pip install torch
pip install soundfile
pip install datasets
```

###  (Optional) Run in Colab

Click below to open the project in Colab and run immediately:

<p align="center">
  <a href="https://colab.research.google.com/drive/156QAcdh8hBxCpIrRqDuAJGY_bPRdsQYl" target="_blank">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open in Colab">
  </a>
</p>

---

##  Example Code

```python
from transformers import pipeline

# Initialize text-to-speech pipeline
tts = pipeline("text-to-speech", model="facebook/mms-tts-eng")

# Provide your text prompt
text = "Welcome to the world of AI voice synthesis powered by Hugging Face!"

# Generate audio output
speech = tts(text)

# Save output as .wav file
with open("output.wav", "wb") as f:
    f.write(speech["audio"])
```

---

##  Example Output

>  Input:
> “Welcome to my AI voice demonstration project.”

>  Output:
> Generates a smooth, natural-sounding audio clip (`output.wav`) stored in your working directory.

---


##  Notes & Tips

<details>
<summary> Expand to view advanced settings</summary>

* Adjust **sampling rate** using the model’s config for higher quality audio.
* Use `.audio` key from the pipeline output to handle audio streams.
* For multilingual synthesis, try `facebook/mms-tts-*` variants.
* For GPU acceleration in Colab:

  ```
  Runtime → Change runtime type → GPU
  ```

</details>

---

##  Example Use Cases

| Use Case              | Description                             |
| --------------------- | ----------------------------------------|
|  Audiobook Creation | Convert chapters into narrated audio      |
|  Accessibility      | Voice output for visually impaired users  |
|  AI Voice Bots      | Integrate natural voice into chatbots     |
|  Content Narration  | Generate spoken versions of written blogs |
|  Language Learning | Practice pronunciation and comprehension   |

---

##  Example Environment

|      Component | Example Value              |
| -------------: | -------------------------- |
| Python Version | 3.11                       |
|      Framework | Transformers               |
|          Model | facebook/mms-tts-eng       |
|       Hardware | CPU / GPU (Colab or Local) |

---

<p align="center">
  <b> Text-to-Speech with Hugging Face — Bringing Words to Life with AI.</b>
</p>
