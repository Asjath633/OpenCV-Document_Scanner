# Document Scanner

### An interactive document scanner built in Python using OpenCV

The scanner takes a poorly scanned image, finds the corners of the document, applies the perspective transformation to get a top-down view of the document, sharpens the image, and applies an adaptive color threshold to clean up the image.

On my test dataset of 280 images, the program correctly detected the corners of the document 92.8% of the time.
### Installation & Setup

1. **Create and Activate Virtual Environment:**
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

2. **Install Dependencies:**
   ```powershell
   pip install -r requirements.txt
   ```

### Usage

You can run the scanner using the virtual environment's python.

**Scan a single image:**
```powershell
python scan.py --image path/to/image.jpg
```

**Scan a single image with interactive mode (drag corners):**
```powershell
python scan.py --image path/to/image.jpg -i
```

**Scan an entire directory of images:**
```powershell
python scan.py --images path/to/image_directory
```

*Note: Scanned images will be saved in the `output/` directory.*
