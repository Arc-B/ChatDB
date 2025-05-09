# 💬 ChatDB

ChatDB is a natural language interface to query both **MongoDB** and **MySQL/CSV** databases using **LLMs** (like Gemini). Upload your data, ask questions in plain English, and get smart query results — all via a Streamlit interface.

---

## 🗂️ Project Structure

```
ChatDB/
├── chatDB_pt1.py              # Main Streamlit app
├── requirements.txt           # Python dependencies

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

```

---

## ⚙️ Setup Instructions

```bash
# 1. Clone this repository
git clone https://github.com/Arc-B/ChatDB.git
cd ChatDB

# 2. Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Run the Streamlit app
streamlit run chatDB_pt1.py
```

---

## 🔐 API Key Setup

1. Go to [Gemini API Console](https://makersuite.google.com/app/apikey).
2. Generate your API key if you haven’t already.
3. In your `chatDB_pt1.py`, look for the following line:

   ```python
   GEMINI_API_KEY = os.getenv("GEMINI_API_KEY")
   ```

4. Set the key using a `.env` file or export it in your terminal before running the app:

   ```bash
   export GEMINI_API_KEY="your_actual_api_key"  # For macOS/Linux
   ```

   ```powershell
   $env:GEMINI_API_KEY="your_actual_api_key"    # For PowerShell on Windows
   ```

   Or add the following to a `.env` file (you’ll need `python-dotenv`):

   ```
   GEMINI_API_KEY=your_actual_api_key
   ```

---

## 📁 Uploading Data

1. **Launch the app** using `streamlit run chatDB_pt1.py`.
2. Use the sidebar interface to upload:
   - **MongoDB JSON files** (e.g., upload all files within a specific folder like 'clinic' to run queries on multiple tables at once. Let's upload `doctors.json` and `visits.json`)
   - **CSV files** (e.g., let's upload `customers.csv`, `products.csv`, and `orders.csv`)
3. Uploaded files are automatically analyzed and loaded into memory.

---

## 🧠 Ask Questions

- After uploading data, try queries like:
  - `"What is the total revenue generated per product category?"` # For SQL 
  - `"List unique reasons patients visited a doctor from ENT specialty."` # For NoSQL
- The LLM interprets your question and auto-generates the corresponding query.

