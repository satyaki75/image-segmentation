# Image Segmentation Algorithms

This repository provides pure Python + NumPy implementations of various image segmentation algorithms, including thresholding, edge detection, clustering, region-based methods, graph-based methods, and deep learning–inspired pipelines.

---

## Getting Started

### 1. Clone the Repository

```bash
git clone <your-repo-url>
cd <your-repo-folder>
```

---

### 2. Create and Activate a Virtual Environment

Use **venv** to create an isolated environment.

```bash
python -m venv venv
```

#### Activate the environment

**Windows**
```bash
venv\Scripts\activate
```

**Mac/Linux**
```bash
source venv/bin/activate
```

---

### 3. Register the Virtual Environment as a Jupyter Kernel

```bash
pip install ipykernel
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```

Then select **Python (venv)** inside Jupyter Notebook.

---

### 4. Install Requirements

All dependencies are listed in `requirements.txt`.

```bash
pip install -r requirements.txt
```

---

## How the Project Works

- The image is loaded and converted to grayscale **only once** at the top of the notebook/script.
- That grayscale image is stored as a **NumPy matrix**.
- Every segmentation algorithm function takes this matrix as input.
- Each function returns a processed output that can be displayed using `matplotlib`.

You **DO NOT reload the image** for every algorithm.  
Just call different algorithm functions on the same `img` variable.

---

## Example Usage

```python
# Load image once
img = load_grayscale_image("path_to_image.jpg")

# Run any segmentation algorithm
segmented = your_algorithm_function(img)

# Display result
show_image(segmented, "Segmentation Result")
```

Replace `your_algorithm_function` with any algorithm provided in the repository.

---

## Notes

- Implementations are written from scratch for learning purposes
- No OpenCV / TensorFlow / PyTorch used
- Focus is on understanding algorithms mathematically
