# Loan-Default-Risk
Loan Default Risk (PySpark ML)
# Loan Default Risk (PySpark)

End-to-end **big data** example using **Apache Spark (PySpark)** for feature engineering and model training with Spark MLlib.  
Stack: **PySpark, Spark ML, Pandas, Docker**.

## Why this repo?
- Demonstrates **Spark SQL** transformations and **ML pipelines** at scale.
- Clean separation of ETL and modeling with a reproducible entrypoint.
- Ships with synthetic loan data inspired by common Kaggle-style schemas.

## Quickstart (local PySpark)
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt

# Train a Spark ML classifier
python src/train_spark.py --input data/raw/loans.csv --output artifacts/model
```

## Project Structure
```
loan-default-risk-pyspark/
├─ data/
│  └─ raw/loans.csv
├─ src/
│  ├─ etl.py               # Spark DataFrame cleaning & feature assembly
│  └─ train_spark.py       # Spark ML training script (LogisticRegression)
├─ tests/
│  └─ test_etl.py          # Minimal unit-style check with local Spark
├─ artifacts/              # Model output path (created at runtime)
├─ .gitignore
├─ Dockerfile
└─ requirements.txt
```

## Notes
- Keeps dependencies minimal to avoid heavy downloads.
- Replace LogisticRegression with XGBoost4J/Spark if needed.
- Add Airflow or Spark submit scripts for production.

---
