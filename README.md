# 🔮 QualiGenAI Enterprise Trust & Lifecycle Management Suite

Welcome to the core engineering workspace of **QualiGenAI**. This master portfolio houses a fully integrated, decoupled suite of AI Quality Engineering platforms designed to transition modern LLM implementations from unverified probabilistic operations into rigorous, deterministic enterprise-grade software systems.

Rather than relying on superficial wrappers or basic prompt iterations, the QualiGenAI architecture wraps production applications inside a strict, multi-tiered validation and monitoring envelope.

---

## 🧱 The 4-Pillar Platform Architecture

The ecosystem is composed of four distinct repositories, each operating as a standalone layer of defense and evaluation:

### 1. 🎯 AI Reliability Engine (`/qualigenai-ai-reliability-engine`)
* **Core Role:** Pre-Production Deterministic Evaluation.
* **Capabilities:** Executes comprehensive automated regression test loops, analyzes chunking strategies, and calculates our custom **Factual Groundedness Index (0.94 Score)** to eliminate silent hallucinations before deployment.

### 🛡️ 2. AI Guardrails Platform (`/ai-guardrails-platform`)
* **Core Role:** Inline Runtime Safety Firewalls.
* **Capabilities:** Operates as a middleware security tokenizer proxy. It blocks adversarial injections, subverts jailbreak payloads, and scans data arrays to prevent critical PII token leaks in real time.

### 📈 3. AI Observability Platform (`/ai-observability-platform`)
* **Core Role:** Continuous Live Telemetry and Data Trails.
* **Capabilities:** Ingests distributed application runtime traces into a localized, ultra-fast **DuckDB** columnar database to track time-series latency, operational token distributions, and performance anomalies.

### ⚖️ 4. AI Governance & Operations Platform (`/qualigenai-central-hub`)
* **Core Role:** Centralized Orchestration, Lifecycles, & Cost Intelligence.
* **Capabilities:** The executive master control panel running an interactive system picker to run cross-repository test gates. Manages your corporate Model Registries, tracks prompt updates using Git-like version tree hashes, tracks token cloud costs, and calculates holistic application risk scorecards using statistical **Z-Scores**.

---

## 🗺️ Deep Technical Architecture Specifications
To view the complete unidirectional data routing flow, database entity relationships, and cross-directory integration layers, read our master technical breakdown:

➡️ **[Explore the Master Core Architecture Blueprint](./ARCHITECTURE.md)**

---

## 🛠️ Local Environment Workspace Activation

To launch the unified executive management dashboard from your local server, open PowerShell and run:

```powershell
# Navigate into the master orchestrator control hub
cd .\qualigenai-central-hub

# Activate the isolated virtual environment
.venv\Scripts\Activate.ps1

# Launch the interactive dual-pane dashboard interface
streamlit run app/dashboard/hub.py --server.port 8502 --client.showErrorDetails=false

Access the control deck interface at: http://localhost:8502

