# Smart Image & Voice-to-Braille Captioning & Input Assistant

## Overview
A cost-effective, portable **“Braille Pad”** that enables visually-impaired users to **read** (refreshable Braille cells + audio) and **write** (Braille keypad) digital content in real time.  
The system captions images, transcribes multilingual speech, and converts any resulting text to tactile Braille or synthesized regional-language speech—all on a Raspberry Pi platform.

---

## Problem Statement
Traditional Braille books are bulky, expensive, and slow to produce, limiting access to timely information.  
Electronic Braille displays exist but remain cost-prohibitive.  
This project delivers an affordable, open-source alternative that bridges the accessibility gap.

---

## Objectives
| Goal | Description |
|------|-------------|
| **Accessible Reading** | Convert images and speech into refreshable Braille patterns and audio. |
| **Accessible Writing** | Accept Braille keypad input and translate it to digital text. |
| **Low-Cost Hardware** | Use readily available components (Raspberry Pi 4, 74HC595, ULN2803, 3-D-printed Braille cells). |
| **Modular Design**    | Chainable Braille cells for flexible display sizes. |

---

## System Architecture
| Stage | Functionality |
|-------|---------------|
| **Inputs** | Images • Speech • Printed text |
| **Processing** | *ASR ➔ Translation ➔ Captioning ➔ Braille mapping ➔ TTS* |
| **Outputs** | Refreshable Braille cells • Braille keypad echo • Regional-language audio • Digital text |

---

## Key Features
- **Image Captioning** – Generates concise descriptions from captured images.  
- **Multilingual Speech Translation** – Recognises speech in regional languages and translates it to English (and vice-versa).  
- **Text-to-Braille Engine** – Maps Unicode text to 6-dot Braille and actuates pins in real time.  
- **Braille-to-Text Input** – 4 × 4 Braille keypad lets users compose messages, which are echoed back in audio.  
- **Standalone Operation** – Entire pipeline runs on Raspberry Pi (no internet required after setup).

---

## Simulation Highlights
- **LED Matrix Prototype** demonstrating correct pin patterns for single letters and multi-cell words.  
- **Timing Analysis** shows reliable, bounce-free actuation within safe current limits.

---

## Software Implementation
| Component | Technology |
|-----------|------------|
| Image captioning | TensorFlow / Keras CNN |
| Speech recognition & translation | Hugging Face Transformers (MarianMT) |
| Text-to-speech | Python TTS modules |
| GPIO control | RPi.GPIO, time-sequenced shift-register logic |
| UI / API | Flask & Gradio dashboards |
| Prototyping | Jupyter notebooks |

---

## Hardware Implementation
- **Controller:** Raspberry Pi 4  
- **Drivers:** 74HC595 shift registers & ULN2803 Darlington array  
- **Display:** Custom 3-D-printed Braille cell caps with pin-actuation mechanism  
- **Peripherals:** Raspberry Pi Camera Module 3, LEDs, resistors, jumper wires, 4 × 4 Braille keypad, custom PCB

---

## Analysis & Results
| Module | Outcome |
|--------|---------|
| Braille cells | Accurate pin patterns; stable sequencing |
| Image captioning | Lightweight model deploys on Pi with acceptable latency |
| Audio translation | Clear, bi-directional translation across tested regional languages |

---

## Future Work
- Cloud storage & sharing of transcribed / translated content  
- Speaker diarisation and meeting summarisation  
- Edge/FPGA acceleration for larger Braille displays

---

## Repository Contents
| File / Folder | Purpose |
|---------------|---------|
| `imageCaptionGenerator.ipynb` | Vision-based captioning prototype |
| `translator.ipynb` | Multilingual speech/text translator |
| `cellController.ipynb` | GPIO control & Braille cell drive logic |
| `README.md` | Project documentation (this file) |
| `Smart-Image-and-Voice-to-Braille-Assistant-PPT.pdf` | Project PPT |

---

## Authors
- **R Kavin Kumar**
- **K Supriya**
- **Jaswanth Kumar N**  

Department of Electronics & Communication Engineering,  
Amrita Vishwa Vidyapeetham, Bengaluru Campus

---

## License
This project is intended for academic and research use only.  
For reuse or publication, please contact the authors directly.
