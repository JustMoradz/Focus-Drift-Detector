# Focus Drift Detector – Chrome Extension

**Focus Drift Detector** is a Chrome extension that measures **user focus stability in real-time** while browsing. Unlike traditional time trackers, it analyzes **scrolling, mouse movements, and tab switching** to provide a **Focus Stability Score** ranging from 0 to 1.

---

## Features

* Floating widget showing current focus on any webpage
* Popup UI with live score and status indicator
* Updates every 2 seconds for real-time feedback
* Lightweight and responsive interface using HTML, CSS, and JavaScript
* Chrome Extension (Manifest v3) leveraging background and content scripts
* Local storage for syncing score across tabs

---

## Mathematical Model

The Focus Stability Score **F** is calculated using behavioral variance metrics:

[
\mathbf{F} = e^{- (0.5 \cdot \mathbf{TS} + 0.3 \cdot \mathbf{SV} + 0.2 \cdot \mathbf{MV})}
]

Where:

* **TS** = Tab Switching Rate
* **SV** = Scroll Variance
* **MV** = Mouse Movement Variance

Weights were chosen empirically based on observed user behavior. The exponential ensures that small increases in variance significantly reduce the score. The result is normalized between 0 (low focus) and 1 (deep focus).

---

## Data Engineering Aspect

This project demonstrates **data engineering principles**:

* Real-time **data collection** from browser interactions
* **Transformation and aggregation** using variance calculations and weighted scoring
* **Local storage** for persistent, structured data
* Can be extended to export data to a server or cloud storage for further analytics

---

## Installation

1. Clone the repository:

```
git clone https://github.com/JustMoradz/Focus-Drift-Detector/
```

2. Open Chrome and go to `chrome://extensions/`
3. Enable **Developer Mode**
4. Click **Load unpacked** and select the project folder

---

## Usage

* Scroll, move your mouse, and switch tabs on any page
* The floating widget shows your real-time focus
* Open the popup to see a live score and status indicator

---

## License

MIT License


* 📂 GitHub: [Add link]
* 🌐 Chrome Web Store: [Add link]
