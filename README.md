# 📸 StreetView To Camera Add-on for Blender v4.0

![StreetView To Camera Preview](image_0.png)

> **Authors:** Gemini (AI), [Your Name/Nickname optional]
> **Version:** 1.7 (Stable)
> **Compatibility:** Blender v4.0+

**StreetView To Camera** is a powerful Blender add-on designed specifically for architects, visualizers, and 3D artists working with geospatial data. It allows you to instantly create a Blender camera that perfectly matches the perspective, position, and Field of View (FOV) of a real-world Google Street View panorama.

The standout feature is **Automatic FOV Calculation**. Google Maps provides the vertical FOV of the panorama. This add-on automatically calculates the correct *horizontal* FOV based on the aspect ratio of your screenshot. This ensures a perfect match between your 3D geometry (e.g., imported via Blosm) and the background image.

---

## ⚡️ Key Features

1.  **Direct Perspective Import:** Creates a camera with precise coordinates (Lat/Lon/Z), Heading (yaw), and Pitch derived directly from the Google URL.
2.  **Smart FOV:** Automatically recalculates Google's vertical FOV (`75y`) into Blender's horizontal FOV, adapting to your screenshot's resolution (e.g., `1866x1076` resolution results in a precise `111°` FOV).
3.  **Auto Background Setup:** Instantly loads your screenshot as the camera's **Background Image**, sets alpha to 0.5, and matches Blender's render resolution to the screenshot's dimensions.
4.  **Blosm Integration:** Allows you to paste BBox (Bounding Box) coordinates directly from the Blosm add-on for accurate camera positioning relative to your 3D world origin.

---

## 🚀 Installation

### Step 1: Download
Download the `streetview_to_camera.py` file from this repository.

### Step 2: Install in Blender
1.  In Blender, go to `Edit` > `Preferences` > `Add-ons`.
2.  Click the **Install...** button in the top right corner.
3.  Select the downloaded `streetview_to_camera.py` file.
4.  Enable the checkbox next to **"Add Mesh: StreetView To Camera"**.

---

## 🛠 Workflow (How to Use)

This add-on works best when paired with the **Blosm for Blender** add-on (for importing 3D buildings) and a dedicated, persistent screenshot file.

### 1. Setup Screenshot Folder (Once)
To speed up your workflow, configure your screenshot software (ShareX, Lightshot, standard Snipping Tool, etc.) so that when you press a hotkey, the screenshot is automatically saved to a specific folder with a consistent name, for example: `C:\Screenshots\maps_sync.png`. The old file must be overwritten.

### 2. In Blender (Preparation)
1.Download and install addon:  [Google_Camera_Import.zip](https://github.com/user-attachments/files/27537517/Google_Camera_Import.zip)
2.  Use **Blosm** to import 3D buildings and terrain for your target location.
3.  Copy the BBox coordinates from the Blosm panel.

### 3. Setup StreetView Add-on
1.  Open the **StreetView** tab in the N-panel (Sidebar on the right).
2.  Click **"Paste from Blosm"** to paste the bounding box coordinates.
3.  In the **"Image Path"** field, select your persistent screenshot file `C:\Screenshots\maps_sync.png`.

### 4. Synchronization
1.  **In Browser:** Open Google Street View and find your desired perspective.
2.  **Screenshot:** Press your screenshot hotkey (the `maps_sync.png` file updates on disk).
3.  **URL:** Copy the URL from the browser's address bar.
4.  **In Blender:** Paste the link into the add-on's **"Google URL"** field and click **"Створити камеру"** (Create Camera).

*The add-on will instantly create the camera at the precise coordinates, tilt it, and load the updated screenshot as the background. Your 3D buildings will align perfectly with the photo.*

---

## 🧩 Technical Details (FOV Math)

Google provides data in the format `@lat,lon,x,fy,h,t`. The key parameter is `fy` — the Vertical Field of View.

Blender uses horizontal FOV by default. For an accurate match, we calculate the horizontal FOV using the screenshot's resolution (Width x Height) and the vertical FOV from Google:

$$FOV_{hor} = 2 \times \arctan\left(\tan\left(\frac{FOV_{ver}}{2}\right) \times \frac{Width}{Height}\right)$$

The v1.7 add-on automates this calculation, pulling Width and Height directly from the screenshot file.

---

## 🤝 Feedback and Contribution

This is the stable version of the add-on (v1.7). If you find a bug or have ideas for improvement, please create an **Issue** or submit a **Pull Request**.

---

## 📜 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
