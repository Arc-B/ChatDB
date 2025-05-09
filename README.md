# ChatDB - Natural Language Interface for SQL & NoSQL

A Streamlit-based web app that uses Gemini models to allow natural language querying over structured data in MySQL and MongoDB.

## 🚀 Features

- Query multiple datasets using natural language
- Supports both SQL (MySQL) and NoSQL (MongoDB)
- Google Gemini 1.5 Pro (or newer) LLM integration
- Upload CSV/JSON files dynamically
- Clean, interactive UI via Streamlit

## 🗂️ Project Structure
ChatDB/
├── chatDB_pt1.py                # Main Streamlit app
├── requirements.txt             # Python dependencies

├── MongoDB databases/
│   ├── clinic/
│   │   ├── doctors.json
│   │   └── visits.json
│   ├── ecommerce/
│   └── university/

├── SQL Databases/
│   ├── ecommerce/
│   │   ├── customers.csv
│   │   ├── orders.csv
│   │   └── products.csv
│   ├── educationdb/
│   └── healthdb/

├── venv/                        # Python virtual environment (excluded from Git)



