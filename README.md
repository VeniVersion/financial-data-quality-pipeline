# financial-data-quality-pipeline
A modular data pipeline for validating, transforming, and tracking financial data using Pydantic, dbt, Airflow, and OpenLineage

##📁 Project Structure.

financial-data-quality-pipeline/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── data/
│   └── sample_data/           # Sample financial datasets
│
├── ingestion/
│   ├── pydantic_schemas.py    # Pydantic models for schema validation
│   ├── extract.py             # API/file ingestion scripts
│   └── validate.py            # Uses Pydantic for validating ingested data
│
├── dags/                      # Apache Airflow DAGs
│   └── data_pipeline_dag.py
│
├── dbt/
│   ├── models/
│   │   ├── staging/
│   │   └── core/
│   └── dbt_project.yml
│
├── expectations/              # Great Expectations suite
│   └── expectations_config.json
│
├── lineage/
│   └── openlineage_config.yaml
│
├── streamlit_app/
│   ├── app.py
│   └── dashboard_config.py
│
├── tests/
│   ├── test_validation.py
│   └── test_etl.py
│
└── requirements.txt
