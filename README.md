# AR Wig Studio

A browser-based augmented reality application that enables real-time virtual wig try-on using a device camera. Built entirely with vanilla JavaScript and the HTML5 Canvas API, with no external dependencies or backend infrastructure.

![Status](https://img.shields.io/badge/status-active-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Privacy](https://img.shields.io/badge/privacy-100%25%20local-purple)
![Dependencies](https://img.shields.io/badge/dependencies-none-success)

---

## Project Summary

AR Wig Studio is a single-page web application that allows users to virtually try on wigs in real time. Users upload a transparent PNG of a wig, position it on their head using intuitive controls, and see themselves wearing it live through their camera.

The project was designed and built independently as a practical exercise in browser-based computer vision, real-time rendering, and responsive UI design. It demonstrates proficiency in the MediaDevices API, Canvas 2D rendering, and client-side state management.

**Live Demo:** [https://yourusername.github.io/wig-app/](https://yourusername.github.io/wig-app/)

---

## Key Features

| Feature | Technical Implementation |
|---------|--------------------------|
| Real-time camera feed | `MediaDevices.getUserMedia()` with front/rear camera switching |
| Live wig overlay | HTML5 Canvas 2D rendering at 30fps using `requestAnimationFrame` |
| Positioning controls | Four real-time sliders for size, horizontal offset, vertical offset, and rotation |
| Image upload | `FileReader` API with base64 encoding for local processing |
| Photo capture | `canvas.toDataURL()` for client-side PNG export |
| Collage builder | Dynamic canvas composition of up to six saved looks |
| Responsive design | CSS Flexbox, custom properties, and media queries for mobile support |
| Privacy-first architecture | Zero network requests; all data remains in the browser |

---

## Technical Stack

| Layer | Technology |
|-------|------------|
| Markup | HTML5 |
| Styling | CSS3 (Flexbox, custom properties, backdrop-filter) |
| Logic | Vanilla JavaScript (ES6+) |
| Rendering | Canvas 2D API |
| Camera | MediaDevices API |
| Storage | Client-side only (no persistence layer) |
| Dependencies | None |
| Build Tools | None |

The entire application is contained in a single `index.html` file, demonstrating the ability to deliver a complete, functional product without relying on frameworks or external libraries.

---

## Architecture Overview
