# Fabio Boila

Data Analyst student at Hyper Island in Stockholm, moving into analytics after 15+ years leading teams in hospitality across Italy and Sweden. I came to data from the operational side — reading daily numbers and making staffing and purchasing decisions from them — and I'm drawn to analytics that supports people doing the same kind of work.

Currently looking for a LIA internship in Stockholm, December 2026 – June 2027.

---

### Working with

**SQL** — Snowflake; window functions, CTEs, quintile scoring

**Python** — pandas, requests, Jupyter

**Pipelines** — dbt, Apache Airflow, Azure Blob Storage

---

### Projects

**[lastfm-pipeline](https://github.com/Boiler82/lastfm-pipeline)** — end-to-end data pipeline
Last.fm API → Python → Azure Blob Storage → Snowflake → dbt → Looker Studio, orchestrated with Apache Airflow. dbt models parse nested JSON, deduplicate with `ROW_NUMBER()`, and use `LAG()` to find day-over-day chart position drops. Built as the final project for Hyper Island's Data Engineering course.

**[sql-customer-segmentation-rfm](https://github.com/Boiler82/sql-customer-segmentation-rfm)** — RFM segmentation in SQL
Customer segmentation on Snowflake's TPC-H dataset. Beyond the model itself, this repo documents what the analysis turned up: Frequency and Monetary correlated at 0.94, making two of the three dimensions largely redundant, while average order value carried independent signal. It also includes a geographic pattern I had to retract once the spread turned out to be within what random variation produces, and the validation queries that catch each problem.

---

### Also working on

A data analyst agent in Python using the Claude API — answering business questions against a SQLite database, with an RFM segmentation model in SQL underneath.

---

📍 Stockholm · [LinkedIn](https://www.linkedin.com/in/fabioboila) · fabioboila82@gmail.com
