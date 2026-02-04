# Web Video Editor Concept

A modern, responsive web-based video editing interface built with **Tailwind CSS** and native **JavaScript**. This project serves as a high-fidelity UI/UX prototype for a browser-based Non-Linear Editor (NLE).

## 🚀 Features

* **Video File Ingestion:** Real-time video uploading using `URL.createObjectURL` for instant preview without server-side processing.
* **Dynamic Timeline:** A visual representation of video tracks that populates automatically upon file upload.
* **Interactive Playhead:** Scrub through the video by clicking or dragging across the timeline area.
* **Responsive Preview:** A centralized video player that maintains aspect ratio and scales across devices.
* **Property Inspection:** Context-aware sidebar that displays clip metadata (duration, name) and conceptual controls (opacity) when a clip is selected.
* **Toolbox UI:** Side navigation for common editing tasks:
    * ✂️ Trim Tool
    * 文字 Text Overlays
    * 🎭 Visual Filters
    * 🎵 Audio Management
* **Timeline Zooming:** Conceptual scaling (0.5x to 5x) to view fine details or the entire project duration.

## 🛠️ Technical Stack

* **Frontend:** HTML5, Tailwind CSS (via CDN)
* **Icons:** Heroicons / Custom SVG
* **Typography:** Inter (Google Fonts)
* **Engine:** Native JavaScript (ES6+)

## 📂 Project Structure

| Component | Description |
| :--- | :--- |
| **Header** | Contains project title and global actions (Upload/Export). |
| **Aside (Toolbar)** | Vertical tool switcher for editing modes. |
| **Main Preview** | The `aspect-video` container for the video playback. |
| **Properties Panel** | Dynamic area that changes based on the active selection. |
| **Footer (Timeline)** | Multi-track area with playhead tracking and timecode display. |

## 📝 Implementation Notes

### Playhead Synchronization
The playhead position is calculated as a percentage of the total video duration:
$$\text{Position \%} = \left( \frac{\text{Current Time}}{\text{Total Duration}} \right) \times 100$$

### Performance
The application uses `URL.revokeObjectURL` after metadata is loaded to ensure memory efficiency during long sessions.

## 🚧 Roadmap (Future Concepts)
- [ ] **Multi-layer Composition:** Support for overlapping video clips.
- [ ] **Canvas Rendering:** Applying real-time CSS/WebGL filters to the video output.
- [ ] **Waveform Generation:** Visualizing audio frequencies in the Emerald track.
- [ ] **FFmpeg.wasm Integration:** Enabling actual video rendering and exporting within the browser.

---
*Created as a UI Concept for Web-based Creative Tools.*
