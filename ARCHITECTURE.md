# 🏛️ QualiGenAI Global Multi-Repository Architecture Manual

This document details the unidirectional orchestration paths, analytical tracking layers, and data validation fabrics across the entire QualiGenAI software ecosystem.

---

## 🎨 Global Ecosystem Technical Schematic

The following live-rendered system chart maps out how execution states route from the high-level Streamlit executive deck, down through target applications, into your isolated test engines, and finally compile inside your DuckDB database store:

```mermaid
graph LR
    %% Global Design Overrides for Premium Obsidian Theme
    classDef hubStyle fill:#0f132a,stroke:#6366f1,stroke-width:2px,color:#E2E8F0,font-family:monospace;
    classDef engineStyle fill:#0b0f19,stroke:#475569,stroke-width:1px,color:#94a3b8,font-family:monospace;
    classDef autStyle fill:#1e1b4b,stroke:#818cf8,stroke-width:1px,color:#e0e7ff,font-family:monospace;
    classDef activeStyle fill:#064e3b,stroke:#10b981,stroke-width:2px,color:#34d399,font-family:monospace;
    classDef storageStyle fill:#02040a,stroke:#38bdf8,stroke-width:1px,color:#38bdf8,font-family:monospace;

    %% 1. ORCHESTRATION & GOVERNANCE LAYER (The Control Plane)
    subgraph CP [🔮 CONTROL PLANE]
        UI[Streamlit Executive Deck<br/>PORT: 8502]:::hubStyle
        Router[Context Router]:::hubStyle
        UI --> Router
    end

    %% 2. TARGET INFRASTRUCTURE (Applications Under Test)
    subgraph TI [🎯 TARGET APPS]
        P1[P1: Core RAG]:::autStyle
        P2[P2: Pilgrim Bot]:::autStyle
        P3[P3: Multi-Agent]:::autStyle
    end
    Router -->|1. Inject Context| TI

    %% 3. AUTOMATED VALIDATION LAYER (The Data Gates)
    subgraph VG [⚙️ QA GATES]
        RE[AI Reliability Engine<br/>• Groundedness: 0.94]:::engineStyle
        GW[AI Guardrails Proxy<br/>• 100% Interception]:::engineStyle
    end
    TI -->|2. Evaluate Context| VG

    %% 4. ANALYTICAL TELEMETRY LAYER (The Persistence Store)
    subgraph OLAP [📊 TELEMETRY VAULT]
        DB[(DuckDB Vault<br/>observability_vault.duckdb)]:::storageStyle
        Obs[AI Observability<br/>• Moving Z-Scores]:::engineStyle
        Gov[AI Governance<br/>• Cost Ledger]:::activeStyle
        DB --> Obs --> Gov
    end
    VG -->|3. Pipe Traces| DB
    Gov -.->|4. Dynamic Matrix Pass/Fail| UI

    %% Visual Layout Subgraph Background Styling
    style CP fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B
    style TI fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B
    style VG fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B
    style OLAP fill:#060814,stroke:#1e293b,stroke-width:1px,color:#64748B