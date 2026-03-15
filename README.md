# Tax-X: Tax Defense & Deduction Tracker
### *Personal Finance Audit Tool for East African Taxpayers*

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat&logo=python&logoColor=white) 
![Status](https://img.shields.io/badge/Module_1-Complete-brightgreen)
![Assignment](https://img.shields.io/badge/CS_Practical-Error_Handling-blueviolet)

**The Goal:** Stop overpaying taxes simply because you don't know what is legally deductible. Tax-X is a Python utility I built to flag missed tax deductions in personal spending while demonstrating production-level error handling and logging.

##  Project Concept
In Uganda, many of us—especially freelancers and small business owners—lose money because we don't track "defensible" expenses. I designed this tool to audit a `.csv` of transactions against local tax categories like internet, professional services, training, and health.

The focus here isn't just the tax math; it's about building **robust software** that doesn't crash when it hits bad data or missing files.

##  How it's Built (Architecture)
I used a modular architecture to keep the logic clean and easy to secure. Instead of one giant script, each part of the process has its own home.

```text
smarttax/
├── main.py              # The "Brain" - orchestrates the audit
├── data/
│   └── transactions.csv # My raw transaction data
├── modules/
│   ├── audit_engine.py  # Production logic with custom exceptions
│   └── audit_engine_bad.py # "The Messy Version" - for assignment comparison
├── utils/
│   ├── logger.py        # Dual-stream logging (Console + .log file)
│   └── exceptions.py    # Custom error classes I defined
└── logs/
    └── smarttax.log     # The full debug trail for auditing
