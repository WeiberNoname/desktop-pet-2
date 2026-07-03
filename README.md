<img width="2816" height="1536" alt="Gemini_Generated_Image_vyd9mdvyd9mdvyd9" src="https://github.com/user-attachments/assets/e0aa6987-5062-4ae5-9bf4-75e99754274e" />

<img width="400" height="209" alt="Recording 2026-07-03 124130" src="https://github.com/user-attachments/assets/1c43d6d2-26f2-472c-be61-02df03884592" />

# 3D Transparent Desktop Mascot Pet 🐰

A floating, borderless, fully transparent (RGBA 0,0,0,0) 3D interactive companion pet application for Windows, powered by **Electron** and **Three.js (WebGL)**.

The mascot floats on top of your working windows, bobbing gently. It captures clicks and drags when hovered directly, and passes clicks straight through to the applications underneath when clicking in transparent areas.

---

## 🚀 How to Run the App

### Option A: Standalone Executable (No Setup Required)
Perfect for instant use without running terminal commands.

1. Open **File Explorer** and navigate to:
   [DesktopPet-win32-x64](file:///C:/Users/space/.gemini/antigravity-ide/scratch/desktop-pet/DesktopPet-win32-x64)
2. Double-click **`DesktopPet.exe`** to start your pet mascot.

> [!TIP]
> Right-click `DesktopPet.exe` ➔ *Send to* ➔ *Desktop (create shortcut)* to launch it directly from your desktop.

---

### Option B: Local Node.js Development
Ideal if you want to inspect, debug, or extend the JavaScript source files.

1. Ensure [Node.js](https://nodejs.org) is installed.
2. Open terminal and navigate to the project directory:
   ```bash
   cd C:\Users\space\.gemini\antigravity-ide\scratch\desktop-pet
   ```
3. Start the dev app:
   ```bash
   npm start
   ```
4. Recompile the production executable after modifying code:
   ```bash
   npm run build
   ```

---

## 🕹️ Controls & Interaction Guide

| Mouse Action | Target | Description |
| :--- | :--- | :--- |
| **Hover** | Over character | Cursor changes to a pointer, enabling interaction. |
| **Left Click** | On character | Plays a squash-and-stretch windup, a high jump, and a 360° spin animation. |
| **Left Click + Drag** | On character | Smoothly repositions the mascot anywhere on your monitor(s). |
| **Click** | Outside character | Passed through to the folders, IDE, or browser behind the window. |

---

## 💡 Customize with Your Own 3D Models (Zero-Code Customization)

The app automatically detects, centers, scales, and animates any 3D asset you drop in:

1. Locate the **`assets/`** folder:
   - Development path: [assets/](file:///C:/Users/space/.gemini/antigravity-ide/scratch/desktop-pet/assets)
   - Executable path: [DesktopPet-win32-x64/assets/](file:///C:/Users/space/.gemini/antigravity-ide/scratch/desktop-pet/DesktopPet-win32-x64/assets)
2. Drop any **`.glb`** or **`.gltf`** model file (e.g. your favorite Pokémon) into this directory.
3. Launch the app. The engine will:
   - **Scan** and read your 3D asset.
   - **Auto-normalize** and center the geometry using bounding-box mathematics (ensures any size asset fits the window bounds perfectly).
   - **Auto-play** the first embedded skeletal animation track (e.g., Idle/Walk).
4. **Fallback:** If you empty the `assets/` folder, the application immediately falls back to rendering the default pink bunny mascot.

---

> [!NOTE]
> To modify the source scripts, open the project inside your editor and make changes directly in [renderer.js](file:///C:/Users/space/.gemini/antigravity-ide/scratch/desktop-pet/renderer.js) or [main.js](file:///C:/Users/space/.gemini/antigravity-ide/scratch/desktop-pet/main.js).
>

error message:
npm : File C:\Program Files\nodejs\npm.ps1 cannot be loaded because running scripts is disabled on this system. For
more information, see about_Execution_Policies at https:/go.microsoft.com/fwlink/?LinkID=135170.
At line:1 char:1
+ npm run build
+ ~~~
    + CategoryInfo          : SecurityError: (:) [], PSSecurityException
    + FullyQualifiedErrorId : UnauthorizedAccess

> [!NOTE]
> fix command: Set-ExecutionPolicy -ExecutionPolicy Bypass -Scope Process
