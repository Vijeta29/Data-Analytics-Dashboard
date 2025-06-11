# Data Science Analytics Dashboard

An interactive web-based dashboard for analyzing CSV and Excel files. Upload your data and instantly get insights through summaries, statistics, and visualizations.

## Features

- 📊 **Interactive Data Analysis**
  - Upload CSV/Excel files with drag & drop
  - Instant file upload confirmation
  - Detailed data summaries
  - Column-wise statistics

- 📈 **Visualization Options**
  - Histogram (for distribution analysis)
  - Box Plot (for outlier detection)
  - Bar Chart (for categorical data)
  - Scatter Plot (for trend analysis)
  - Line Plot (for time series)
  - Violin Plot (for distribution comparison)

## Quick Start

### Method 1: Using start.bat (Recommended)

1. Open Command Prompt or PowerShell
2. Navigate to the project directory:
   ```
   cd "C:\Users\Vijeta thakur\OneDrive\Desktop\DS - Project"
   ```
3. Run the start script:
   ```
   .\start.bat
   ```
4. Your default web browser will open automatically to http://localhost:8051

### Method 2: Manual Setup

1. Create and activate virtual environment:
   ```
   python -m venv venv
   .\venv\Scripts\activate
   ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

3. Run the dashboard:
   ```
   python data_science_dashboard.py
   ```

4. Open your browser and go to http://localhost:8051

## How to Use

1. **Upload Data**
   - Click the upload area or drag & drop your CSV/Excel file
   - You'll see a confirmation message with the file name
   - Data summary will appear automatically

2. **View Data Summary**
   - Number of rows and columns
   - Data types for each column
   - Select a column to view detailed statistics

3. **Create Visualizations**
   - Choose a column to analyze
   - Select your preferred visualization type
   - The plot will update automatically

## Requirements

- Python 3.8 or higher
- Required packages (automatically installed):
  - dash==2.9.3
  - plotly==5.14.1
  - pandas==2.0.0
  - numpy==1.24.3
  - And more in requirements.txt

## Project Structure

```
DS - Project/
├── data_science_dashboard.py  # Main dashboard application
├── requirements.txt          # Python dependencies
├── start.bat                # Quick start script
└── src/
    └── dashboard/
        └── ecommerce_dashboard.py  # Separate e-commerce analytics
```

## Troubleshooting

- If the dashboard doesn't start, check if:
  - Python is installed and in your PATH
  - Port 8051 is available
  - All requirements are installed correctly

- If file upload fails:
  - Check if the file is a valid CSV or Excel format
  - Ensure the file isn't corrupted or empty

## Support

For any issues or questions, please check:
1. The error messages in the command prompt
2. Your Python version and installed packages
3. If the port 8051 is not being used by another application

Created by: Vijeta Thakur
