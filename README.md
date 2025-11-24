🚀 Python Parallel Text Handling – Compliance Checking System
A high-performance Python system for parallel text processing, rule-based compliance validation, large-file handling, and automated reporting.
Built with a modular architecture including loaders, text breakers, compliance rules, search utilities, storage modules, performance testers, and a full Streamlit dashboard.


🧩 Overview
This project provides a complete parallel text compliance processing pipeline, designed to handle large documents with speed and accuracy.
It uses:
	• Parallel processing
	• Custom rule engine
	• Automated storage + search system
	• Performance benchmarking tools
	• Streamlit UI for interactive analysis
It is ideal for domains like Finance, Healthcare, E-commerce, Technology, Manufacturing, or any industry where compliance text validation is required.


⭐ Key Features
✔ Parallel Text Processing
Efficiently loads and splits massive text into blocks using multiprocessing.
✔ Rule-Based Compliance Checker
Each text chunk is evaluated against customizable rule sets.
✔ Streamlit Dashboard
Upload text, run compliance checks, view insights, download results.
✔ Storage & Search System
Save outputs, improve file structure, and search across stored results.
✔ Performance & Stress Testing
Benchmark modules ensure system stability under heavy load.
✔ Email Report Sending
Send compliance summaries via SMTP.


🏗️ Architecture
                ┌────────────────────────┐
                │      Text Loader       │
                └────────────┬───────────┘
                             ▼
                ┌────────────────────────┐
                │    Text Breaker        │
                └────────────┬───────────┘
                             ▼
                ┌────────────────────────┐
                │ Parallel Break Loader  │
                └────────────┬───────────┘
                             ▼
                ┌────────────────────────┐
                │   Compliance Checker   │
                │   + Rule Engine        │
                └────────────┬───────────┘
                             ▼
         ┌───────────────────────────────┐
         │ Storage / Search / Export     │
         └───────────────────────────────┘
                             ▼
                ┌────────────────────────┐
                │ Streamlit UI + Email   │
                └────────────────────────┘



📁 Folder Structure
PYTHON PROJECT/
│
├── app/
│   ├── checker/
│   │   ├── checker.py
│   │   └── rules.py
│   │
│   ├── perfomance_tests/
│   │   ├── perfomance_test.py
│   │   └── test_big_texts.py
│   │
│   ├── search_export/
│   │   ├── emailer.py
│   │   └── search_save.py
│   │
│   ├── storage/
│   │   ├── storage_improver.py
│   │   └── storage.py
│   │
│   └── text_processing/
│       ├── parallel_break_loader.py
│       ├── text_breaker.py
│       ├── text_loader.py
│       └── utils.py
│
├── data/
│   └── checks.db
│
├── .env
├── .gitignore
├── README.md
├── requirements.txt
├── run.py
└── streamlit_app.py



⚙️ Installation
1. Clone the Repository
git clone https://github.com/your-username/Python-Parallel-Text-Handling.git
cd Python-Parallel-Text-Handling
2. Create Virtual Environment
python -m venv venv
Activate:
Mac/Linux
source venv/bin/activate
Windows
venv\Scripts\activate
3. Install Dependencies
pip install -r requirements.txt


▶️ How to Run
Run Full Pipeline (CLI)
python run.py
Run Streamlit Dashboard
streamlit run streamlit_app.py


🔄 Project Workflow
1. Load Text
text_loader.py loads raw text or files.
2. Break Text
text_breaker.py splits the content into smaller manageable blocks.
3. Parallel Processing
parallel_break_loader.py processes chunks using multiprocessing.
4. Compliance Checking
checker.py applies rules from rules.py to identify violations.
5. Store Results
storage.py saves outputs (JSON / DB).
storage_improver.py improves formatting.
6. Search & Export
search_save.py allows searching within stored results.
emailer.py can send reports.
7. Streamlit Visualization
streamlit_app.py provides a UI for all features.


🧠 Rule Engine
Rules are defined in rules.py as simple Python dictionaries:
{
    "id": "R1",
    "description": "Detect prohibited keywords",
    "keywords": ["fraud", "illegal"],
    "severity": "high"
}
The engine loops through each rule and flags violations with context.


📊 Performance Tools
Performance Benchmark
python app/perfomance_tests/perfomance_test.py
Large Text Stress Test
python app/perfomance_tests/test_big_texts.py


🔮 Future Enhancements
	• AI-generated compliance rules
	• FastAPI/Flask API integration
	• Cloud storage support (AWS S3, Azure)
	• Database integration (PostgreSQL, MongoDB)
	• Real-time compliance alerts
	• Role-based dashboard & access levels


🛠 Tech Stack
	• Python 3.x
	• Streamlit
	• Multiprocessing
	• SQLite
	• SMTP Email
	• Custom Rule Engine Architecture


📄 License
This project is licensed under the MIT License.
![Uploading image.png…]()
