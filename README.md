# AIoT Learning Explorer — Interactive Knowledge Tree

The **AIoT Learning Explorer** is an interactive, web-based educational dashboard designed by NIELIT Ropar. It provides a structured, visually engaging "knowledge tree" for students and enthusiasts to explore concepts in Artificial Intelligence of Things (AIoT), Arduino programming, and RoboCar fundamentals. 

## ✨ Features

* **Interactive Knowledge Tree Layout**: Hierarchical navigation that lets users seamlessly drill down from high-level Domains (e.g., Auduino, Robo Car) to specific Categories (e.g., DC Motor, LED Button) and ultimately to actionable Topics.
* **Live Google Sheets Integration**: Fetch and render syllabus and practical contents dynamically from a published Google Sheet CSV URL. A built-in dataset acts as a fallback.
* **Progress Tracking & Gamification**: Users can click on individual practical steps to mark them as complete. The application calculates overall learning progress, saves it locally (`localStorage`), and triggers a confetti animation when an entire topic is mastered.
* **Dark & Light Modes**: Fully responsive UI with a built-in theme toggle for comfortable day or night reading.
* **Search & Shortcuts**: Includes a powerful client-side search bar to quickly filter topics, domains, and categories. Press `/` on your keyboard to instantly focus the search bar.
* **Resource Links**: Direct integration with external simulators (like TinkerCAD) for hands-on, browser-based practice.
* **Interactive Visuals**: Features an animated HTML5 canvas particle background and dynamic CSS grid-shift animations.

## 🗂 Project Structure

```text
NIELITAIoT/
├── index.html                 # Main dashboard UI, styling, and application logic
└── assets/
    ├── ndu-logo.png           # NIELIT Deemed to be University branding logo
    └── AIOT PROJECT.csv       # Sample dataset containing domains, topics, and practical steps

```

## 🚀 Getting Started

Since this is a client-side application built with plain HTML, CSS, and Vanilla JavaScript, no complex installation or build steps are required.

1. **Clone the repository**:
```bash
git clone [https://github.com/nielitropar/NIELITAIoT.git](https://github.com/nielitropar/NIELITAIoT.git)

```


2. **Open the application**:
Simply open `index.html` in any modern web browser.
```bash
open index.html

```



## 📊 Using Custom Data (Google Sheets Sync)

By default, the dashboard loads a built-in set of Arduino and RoboCar tutorials. You can easily feed your own curriculum into the dashboard using Google Sheets.

### CSV Format Requirements

Your dataset (like the provided `AIOT PROJECT.csv`) must contain the following headers:

* `Domain`: The top-level category (e.g., *Auduino*, *Robo Car*).
* `Tabcat`: The sub-category (e.g., *Button*, *DC Motor*).
* `Tab`: The specific lesson or topic name (e.g., *Button Interfacing with Arduino*).
* `Practical Content`: A numbered list of steps (separated by line breaks) defining the hands-on instructions.
* `Links` (Optional): A URL for external learning, such as a TinkerCAD simulator link.
* `Pics` (Optional): A URL to a reference image for the circuit or project.

### How to Sync:

1. Create a Google Sheet formatted with the columns above.
2. Go to **File** > **Share** > **Publish to web** and select **CSV**. Alternatively, ensure the link sharing is set to "Anyone with the link can view".
3. Paste the URL into the "Paste Google Sheet URL" bar at the top right of the dashboard and click **⚡ Load**.

## 🛠 Tech Stack

* **Frontend**: HTML5, Vanilla JavaScript (ES6+).
* **Styling**: Pure CSS3 (CSS Variables, Flexbox, UI Animations, Hover Effects).
* **Storage**: Browser `localStorage` for persisting theme preferences and learning progress.

## 🎓 About NIELIT Ropar

This project is developed under the **National Institute of Electronics & Information Technology (NIELIT), Ropar** to foster accessible, structured, and interactive education in the rapidly growing field of AIoT and Embedded Systems.

