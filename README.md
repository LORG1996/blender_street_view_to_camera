# 📸 StreetView To Camera for Blender v4.0

<img width="700" height="350" alt="Gemini_Generated_Image_9mh2bf9mh2bf9mh2" src="https://github.com/user-attachments/assets/5d74db68-ce82-4b31-87fc-8e92e62f8bcd" />

Instantly create a Blender camera matching the position, rotation, and Field of View (FOV) of any Google Street View panorama. **Includes automatic vertical-to-horizontal FOV correction based on your screenshot's aspect ratio.**

---

## 🚀 Installation

1.  **Download** [Google_Camera_Import.zip](https://github.com/user-attachments/files/27537517/Google_Camera_Import.zip).
2.  In Blender, go to `Edit` > `Preferences` > `Add-ons` > **Install...**
3.  Select the file and **enable** the add-on.

---

## 🛠 Quick Start Workflow

Best used with **Blosm** https://github.com/vvoovv/blosm add-on (for 3D buildings) and a persistent screenshot file.

1.  **Setup (Once):** Configure your screenshot software to auto-save and overwrite a specific file (e.g., `C:\Screenshots\sync.png`).
2.  **Blender:** Import buildings via **Blosm**, copy the BBox coords, and paste them into the **StreetView** panel (N-panel). Select your `sync.png` as the **Image Path**.
3.  **Sync:** Find a view in Google Street View, take a screenshot, copy the browser URL, paste it into Blender, and click **"Створити камеру"** (Create Camera).

---

## 🤝 Contribution & License

Found a bug? Create an **Issue**. Licensed under **MIT**.
