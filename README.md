# SOM Monitoring Daily

Automation monitoring dan rekap data SOM menggunakan Python dan Pandas.

---

# Features

- Load multiple Excel files
- Cleaning dan standardisasi data
- Merge seluruh data SOM
- Validasi data
- Generate rekap otomatis
- Export hasil ke Excel

---

# Tech Stack

- Python
- Pandas
- Openpyxl
- NumPy

---

# Project Structure

```text
project/
│
├── data/
├── output/
├── scripts/
├── config/
├── SOM_MONITORING_TERPADU.ipynb
├── requirements.txt
└── README.md
```

---

# Workflow

```mermaid
flowchart TD

    A[START]

    A --> B[Read Configuration]
    B --> C[Loop File Config]

    C --> D[Load Excel File]

    D --> E{Sheet Exists?}

    E -- Yes --> F[Read Sheet]
    E -- No --> G[Skip & Log Error]

    F --> H[Cleaning Data]
    H --> I[Rename Columns]
    I --> J[Transform Data]
    J --> K[Append to Master DataFrame]

    G --> C
    K --> C

    C --> L{All Files Processed?}

    L -- No --> C
    L -- Yes --> M[Merge Final Data]

    M --> N[Validation Checking]
    N --> O[Generate Rekap]
    O --> P[Export Excel Output]

    P --> Q[END]
```

---

# Installation

```bash
pip install -r requirements.txt
```

---

# Run Project

```bash
jupyter notebook
```

atau

```bash
python main.py
```

---

# Output

- Rekap SOM
- Monitoring report
- Cleaned dataset

---

# Future Improvement

- Add logging
- Config YAML
- Dashboard integration
- Scheduling automation
