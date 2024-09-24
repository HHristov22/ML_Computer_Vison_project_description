# ML_Computer_Vison_project_description

# Project: Text and Color Recognition from eBike Display (BOSCH electric bike)

## Project Description:
Monitoring the display via a camera and recognizing its content - specific corporate text (OCR, fine-tuned with a specific font), text color, exact background color, and color of certain elements on the display.

## Challenges and Solutions:

### 1. Accurate Color Recognition:
- **Problem Definition:** Built-in color recognition libraries search for similar colors within a cubic neighborhood centered around the original color. This leads to inaccuracies when recognizing similar colors.
- **Solution Applied:** Replacing the cubic neighborhood with a spherical one. This improves color recognition accuracy by up to 48%, allowing for more precise differentiation of similar colors (example: cyan & turquoise – bike mode).

### 2. Light Noise:
- **Problem Definition:** The difficulty of eliminating light noise through physical isolation (e.g., placing the camera and display in a cabinet) requires a software solution.
- **Solution Applied:** Calibration of background noise using a reference point – the animation during the display’s startup (welcome pattern), as well as the current time of day. The algorithm determines the amount of light noise, using pre-input data for more accurate calibration.

## Technologies and Libraries Used:
- **ML:** Algorithms for predicting and compensating for light noise and algorithms for color classification.
- **Standard Libraries:** OpenCV, NumPy, Tesseract OCR, and others.

## Final Results:
- **Recognition Accuracy:** Achieved approximately 95% accuracy in recognizing text, text color, exact background color, and the color of certain elements on the display.
- **Distinguishing Similar Colors:** Successfully differentiated very similar colors (example: cyan & turquoise).
