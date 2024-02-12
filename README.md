
![Designer1](https://github.com/farhanaugustine/DeepLabCut-Analysis-Jupyter-Scripts/assets/54376988/2ecdea02-bfc7-4b64-af3c-37f534ec456f)

---
# Analysis of Mouse Movement Data
---

## Overview
### While DLCAnalyzer and DLC Helper functions are great. They fail to accommodate a vast range of behavior investigator's needs. The Jupyter script provided here is meant for post processing/analyzing DeepLabCut (DLC) CSV files. The script allows user to filter data, calculate velocities, draw Region of Interest (ROI), and more.
This document provides a summary of a Python script designed to analyze mouse movement data. The script is structured as a Jupyter Notebook and includes various functionalities such as loading data, defining regions of interest (ROIs), and calculating distances and velocities.

## Package Requirements
The script requires the following Python packages:
- `pandas` for data manipulation and analysis.
- `numpy` for numerical operations.
- `scipy.signal` for signal processing tasks.
- `matplotlib` for plotting graphs.
- `matplotlib.widgets` for interactive graph features.

## Data Loading
The script loads a CSV file containing mouse movement data into a pandas DataFrame. This data is expected to have multiple header rows that define body parts and their corresponding x, y coordinates, and likelihood values.

## Data Preparation
A dictionary called `body_part_data` is created to map body part names to their respective coordinate columns and likelihood values. This allows for easy access to each body part's data throughout the analysis.

## Region of Interest (ROI) Definition
The script includes functionality for the user to define an ROI by drawing a rectangle on a plot of the data. The coordinates of the ROI are stored for further analysis.

## Movement Analysis
The script calculates the distance moved by each body part, taking into account the likelihood of detection to filter out noise. It also calculates velocities using the Savitzky-Golay filter to smooth the data.

## Output
The script outputs the following:
- The total distance moved by each body part within the ROI.
- The average velocity of each body part.
- The total time each body part spent within the ROI.
- Any detected jumps or significant movements between frames that exceed a predefined threshold.

## Conclusion
The script is a comprehensive tool for analyzing mouse movement data, providing insights into the behavior and movement patterns of the subject. It is designed to be adaptable to different datasets and can be modified to suit specific analysis needs.

---

Please ensure that all the necessary data files are correctly located and that the required Python packages are installed before running the script. For detailed instructions on how to use each functionality, refer to the comments and documentation within the script itself. If you encounter any issues or have further questions, please consult the troubleshooting section or reach out for support.
