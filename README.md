# Fabio Boila

Data Analyst student at Hyper Island in Stockholm, moving into analytics after 15+ years leading teams in hospitality across Italy and Sweden. I came to data from the operational side, reading daily numbers and making staffing and purchasing decisions from them and I'm drawn to analytics that supports people doing the same kind of work.

Currently looking for a LIA internship in Stockholm, 7 December 2026 – 6 June 2027.

---

### Working with

**SQL** — Snowflake, SQLite; window functions, CTEs, quintile scoring

**Python** — pandas, matplotlib, requests, Jupyter

**AI** — Claude API, tool-using agents, LLM evaluation

**Pipelines** — dbt, GitHub Actions, Apache Airflow, Azure Blob Storage

**BI** — Data Studio (formerly Looker Studio), Power BI, Tableau

**Other** — Git, Excel / Google Sheets

---

### Projects

**[data-analyst-agent](https://github.com/Boiler82/data-analyst-agent)**: an AI agent that answers questions about e-commerce data

Ask a question in plain English and the agent writes its own SQL, runs it on the Olist dataset (99,441 orders, 9 tables) and answers in words or with a chart. Built in Python with the Claude API, on a read-only database. I tested it on 15 questions with SQL answer keys: Claude Sonnet scored 15/15, while the smaller Claude Haiku scored 14/15. It fell into a trap where `customer_id` changes with every order, so it counted orders instead of people. One note about the data in the agent's instructions brought Haiku to 15/15. I also caught a chart showing revenue crashing to zero; the data simply ends in late 2018, so the agent now leaves out incomplete periods.

**[billboard-25-year-analysis](https://github.com/Boiler82/billboard-25-year-analysis)**: 25 years of the Billboard Hot 100 in Python

Follows 11,026 songs that entered the chart from 2000 to 2024. In the streaming era, 75% of new songs peak in their first week (6% in 2000), and the typical chart run fell from 19 weeks to 3. The data has no song ID, so I built one and validated it against Billboard's own week counts (99% match). Runs on public data, so anyone can reproduce it.

**[lastfm-pipeline](https://github.com/Boiler82/lastfm-pipeline)**: end-to-end data pipeline

Last.fm API → Python → Snowflake → dbt → Data Studio, running every day on GitHub Actions. Built as the final project for Hyper Island's Data Engineering course on Airflow in Docker, then migrated to the cloud so it no longer depends on my laptop. dbt models parse nested JSON, deduplicate with `ROW_NUMBER()`, and use `LAG()` to find day-over-day chart position drops, checked by 15 automated tests. Snowflake access uses key-pair authentication and least-privilege roles, including a read-only user for the dashboard. [dbt docs & lineage graph](https://boiler82.github.io/lastfm-pipeline/)

**[sql-customer-segmentation-rfm](https://github.com/Boiler82/sql-customer-segmentation-rfm)**: RFM segmentation in SQL

Customer segmentation on Snowflake's TPC-H dataset. Frequency and Monetary correlated at 0.94, making two of the three dimensions largely redundant, so I switched Monetary to average order value. The repo also covers a geographic pattern I had to retract once it turned out to be random variation, and the validation queries that catch each problem.

---

📍 Stockholm · [LinkedIn](https://www.linkedin.com/in/fabioboila) · fabioboila82@gmail.com
