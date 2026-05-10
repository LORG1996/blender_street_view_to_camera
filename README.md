# 📸 StreetView To Camera for Blender v4.0

<img width="700" height="350" alt="Gemini_Generated_Image_9mh2bf9mh2bf9mh2" src="https://github.com/user-attachments/assets/5d74db68-ce82-4b31-87fc-8e92e62f8bcd" />

Instantly create a Blender camera matching the position, rotation, and Field of View (FOV) of any Google Street View panorama. **Includes automatic vertical-to-horizontal FOV correction based on your screenshot's aspect ratio.**

---

## 📺 Video Tutorial
[![Video Tutorial](https://img.youtube.com/vi/FqP5FiTVVic/0.jpg)](https://www.youtube.com/watch?v=FqP5FiTVVic)

## ⚠️ MANDATORY REQUIREMENT

To ensure the camera aligns correctly with real-world coordinates:
*   The **[Blosm](https://github.com/vvoovv/blosm)** (formerly BlenderOSM) add-on **must** be installed.
*   When loading the base (terrain or buildings) via **Blosm**, you **must copy the BBox (bounding box) coordinates** from the Blosm interface and paste them into this script's panel. This syncs the coordinate origin of both tools.

---

## 🚀 Installation

1.  **Download** [Google_Camera_Import.zip](https://github.com/user-attachments/files/27538381/Google_Camera_Import.zip).
2.  In Blender, go to `Edit` > `Preferences` > `Add-ons` > **Install...**
3.  Select the file and **enable** the add-on.

---

## 🛠 Quick Start Workflow

Best used with the **Blosm** add-on (for 3D buildings) and a persistent screenshot file.

1.  **Setup (Once):** Configure your screenshot software to auto-save and overwrite a specific file (e.g., `C:\Screenshots\sync.png`).
2.  **Blender:** Import buildings via **Blosm**, **copy the BBox coords**, and paste them into the **StreetView** panel (N-panel).
3.  **Sync:** Find a view in Google Street View, take a screenshot, copy the browser URL, paste it into Blender **StreetView** panel (N-panel)., and click **"Create Camera"**.

---

## 🤝 Contribution & License

Found a bug? Create an **Issue**. Licensed under **MIT**.
