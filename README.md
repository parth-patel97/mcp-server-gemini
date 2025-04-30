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

> Replace this image with your screenshot of the Streamlit output.

![Flight Search UI Screenshot](assets/sample_output.png)

---

## 🔁 Flow Diagram

> Replace this with a diagram showing how data flows between user → Streamlit → Gemini → MCP → SERP API.

![Flow Diagram](assets/flow_diagram.png)

---

## 🧠 How it Works

1. User enters a natural language query.
2. Streamlit sends the query to Gemini 2.5.
3. Gemini interprets the query and generates a function call (tool use).
4. The tool is executed via MCP (`mcp-flight-search`) which fetches data from SERP API.
5. The response is formatted and shown in the Streamlit UI.

---
