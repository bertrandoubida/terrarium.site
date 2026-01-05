🌱 Terrarium — 3D Web Demo

This project is a simple 3D terrarium rendered directly in the browser.
It’s intentionally minimal, fast, and easy to deploy, while still using modern, production-ready tools.

The goal was not to build a large application — it was to create a clean, reliable way to display a 3D model on the web and deploy it smoothly to GitHub Pages.

✨ What This Project Shows

A 3D terrarium rendered using WebGL

Smooth camera interaction (rotate, view from different angles)

Works in development and production

Automatically deploys to GitHub Pages

🧠 Why These Tools Were Chosen (In Plain English)
Three.js

Three.js is the core 3D engine.

Why it’s used:

It’s the most widely adopted WebGL library

Handles lighting, cameras, and 3D model loading

Works directly in the browser with good performance

Without Three.js, building this would require low-level WebGL code, which is unnecessary for this use case.

GLTF / GLB Models

The terrarium is loaded as a .gltf (or .glb) model.

Why this format:

It’s the web standard for 3D assets

Loads faster than older formats

Keeps geometry, materials, and textures organized

Works natively with Three.js

This makes the model portable and easy to swap out later.

React

React is used only as a stable application wrapper, not for complex UI logic.

Why React is included:

StackBlitz previews React projects more reliably

React gives a predictable lifecycle (useEffect)

Makes cleanup and re-rendering safer

Keeps the Three.js setup contained in one place

React is not doing the 3D work — it simply ensures the page mounts cleanly.

Vite

Vite is the build and dev tool.

Why Vite was chosen:

Extremely fast startup

Minimal configuration

Works well with modern JavaScript and React

Produces a static build that GitHub Pages can serve

This keeps development fast and deployment simple.

GitHub Pages + GitHub Actions

Deployment is handled automatically using GitHub Actions.

Why this approach:

No manual build uploads

Every push to main triggers a fresh deploy

Ensures the live site always matches the repo

No server or backend required

GitHub Pages only serves static files, which makes it reliable and inexpensive.

🔁 How Development vs Deployment Works
Development (Local or StackBlitz)
npm run dev


Starts a live dev server

Changes show instantly

Used for previewing and debugging

Deployment (Automatic)
git push origin main


GitHub runs npm run build

Outputs static files

Publishes to GitHub Pages automatically

No manual steps required.

📁 Project Structure (Simplified)
.
├── public/           # Static assets (3D models, textures)
├── src/
│   ├── main.jsx      # React entry point
│   └── App.jsx       # Three.js scene setup
├── vite.config.js    # Build configuration
└── .github/workflows # Auto-deploy workflow


Each piece has a single responsibility, which keeps the project easy to understand and maintain.

🎯 Why This Setup Works Well

Minimal moving parts

No backend required

Fast load times

Easy to debug

Easy to deploy

Easy to extend later (UI, text, animations)

This setup is intentionally simple but scalable.

🚀 Possible Next Steps

Add a loading indicator

Add subtle animation or rotation

Add text or links overlayed on the scene

Replace the terrarium with another 3D model

Add mobile-specific camera tuning

🧩 Final Note

This project is designed to be understandable first, and impressive second.
Everything here was chosen because it solves a real problem cleanly, not because it adds complexity.
