## Data Visualization Pipeline for Experimental Time-Series in Python (Matplotlib)

This project implements a command-line Python tool for visualizing time-series experimental data using Matplotlib. It supports plotting single and multiple datasets, handling replicates, and displaying statistical summaries such as mean and standard deviation.

---

## Project Overview

The goal of this project is to read experimental data from text files and generate publication-quality plots that show changes in cell counts over time under different conditions.

Each input file contains:

- A header specifying the experimental condition  
- Time-series data (x, y values or multiple replicates)  

The pipeline progressively builds functionality from simple plotting to advanced visualization with error bars.

---

## Key Features

### Single Dataset Plotting

- Reads input file with time and measurements  
- Generates line plots using Matplotlib defaults  
- Saves output as PNG  

---

### Axis Labels and Legend

- Adds:
  - X-axis label (time)  
  - Y-axis label (cell count)  
- Includes legend using dataset name  
- Uses automatic legend placement (`loc='best'`)  

---

### Multi-Dataset Plotting

- Supports plotting multiple input files  
- Each dataset plotted as a separate line  
- Enables comparison across experimental conditions  

---

### Flexible Input Handling

- Accepts an arbitrary number of input files  
- Uses command-line arguments (`sys.argv`)  

---

### Replicate Handling and Statistics

- Supports multiple replicate measurements per time point  
- Computes:
  - Mean for each time point  
  - Standard deviation  

- Plots:
  - Mean values as line plot  
  - Error bars representing variability  

---

## Input Format

### Single Measurement per Timepoint

No drug
0,72
20,71
40,77


### Multiple Replicates per Timepoint

No drug
0,72,39,16,62
20,71,45,17,67
40,77,51,21,77


## Technologies Used

- Python  
- Matplotlib  
- NumPy  
- sys (command-line arguments)  

---

## Implementation Details

- Uses `matplotlib.use('Agg')` to enable headless plotting  
- Parses input files using file I/O and string manipulation  
- Computes statistics using NumPy  
- Generates consistent plots using default Matplotlib settings  

---

## Output

- PNG image files showing:
  - Time vs cell count  
  - Multiple experimental conditions  
  - Mean trends with standard deviation error bars  

---

## Key Skills Demonstrated

- Data visualization in Python  
- Command-line interface (CLI) design  
- File parsing and data processing  
- Statistical analysis (mean, standard deviation)  
- Handling multiple datasets dynamically  
- Reproducible plotting workflows  

---

## Notes

- Plots are designed to match reference outputs exactly  
- Minor visual differences may occur depending on environment  
- Error bars represent variability across replicates  

---

## Author

Lakshita Arunkumar
