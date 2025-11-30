# 🏨 Azure Hotel Information AI Agent

An end-to-end **AI agent built on Microsoft Azure AI Foundry** that answers hotel guest queries about rooms, amenities, policies, and nearby attractions using **RAG (Retrieval-Augmented Generation)** and tool-calling.

---

## 🚀 Highlights

- Built with **Microsoft Azure AI Foundry**
- Uses **Azure OpenAI** for natural language understanding
- **Azure AI Search** over hotel knowledge base (rooms, amenities, FAQs)
- Simple **web UI** for chatting with the agent
- Production-style structure: configs, tests, prompt experiments

> This project is part of my Azure AI Foundry learning path and certification.

---

## 🎯 Use Case

Typical questions the agent can handle:

- “Do you have rooms available with a sea view?”
- “Is breakfast included in the price?”
- “What is the check-in/check-out time?”
- “Is there parking available at the hotel?”
- “Recommend nearby restaurants for vegetarian food.”

---

## 🧱 Architecture

**Components:**

1. **Frontend**
   - Streamlit / React-based chat UI
2. **Backend**
   - Python (FastAPI / Flask) agent endpoint
   - Agent orchestration using Azure AI Foundry (Prompt Flow / Agent)
3. **AI Services**
   - Azure OpenAI (chat + function calling)
   - Azure AI Search for hotel knowledge base (documents + metadata)
4. **Data**
   - Sample hotel data (`data/hotels.csv`)
   - FAQ and policy documents (`data/kb/*.md`)

You can find a detailed architecture explanation in [`docs/architecture.md`](docs/architecture.md).

---

## 🧪 Features

- ✅ Natural-language Q&A about hotel information
- ✅ RAG over hotel policies and FAQs
- ✅ Tool-calling to:
  - Look up room types and price ranges
  - Check amenity availability (gym, Wi-Fi, pool, etc.)
- ✅ Basic evaluation notebooks for prompt and response quality
- ✅ Configurable and environment-based settings

---

## 🛠️ Tech Stack

- **Language:** Python
- **Cloud:** Microsoft Azure
- **AI Platform:** Azure AI Foundry
- **Models:** Azure OpenAI (GPT-style chat model)
- **Search:** Azure AI Search
- **Frameworks:** FastAPI / Flask, Streamlit
- **Other:** Docker (optional), pytest

---

## 🧩 Project Structure

```text
src/
  app.py               # App entrypoint (API)
  agents/hotel_agent.py
  tools/search_client.py
  tools/booking_faq.py
  config/settings.py
  ui/web_app.py

data/
  hotels.csv
  kb/*.md

notebooks/
  prompt_experiments.ipynb

tests/
  test_agent_logic.py
  test_tools.py
