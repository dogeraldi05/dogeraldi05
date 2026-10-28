# Douglas Geraldi

Applied data scientist and data analyst with a power systems and energy background. I have 15 years in the energy sector, from utility metering and system integration at CPFL to delivering 100+ solar projects. I build Python models that turn operational data into decisions.

Based in Brazil (UTC-3). Open to remote Data Analyst and Applied Data Scientist roles worldwide, with a focus on energy, utilities, climate, and industrial analytics.

## Featured project

### [PV-anomaly-detection](https://github.com/dogeraldi05/PV-anomaly-detection)

Which solar inverters lost energy, why, and how much?

The method comes from my professional work on PV plant performance (2024) and is rebuilt here on public and synthetic data. Each inverter's output is compared with a weather baseline learned from its own history (robust regression on irradiance and module temperature). The project separates plant-level events, such as a grid trip, from individual inverter faults, and raises alarms with a probable cause and the energy lost in kWh.

- Four detection rules: zero output in daylight, missing data, new fault, and chronic underperformance.
- A step report that dates the day a lasting drop started, such as a string opening.
- 17 automated tests with pytest.
- Validated on a synthetic plant with injected faults and on two public plants (22 inverters, 34 days).
- Stated limits: daily alarms are reliable from about 10% loss, and the step report catches about 5%. The real plants have no labeled faults.

Stack: Python, pandas, scikit-learn, matplotlib, pytest.

## Other projects

- [OutagesUSA_1](https://github.com/dogeraldi05/OutagesUSA_1): PySpark analysis of 77,000+ US power outage records (2023). Random Forest to classify outage event types and Linear Regression to predict outage duration.
- [etl-toolkit-test01](https://github.com/dogeraldi05/etl-toolkit-test01): small ETL utilities and studies on retry strategies, timing, and decorators.

## Skills

| Area | Tools |
|---|---|
| Programming and data | Python (pandas, NumPy, scikit-learn, matplotlib), SQL, PySpark, Jupyter, Git, AWS EC2 |
| Analytics and BI | Power BI, Tableau, Excel (Power Query), dashboards, KPI design |
| Methods | anomaly detection, predictive modeling, forecasting, exploratory data analysis, data quality |
| Data systems | master data management (MDM), systems integration testing (SAP, MDM, AMI) |
| Domain | photovoltaic performance, power systems, distributed generation, meter data |

## Background

- CPFL Energia: worked with the IT team on the MDM rollout for 25,000+ commercial and industrial customers, validating the integrations between SAP modules, the eMeter MDM, Itron ZFA, and Silver Spring UIQ, and running end-to-end tests from meter data collection to the start of billing.
- Solstício Energia: led project delivery and new business, with 100+ solar projects and 50+ MWp commissioned. Built an account scoring model (2024) that doubled qualified B2B
