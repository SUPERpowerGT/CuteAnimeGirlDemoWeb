<p align="center">
  <img 
    src="https://github.com/user-attachments/assets/382eb332-40ea-4b83-a9a2-0c191b33698d"
    alt="Cute Anime Girl Logo"
    width="320"
  />
</p>


<h1 align="center">🌸 Cute Anime Girl 3D Demo</h1>

<p align="center">
  <em>A Unity WebGL interactive demo – fully playable in your browser ✨</em>
</p>

<p align="center">
  🎮 <b>Play Online:</b>  
  👉 <a href="https://superpowergt.github.io/CuteAnimeGirlDemoWeb/" target="_blank">
  https://superpowergt.github.io/CuteAnimeGirlDemoWeb/
  </a>
</p>

---

## ✨ Overview

This demo showcases the **full pipeline of creating an interactive 3D character experience** — from modeling and animation to Web deployment.

### 🌈 Features & Workflow
- 🧍‍♀️ **3D Anime Character Creation**
  - Designed and edited in **Blender**, including mesh cleanup, hair shaping, and material tuning.
  - Exported as `.fbx` for animation retargeting and Unity integration.
- 🕺 **Character Animation**
  - Motion sequences imported and retargeted from **Mixamo** (Idle, Walk, Wave, Yawn, Hand Gesture).
  - Animator Controller built in Unity to manage animation state transitions via key input (2–5) or UI buttons.
- 🎥 **Camera System**
  - Custom **Orbit Camera Controller** supports:
    - Left mouse drag → rotate character  
    - Scroll wheel → zoom in/out  
    - **R key** → reset view  
- 💡 **Scene Composition**
  - Simple gradient background with soft lighting and real-time shadows.
  - Optimized for performance under Unity **URP (Universal Render Pipeline)**.
- 🖼️ **UI & Interaction**
  - Built with **Unity Canvas + TMP (TextMeshPro)**.  
  - Responsive design for both **Web** and **Mobile**.
  - Click or press number keys to trigger character actions (2–5).
- 🔊 **Audio Integration**
  - Ambient BGM with dynamic pause/resume logic.
  - Button click sounds linked via `UIClickSound.cs`.
- 🧩 **Scripting & Logic**
  - Modular C# scripts for each system:
    - `CuteGirlController.cs` – animation logic  
    - `OrbitCameraController.cs` – camera orbit + zoom  
    - `SceneFadeIn.cs` – fade-in scene entry  
    - `UIClickSound.cs` – UI sound effects
- 🚀 **WebGL Build & Deployment**
  - Exported through Unity **WebGL Build System**.
  - Hosted publicly via **GitHub Pages**, accessible from any browser.

> This demo represents a complete workflow — from 3D modeling to animation, rendering, UI design, interactivity, and Web deployment.

---

## 🎮 Controls

| Action | PC (Keyboard / Mouse) | Mobile (Touch) |
|--------|------------------------|----------------|
| Rotate character | **Left mouse button** and drag | Drag with one finger |
| Zoom in/out | **Mouse scroll wheel** | Pinch gesture |
| Switch to “Moon” action | Press **2** | Tap the “Moon” icon |
| Switch to “Shit” action | Press **3** | Tap the 💩 icon |
| Switch to “Expression” action | Press **4** | Tap the “Face” icon |
| Toggle Walk / Idle state | Press **5** | Tap the “Footstep” icon |
| Reset camera view | Press **R** | — |

> 💡 **Tips:**  
> • You can switch all actions either by clicking the UI icons or using number keys (2–5).  
> • Left mouse drag to orbit the character, scroll to zoom at any time.  
> • Press **R** to quickly reset the camera to its default angle.

---

## 🖼️ Preview
<p align="center">
<img width="1024" height="699" alt="63069390bb8239ef8273880292f0e0a4" src="https://github.com/user-attachments/assets/2ebef078-dbab-4208-831d-46442eda7437" />
</p>

---

## 🛠️ Tech Stack

| Component | Description |
|------------|--------------|
| 🎮 **Engine** | Unity 6.2 (URP Render Pipeline) |
| 🧱 **Export Target** | WebGL |
| ☁️ **Hosting** | GitHub Pages |
| 💡 **Language** | C# |
| 🧩 **UI Toolkit** | Unity UI (Canvas + Image + TMP) |
| 🔊 **Audio** | Integrated with camera and animation controls |
| 🧍‍♀️ **3D Modelling** | Blender — used for character mesh editing and pose adjustment |
| 🕺 **Animation Rigging** | Mixamo — applied for motion retargeting and animation import |

---

## 🧱 Project Structure

```text
CuteAnimeGirlDemo/
├── Assets/
│   ├── 🎵 Audio/
│   │   ├── Bg_music_soft_chile.mp3 — background BGM
│   │   ├── button_click.wav — UI button click sound
│   │   └── fart.wav — funny sound effect for testing
│   │
│   ├── 🧍‍♀️ Character/
│   │   ├── Animations/ — imported Mixamo motion clips (idle, walk, wave, etc.)
│   │   ├── Controllers/ — Animator Controllers for character states
│   │   ├── Materials/ & Textures/ — character visual assets
│   │   └── CuteGirl_Idle.prefab — main playable 3D model prefab
│   │
│   ├── 🔤 Fonts/
│   │   ├── Pacifico-Regular — UI title font
│   │   └── Font Material & Font Texture — TMP rendering assets
│   │
│   ├── 🖼️ Images/
│   │   ├── moon.png, poop.png, boring.png — emoji action icons
│   │   ├── settings.png, return.png, Exit.png — UI control buttons
│   │   └── circle.png, RoundRec.png — reusable UI shape masks
│   │
│   ├── 🎨 Materials/
│   │   └── SoftGradientBackground.mat — background gradient material
│   │
│   ├── 🎬 Scenes/
│   │   └── MainScene.unity — main demo scene
│   │
│   ├── 💻 Scripts/
│   │   ├── CuteGirlController.cs — character animation logic
│   │   ├── CuteGirlUIController.cs — manages UI → animation interaction
│   │   ├── OrbitCameraController.cs — rotate / zoom camera
│   │   ├── PauseMenuController.cs — pause system (for dev test)
│   │   ├── SceneFadeIn.cs, SceneFadeInTitle.cs — smooth scene transitions
│   │   ├── ButtonFartSound.cs — trigger sound from UI event
│   │   └── UIClickSound.cs — unified button sound manager
│   │
│   ├── 🔠 TextMesh Pro/
│   │   ├── Fonts & Materials — TMP internal resources
│   │   ├── Sprites — emoji font atlas
│   │   └── TMP Settings — project-wide TMP config
│   │
│   ├── ⚙️ Settings/
│   │   └── InputSystem_Actions — defines Unity Input Action mappings
│   │
│   ├── 📘 TutorialInfo/ — default Unity tutorial folder
│   ├── 🎛️ CuteGirlControls/ — input actions for gameplay keys (2–5)
│   └── 📄 Readme — project-level documentation file
│
├── Build/ — WebGL build output
├── TemplateData/ — Unity WebGL template files
├── index.html — entry point for WebGL build
└── README.md — documentation with controls & info
```

---

## 💖 Credits
Created by [SUPERpowerGT](https://github.com/SUPERpowerGT)  
Built with Unity • Blender • Mixamo • GitHub Pages  


