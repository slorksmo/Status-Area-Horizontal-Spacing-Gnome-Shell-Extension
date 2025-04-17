# Status Area Horizontal Spacing – GNOME Shell Extension (Updated for GNOME 48)

This GNOME Shell extension reduces the horizontal spacing between status area icons (top-right of the panel: volume, battery, wifi, etc). 

Tested and fully working on:
- GNOME 3.2 → 3.38
- GNOME 40 → 45
- ✅ **GNOME 48 (manually patched)**

---

## 🔍 Before vs After

**Default spacing (12px):**
![original (12px padding)](status_area_original.png)

**Reduced spacing (6px):**
![after with 6px padding](status_area_6px.png)

---

## 📥 Quick Demo

🎥 [Watch video on how the extension works (YouTube)](https://youtu.be/demo-status-area)

Or preview the result in this short clip:
![demo gif](status_area_spacing_demo.gif)

---

## 📦 Installation

### 🔘 One-click (GNOME 3.x–45):
From extensions.gnome.org: [link here](https://extensions.gnome.org/extension/355/status-area-horizontal-spacing/)

### 🧰 Manual (GNOME 46–48):
1. Download the patched ZIP (compatible with GNOME 48)
2. Extract to:
   ```
   ~/.local/share/gnome-shell/extensions/status-area-horizontal-spacing@mathematical.coffee@gmail.com/
   ```
3. Compile GSettings schemas (if needed):
   ```
   glib-compile-schemas ~/.local/share/gnome-shell/extensions/status-area-horizontal-spacing@mathematical.coffee@gmail.com/schemas/
   ```
4. Restart GNOME Shell:
   - X11: `Alt + F2`, then type `r` → Enter
   - Wayland: Logout and log back in
5. Enable the extension:
   ```
   gnome-extensions enable status-area-horizontal-spacing@mathematical.coffee@gmail.com
   ```

---

## ⚙️ Configuration

Open the Preferences window via:
```bash
gnome-extensions prefs status-area-horizontal-spacing@mathematical.coffee@gmail.com
```
Or from the **Extensions** app.

### Options available:
- Adjust horizontal padding between panel icons (default: 6px)
- Fine-tune spacing to fit your theme or layout

---

## 💬 Support

🛠 Facing issues or want to contribute?
- Open an issue on GitHub: [GitHub Issues](https://github.com/slorksmo/Status-Area-Horizontal-Spacing-Gnome-Shell-Extension/issues)
- Pull requests welcome!

📧 Contact Maintainer:
- Email: slorksmo@gmail.com
- Discussions: [GitHub Discussions](https://github.com/slorksmo/Status-Area-Horizontal-Spacing-Gnome-Shell-Extension/discussions)

🤝 You can also reach out via [chat on Matrix](https://matrix.to/#/#gnome-ext:matrix.org)

---

## 🧑‍💻 For Developers

### Branches:
- `main` → updated version supporting GNOME 48
- `gnome3.2` → legacy branch, manual config via `extension.js`
- `gnome3.4`, `gnome3.10+` → legacy UI-configurable branches
- `stable` → obsolete

---

## 🪛 Alternative (not recommended)
You can manually patch your system theme file:
```css
.panel-button {
    -natural-hpadding: 6px;
}
```
But this change will be lost upon theme updates, GNOME upgrades, or shell resets. Use the extension for persistent results.

---

## 🙌 Contributors
Originally created by [mathematical.coffee@gmail.com](mailto:mathematical.coffee@gmail.com)  
Patched for GNOME 48 compatibility by [slorksmo](https://github.com/slorksmo)
