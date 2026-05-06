# 🕹️ Slink-Console

A high-fidelity retro snake engine built with vanilla JavaScript and HTML5 Canvas. **Slink-Console** features a custom-designed handheld UI and is optimized for zero-latency play on both desktop and mobile devices.

### 🔗 [Live Demo](https://YOUR_USERNAME.github.io/Slink-Console/)

---

## ✨ Features
* **Adaptive Viewport**: Automatically switches between an "Arcade Cabinet" desktop view and a "Handheld Console" mobile view.
* **Zero-Lag Touch Logic**: Uses a custom-built continuous slide sensor that resets anchors on every turn, allowing for fluid movement without lifting your finger.
* **Input Queueing**: A movement buffer that processes rapid "L-turn" inputs, preventing 180-degree self-collisions and missed turns.
* **Aesthetic Customization**: Includes a "Set-Up" menu to toggle background colors and snake variants like Charcoal, Gold, and Neon Blue.
* **Visual Realism**: Optimized sprite rendering with dynamic filters to provide a "Jam Red" fruit aesthetic.

## 🛠️ Tech Stack
* **Language**: Vanilla JavaScript (ES6+)
* **Graphics**: HTML5 Canvas API
* **Styling**: CSS3 (Media Queries, Flexbox, Glassmorphism)
* **Performance**: Optimized for 60fps rendering with a dedicated input queue for responsive controls.

## 🎮 How to Play
### Desktop
- **Movement**: Arrow Keys or `WASD`
- **Pause**: `SPACE`
- **Reset**: `R` key or the Reset button

### Mobile
- **Movement**: Slide your finger anywhere on the screen in the direction you want to turn.
- **D-Pad**: Use the physical-style cross buttons for precise navigation.
- **Pause/Settings**: Use the dedicated circular console buttons.

## 🚀 Deployment (GitHub Pages)
1. Push your code to the `main` branch.
2. Go to **Settings > Pages** in your GitHub repository.
3. Select `main` branch as the source and click **Save**.
4. Your console will be live at `https://<your-username>.github.io/Slink-Console/`.

---

## ⚖️ License
Distributed under the MIT License. See `LICENSE` for more information.
