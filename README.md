# Document Scanner

### An interactive document scanner built in Python using OpenCV

The scanner takes a poorly scanned image, finds the corners of the document, applies the perspective transformation to get a top-down view of the document, sharpens the image, and applies an adaptive color threshold to clean up the image.

On my test dataset of 280 images, the program correctly detected the corners of the document 92.8% of the time.

This project makes use of the transform and imutils modules from pyimagesearch (which can be accessed [here](http://www.pyimagesearch.com/2014/09/01/build-kick-ass-mobile-document-scanner-just-5-minutes/)). The UI code for the interactive mode is adapted from `poly_editor.py` from [here](https://matplotlib.org/examples/event_handling/poly_editor.html).

* You can manually click and drag the corners of the document to be perspective transformed:
![Example of interactive GUI](https://github.com/andrewdcampbell/doc_scanner/blob/master/ui.gif)

* The scanner can also process an entire directory of images automatically and save the output in an output directory:
![Image Directory of images to be processed](https://github.com/andrewdcampbell/doc_scanner/blob/master/before_after.gif)

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
