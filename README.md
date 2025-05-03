# 📦 Product Invoice Analyzer
[![Open in Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svgrn Streamlit app for visualizing, editing, and forecasting invoice product data.
Upload your Excel invoice(s) and get instant analytics, summaries, and export-ready files!

===

## 🌟 Features

- ✅ **Interactive Data Editing**
- ✅ **Adaptive Visualizations (bar, treemap, line charts)**
- ✅ **Batch & Single File Processing**
- ✅ **Automatic Vessel & Agent Extraction**
- ✅ **Forecasting with Prophet**
- ✅ **Bullet Point Summaries**
- ✅ **Export to Excel Template**
- ✅ **Modern UI with Splash Screen and Lottie Animation**

---

## 🚀 Getting Started

###Prerequisites

Python 3.8 or higher

## Installation

1. **Clone the repository**
    ```
    git clone https://github.com/your-username/invoice-analyzer.git
    
    cd invoice-analyzer
    ```

2. **Install dependencies**
    ```
    pip install -r requirements.txt
    ```
    ```
    pip install streamlit streamlit-lottie pandas plotly openpyxl prophet
    ```

    ```
    Place your template.xlsx and assets/animation.json in the project root.
    ```

3. **Run the application**
    ```
    streamlit run app.py
    ```

    
## 📂 File Structure


invoice-analyzer/
├── app.py               # Main Streamlit application
├── requirements.txt     # Dependency list
├── README.md            # This file
├── assets/
│   └── animation.json   # Lottie animation for sidebar
├── template.xlsx        # Excel template for export
└── Data.xlsx            # Example invoice data


---

## 🧮 Core Functionality

Extracts product tables from your invoice Excel file (analysis sheet).

Displays vessel and agent (if present) above the table in single file mode.

Interactive editing of product data.

Visualizes:

Product quantities (bar/treemap)

Trends and recurring items (line/bar)

Price and quantity outliers (scatter)

Forecasts future quantities using Facebook Prophet.

Exports:

Edited data as Excel

Single file mode: fills your template.xlsx with all info

    
## 📊 Supported Data Formats

Format	Features
Excel	Full support (analysis sheet as shown below)
CSV	Not supported (convert to Excel first)
JSON	Not supported

## 📝 Invoice Format Example
Your Excel file should have an analysis sheet like:

AGENT	...	...
VESSEL	...	...
DOD	...	...
...	...	...
NO	PRODUCT DESCRIPTION	UNIT/PRC
1	Cabbage White	1.2
...	...	...

---

##💡 Usage Tips

1. **Data Requirements**
    - Must contain `Number`, `Product Description`, `Unit/Prc`, `Unit`, `Qty`, and `Total USD`       columns
    - Date format: `YYYY-MM-DD`
    - Numeric columns should be clean    
    - AGENT and VESSEL fields are auto-extracted if present
    

3. **Performance**
    - Optimal dataset size: <100,000 rows
    - For large datasets, enable caching with `@st.cache`
      
---

## 🧪 Testing
Test your data extraction and forecasting logic with:

python
python -m pytest tests/

---

## 🤝 Contributing

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

📜 License
Distributed under the MIT License.

## 📞 Contact

**Project Maintainer:** Nguriathi
Live App: https://chandler.streamlit.app/

## 🏆 Deployment Options

### 1. Streamlit Community Cloud

[![Deploy to Streamlit](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://streamlit.io/cloud)

### 2. Linux Server

sudo apt install python3-pip
pip install -r requirements.txt
streamlit run app.py --server.port 80



### 3. Docker

FROM python:3.9-slim
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
EXPOSE 8501
CMD ["streamlit", "run", "app.py"]

Built with ❤️ using Streamlit for actionable invoice analytics and business intelligence.
