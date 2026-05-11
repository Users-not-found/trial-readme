# ZenithWriter 📄

**ZenithWriter** is a high-performance, local-first Markdown workspace designed for developers who value privacy, speed, and a professional aesthetic. It eliminates the middleman by connecting your browser directly to your local file system.

<hr style="border: none; border-top: 1px solid #444;">

## ✨ Core Features

*   **Modular Architecture:** Cleanly separated HTML5, CSS3, and Vanilla JavaScript for easy customization.
*   **Native File System Access:** Uses the modern File System Access API to open, edit, and save files directly to your machine.
*   **Persistent Workspace:** Integrated **IndexedDB** caching ensures your open file list and active session are restored instantly upon browser refresh.
*   **Real-time GFM Preview:** Instant GitHub Flavored Markdown rendering powered by `marked.js`.
*   **Advanced Explorer:** 
    *   System-to-browser **Drag & Drop** support.
    *   Manual reordering with **Drag Handles (⠿)**.
    *   Collapsible file info (**ⓘ**) for metadata.
    *   Bulk deletion using selection markers.
*   **"Zero-Footprint" UI:** 
    *   Cinematic dark aesthetic with Rembrandt lighting.
    *   **No-Blink Protocol:** Caret transparency on UI elements to prevent distraction.
    *   **Resizable Layout:** Custom-built column resizers for a flexible workspace.

<hr style="border: none; border-top: 1px solid #444;">

## 🛠️ Technical Details

*   **Logic:** Vanilla JavaScript (ES6+)
*   **Persistence:** Local IndexedDB (`ZenithCache`)
*   **Markdown Engine:** [Marked.js](https://marked.js.org/)
*   **Font Stack:** Inter (UI) & Fira Code (Editor)
*   **Environment:** 100% Offline-capable, no external API dependencies.

<hr style="border: none; border-top: 1px solid #444;">

## 📁 Project Structure

```text
/ZenithWriter
  ├── index.html   # Structure & UI Layout
  ├── style.css    # Professional Dark Aesthetic & Layout Logic
  ├── script.js    # Core Logic, File System API, & Persistence
  ├── README.md    # Project Documentation
  └── LICENSE      # MIT License

```
<hr style="border: none; border-top: 1px solid #444;">

## 🚀 Setup & Usage
1. Download:
* Save all project files into a single folder.

2. Launch:
* Open index.html in any modern web browser (Chrome or Edge recommended).

3. Edit:
* Use Open File to sync with your local .md, .js, or .txt files.
* Type in the editor; the Live Preview updates instantly.
* Use Save As to commit changes back to your local disk.

<hr style="border: none; border-top: 1px solid #444;">

## 📜 License
Distributed under the MIT License. See the LICENSE file for details.

Created with ❤️ by ALWIN K J
