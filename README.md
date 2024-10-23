```mermaid
flowchart TB
    %% Beschreibung der Swimlane-Darstellung

    %% Lane 1: Positiver Stream
    subgraph POSITIVE_STREAM[Positiver Stream: Effiziente Anpassung]
        direction TB
        A1[Anpassung im Fachgeschäft] --> A2[✅ Strumpf passt: Kundenzufriedenheit]
        A2 --> A3[👍 Nachbestellung]
        A3 --> A4[🌟 Zufriedener Endkunde]
    end

    %% Lane 2: Negativer Stream
    subgraph NEGATIVE_STREAM[Negativer Stream: Rücksendung und Neubestellung]
        direction TB
        B1[Anpassung im Fachgeschäft] --> B2[⚠️ Strumpf passt nicht]
        B2 --> B3[🔄 Neu-Anmessung nötig, 20 Min]
        B3 --> B4[📦 Retoure anmelden und verpacken]
        B4 --> B5[🚚 Rücksendung zu SIGVARIS, 1-3 Tage]
        B5 --> B6[🔍 Prüfung der Retoure durch SIGVARIS, 25 Min]
        B6 --> B7[🛒 Neubestellung]
        B7 --> B8[⏳ Anprobe erneut im Fachgeschäft, 20 Min]
        B8 --> B9[❌ Potenzielle weitere Rücksendung, höhere Kosten]
    end

    %% Label zur Verdeutlichung der Parallelität
    POSITIVE_STREAM --> |Vergleich| NEGATIVE_STREAM
