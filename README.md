# Air-canvas-by-hand

A project that lets you draw “in the air” by hand gestures — turning motion into canvas strokes, using computer vision and hand tracking.

## Table of Contents

* [About](#about)
* [Features](#features)
* [Demo / Screenshot](#demo-screenshot)
* [Requirements](#requirements)
* [Installation](#installation)
* [Usage](#usage)
* [How It Works](#how-it-works)
* [Future Improvements](#future-improvements)
* [License](#license)
* [Author](#author)

## About

This project uses hand-tracking (via webcam) to detect finger movements and allows the user to “paint” in the air. It demonstrates real-time gesture recognition and mapping those gestures to drawing events on a virtual canvas.

## Features

* Real-time hand detection and tracking using the webcam
* Gesture recognition: e.g., index finger up = drawing mode, fist = pause/stop
* Virtual canvas on screen showing the drawn strokes
* Optional: change brush colour or thickness via hand gestures (if implemented)
* Notebook version (Jupyter) for step-by-step explanation and visualisation

## Requirements

* Python 3.x
* OpenCV
* Mediapipe (or other hand-tracking library)
* Numpy (and other standard scientific packages)
* Jupyter Notebook (if you wish to run the notebook version)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/akshat142005/Air-canvas-by-hand.git  
   cd Air-canvas-by-hand  
   ```
2. Create and activate a virtual environment (optional but recommended):

   ```bash
   python3 -m venv venv  
   source venv/bin/activate   # On Windows: venv\Scripts\activate  
   ```
3. Install dependencies:

   ```bash
   pip install -r requirements.txt  
   ```

   *(If you don’t already have a `requirements.txt`, create one with: `opencv-python`, `mediapipe`, `numpy`, etc.)*

## Usage

* Open the notebook `air canvas in step.ipynb` (or run the main script if you converted it)
* Make sure your webcam is enabled
* Execute the code cell to start capturing hand gestures
* Raise your index finger to draw on the virtual canvas
* Close the window or stop the script when done

## How It Works

1. The webcam captures video frames.
2. Hand detection and landmark tracking are performed (via Mediapipe or similar).
3. Based on the hand landmarks, determine which fingers are up/down (e.g., index finger only = draw mode; index + middle = erase mode; fist = pause).
4. Map the index finger tip position to canvas coordinates and draw lines accordingly.
5. Display the resulting image on screen, refresh for each frame.

## Future Improvements

* Add annotations or GUI for colour/thickness selection
* Add an “undo” or “clear canvas” gesture
* Improve gesture accuracy and robustness under various lighting/backgrounds
* Export the canvas drawing as an image file or video animation
* Optimize performance for lower‐end hardware

## Author

**Akshat Gupta**
B.Tech Computer Science (Data Science) | Oriental Institute of Science and Technology, Bhopal
GitHub: [akshat142005](https://github.com/akshat142005)
Feel free to reach out for contributions, suggestions or feedback.
