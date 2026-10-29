# Raúl Jiménez Delgado

**Software Developer → Data Engineer** · Python · SQL · Airflow · dbt · Kafka · Spark · AWS

📍 Gran Canaria, Spain · 🇬🇧 English B2 (worked 14 months in an English-speaking environment in Ireland)

I design and build data pipelines end to end: ingestion, orchestration, modeling, serving and dashboards. I come from backend development (Java / Spring Boot), so I bring software engineering habits (clean code, testing, version control, CI) to the data lifecycle. I currently focus on batch and streaming pipelines, lakehouse architectures and ML serving.

Data Engineer & Automation Specialist | Python · AWS · Google Workspace | Currently @ Dinosol (HiperDino)

---

### Technical Competencies

| Domain | Stack |
| :--- | :--- |
| **Orchestration & Modeling** | ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white) ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square&logo=dbt&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) |
| **Streaming & Lakehouse** | ![Apache Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apache-kafka&logoColor=white) ![Apache Spark](https://img.shields.io/badge/Spark_Structured_Streaming-E25A1C?style=flat-square&logo=apachespark&logoColor=white) ![Delta Lake](https://img.shields.io/badge/Delta_Lake-003B57?style=flat-square) ![MinIO](https://img.shields.io/badge/MinIO-S3_Compatible-C72E49?style=flat-square) ![DuckDB](https://img.shields.io/badge/DuckDB-FFF000?style=flat-square&logo=duckdb&logoColor=black) |
| **Databases & Storage** | ![ClickHouse](https://img.shields.io/badge/ClickHouse-FFCC01?style=flat-square&logo=clickhouse&logoColor=black) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white) ![PostGIS](https://img.shields.io/badge/PostGIS-Geospatial-336791?style=flat-square) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white) |
| **ML & Analytics** | ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) ![XGBoost](https://img.shields.io/badge/XGBoost-337AB7?style=flat-square) ![LightGBM](https://img.shields.io/badge/LightGBM-02A676?style=flat-square) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white) |
| **APIs & Backend** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white) ![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) |
| **Visualization & Frontend** | ![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white) ![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white) ![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black) ![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=flat-square&logo=leaflet&logoColor=white) |
| **Cloud & Infrastructure** | ![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square&logo=amazon-aws&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![Docker Compose](https://img.shields.io/badge/Docker--Compose-2496ED?style=flat-square&logo=docker&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) |
| **Languages & Tools** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Bash](https://img.shields.io/badge/Shell_Script-121011?style=flat-square&logo=gnu-bash&logoColor=white) |

---

### Selected Projects

#### 🌊 [DeepWave Canarias](https://github.com/raulJD13/deepwave-canarias)
**Wave, wind and maritime risk forecasting for 14 coastal zones of the Canary Islands.**
A medallion-style data pipeline (Bronze → Silver → Gold) and LightGBM models for wave height, period and wind at +3h to +48h horizons, plus interpretable rules for beach risk, navigation risk and a surf score. Predictions are exported as lightweight JSON artifacts and served by a FastAPI backend to an interactive web command center (Leaflet + Chart.js).

* **Stack:** Python, LightGBM, FastAPI, Pydantic, pytest, Docker, Leaflet.js, Chart.js.
* **Highlights:** Wave height MAE of 0.32 m at +24h and 0.44 m at +48h, 32 automated tests (API, data contract, frontend, Docker), and a production runtime with no ML dependencies. The served predictions are precomputed demo artifacts, not a live inference pipeline (documented in the repo).


#### 🛰️ [Space Pulse](https://github.com/raulJD13/space-pulse)
**Real-time space threat monitoring platform built on seven NASA APIs.**
Six scheduled Airflow pipelines (async clients with retries and rate limiting) archive raw JSON in MinIO and write typed records to ClickHouse, with TTL policies per table. A dbt layer (14 models) builds Grafana-ready marts, a FastAPI backend serves a React dashboard, and satellite anomalies are detected with an Isolation Forest and published to Kafka.

* **Stack:** Python, Airflow, Kafka, MinIO, ClickHouse, dbt, Grafana, FastAPI, React, scikit-learn, Docker.
* **Highlights:** Consistent extract → archive → load pattern across all DAGs, an asteroid risk-scoring formula implemented both in Python and in dbt, and a documented list of known limitations.


#### 🚢 [Atlantic Ops Lakehouse](https://github.com/raulJD13/Atlantic-Ops) · [Live demo](https://atlantic-ops.streamlit.app/)
**Real-time maritime logistics intelligence platform.**
Ingests AIS vessel positions in real time, validates them with strict data contracts, detects operational events through geofencing, and stores a reliable historical record with ACID guarantees on a lakehouse.

* **Stack:** Python, Kafka, Spark Structured Streaming, Delta Lake, MinIO, DuckDB, Streamlit, PyDeck, Docker.
* **Highlights:** Full streaming path from AIS ingestion through Kafka and Spark ETL to Delta Lake on S3-compatible storage, served with DuckDB and visualised in a real-time dashboard with geofencing alerts and fleet KPIs.

#### 🔥 [Eco Pulse Lakehouse](https://github.com/raulJD13/eco-pulse-lakehouse)
**Real-time distributed streaming and lakehouse architecture for wildfire risk.**
Ingests satellite telemetry (NASA) and IoT sensor data to estimate wildfire spread risk in real time.

* **Stack:** Python, Kafka, Spark Structured Streaming, Delta Lake, MinIO, Docker.
* **Highlights:** Medallion architecture with geospatial joins between disparate streams and ACID guarantees through Delta Lake.

#### ☁️ [CanaryAir Data Engineering](https://github.com/raulJD13/CanaryAir-Data-Engineering) · [Live demo](https://canaryair-data-engineering.streamlit.app/)
**Automated ETL for air quality and dust-storm monitoring in Gran Canaria.**
Python ETL with validation and error handling, loading into a cloud PostGIS database (Neon) on a schedule, with CI/CD through GitHub Actions and a public Streamlit dashboard.

* **Stack:** Python, PostgreSQL/PostGIS, GitHub Actions, Streamlit, Docker.


#### ⚽ [Football Analytics](https://github.com/raulJD13/football-analytics)
**End-to-end data engineering & ML platform for LaLiga match prediction.**
Ingests match data from football-data.org and API-Football through Airflow DAGs into MinIO (raw Parquet) and ClickHouse, transforms it with a layered dbt project (staging → intermediate → marts), trains Poisson and XGBoost models tracked in MLflow, and serves predictions through FastAPI and a Next.js dashboard. The whole stack starts with a single `docker compose up`.

* **Stack:** Python, Airflow, dbt, ClickHouse, MinIO, MLflow, FastAPI, Next.js, XGBoost, Docker.
* **Highlights:** Temporal cross-validation to avoid leakage, a weekly retraining DAG, and a documented benchmark of XGBoost vs CatBoost vs FT-Transformer. XGBoost reaches **50.4% ± 3.4%** mean CV accuracy (55.9% on the last fold) against a 49.0% home-win baseline. Football is a noisy target, so the project focuses on pipeline quality and honest evaluation rather than headline accuracy.


---

### More projects

| Project | What it is | Stack |
| :--- | :--- | :--- |
| [ATP Match Predictor](https://github.com/raulJD13/atp-match-predictor) · [Demo](https://atp-predictor-web.onrender.com/) | Full-stack ML app that predicts ATP tennis match winners, deployed as Docker microservices | Python, Docker, Render |
| [Investigating Agent](https://github.com/raulJD13/Investigating-Agent) · [Demo](https://huggingface.co/spaces/RaulJimenez/agente-investigador) | Conversational AI agent that uses an LLM (Gemini) with tools to perform real-world tasks | Python, Gemini API, Hugging Face Spaces |
| [Customer Churn Prediction](https://github.com/raulJD13/Customer-Churn-Prediction) | Churn modeling for an e-commerce platform: preprocessing, feature engineering and evaluation | Python, scikit-learn, Pandas |

---

### Education & Certifications

* Specialization in Big Data & Artificial Intelligence, IES El Rincón
* CFGS Multiplatform Application Development (DAM), IES El Rincón (2023 – 2025)

---

<div align="left">
  <a href="https://www.linkedin.com/in/rauljimenezdelgado/">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
  </a>
  <a href="mailto:raul.jimenez.del@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact_Me-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</div>
