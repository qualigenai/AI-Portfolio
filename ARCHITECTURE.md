# 🏛️ QualiGenAI Global Multi-Repository Architecture Manual

This document details the unidirectional orchestration paths, analytical tracking layers, and data validation fabrics across the entire QualiGenAI software ecosystem.

---

## 🎨 Global Ecosystem Technical Schematic

The following live-rendered system chart maps out how execution states route from the high-level Streamlit executive deck, down through target applications, into your isolated test engines, and finally compile inside your DuckDB database store:

```mermaid
graph TD
    %% Global Design Overrides for Premium Theme
    classDef hubStyle fill:#0f132a,stroke:#6366f1,stroke-width:2px,color:#E2E8F0,font-family:monospace;
    classDef engineStyle fill:#0b0f19,stroke:#475569,stroke-width:1px,color:#94a3b8,font-family:monospace;
    classDef autStyle fill:#1e1b4b,stroke:#818cf8,stroke-width:1px,color:#e0e7ff,font-family:monospace;
    classDef activeStyle fill:#064e3b,stroke:#10b981,stroke-width:2px,color:#34d399,font-family:monospace;
    classDef storageStyle fill:#02040a,stroke:#38bdf8,stroke-width:1px,color:#38bdf8,font-family:monospace;

    %% 1. ORCHESTRATION & GOVERNANCE LAYER (The Control Plane)
    subgraph CP [🔮 CONTROL PLANE - CENTRAL HUB]
        UI[Streamlit Executive Deck<br/>PORT: 8502]:::hubStyle
        Router[Python Subprocess Context Router]:::hubStyle
        Gov[AI Governance Platform<br/>• Model registries<br/>• Prompt version history<br/>• Cost intelligence ledger]:::activeStyle
    end

    %% 2. TARGET INFRASTRUCTURE (Applications Under Test)
    subgraph TI [🎯 TARGET WORKLOAD PORTFOLIO]
        P1[P1: Core RAG Engine]:::autStyle
        P2[P2: Srisailam Pilgrim Bot]:::autStyle
        P3[P3: Multi-Agent System]:::autStyle
    end

    %% 3. AUTOMATED VALIDATION LAYER (The Data Gates)
    subgraph VG [⚙️ DISCRETE QA VALIDATION GATES]
        RE[AI Reliability Engine<br/>• Factual Groundedness Index<br/>• Regression Stress Arrays]:::engineStyle
        GW[AI Guardrails Platform<br/>• Security Tokenizer Proxy<br/>• Adversarial Injection Probes]:::engineStyle
    end

    %% 4. ANALYTICAL TELEMETRY LAYER (The Persistence Store)
    subgraph OLAP [📊 DATA STORAGE & TELEMETRY]
        DB[(Centralized DuckDB Storage<br/>observability_vault.duckdb)]:::storageStyle
        Obs[AI Observability Engine<br/>• SLA Latency Trendlines<br/>• Rolling Window Z-Scores]:::engineStyle
    end

    %% Data Routing Interconnections
    UI -->|1. Trigger Selection & Profile| Router
    Router -->|2. Inject Context Target Context| TI
    TI -->|3. Evaluate System Behavior| VG
    VG -->|4. Pipe Real-time Ingestion Traces| DB
    DB -->|5. Aggregate Telemetry Data| Obs
    Obs -->|6. Sync Metric Models| Gov
    Gov -.->|7. Render Live Verification Grid PASSED| UI

    %% Visual Layout Styling
    style CP fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B
    style TI fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B
    style VG fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B
    style OLAP fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B