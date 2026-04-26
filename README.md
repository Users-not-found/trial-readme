# Pixaro ✂️

Pixaro is a lightweight, web-based tool designed for smart background removal and sticker creation. It leverages AI directly in the browser to detect subjects and provides a suite of editing tools to customize your images.

## ✨ Features

* **Smart Background Removal**: Powered by the `u2netp` model via ONNX Runtime Web for fast, local inference.
* **Sticker Tools**: Easily reposition, align, and scale detected subjects.
* **Text & Customization**: Add stylized text with various fonts, draw with a brush, or clean up edges with an eraser.
* **Canvas Controls**: Support for panning, zooming, and undo/redo functionality.
* **Export**: Save your creations directly as `.webp` files.

## 🛠️ Technical Stack

* **Engine**: ONNX Runtime Web (WASM backend)
* **AI Model**: U2NetP (Universal Background Removal)
* **Frontend**: Vanilla JavaScript, HTML5 Canvas, CSS3
* **Security**: Includes `coi-serviceworker` to enable cross-origin isolation for high-performance multithreading.

## 🚀 Getting Started

1.  **Clone or Unzip**: Extract the project files to your local directory.
2.  **Web Server**: Due to the use of Service Workers and WASM, the project must be served via a local web server (e.g., Live Server in VS Code or `python -m http.server`).
3.  **Open**: Navigate to `index.html` in your browser.

### Usage
* Click **Open Image** to upload a photo.
* Use the **Scan Subject** tool to preview boundaries.
* Use the **Align** tool to snap the sticker to the center or edges.
* Add text and decorations before hitting **Export**.

## ⌨️ Shortcuts

| Shortcut | Action |
| :--- | :--- |
| **Space + Drag** | Pan the canvas |
| **Scroll Wheel** | Zoom in/out at the cursor position |
| **Ctrl + Z / Y** | Undo and Redo actions |
| **ESC** | Unselect tools or close modals |
| **DEL / Backspace** | Remove selected text elements |
