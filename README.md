# ☀️ Tangled — Where the Sun's Magic Lives ✨

An interactive, gesture-controlled web experience inspired by Disney's *Tangled*. This application uses a standard webcam to track your hand movements in real-time, allowing you to release the sun's magic, paint with golden light, and summon a festival of floating lanterns.

🚀 **[Live Interactive Demo Link](YOUR_GITHUB_PAGES_LINK_HERE)**

---

## 🤖 Collaborative AI Engineering
This project was designed and engineered in an advanced human-AI pairing workflow using **Claude AI**. Through iterative prototyping and optimization, we built a highly performant, custom interactive engine from scratch. 

By avoiding heavy external rendering frameworks and relying entirely on a pure, vanilla HTML5 Canvas execution loop, the application comfortably maintains a fluid **60 FPS** while managing complex machine learning hand geometries and tracking hundreds of independent particle entities.

---

## 🖐️ Magic Gesture Guide

To navigate through the magic, face your webcam and use these specific hand shapes:

| Gesture Identity | Real-World Action | System Response | Phase |
| :--- | :--- | :--- | :--- |
| 🖐️ **Open Palm (Center)** | Hold open hand over the screen center | Charges & blooms the golden sun flower | Bloom Phase |
| ☝️ **Pointing Index** | Extend index finger (keep others closed) | Paints fluid, glowing strokes on the canvas | Canvas Phase |
| ✋ **Open Palm (Canvas)** | Wave your hand flat over your drawing | Acts as a wide eraser to clear lines | Canvas Phase |
| ✊ **Closed Fist** | Hold a tight fist for 2 seconds | Triggers phase transitions (Canvas ⇄ Lanterns) | Canvas / Lanterns |

---

## 🛠️ How It Works Behind the Scenes

* **Finite State Machine:** The app follows a strict state progression (`INIT` ➔ `BLOOM` ➔ `CANVAS` ➔ `LANTERNS`) to ensure clean transitions and zero background logic pollution.
* **Google MediaPipe Hands:** Processes real-time localized camera frames right in your browser to accurately map a 21-point hand skeleton.
* **Vector Smoothing (Lerp):** To prevent shaky lines from raw camera feeds, brush positions are mathematically smoothed so the trail flows elegantly behind your finger.
* **Dual Buffering Canvas:** Drawing data is drawn onto an offscreen canvas layer while the background particle systems render on the main loop, maximizing hardware acceleration.

---

## 🚀 Setting Up & Running Locally

The absolute easiest way to run and test this project is to open it directly using Google Chrome:

1. **Clone or Download the Repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/tangled-magic-canvas.git](https://github.com/YOUR_USERNAME/tangled-magic-canvas.git)
   cd tangled-magic-canvas

2.**Open with Google Chrome**: Simply double-click the index.html file, or drag and drop it straight into an open Google Chrome browser window.

⚠️ Webcam Troubleshooting Note: Modern browsers like Google Chrome have strict security rules regarding camera permissions. If you open the file directly (your URL bar starts with file:///) and the webcam fails to load, Chrome is blocking it for safety.

To fix this, you just need to host it on a local server context so Chrome knows it is safe:

Using VS Code: Right-click index.html and select Open with Live Server.
Using Terminal: Run a quick local Python server:
python -m http.server 8000
Then navigate to http://localhost:8000 in Chrome.

📜 **Built With:**

Vanilla JavaScript (ES6+), HTML5 Canvas, & CSS3

Google MediaPipe (hands.js & camera_utils.js)

Fairytale Typography via Google Fonts (Cinzel Decorative & Cormorant Garamond)
