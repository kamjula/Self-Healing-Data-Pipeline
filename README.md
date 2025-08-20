# Self-Healing Data Pipeline

A data pipeline that detects its own issues and fixes them — things like missing values, schema changes, duplicates, and outliers — without needing someone to manually step in every time something breaks.

I built this because I kept running into the same problem: pipelines fail silently or dump bad data downstream and you only find out later. The idea here is to catch failures at each stage, classify what went wrong, and apply a recovery strategy automatically.

## How it works

Each batch of data goes through four stages:

1. **Ingest** — pull in the raw data
2. 2. **Validate** — check for schema drift, nulls, duplicates, statistical outliers
   3. 3. **Recover** — if something's off, apply the right fix (impute, quarantine, retry, etc.)
      4. 4. **Load** — write clean data to the target store
        
         5. Every run gets logged so you have a full audit trail of what was detected and what was done about it.
        
         6. ## Tech
        
         7. Python, Pandas, SQL (SQLite / Postgres), standard logging
        
         8. ## Run it
        
         9. ```bash
            git clone https://github.com/kamjula/Self-Healing-Data-Pipeline.git
            cd Self-Healing-Data-Pipeline
            pip install pandas numpy pytest
            python pipeline/ingest.py
            ```

            ## Structure

            ```
            Self-Healing-Data-Pipeline/
            ├── pipeline/
            │   ├── ingest.py
            │   ├── validate.py
            │   ├── transform.py
            │   ├── load.py
            │   └── recover.py
            ├── tests/
            ├── logs/
            ├── data/
            └── README.md
            ```

            ---

            Sravani Kamjula
