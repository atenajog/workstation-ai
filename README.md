# workstation-ai

A modular **multi-agent AI operating framework** with autonomous orchestration, governance, trading safety layers, memory systems, and plugin architecture.

Designed for building intelligent assistants, automation systems, and advanced AI decision-making pipelines.

---

## Features

- Multi-agent governance system (executive + operational)
- Autonomous orchestration engine
- Model routing (OpenAI, Groq, Llama, Qwen, Mistral…)
- Short-term + long-term memory
- Plugin system (tools / connectors)
- Trading safety framework (risk limits, compliance, guards)
- Background scheduler + event bus
- CLI, API Server, and future Web UI
- Fully modular and extensible

---

## 📁 Project Structure

### **Root**
```plaintext
workstation-ai/
├── README.md
├── requirements.txt
├── pyproject.toml
├── .gitignore
├── .env.example
├── config/
├── docs/
├── diagrams/
├── prompts/
├── src/
├── tests/
└── .github/

config/
├── agents.yml
├── models.yml
├── memory.yml
├── scheduler.yml
├── logging.yml
├── trading.yml
├── security.yml
└── app.yml

src/agents/
├── base_agent.py
├── executive/
└── operational/

src/core/
├── orchestrator.py
├── vote_engine.py
├── scheduler.py
├── event_bus.py
├── state_manager.py
├── security.py
└── settings.py

src/models/
├── registry.py
├── router.py
└── backends/
    ├── llama_backend.py
    ├── qwen_backend.py
    ├── mistral_backend.py
    ├── phi_backend.py
    ├── openai_backend.py
    └── groq_backend.py

src/memory/
├── short_term.py
├── long_term.py
├── vector_store.py
└── state_store.py

src/tools/
├── web_search.py
├── pdf_reader.py
├── docx_reader.py
├── csv_reader.py
├── whatsapp_client.py
├── email_sender.py
├── calendar_google.py
├── storage_client.py
├── trading_exchange.py
└── browser_api.py

src/trading/
├── risk_guard.py
├── compliance_check.py
├── order_builder.py
├── exchange_connector.py
└── strategy_states.py

src/apps/
├── cli/
│   └── main.py
└── api/
    └── server.py

tests/
├── test_agents_executive.py
├── test_agents_operational.py
├── test_core_orchestrator.py
├── test_memory.py
├── test_tools.py
├── test_model_router.py
└── test_trading_module.py

git clone https://github.com/atenajog/workstation-ai.git
cd workstation-ai
pip install -r requirements.txt

python -m src.apps.cli.main
