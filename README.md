# 🌌 Star-Identifier – Automatic Star Detection & Matching

**Star-Identifier** is an advanced algorithm developed to automatically detect and match stars across astronomical images. Designed specifically for robust star identification, it handles challenges such as noise, rotation, translation, and scaling effectively. The project was created for the *Introduction to Space Engineering* course.


## 🎯 Project Objectives

- Automatically detect and extract star features from astronomical images.
- Develop geometric algorithms for robust star matching.
- Evaluate and validate the algorithm's performance on diverse datasets.

---

## 🛠️ Methodology Overview

### **1. Star Detection (`star_detection.py`)**
- Converts images to grayscale.
- Applies Gaussian blur for noise reduction.
- Detects stars using Laplacian of Gaussian (LoG) blob analysis.
- Extracts detailed star features: coordinates `(x, y)`, radius `(r)`, brightness `(b)`.

### **2. Geometric Matching (`star_matching.py`)**
- Constructs triangles from detected stars.
- Generates scale- and rotation-invariant triangle descriptors using side-length ratios.
- Matches triangles between images based on descriptor similarity.
- Utilizes a voting system for accurate star-to-star correspondences.

---

## 📈 Results & Validation

- Successfully matched ~30 stars per image pair during validation tests.
- Demonstrated resilience to real-world image conditions including noise, rotation, and positional shifts.

---

## 🚀 Getting Started

### Requirements
Ensure you have Python 3 installed with the following dependencies:
```bash
pip install opencv-python numpy scipy matplotlib pandas
```

### How to Run the Project
1. **Star Detection**
```bash
python star_detection.py
```
*Outputs star features into a CSV file.*

2. **Star Matching**
```bash
python star_matching.py
```
*Matches star features from two CSV files and outputs matched star pairs.*

3. **Visualization & Analysis**
Explore detailed experiments and visualizations in:
- `Star_Identifier_Notebook.ipynb`

---

## 📂 Project Structure

```
Star-Identifier/
├── star_detection.py                  # Detect stars and extract features
├── star_matching.py                   # Match stars across images
├── Star_Identifier_Notebook.ipynb     # Notebook with analysis and experiments
├── Star_Identifier_Project_Report.pdf # Comprehensive technical report
├── README.md                          # Project documentation
```

---

## 📚 Resources & References

- [Stellarium](https://stellarium.org/) – Planetarium software used for simulation and validation.
- Geometric star identification and pattern-matching literature.
- [OpenCV Documentation](https://docs.opencv.org/) – Used extensively for image processing.

---

## 📧 Feedback & Contribution

Feel free to contact us or raise an issue for improvements and contributions to the project.
