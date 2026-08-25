# TraceIQ — Digital Evidence Analysis & Forensic Investigation Platform

TraceIQ is a beginner-friendly Python-based digital forensics application for analyzing digital evidence from files and folders.

---

## 🎯 Objectives

- Analyze files and folders for digital evidence.
- Extract file metadata and timestamps.
- Generate SHA-256 hashes for evidence verification.
- Identify duplicate files.
- Identify potentially suspicious files using forensic rules.
- Generate a basic forensic timeline.
- Generate an automated investigation report.

---

## 🔄 How TraceIQ Works

1. Select a folder containing digital evidence.
2. Scan files and extract metadata.
3. Generate SHA-256 hashes.
4. Detect duplicate files.
5. Identify potentially suspicious files.
6. Generate a forensic timeline.
7. Store investigation data.
8. Generate an investigation report.

---

## ⚠️ Important Note

TraceIQ is an educational digital forensics project. It identifies potentially suspicious files using rule-based indicators and does not guarantee that a file is malicious. Further investigation is required to determine whether a file is actually harmful.

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
