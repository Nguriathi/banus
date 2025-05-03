📦 Product Invoice Analyzer
(https://chandler.streamlit.app/)

🚀 Features
Single & Batch File Processing: Analyze one or many invoice Excel files at once.

Vessel & Agent Extraction: Automatically display vessel and agent information from your invoice.

Interactive Data Editing: Edit product tables directly in the browser.

Adaptive Visualizations:

Bar charts, treemaps, and line charts for product quantities and trends

Outlier detection (scatter plot)

Recurring item detection

Forecasting: Predict future product quantities with Prophet.

Bullet Point Summaries: Each analysis is summarized in clear bullet points.

Template Export: Download your edited data in a pre-defined Excel template.

Modern UI: Splash screen, sidebar animation, and a gradient-matching navbar.

🌐 Live Demo
https://chandler.streamlit.app/
Try the app instantly in your browser-no installation needed!

🏗️ How It Works
Start the App:
Launch with Streamlit and enjoy a modern splash screen.

Choose Processing Mode:

Single File: For individual invoices (shows vessel/agent, uses template export)

Batch: For multiple invoices (trend analysis, forecasting, batch summary)

Upload Invoice File(s):
Accepts .xlsx files with an analysis sheet in the expected format.

Analyze & Edit:

View adaptive visualizations and bullet-point summaries

Edit product tables as needed

Export:

Single: Download a filled-in Excel template with all invoice data.

Batch: Download a combined Excel summary.

🛠️ Setup & Usage
Clone the repo:

bash
git clone https://github.com/your-username/invoice-analyzer.git
cd invoice-analyzer
Install dependencies:

bash
pip install -r requirements.txt
Or manually:

bash
pip install streamlit streamlit-lottie pandas plotly openpyxl prophet
Add your files:

Place your template.xlsx and assets/animation.json in the project root.

Run the app:

bash
streamlit run app.py
Upload your invoice(s) and enjoy!

📝 Invoice Format Example
Your Excel file should have an analysis sheet with this structure:

AGENT	...	...
VESSEL	...	...
DOD	...	...
...	...	...
NO	PRODUCT DESCRIPTION	UNIT/PRC
1	Cabbage White	1.2
...	...	...
📊 Example Bullet Summary
This invoice contains 32 unique products.

Total quantity: 320.

Total value: $1,420.80.

Top product: Cabbage White.

Most significant product by quantity: Cabbage White.


🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

📄 License
MIT

🙏 Acknowledgements
Streamlit

Plotly

Prophet

eazyBI Data Visualization Blog

LottieFiles

Built for invoice analytics and business intelligence.
