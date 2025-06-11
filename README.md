# Data-Analytics-Dashboard
# Sales Data Analysis Dashboar

A comprehensive sales analytics dashboard built with Python, Flask, and Waitress, featuring interactive visualizations and Indian Rupee (INR) currency formatting.

## Author
**Vijeta Thakur**
- GitHub: [Vijeta Thakur](https://github.com/vijetathakur)
- Project Created: March 2024

## Features

- **Real-time Data Processing**: Analyzes sales data and generates insights
- **Currency Support**: All financial data displayed in Indian Rupees (₹)
- **Interactive Visualizations**:
  - Daily Sales Trends (Line Chart)
  - Best-Selling Products (Bar Chart)
  - Sales Performance Heatmap
  - Product Revenue Analysis
- **Summary Statistics**:
  - Total Revenue (in ₹)
  - Total Items Sold
  - Best Selling Product
  - Highest Revenue Product
  - Analysis Period
- **Production-Ready**: Uses Waitress WSGI server for production deployment

## Technology Stack

- **Backend**: Python 3.x, Flask
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Frontend**: HTML5, Bootstrap 5, Custom CSS
- **Server**: Waitress WSGI Server

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd <project-directory>
```

2. Create and activate a virtual environment (recommended):
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python -m venv venv
source venv/bin/activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Usage

1. Start the application:
```bash
python app.py
```

2. The application will automatically find an available port and display the URL in the console. By default, it tries ports in this order:
   - First attempt: Ports 5000-5010
   - If permission error occurs: Ports 8000-8010

3. Open your web browser and navigate to the URL shown in the console (typically something like):
```
http://127.0.0.1:5000
```

### Troubleshooting Port Issues

If you encounter port-related errors:

1. **Permission Error**: 
   - The application will automatically try alternative ports
   - Check the console output for the actual port being used

2. **All Ports Busy**:
   - Close other applications that might be using the ports
   - You can modify the port range in `app.py` by changing the `find_available_port()` parameters

3. **Manual Port Configuration**:
   - Open `app.py`
   - Modify the `PORT` constant to your preferred port number

## Data Format

The application expects a CSV file (`sales_data.csv`) with the following columns:
- Date: Transaction date (YYYY-MM-DD)
- Product: Product name
- Category: Product category
- Price: Unit price (will be converted to INR)
- Quantity_Sold: Number of units sold
- Total_Revenue: Total revenue (will be converted to INR)

## Project Structure

```
├── app.py                 # Main application file
├── requirements.txt       # Project dependencies
├── sales_data.csv        # Sample sales data
├── static/
│   ├── css/
│   │   └── style.css     # Custom styling
│   └── images/           # Generated visualizations
└── templates/
    └── dashboard.html    # Dashboard template
```

## Features in Detail

### 1. Data Processing
- Automatic currency conversion (USD to INR)
- Date parsing and formatting
- Aggregation and statistical analysis

### 2. Visualizations
- **Daily Sales Trends**: Track revenue patterns over time
- **Product Performance**: Compare product sales quantities
- **Revenue Analysis**: Analyze revenue distribution by product
- **Sales Heatmap**: Visualize sales patterns across weekdays and products

### 3. Currency Formatting
- Supports Indian currency format (₹)
- Automatic conversion to Lakhs and Crores for large numbers
- Properly formatted currency displays in all visualizations

### 4. Production Features
- Production-grade WSGI server (Waitress)
- Multi-threading support
- Error handling and logging

## Customization

### Currency Conversion
The default USD to INR conversion rate is set to 83. To modify this:
1. Open `app.py`
2. Update the `USD_TO_INR` constant

### Visualization Styling
- Modify `static/css/style.css` for dashboard appearance
- Adjust plot parameters in `generate_plots()` function

## Security Notes

- The application uses Waitress as a production server
- Default configuration includes:
  - 4 worker threads
  - Local host binding (127.0.0.1)
  - Port 8080

## Contributing

Feel free to:
- Report issues
- Submit pull requests
- Suggest new features
- Improve documentation

## License

This project is open-source and available under the MIT License.

## Copyright

Copyright © 2024 Vijeta Thakur. All rights reserved.

This project was developed by Vijeta Thakur. The code and documentation in this project are protected by copyright law. While the project is open-source under the MIT License, proper attribution is required when using or redistributing this code. 
