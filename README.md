# 🖼️ Image Processing Utility Tool

> A batch image processing pipeline built with Python — applies grayscale conversion, resizing, brightness adjustment, blur filtering, and edge detection across multiple images with pixel intensity visualisation.

**Author:** Shreya Mishra | BIT Mesra, Jaipur
**Period:** Oct 2024 – Dec 2024

---

## ✨ Features

- **Grayscale conversion** — converts RGB images to single-channel grayscale
- **Resizing** — standardises all images to 256×256 using LANCZOS resampling
- **Brightness adjustment** — configurable enhancement factor (default 1.3×)
- **Gaussian blur** — smoothing filter with configurable radius
- **Edge detection** — highlights structural boundaries using PIL's FIND_EDGES filter
- **Pixel intensity histograms** — visualises tonal distribution per image
- **Batch processing** — processes all `.png` and `.jpg` files in a folder automatically
- **Per-image stats** — reports mean, std, min, max pixel values for each image

---

## 📂 Project Structure

```
image-processing-tool/
│
├── image_processing_tool.ipynb   # Main notebook
├── sample_images/                # Input images (auto-generated if empty)
├── processed_images/             # Output folder (created on run)
├── image_processing_demo.png     # Pipeline visualisation (first image)
├── batch_histograms.png          # Pixel histograms for all images
└── README.md
```

---

## 🚀 Getting Started

**Clone the repo:**
```bash
git clone https://github.com/your-username/image-processing-tool.git
cd image-processing-tool
```

**Install dependencies:**
```bash
pip install pillow numpy matplotlib
```

**Run the notebook:**
```bash
jupyter notebook image_processing_tool.ipynb
```

> 💡 No images? No problem. The notebook auto-generates 5 coloured demo images in `sample_images/` so you can run the full pipeline instantly.

---

## 🖼️ Pipeline Overview

| Step | Operation | Output File Suffix |
|---|---|---|
| 1 | Resize to 256×256 | *(base for all steps)* |
| 2 | Grayscale conversion | `_gray.png` |
| 3 | Brightness enhancement | `_bright.png` |
| 4 | Gaussian blur | `_blur.png` |
| 5 | Edge detection | `_edges.png` |

---

## ⚙️ Configuration

Edit these variables at the top of the notebook to customise behaviour:

```python
INPUT_DIR  = 'sample_images'   # Folder with source images
OUTPUT_DIR = 'processed_images' # Folder for processed outputs
RESIZE_TO  = (256, 256)         # Target resolution
BRIGHTNESS = 1.3                # Brightness multiplier (1.0 = no change)
```

---

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| Pillow (PIL) | Image loading, transformations, filters |
| NumPy | Pixel array operations and statistics |
| Matplotlib | Histogram and pipeline visualisation |

**Environment:** Python 3.10 · Jupyter Notebook / Google Colab

---

## 👩‍💻 Author

**Shreya Mishra** — BIT Mesra, Jaipur

---

## 📄 License

For academic and portfolio purposes.
