# BSP2a — Audio-Driven Visualisation Template

**BSc (Hons) Computer Science — Norwich University of the Arts**
Unit: BSP2a: Models, Methods and Practice in Computer Science

---

## Overview

This template provides the starting structure for your BSP2a project. It includes a render loop skeleton in three rendering engines and an audio analysis pipeline stub. You will build your visualisation on top of it.

Fork this repository to your own GitHub account. All your work lives in your fork — commit regularly.

---

## Getting Started with GitHub Codespaces

1. On your forked repository, click the green **Code** button
2. Select the **Codespaces** tab
3. Click **Create codespace on main**

Your environment will open in the browser with all dependencies already available. No installation required.

To run the project:

```bash
python main.py
```

---

## Project Structure

```
bsp2a-template/
│
├── main.py                  # Entry point — set your rendering engine here
│
├── audio/
│   ├── analyser.py          # Audio analysis pipeline — implement your analysis here
│   └── your_audio_file.mp3  # Replace with your chosen audio file
│
├── engines/
│   ├── base.py              # RenderEngine base class
│   ├── pygame_engine.py     # PyGame engine — implement your visualisation here
│   ├── pyglet_engine.py     # Pyglet engine — implement your visualisation here
│   └── moderngl_engine.py   # ModernGL engine — implement your visualisation here
│
└── requirements.txt
```

---

## Rendering Engines

Three rendering engines are provided. Choose one and implement your visualisation inside it. Each gives you a blank window and a running render loop — everything else is yours to build.

| Engine | Description |
|---|---|
| **PyGameEngine** | 2D software rendering. Start here if you are new to real-time graphics. |
| **PygletEngine** | OpenGL-accelerated 2D/3D rendering. More performant than PyGame. |
| **ModernGLEngine** | Direct GPU access via OpenGL and GLSL shaders. |

Set your chosen engine in `main.py`:

```python
engine = setRenderingEngine(PyGameEngine)
```

---

## Audio Analysis

`audio/analyser.py` is where your audio analysis code lives. You will implement this as part of the unit. Your render loop will call into it each frame to get the current state of the audio.

Add your chosen audio file to the `audio/` folder and update the filename in `main.py`.

---

*For assessment requirements and submission details, refer to the BSP2a Unit Handbook and Project Brief.*