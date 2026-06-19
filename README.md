# Python Document Scanner
> Last automated login update: 2026-06-20 00:15:49

A simple OpenCV-based document scanner that detects the largest document-like contour in an image and crops it from the background.

## What it does

This project loads a source image, converts it to grayscale, applies blur and edge detection, finds contours, and tries to identify the document boundary. If a suitable contour is found, the script crops the detected region and displays the result.

## Features

- Image loading with OpenCV
- Grayscale conversion and Gaussian blur preprocessing
- Canny edge detection
- Contour detection and sorting by area
- Document region cropping
- Error handling when the image path is invalid

## Requirements

- Python 3.x
- OpenCV
- NumPy

Install dependencies with:

```bash
pip install opencv-python numpy
```

## How to use

1. Open `Scanner.py`
2. Update the image path in the script to point to your own image
3. Run the script

```bash
python Scanner.py
```

## How it works

The script follows these steps:

1. Load the input image
2. Resize the image for consistent processing
3. Convert to grayscale
4. Apply Gaussian blur
5. Detect edges with Canny
6. Find contours
7. Select the largest contour
8. If the contour looks document-like, crop and display it

## Notes

- The current script uses a hardcoded local file path, so you must replace it with a valid path on your machine.
- The detection logic is basic and works best when the document has clear edges and good contrast.
- For better scanning quality, perspective correction and adaptive thresholding can be added later.

## Possible Improvements

- Perspective transform for true scan-style output
- Automatic rotation correction
- Better contour filtering
- Save scanned output to file
- Support for webcam or live camera input

## License

No license has been specified for this project.