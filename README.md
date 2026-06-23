<img width="1912" height="906" alt="Screenshot 2026-06-23 075539" src="https://github.com/user-attachments/assets/2400bc52-2657-4481-ab69-3382beac6bb2" />
# 🌍 Potree Point Cloud Viewer — Customized 3D Visualization App

> An interactive, localized 3D viewer for large-scale LiDAR/point cloud datasets, built by customizing the open-source [Potree](https://github.com/potree/potree) WebGL renderer.

🔗 **Live Demo:** *(https://hagerhamdy-dev.github.io/3d-pointcloud-viewer-potree/)*
🔗 **ScreenShots**
![Uploading Screenshot 2026-06-23 075539.png…]()
![Uploading Screenshot 2026-06-23 025637.png…]()

---

## Overview

This project delivers a customized 3D point cloud viewer capable of rendering millions of points directly in the browser, with no plugins required. It was originally developed to support a GIS data-visualization task involving large LiDAR datasets, and demonstrates the ability to work inside a complex third-party JavaScript codebase, extend its core functionality, and adapt it to specific project and language requirements.

> **Data note:** This public demo uses an open LiDAR sample dataset from Auckland, New Zealand, shown here purely to illustrate the customized viewer. The original work was carried out as part of a client GIS project; the client's actual dataset is not shown here for confidentiality reasons.

## ✨ Key Features

- **Massive point cloud rendering** — adaptive point budget control (tested up to 2,000,000 points) for smooth performance on large datasets
- **Eye-Dome Lighting (EDL)** — adjustable radius, strength, and opacity for enhanced depth perception without normals
- **Multiple display modes** — switch between elevation-based coloring, RGB, intensity, and classification attributes
- **Arabic localization** — UI fully translated by editing the library's `i18next` translation files, alongside the existing EN/FR/DE/JP/ES language options
- **Custom tool configuration** — selective show/hide of sidebar panels (Appearance, Tools, Clipping) based on project requirements, controlled programmatically rather than relying on default library behavior
- **Custom-built functions** — additional tools added directly into the viewer beyond the library's default toolset
- **Background & display customization** — gradient/skybox/solid background options, adjustable splat quality and node size for performance tuning

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Rendering engine | [Potree](https://github.com/potree/potree) (built on Three.js / WebGL) |
| Data pipeline | [PotreeConverter](https://github.com/potree/PotreeConverter) — converts raw LAS/LAZ files into an optimized octree structure |
| Localization | i18next |
| UI | jQuery, jQuery UI, jstree (from the Potree toolkit) |
| Core language | JavaScript (ES6) |

## 🧩 My Contribution

This is **not** a viewer built from scratch — it is a customized application built on top of the open-source Potree library. My specific contributions were:

- Converting raw point cloud data (LAS/LAZ) into a web-optimized octree using PotreeConverter
- Setting up and configuring a dedicated viewer instance (point budget, description, GUI behavior) tailored to project needs
- Localizing the interface into Arabic by modifying the library's `i18next` translation files
- Customizing the original library's UI/JS files to control which tool panels appear, and in what state, on load
- Designing and implementing additional custom tools/functions integrated directly into the viewer's toolbar
- Adjusting material, lighting (EDL), and styling defaults to match project visual requirements



## 📂 Project Structure

```
├── auckland.html          # Main viewer entry point
├── libs/                  # Required Potree dependencies (three.js, i18next, jquery, etc.)
└── pointclouds/
    └── auckland/
        ├── metadata.json
        ├── hierarchy.bin
        └── octree.bin
```


## 🙏 Credits

Built on top of [Potree](https://github.com/potree/potree) by Markus Schütz and contributors, used under its open-source license. This project does not claim authorship of the core Potree rendering engine — only of the customizations, localization, and configuration described above.

## 👤 Author

**Hager Hamdy** — Web GIS Developer
[LinkedIn](https://www.linkedin.com/in/hager-hamdy-dev) · [GitHub](https://github.com/hagerhamdy-dev)
