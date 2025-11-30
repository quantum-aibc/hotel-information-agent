# hotel-information-agent
Hotel information AI assistant built with Microsoft Azure AI Foundry (RAG + Azure OpenAI + AI Search) following professional agent-building best practices.
azure-hotel-info-agent/
│
├─ src/
│  ├─ app.py                # main API / app entrypoint
│  ├─ agents/
│  │   ├─ hotel_agent.py    # orchestrates tools + LLM
│  ├─ tools/
│  │   ├─ search_client.py  # wrapper around Azure AI Search
│  │   ├─ booking_faq.py    # sample business-logic functions
│  ├─ config/
│  │   ├─ settings.py       # env vars, Azure keys (use .env example)
│  └─ ui/
│      └─ web_app.py        # Streamlit or FastAPI+Jinja UI
│
├─ data/
│  ├─ hotels.csv            # sample hotel data
│  └─ kb/                   # markdown/text files for RAG
│
├─ infra/
│  ├─ bicep/terraform/      # optional: infra as code
│  └─ azure-setup-notes.md  # manual steps if not using IaC
│
├─ tests/
│  ├─ test_agent_logic.py
│  └─ test_tools.py
│
├─ notebooks/
│  └─ prompt_experiments.ipynb
│
├─ .env.example
├─ requirements.txt or pyproject.toml
├─ README.md
└─ LICENSE
