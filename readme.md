# IF3024 Hands-On

This repository belongs to:

| Nama | NIM |
|--|--|
| Fathan Andi Kartagama | 122140055 |

Repositori ini berisi `Hands-On` untuk mata kuliah `Pengolahan Sinyal Digital (IF3024)`[ITERA](https://www.itera.ac.id/). Tugas ini mencakup pembuatan dan analisis sinyal sinusoidal menggunakan `Python` dalam lingkungan `Jupyter Notebook`. Proyek ini bertujuan untuk memahami konsep dasar sinyal, seperti amplitudo, frekuensi, dan pergeseran fase, serta cara memvisualisasikannya dengan matplotlib.

---

This repository contains `Hands-On` for the course `Digital Signal Processing (IF3024)`[ITERA](https://www.itera.ac.id/). This assignment covers the creation and analysis of sinusoidal signals using `Python` in the `Jupyter Notebook` environment. This project aims to understand the basic concepts of signals, such as amplitude, frequency, and phase shift, and how to visualize them with matplotlib.

---

# Respiratory Rate Analysis

This script analyzes a video to calculate respiration rate (breaths per minute) using MediaPipe facial landmarks and optical flow techniques.

## How it Works

1. **MediaPipe Face Mesh**: Detects facial landmarks in each video frame
2. **Lucas-Kanade Optical Flow**: Tracks movements of key facial landmarks between frames
3. **Signal Processing**: Filters the movement signal and detects respiratory cycles
4. **Comparison**: Compares calculated respiration rate with ground truth data

## Lucas-Kanade Optical Flow

The Lucas-Kanade method is a differential approach for optical flow estimation. It assumes:
- Brightness constancy (pixel intensities don't change between frames)
- Small motion (points don't move far between frames)
- Spatial coherence (neighboring pixels have similar motion)

It's particularly effective for tracking specific features like facial landmarks across frames, making it ideal for respiratory motion tracking.

## Requirements

- Python 3.7+
- OpenCV
- NumPy
- Pandas
- MediaPipe
- Matplotlib
- SciPy

Install dependencies:
```
pip install opencv-python numpy pandas mediapipe matplotlib scipy
```

## Usage

Run the script:
```
python respiratory_analysis.py
```

The script processes the video file located at `hands-on-03/media/122140055.mp4` and compares the results with ground truth data from `hands-on-03/media/stopwatch_data.csv`.

## Output

- Terminal output showing calculated respiration rate and comparison with ground truth
- Visualization of the respiratory signal and detected breath cycles saved as `respiratory_signal_analysis.png`
