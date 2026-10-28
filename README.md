# Douglas Geraldi

Applied data scientist and data analyst with a power systems and energy background. I have 15 years in the energy sector, from utility metering and data management at CPFL to delivering 100+ solar projects. I build Python models that turn operational data into decisions.

Based in Brazil (UTC-3). Open to remote Data Analyst and Applied Data Scientist roles worldwide, with a focus on energy, utilities, climate, and industrial analytics.

## Featured project

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
| Programming and data | Python (pandas, NumPy, scikit-learn, matplotlib), SQL, PySpark, Jupyter, Git |
| LLM applications | RAG (hybrid search, reranking, citations, abstention), sentence-transformers, LangChain |
| Analytics and BI | Power BI, Tableau, Excel (Power Query), dashboards, KPI design |
| Methods | anomaly detection, predictive modeling, forecasting, exploratory data analysis, data quality |
| Domain | photovoltaic performance, power systems, distributed generation, meter data management |

## Background

- Metering and data management at CPFL Energia, including the MDM implementation for 25,000+ commercial and industrial customers.
- Led project delivery and new business at Solstício Energia: 100+ solar projects, 50+ MWp commissioned. Built an account scoring model that doubled qualified B2B leads in 3 months.
- Electrical Engineering (B.Sc. and M.Sc.) at UNICAMP and an MBA in Executive Strategy at FGV. DataCamp Associate Data Scientist.
- Portuguese (native) and English (full professional).

## Contact

[LinkedIn](https://www.linkedin.com/in/douglas-geraldi)
