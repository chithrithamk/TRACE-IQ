# TraceIQ — Digital Evidence Analysis & Forensic Investigation Platform

TraceIQ is a beginner-friendly Python-based digital forensics application for analyzing digital evidence from files and folders.

---

## 📁 Project Architecture

```text
TRACE IQ/
├── app.py                      # Main Streamlit UI entry point
├── requirements.txt            # Project dependencies (streamlit, pandas)
├── README.md                   # Project documentation & module guide
│
├── src/                        # Modular Forensics Engine
│   ├── __init__.py             # Package marker
│   ├── scanner.py              # Directory traversal & metadata extraction
│   ├── hasher.py               # SHA-256 evidence hashing
│   ├── duplicates.py           # Duplicate file detector
│   ├── suspicious.py           # Explainable rule-based suspicious file analyzer
│   ├── timeline.py             # Forensic chronological timeline generator
│   ├── database.py             # SQLite case and evidence persistence
│   └── reporter.py             # Forensic report builder and exporter
│
└── data/                       # Local SQLite database and exported reports
    └── .gitkeep
```

---

## 🧩 Module Overview

1. **`src/scanner.py`**: Scans user-specified directories and extracts file metadata (name, extension, size, creation/modification/access timestamps, hidden status).
2. **`src/hasher.py`**: Generates SHA-256 cryptographic hashes for evidence integrity verification.
3. **`src/duplicates.py`**: Groups and identifies duplicate files based on identical SHA-256 hashes.
4. **`src/suspicious.py`**: Evaluates files against explainable forensic heuristics (executable/script extensions, double extensions, hidden files, zero-byte files, timestamp anomalies).
5. **`src/timeline.py`**: Builds a chronological timeline of filesystem activity from file MAC timestamps.
6. **`src/database.py`**: Manages case storage and evidence indexing using lightweight standard SQLite (`sqlite3`).
7. **`src/reporter.py`**: Generates formatted forensic investigation reports.
8. **`app.py`**: Streamlit-based interactive digital forensics dashboard.
