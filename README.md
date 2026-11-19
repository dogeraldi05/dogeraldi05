# Douglas Geraldi

Applied data scientist and data analyst with a power systems and energy background. I have 15 years in the energy sector, from utility metering and data management at CPFL to joining a solar company as an early partner and scaling it through 100+ delivered projects. I build Python models that turn operational data into decisions, and I have run the business those decisions affected.

Based in Brazil (UTC-3). Open to remote Data Analyst and Applied Data Scientist roles worldwide, with a focus on energy, utilities, climate, and industrial analytics.

## Featured projects

### [ONS_forecast](https://github.com/dogeraldi05/ons_forecast)

Does a machine learning model actually beat a well-chosen naive baseline on daily peak electricity demand?

Forecasting daily peak demand for Brazil's National Interconnected System on ONS open data. The data layer is SQL on DuckDB: lags, rolling means and calendar features as window functions, every one of them at least 7 days old so nothing leaks at a 7-day horizon.

- Walk-forward cross-validation over five folds, plus a holdout touched once.
- +8.9% skill over the seasonal naive across subsystems, +29.2% on Southeast/Midwest.
- The same pipeline runs on CSV and Parquet, with the trade-off measured rather than asserted: 358 KB vs 138 KB on disk, ~1,400 ms vs ~30 ms ingestion, typed on read or not.
- A 2027 long-horizon forecast using a linear trend per subsystem times an XGBoost seasonal ratio, backtested at +24.4% over the annual naive.
- Stated limits: no weather data, three years of history, point forecasts only, and a linear trend fitted on under three years.

Stack: DuckDB, SQL, Python, pandas, XGBoost, matplotlib.

### [PV-anomaly-detection](https://github.com/dogeraldi05/PV-anomaly-detection)

Which solar inverters lost energy, why, and how much?

The project compares each inverter's output with a weather baseline learned from its own history (robust regression on irradiance and module temperature). It separates plant-level events, such as a grid trip, from individual inverter faults, and raises alarms with a probable cause and the energy lost in kWh.

- Four detection rules: zero output in daylight, missing data, new fault, and chronic underperformance.
- A step report that dates the day a lasting drop started, such as a string opening.
- 17 automated tests with pytest.
- Validated on a synthetic plant with injected faults and on two public plants (22 inverters, 34 days).
- Stated limits: daily alarms are reliable from about 10% loss, and the step report catches about 5%. Real-data validation has no labeled faults.

Stack: Python, pandas, scikit-learn, matplotlib, pytest.

### [solar-rag](https://github.com/dogeraldi05/solar-rag)

A minimal retrieval-augmented generation pipeline in about 150 lines of Python, built as a reference implementation on a small photovoltaic corpus.

- Hybrid search: BM25 plus dense embeddings, merged with Reciprocal Rank Fusion, with an optional reranker.
- Refuses to answer when the evidence is weak, using a similarity threshold calibrated on sample questions.
- Answers with numbered citations, through any OpenAI-compatible model or as extracted passages.
- Small evaluation script: hit rate@3, MRR and refusal of out-of-scope questions (7/7, 1.00, 2/2 on the demo set).
- Stated limits: a tiny demo corpus, section-based chunking, in-memory index.

Stack: Python, sentence-transformers, NumPy.

## Other projects

- [OutagesUSA_1](https://github.com/dogeraldi05/OutagesUSA_1): PySpark analysis of 77,000+ US power outage records (2023). Random Forest to classify outage events and Linear Regression to predict outage duration.
- [etl-toolkit-test01](https://github.com/dogeraldi05/etl-toolkit-test01): small ETL utilities and studies on retry strategies, timing, and decorators.

## Skills

| Area | Tools |
|---|---|
| Programming and data | Python (pandas, NumPy, scikit-learn, XGBoost, matplotlib), SQL (window functions, CTEs), DuckDB, PySpark, Jupyter, Git |
| LLM applications | RAG (hybrid search, reranking, citations, abstention), sentence-transformers, LangChain |
| Analytics and BI | Power BI, Tableau, Excel (Power Query), dashboards, KPI design |
| Methods | time series forecasting, walk-forward validation, baseline benchmarking, anomaly detection, predictive modeling, exploratory data analysis, data quality |
| Business | P&L ownership, business development, pricing, contract negotiation, commercial forecasting, stakeholder management |
| Domain | photovoltaic performance, power systems, electricity demand, distributed generation, meter data management |

## Background

**Entrepreneur and business developer.** Partner at Solstício Energia, where I came in early to lead the electrical engineering side and stayed 10 years running the company from both sides of the table: P&L ownership, business development, pricing and contract negotiation, and a B2B commercial unit I coordinated from 2018 to 2024 with two direct reports. 100+ solar projects delivered, 50+ MWp commissioned, USD 2.5M+ in new business closed.

That work is where my analytics habit started. An account scoring model doubled qualified B2B leads in three months. A KPI-driven contract tracking framework over 10+ concurrent contracts cut client disputes by half. Both were built because the business needed them, not as exercises.

**Utility engineering.** Metering and data management at CPFL Energia, including the MDM implementation for 25,000+ commercial and industrial customers, and the statistical checks that kept that measurement data trustworthy.

**Education.** Electrical Engineering (B.Sc. and M.Sc.) at UNICAMP. MBA in Strategic Business Management at Fundação Getulio Vargas (FGV), one of Brazil's leading business schools. DataCamp Associate Data Scientist.

**Languages.** Portuguese (native) and English (full professional).

## Contact

[LinkedIn](https://www.linkedin.com/in/douglas-geraldi)
