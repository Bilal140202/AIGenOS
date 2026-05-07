<div align="center">
  <h2>AIGenOS: Master Build Blueprint</h2>
</div>

> [!NOTE]
> This document is designed for an AI Coding Assistant to automatically build the AIGenOS platform from scratch using the NYOK model and Pollinations endpoint.

## 1. Architectural Vision
AIGenOS acts as a virtual desktop environment for AI agents. It should look and feel like an operating system interface running inside the browser, featuring draggable windows, a taskbar, and a unified file system for generated assets.

## 2. Technical Stack
*   **Core:** Next.js (App Router), TypeScript, React 18+.
*   **Aesthetics:** Tailwind CSS with a "Neon Cyber" theme. Heavy use of \ackdrop-blur\ for glassmorphism.
*   **Window Management:** \eact-rnd\ or \ramer-motion\ for draggable/resizable OS windows.
*   **State:** Zustand (global OS state: open windows, active agent, memory).
*   **AI Integration:**
    *   **NYOK Core API:** For system-level logic and agent reasoning.
    *   **Pollinations Endpoint:** For generating UI assets and abstract visuals for the OS wallpaper.

---

## 3. Step-by-Step AI Prompt Instructions

### Step 1: Base Operating System Shell
**Prompt to AI:** *"Initialize a Next.js App Router project with Tailwind CSS. Create a main \DesktopLayout\ component. The background should fetch a dynamic, abstract wallpaper from the Pollinations image endpoint based on the seed 'cyberpunk OS'. Implement a bottom Taskbar component with a start menu."*

### Step 2: Window Management System
**Prompt to AI:** *"Implement a global Zustand store to track an array of \openWindows\. Create a reusable \WindowFrame\ component using framer-motion that allows the user to drag and resize windows. The styling must use premium glassmorphism (translucent dark background with a slight white border)."*

### Step 3: NYOK Terminal App
**Prompt to AI:** *"Create a 'Terminal' app within the OS. This app will communicate with the NYOK model API. Create a Next.js API route \/api/nyok-os\ that pre-inserts a system limit message: 'You are the root kernel of AIGenOS. Respond in concise shell-like outputs.' Stream the NYOK response back to the Terminal window."*

### Step 4: Asset Manager App
**Prompt to AI:** *"Create a 'Files' app window that displays images and text generated during the session. Connect it to the Pollinations endpoint so users can type a query and immediately save the generated image to their virtual OS file system."*

---

## 4. Edge Cases & Constraints
*   **Memory Management:** The browser can lag if too many glassmorphic windows are open. Implement virtualization or disable blur effects when windows are dragging.
*   **API Timeouts:** Handle NYOK API timeouts gracefully by showing a 'Kernel Panic' stylized error message inside the terminal window rather than breaking the whole UI.
