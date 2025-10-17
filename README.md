
## 🛰️ SAR Image Change Detection using OpenCV and Flask

### 📖 Overview

This project focuses on **Synthetic Aperture Radar (SAR) image change detection**, a critical task in **disaster monitoring**, **urban expansion tracking**, and **environmental analysis**. The system identifies and highlights **changes between two temporal SAR images** of the same geospatial area using **image processing algorithms implemented in OpenCV**. A **Flask-based web interface** allows users to upload “before” and “after” images and visualize detected changes interactively.

---

### 🧠 Research Motivation

SAR imagery offers all-weather, day–night imaging capabilities, making it ideal for monitoring regions prone to **floods, landslides, and glacier melts**. However, manual interpretation of these images is time-consuming and prone to error. This work automates change detection through a **pixel-level difference analysis**, serving as a foundation for integrating **AI-assisted disaster detection systems**.

---

### ⚙️ System Architecture

1. **Frontend (Flask Web App)**

   * Uploads *before* and *after* SAR images.
   * Displays visual output with highlighted change regions.

2. **Backend (OpenCV Core)**

   * Preprocesses both images (resizing, denoising, grayscale conversion).
   * Performs absolute difference calculation.
   * Applies thresholding and contour detection to isolate significant changes.

3. **Result Generation**

   * Outputs a *change mask* visualizing altered areas.
   * Displays results directly on the web interface.

---

### 🧩 Methodology

| Step                           | Description                                                                            |
| ------------------------------ | -------------------------------------------------------------------------------------- |
| **1. Image Preprocessing**     | Resize and normalize SAR image pair for consistent pixel alignment.                    |
| **2. Difference Computation**  | Compute absolute pixel-wise difference between temporal frames using `cv2.absdiff()`.  |
| **3. Thresholding**            | Convert difference map to binary mask using adaptive thresholding.                     |
| **4. Morphological Filtering** | Use OpenCV morphological operations to remove noise and highlight meaningful clusters. |
| **5. Contour Extraction**      | Identify and draw boundaries of changed regions.                                       |
| **6. Visualization**           | Overlay change map on original image and display results via Flask frontend.           |

---

### 🧪 Example Workflow

1. Run the Flask server

   ```bash
   python app.py
   ```
2. Open the browser and navigate to

   ```
   http://127.0.0.1:5000
   ```
3. Upload two SAR images (before and after).
4. The application automatically detects and displays change areas.

---

### 🧰 Tech Stack

* **Language:** Python
* **Libraries:** OpenCV, NumPy, Flask
* **Frontend:** HTML, CSS, Bootstrap (responsive design)
* **Image Type:** Sentinel-1 SAR imagery (VV/VH polarization)

---

### 🔬 Results

The model successfully identifies significant terrain or urban changes between two Sentinel-1 temporal captures. This enables fast assessment of:

* Flood-affected zones
* Landslide-prone areas
* Urban development over time

> Example: Detected water-level rise along river basins post heavy rainfall using SAR data from July and November 2016.

---

### 🚀 Future Work

* Integrate **Ollama-based LLMs** for **automated scene reasoning** and report generation.
* Use **deep learning (CNN-based)** architectures for more precise feature extraction.
* Incorporate **geospatial metadata** (latitude, longitude) for accurate regional mapping.
* Build temporal datasets for continuous monitoring and alert systems.

---

### 📁 Repository Structure

```
SAR-Image-Change-Detection/
│
├── app.py                # Flask web server
├── static/               # CSS, JS, and result storage
├── templates/            # HTML pages for the web interface
├── detect_changes.py     # Core OpenCV change detection logic
├── uploads/              # Uploaded images (before/after)
├── results/              # Processed output images
├── styles.css            # Custom styling
└── README.md             # Project documentation
```

---

### 🧾 Citation

If you use this work in your research or project, please cite:

> **Soham Banerjee**, *SAR Image Change Detection using OpenCV and Flask*, 2025.

---

### 👨‍🚀 Author

**Soham Banerjee**
Researcher in AI, Aerospace & Computer Vision
📧 [banerjee.soham08122001@gmail.com](mailto:banerjee.soham08122001@gmail.com)


