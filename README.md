# 🌱 Terrarium — 3D Web Demo

This project is a **minimal 3D terrarium rendered directly in the browser**.  
It focuses on clarity, performance, and reliability rather than complexity.

The goal is simple: **load a 3D model cleanly, preview it easily, and deploy it reliably** using modern web tools.

---

## ✨ What This Project Does

- Renders a 3D terrarium using WebGL
- Allows smooth camera interaction (rotate / inspect)
- Works in local development and online previews
- Automatically deploys to GitHub Pages

---

## 🧠 Why These Tools Were Chosen (Plain English)

### **Three.js**
Three.js handles all 3D rendering.

**Why it’s used:**
- Industry-standard WebGL library
- Handles lighting, cameras, and model loading
- Saves writing low-level WebGL code

---

### **GLTF / GLB Models**
The terrarium is loaded as a `.gltf` file.

**Why this format:**
- Web-native 3D standard
- Fast loading and efficient
- Keeps geometry, materials, and textures together
- Fully supported by Three.js

---

### **React**
React is used **only as a lightweight application wrapper**.

**Why React is included:**
- Provides a predictable lifecycle (`useEffect`)
- Prevents duplicate renders and memory leaks
- Makes previews more reliable in StackBlitz
- Keeps Three.js setup isolated and stable

React is not responsible for rendering the 3D scene — it simply manages when it mounts.

---

### **Vite**
Vite is used as the development and build tool.

**Why Vite was chosen:**
- Very fast startup
- Minimal configuration
- Works well with modern JavaScript and React
- Produces static files GitHub Pages can serve

---

### **GitHub Pages + GitHub Actions**
Deployment is fully automated.

**Why this approach works well:**
- No manual builds
- No servers to manage
- Every push to `main` triggers a new deployment
- Live site always matches the repository

---

## 🔁 Development vs Deployment

### Development (Local / StackBlitz)
```bash
npm run dev
```

## 🧩 Final Note

This project is designed to be understandable first, and impressive second.
Everything here was chosen because it solves a real problem cleanly, not because it adds complexity.
