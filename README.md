AR Wig Studio
A browser-based augmented reality application that enables real-time virtual wig try-on using a device camera. Built entirely with vanilla JavaScript and the HTML5 Canvas API, with no external dependencies or backend infrastructure.

https://img.shields.io/badge/status-active-brightgreen
https://img.shields.io/badge/license-MIT-blue
https://img.shields.io/badge/privacy-100%25%20local-purple
https://img.shields.io/badge/dependencies-none-success

Project Summary
AR Wig Studio is a single-page web application that allows users to virtually try on wigs in real time. Users upload a transparent PNG of a wig, position it on their head using intuitive controls, and see themselves wearing it live through their camera.

The project was designed and built independently as a practical exercise in browser-based computer vision, real-time rendering, and responsive UI design. It demonstrates proficiency in the MediaDevices API, Canvas 2D rendering, and client-side state management.

Live Demo: https://Udedavid12.github.io/wig-app/

Key Features
Feature	Technical Implementation
Real-time camera feed	MediaDevices.getUserMedia() with front/rear camera switching
Live wig overlay	HTML5 Canvas 2D rendering at 30fps using requestAnimationFrame
Positioning controls	Four real-time sliders for size, horizontal offset, vertical offset, and rotation
Image upload	FileReader API with base64 encoding for local processing
Photo capture	canvas.toDataURL() for client-side PNG export
Collage builder	Dynamic canvas composition of up to six saved looks
Responsive design	CSS Flexbox, custom properties, and media queries for mobile support
Privacy-first architecture	Zero network requests; all data remains in the browser
Technical Stack
Layer	Technology
Markup	HTML5
Styling	CSS3 (Flexbox, custom properties, backdrop-filter)
Logic	Vanilla JavaScript (ES6+)
Rendering	Canvas 2D API
Camera	MediaDevices API
Storage	Client-side only (no persistence layer)
Dependencies	None
Build Tools	None
The entire application is contained in a single index.html file, demonstrating the ability to deliver a complete, functional product without relying on frameworks or external libraries.

Architecture Overview
text
User Device
├── Camera Stream (MediaDevices API)
│   └── Live video feed
├── Canvas Layer (2D Context)
│   ├── Video frame rendering (mirrored)
│   └── Wig overlay rendering
├── UI Layer (HTML/CSS)
│   ├── Slider controls
│   ├── Upload interface
│   └── Capture and export buttons
└── State Management (JavaScript)
    ├── Wig image reference
    ├── Transform values (size, position, angle)
    └── Camera facing mode
The architecture follows a unidirectional data flow: user input updates state, state drives rendering, and rendering occurs on every animation frame. This ensures smooth, lag-free performance even on mid-range mobile devices.

Engineering Decisions
Decision	Rationale
No frameworks	Reduces bundle size, eliminates dependency risk, and demonstrates core JavaScript proficiency
Single-file architecture	Simplifies deployment, improves portability, and lowers hosting complexity
Canvas-based rendering	Provides precise control over image composition and enables pixel-perfect export
Client-side processing only	Guarantees user privacy, eliminates server costs, and removes latency
Slider-based positioning	Gives users full control without requiring face detection or machine learning models
How to Use
1. Obtain a Wig Image
Search for "wig png transparent" on Google Images, or use a background removal tool such as remove.bg to isolate a wig from a screenshot.

2. Open the Application
Navigate to the hosted URL. The application works on desktop, tablet, and mobile browsers.

3. Try On Wigs
Tap Start and allow camera access.

Tap Upload Wig and select a PNG file.

Adjust the sliders to position the wig naturally.

Tap Save to export the current frame as a PNG.

Tap Flip if the wig needs to be mirrored.

Tap Switch Camera to toggle between front and rear cameras.

Installation and Deployment
Option 1: GitHub Pages (Recommended)
Fork or clone this repository.

Navigate to Settings > Pages.

Under Branch, select main and click Save.

Wait one to two minutes for deployment.

Access the site at https://Udedavid12.github.io/wig-app/.

Option 2: Local Development
Camera access is blocked for file:// URLs by browser security policy. Use a local HTTP server:

bash
# Node.js
npx serve

# Visual Studio Code
Install the "Live Server" extension, then right-click index.html and select "Open with Live Server".
Then visit http://localhost:8000 in your browser.

Option 3: CodePen
Paste the contents of index.html into the HTML panel at codepen.io/pen and save.

Browser Compatibility
Browser	Supported
Chrome	Yes
Edge	Yes
Firefox	Yes
Safari	Yes
Samsung Internet	Yes
Camera access requires a secure context (HTTPS). GitHub Pages, CodePen, and Netlify provide HTTPS by default.

Testing Checklist
Test	Status
Camera initializes on desktop	Pass
Camera initializes on mobile	Pass
Wig uploads and renders correctly	Pass
Sliders update the wig position in real time	Pass
Capture exports a valid PNG	Pass
Front and rear camera switching works	Pass
Responsive layout on 375px width	Pass
No console errors on load	Pass
Skills Demonstrated
Skill	Evidence
JavaScript (ES6+)	Full application logic, state management, event handling
HTML5 Canvas	Real-time rendering, image composition, export pipeline
MediaDevices API	Camera stream acquisition, constraint configuration, track management
Asynchronous JavaScript	async/await for camera initialization and stream handling
Responsive CSS	Flexbox layouts, media queries, mobile-first design
File API	Client-side image upload and base64 encoding
Debugging	Error handling for camera permissions, missing devices, and invalid input
Product thinking	Intuitive UI, clear status feedback, and graceful fallbacks
Future Enhancements
□ Optional face detection for automatic wig positioning
□ Multiple wig layers for stacked styles
□ Hue and saturation adjustment for color matching
□ Social media sharing integration
□ Pre-loaded wig library for instant try-on
□ Progressive Web App (PWA) support for offline use
Project Structure
text
wig-app/
├── index.html      Application (HTML, CSS, JavaScript)
├── README.md       Documentation
└── LICENSE         MIT License
Lessons Learned
Building this project reinforced several key engineering principles:

Constraint-driven design works. Limiting the project to a single file and zero dependencies forced creative problem-solving and deeper understanding of core web APIs.

User experience matters as much as functionality. Clear status messages, responsive controls, and graceful error handling make the difference between a demo and a product.

Privacy can be a feature. By keeping all processing client-side, the application offers a level of privacy that server-based alternatives cannot match.

Deployment is part of development. Understanding HTTPS requirements, browser security policies, and hosting options is essential for shipping real products.

License
This project is licensed under the MIT License. See the LICENSE file for details.

Contact
For questions, feedback, or collaboration opportunities, please open an issue in this repository or reach out via GitHub.
