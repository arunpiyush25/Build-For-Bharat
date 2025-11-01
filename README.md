# 🌾 Project Samarth — Bharat Agriculture cum Climate Assistant

> **An Intelligent, Live Data-Driven Q&A System for India’s Agriculture and Climate Insights**

---

## 📘 Overview

**Project Samarth** is an intelligent **Q&A system** built over India’s **agriculture and climate datasets** from [data.gov.in](https://data.gov.in).  
It enables policymakers, researchers, and citizens to ask **natural language questions** like:

> “Compare the average annual rainfall in Punjab and Andhra Pradesh for the last 5 years. Also list top 3 crops in each state.Compare the average annual rainfall in Punjab and Andhra Pradesh for the last 5 years. Also list top 3 crops in each state.”

The system understands the query, identifies relevant datasets, fetches live data, performs reasoning, and generates a **traceable, data-backed answer** — all in real-time.

---

## 🎯 Problem Statement

Government datasets exist in silos across ministries like the **Ministry of Agriculture & Farmers Welfare** and the **India Meteorological Department (IMD)**.  
These datasets vary in structure and schema, making cross-domain insights difficult.

**Project Samarth** solves this challenge by integrating these heterogeneous datasets and allowing **live question-answering** over them — enabling evidence-based policy analysis.

---

## 🧠 Key Features

✅ **Live Data Fetching** – Fetches datasets daily from [data.gov.in](https://data.gov.in) (For updating the dataset - Automatically fetches data at 1 AM every night.)
✅ **Intelligent Query Understanding** – Uses **Gemini 2.0 Flash** to parse natural queries into structured intent.  
✅ **Dynamic Data Integration** – Merges IMD rainfall data and agriculture crop data into one unified schema.  
✅ **Automated Reasoning** – Computes insights, correlations, and trends automatically.  
✅ **Computational Calculations** – Uses Pandas library for calculations because LLMs sometimes hallucinate in computaions.
✅ **Traceability & Source Citation** – Every data point is linked back to its dataset of origin.  
✅ **Interactive UI** – Built using **Gradio** for a fast, intuitive Q&A experience within Google Colab.

---

## 🔄 Workflow Overview

The end-to-end workflow of **Project Samarth** operates in four intelligent stages:

1. **🧑‍💬 User Query Input**  
   - User enters a natural language question like *“Which state had the highest rice yield last year?”*  

2. **🧠 Intent Extraction (Gemini 2.0 Flash)**  
   - The Gemini LLM parses the query to identify the type of task (comparison, trend, correlation, etc.)  
   - Generates a structured JSON intent specifying what data to fetch and what to compute.

3. **📊 Data Fetching & Computation (Pandas + APIs)**  
   - The system queries live government datasets via the **Data.gov.in API**.  
   - Relevant data is preprocessed, merged, and computed using **Pandas**.

4. **💬 Final Answer Generation (Gemini)**  
   - The computed results are passed back to Gemini for human-readable summarization.  
   - The answer includes insights, context, and dataset citations for full transparency.

---

## 💻 Tech Stack

| Layer | Technology |
|-------|-------------|
| **Language Model** | Gemini 2.0 Flash |
| **Frontend** | Gradio (in Colab) |
| **Backend** | Python |
| **Data Handling** | Pandas |
| **APIs** | Data.gov.in APIs |
| **Automation** | Colab Scheduler (daily at 1 AM) |

---

## 🌐 Data Sources

| Dataset | Source | URL |
|----------|---------|-----|
| **Rainfall Data** | India Meteorological Department | [Link]([https://data.gov.in/resource/8e0bd482-4aba-4d99-9cb9-ff124f6f1c2f](https://www.data.gov.in/resource/sub-divisional-monthly-rainfall-1901-2017)) |
| **Crop Production Data** | Ministry of Agriculture & Farmers Welfare | [Link]([https://data.gov.in/resource/35be999b-0208-4354-b557-f6ca9a5355de](https://www.data.gov.in/resource/district-wise-season-wise-crop-production-statistics-1997)) |

---

## 🔍 Example Queries

- “Compare the average annual rainfall in Punjab and Haryana for the last 5 years and list the top 3 crops in each state.”
- “Identify the district in Maharashtra with the highest sugarcane production in the latest year available.”
- “Analyze the production trend of rice in Tamil Nadu over the last decade and correlate it with rainfall.”
- “What are the top drought-resistant crops in Rajasthan over the past decade?”

---

## 🧩 Core Functionalities

1. **Data Fetching Layer**  
   - Fetches all records using Data.gov.in REST API with retry and pagination.  
   - Includes a scheduler to fetch new data daily at **1 AM**.

2. **Data Pre-Processing Layer**  
   - Cleans, merges, and maps rainfall subdivisions to states.  
   - Aggregates crop production data by year and crop type.

3. **Reasoning Layer**  
   - Gemini model interprets natural language queries into structured JSON intents.  
   - Pandas executes the query logic to derive insights (e.g., trends, comparisons).
   - Again LLM called for giving a natural language answers with the help of insights derived by the Pandas.

4. **Presentation Layer**  
   - Displays parsed intent, query result, and final summarized answer.  
   - All results include **source citations** for transparency.

---

## 🎨 User Interface (Gradio)

A simple and clean interface that lets users:
- Type natural questions
- See parsed query intent
- View structured data results
- Get final human-readable answers with citations

---

## 📅 Daily Automation

- The notebook includes a scheduler cell that fetches **fresh datasets automatically every midnight (1 AM)**.
- Ensures that the answers are **live and always up to date**.

---

## 🏁 Outcomes

✅ Fully functional end-to-end prototype  
✅ Live data integration from government APIs  
✅ Reasoning and synthesis using Gemini 2.0 Flash  
✅ Transparent answers with data citations  
✅ Interactive, ready-to-demo Gradio frontend

---

## 📽️ Demo Video

 [**Watch 2-Minute Loom Walkthrough**](https://drive.google.com/file/d/1cEUAM0WGSYXiUS-ltUA0E10cL9GD8dKa/view?usp=sharing)  
*(Showcasing data fetching, reasoning pipeline, and UI demo)*

---

## ⚙️ How to Run

1. Open the notebook in **Google Colab**  
2. Run all setup cells (API keys to be changed with you own, fetch functions, etc.)  
3. Launch the **Gradio app** cell  
4. Ask your question in natural language — get instant insights!

---

## 🧑‍💻 Author

**Piyush Arun [@arunpiyush25]**  
📍 M.Tech, Computer Science & Engineering — NIT Calicut  
🚀 Passionate about GenAI, Multi Agent systems, RAG, Langchain, LLMs, etc

---

## 🏆 Acknowledgements

- [data.gov.in](https://data.gov.in)
- [India Meteorological Department](https://mausam.imd.gov.in)  
- [Ministry of Agriculture & Farmers Welfare](https://agricoop.gov.in)  
- [Gemini API by Google DeepMind](https://ai.google.dev)  

---

> *“Data, when made intelligent and accessible, drives better decisions for the nation.”* 🇮🇳

