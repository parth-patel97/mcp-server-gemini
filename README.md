# ✈️ Flight Search Assistant (Powered by Gemini + MCP)

This is a simple and powerful Streamlit-based flight search tool that uses **Google's Gemini AI model** and **MCP (Modular Command Platform)** to find real-time flight information using natural language queries.

Users can search for flights like:

> "Find flights from Atlanta to Las Vegas on 2025-05-05"

Gemini interprets the query, identifies the right function/tool to use, and fetches flight data from the `mcp-flight-search` backend.

---

## 🔧 Features

- ✅ Natural language flight search
- ✅ Real-time flight data (via SERP API through MCP)
- ✅ Gemini Pro 2.5 model for query understanding
- ✅ Interactive UI using Streamlit
- ✅ Cleanly formatted flight results
- ✅ Error handling and fallback messaging

---

## 📦 Setup Instructions

### 1. Clone the repo

```bash
git clone https://github.com/your-username/flight-search-assistant.git
cd flight-search-assistant
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Create a `.env` file

Create a `.env` file in the root of your project:

```env
GEMINI_API_KEY=your-gemini-api-key
SERP_API_KEY=your-serp-api-key
```

The app will automatically load these using `python-dotenv`.

### 4. Run the app

```bash
streamlit run flight_search_ui.py
```

---

## 🖼 Sample Screenshot

<img width="844" alt="Screenshot 2025-04-30 at 4 22 25 PM" src="https://github.com/user-attachments/assets/3e6cc192-e7e1-4d02-9806-5bf0a55f3c8c" />

---

## 🔁 Flow Diagram

<img width="1277" alt="Screenshot 2025-04-30 at 4 02 40 PM" src="https://github.com/user-attachments/assets/3b2f192e-cee9-4e01-84c9-8fe49e2964e3" />

---

## 🧠 How it Works

1. User enters a natural language query.
2. Streamlit sends the query to Gemini 2.5.
3. Gemini interprets the query and generates a function call (tool use).
4. The tool is executed via MCP (`mcp-flight-search`) which fetches data from SERP API.
5. The response is formatted and shown in the Streamlit UI.

---
