License-Plate-Recognition-in-Challenging-Conditions-using-Custom-EasyOCR
License plate recognition system designed with custom-trained EasyOCR and advanced image processing techniques, optimized for real-world challenging conditions. Developed under supervision of Prof. Dr. Devrim Ünay at Izmir Democracy University

License Plate Recognition in Challenging Conditions using Custom EasyOCR

This repository contains my graduation project from Izmir Democracy University, supervised by Prof. Dr. Devrim Ünay, for the Electrical-Electronics Engineering Department. The project aims to develop a robust, high-accuracy Automatic License Plate Recognition (ALPR) system using deep learning-based Optical Character Recognition (OCR).

## Motivation
Automated license plate recognition is critical for smart city applications including traffic management, security, and access control. However, real-world conditions pose significant challenges such as foggy weather, low-resolution images, angled perspectives, occlusions, and non-standard fonts.

## Project Pipeline

1. **Image Preprocessing**
   - Grayscale conversion
   - White balancing (LAB)
   - Median denoising & mild sharpening
   - Contrast Limited Adaptive Histogram Equalization (CLAHE)

2. **Plate Localization**
   - Edge detection (Canny)
   - Contour analysis & aspect ratio filtering
   - Heuristic alignment filtering

3. **OCR (Custom EasyOCR)**
   - Fine-tuning on a diverse license plate dataset
   - Post-correction based on common OCR errors

4. **Post-processing**
   - String normalization (uppercase, removal of special characters)
   - Similarity scoring using Levenshtein distance
   - Selection of best-matching OCR candidate

5. **Output**
   - Results saved in Excel format
   - Bounding box visualizations stored separately
    <img width="850" height="500" alt="excel" src="https://github.com/user-attachments/assets/c17176f6-b579-47ae-93bf-e1949924c8de" />

## Results
- **Perfect Match:** 26%
- **High Similarity (80-99%):** 42%
- **Moderate Similarity (55-79%):** 12%
- **Low Similarity (<55%):** 20%
<img width="1250" height="1000" alt="Accuracyy_piechart_v2" src="https://github.com/user-attachments/assets/78dd9461-12b6-46f3-bcc4-e5e214eaeb34" />



These results reflect significant improvement due to tailored preprocessing and model fine-tuning.

## Sample Results
-You can find some of them in this section!

<img width="350" height="325" alt="100" src="https://github.com/user-attachments/assets/65929674-d848-4e35-89ac-43bc0d4a374f" />
<img width="350" height="325" alt="100" src="https://github.com/user-attachments/assets/db013d3d-73bc-4741-8e8c-02174974a4fa" />
<img width="350" height="325" alt="100" src="https://github.com/user-attachments/assets/e18aacf2-c136-47b1-ad13-5673f869a67b" />
<img width="350" height="325" alt="100" src="https://github.com/user-attachments/assets/3efab505-4584-45a3-a97b-5ee844469f5b" />
<img width="350" height="325" alt="100" src="https://github.com/user-attachments/assets/2b97d33b-9b5c-4d86-a1de-27e34837370f" />



## Requirements
```bash
pip install -r requirements.txt

-easyocr==1.6.2
-opencv-python==4.8.0.76
-numpy==1.23.5
-pandas==1.5.3
-matplotlib==3.7.1
-python-Levenshtein==0.23.0
-torch
-torchvision
