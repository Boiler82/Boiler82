# Fabio Boila

Data Analyst student at Hyper Island in Stockholm, moving into analytics after 15+ years leading teams in hospitality across Italy and Sweden. I came to data from the operational side, reading daily numbers and making staffing and purchasing decisions from them and I'm drawn to analytics that supports people doing the same kind of work.

Currently looking for a LIA internship in Stockholm, December 2026 – June 2027.

---

### Working with

**SQL** — Snowflake; window functions, CTEs, quintile scoring

**Python** — pandas, matplotlib, requests, Jupyter

**Pipelines** — dbt, Apache Airflow, Azure Blob Storage

**BI** — Looker Studio, Power BI, Tableau

**Other** — Git, Excel / Google Sheets

---

### Projects

**[billboard-25-year-analysis](https://github.com/Boiler82/billboard-25-year-analysis)**: 25 years of the Billboard Hot 100 in Python

Follows 11,026 songs that entered the chart from 2000 to 2024. In the streaming era, 75% of new songs peak in their first week (6% in 2000), and the typical chart run fell from 19 weeks to 3. The data has no song ID, so I built one and validated it against Billboard's own week counts (99% match). Runs on public data, so anyone can reproduce it.

**[lastfm-pipeline](https://github.com/Boiler82/lastfm-pipeline)**: end-to-end data pipeline

Last.fm API → Python → Azure Blob Storage → Snowflake → dbt → Looker Studio, orchestrated with Apache Airflow. dbt models parse nested JSON, deduplicate with `ROW_NUMBER()`, and use `LAG()` to find day-over-day chart position drops. Built as the final project for Hyper Island's Data Engineering course.

**[sql-customer-segmentation-rfm](https://github.com/Boiler82/sql-customer-segmentation-rfm)**: RFM segmentation in SQL

Customer segmentation on Snowflake's TPC-H dataset. Frequency and Monetary correlated at 0.94, making two of the three dimensions largely redundant, so I switched Monetary to average order value. The repo also covers a geographic pattern I had to retract once it turned out to be random variation, and the validation queries that catch each problem.

---
### Also working on

A data analyst agent in Python using the Claude API — answering business questions against a SQLite database, with an RFM segmentation model in SQL underneath.

---

📍 Stockholm · [LinkedIn](https://www.linkedin.com/in/fabioboila) · fabioboila82@gmail.com
