# Awesome-Cloud-Big-Data-Platform

# Awesome-Cloud-Big-Data-Platform

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Managed Spark/Hadoop, Data Lakehouses, Query Engines & Batch/Stream Processing*  
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Big Data Platforms**. These tools help organizations process, analyze, and derive insights from massive datasets using distributed computing frameworks like Apache Spark, Hadoop, Flink, and Trino.

**Examples** include Azure HDInsight, Amazon EMR, Google Cloud Dataproc, Cloudera Data Platform, Qubole, Databricks, Ahana Cloud, Treasure Data, Upsolver, and Starburst (the category leaders).

**Open-source emphasis**: Cloud big data has one of the **most mature open-source ecosystems in data engineering**. **Apache Spark** remains the de facto standard for distributed data processing, while **Apache Flink** leads in true stream processing. **Trino** (formerly PrestoSQL) powers federated SQL queries across disparate sources, with **Starburst** commercializing it. **Apache Iceberg** has emerged as the open table format standard, and **Delta Lake** provides ACID transactions on data lakes. This section documents these production-grade solutions.

Contributions welcome! Open an Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## 📖 Table of Contents

- [☁️ SaaS/Hosted Platforms](#-saas-hosted-platforms)
- [🔓 Open-Source GitHub Projects](#-open-source-github-projects)
- [🤝 How to Contribute](#-how-to-contribute)
- [⚠️ Disclaimer](#-disclaimer)

## ☁️ SaaS/Hosted Platforms

> **📊 Market Context**: The global big data analytics market is estimated at **~$348B in 2026**, growing toward **~$924B by 2032** at a **~17.8% CAGR** (Fortune Business Insights / MarketsandMarkets estimates). The sector is **moderately concentrated** at the platform tier — **Databricks** dominates with **$7B+ annualized revenue** and a **$190B valuation** , while **Cloudera** holds a substantial enterprise installed base . Hyperscalers (AWS, Azure, GCP) compete on managed services, and a fragmented mid-market of specialized platforms (Starburst, Qubole, Upsolver) serves niche workloads. No single vendor holds a winner-take-all position; enterprise buyers typically run multi-platform stacks for different workloads.

| Platform | Description | Pricing (Starting Tier) | Free Tier Limits | Company Size |
|----------|-------------|------------------------|------------------|--------------|
| **[Databricks](https://www.databricks.com/)** | Unified lakehouse platform built on Apache Spark. Original creators of Spark. SQL Serverless, ML, and data engineering workloads. | **SQL Serverless**: **$0.70/DBU** (includes cloud instance cost); **SQL Classic**: **$0.55/DBU**; **SQL Pro**: **$0.22/DBU** . **All-Purpose Compute**: From ~$0.40/DBU. | **14-day free trial** with full platform access. No perpetual free tier . | **$7B+ annualized revenue, $190B valuation, $5B raised (2026)**  |
| **[Cloudera Data Platform](https://www.cloudera.com/)** | Enterprise data platform for hybrid cloud. Data Engineering, Data Warehouse, AI, and Operational Database services. | **Data Hub**: **$0.04/CCU** (Cloudera Compute Unit); **Data Engineering Core**: **$0.07/CCU**; **AI Workbench**: **$0.20/CCU**; **AI Inference**: **$0.25/CCU**; **Data Flow**: **$0.30/CCU** + **$0.10/invocation** . Infrastructure costs billed separately by cloud provider. | **None** — enterprise sales engagement required. No public free tier . | **Private (CDP), FY2026 record revenue, ARR growing, 50%+ new customer growth YoY**  |
| **[Starburst](https://www.starburst.io/)** | Enterprise Trino platform for federated data access. Query data across lakes, warehouses, and databases without moving it. | **Free**: $0 (3 clusters); **Pro**: **$0.50/credit**; **Enterprise**: **$0.75/credit**; **Mission-Critical**: **$1.00/credit** . | **Free forever**: Up to **3 clusters**, standard execution mode for ad hoc queries . **30-day free trial**: $500 in Starburst Galaxy compute credits, access to Enterprise features . | **$100M+ ARR (2025), ~40% YoY growth, $20M AI ARR**  |
| **[Google Cloud Dataproc](https://cloud.google.com/dataproc)** | Managed Spark and Hadoop service on Google Cloud. Batch processing, querying, streaming, and ML. | **$0.01/vCPU/hour** (Dataproc service fee) on top of underlying GCE resources . **Preemptible instances** available for lower compute costs. | **$300 Google Cloud free credits** for new accounts (90 days). No perpetual free tier for Dataproc. | **~$350B revenue (Alphabet FY2025)** |
| **[Azure HDInsight](https://azure.microsoft.com/en-us/products/hdinsight/)** | Managed cloud service for open-source analytics frameworks. Hadoop, Spark, Kafka, HBase, Storm, and Interactive Query. | **Base price/node-hour** + **¥0/core-hour** (standard); **Enterprise Security Package**: +**¥0.06/core-hour** . **F1 compute node**: ~**¥0.531/hour** (~$0.075/hour) . | **30-day free trial** of Defender for Cloud (not HDInsight itself). No perpetual free tier. | **~$281B revenue (Microsoft FY2025)** |
| **[Amazon EMR](https://aws.amazon.com/emr/)** | Managed Hadoop, Spark, Hive, Presto, and Flink service on AWS. | **EMR service fee**: **$0.015/hour per instance** (standard); **$0.030/hour per instance** (EMR Studio). **EC2 instance costs billed separately**. **Spot instances** can save **up to 90%** vs on-demand . | **AWS Free Tier**: 100 GB warm storage free for **12 months** (new accounts). No perpetual free tier for EMR. | **~$638B revenue (Amazon FY2025)** |
| **[Qubole](https://www.qubole.com/)** | Open, simple, and secure data lake platform. Workload-aware autoscaling and Spot management. | **On-Demand**: **$0.24/QCU/hour** + **$108/user/month**; **Enterprise Edition**: **$0.168/QCU/hour** (annual contract, excludes user fees) . | **30-day full-featured free trial**; **Business Edition**: Free with **30,000 QCPU/month limit** (worth ~$1,000) . | **Private (~$100M+ raised, acquired by Idera)** |
| **[Upsolver](https://www.upsolver.com/)** | Real-time data ingestion and Iceberg optimization. Consumption-based pricing. | **Consumption-based pricing** — charged by **data volume** (not active rows like Fivetran). Order-of-magnitude savings at scale . | **Free trial available** — details require sales contact. | **Private, acquired by Qlik (2024)** |
| **[Treasure Data](https://www.treasuredata.com/)** | AI-native CDP with decoupled pricing (profiles + behaviors, not compute). | **Annual Intelligent CDP subscription** based on **customer profiles and behavioral events** — not compute . **Trade-Up program**: Switch from incumbent CDP and pay after contract ends; replace ESP/CEP for **up to 24 months free** . | **None** — enterprise sales required. | **Private (~$230M+ raised)** |
| **[Ahana Cloud](https://ahana.io/)** | Managed Presto/Trino service for AWS. Now part of IBM. | **Ahana Cloud Credit Usage Fee** per hour as outlined in AWS Marketplace Subscription Listing . | **Free trial available** via AWS Marketplace. | **Private (acquired by IBM, 2023)** |

## 🔓 Open-Source GitHub Projects

Sorted by star count (descending). Star badge links to each repo's stargazers page.

| Repo | Description | Stars |
|---|---|---|
| **[Apache Spark](https://github.com/apache/spark)** — Unified analytics engine for large-scale data processing. Batch, streaming, SQL, ML, and graph processing. The de facto standard for distributed data processing. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/spark?style=social&color=white)](https://github.com/apache/spark/stargazers) | ~42,000 |
| **[Apache Flink](https://github.com/apache/flink)** — Stateful computations over unbounded and bounded data streams. True event-at-a-time stream processing with exactly-once semantics. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/flink?style=social&color=white)](https://github.com/apache/flink/stargazers) | ~25,000 |
| **[Trino](https://github.com/trinodb/trino)** — Distributed SQL query engine for big data. Federated queries across data lakes, warehouses, and databases. Apache-2.0. Powers Starburst. | [![Stars](https://img.shields.io/github/stars/trinodb/trino?style=social&color=white)](https://github.com/trinodb/trino/stargazers) | ~11,500 |
| **[Apache Iceberg](https://github.com/apache/iceberg)** — Open table format for huge analytic datasets. ACID transactions, schema evolution, time travel. The emerging standard for lakehouse tables. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/iceberg?style=social&color=white)](https://github.com/apache/iceberg/stargazers) | ~7,500 |
| **[Delta Lake](https://github.com/delta-io/delta)** — Storage framework bringing ACID transactions to Apache Spark and big data workloads. Originally from Databricks. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/delta-io/delta?style=social&color=white)](https://github.com/delta-io/delta/stargazers) | ~8,000 |
| **[Apache Hadoop](https://github.com/apache/hadoop)** — Distributed processing of large data sets across clusters. HDFS, MapReduce, YARN. The original big data platform. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/hadoop?style=social&color=white)](https://github.com/apache/hadoop/stargazers) | ~15,000 |
| **[Apache Hudi](https://github.com/apache/hudi)** — Upserts, deletes, and incremental data processing on data lakes. Streaming ingestion and near-real-time analytics. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/hudi?style=social&color=white)](https://github.com/apache/hudi/stargazers) | ~5,800 |
| **[Apache Storm](https://github.com/apache/storm)** — Free, open-source, distributed real-time computation system. Processes unbounded streams at high velocity (1M+ tuples/sec/node). Apache-2.0 . | [![Stars](https://img.shields.io/github/stars/apache/storm?style=social&color=white)](https://github.com/apache/storm/stargazers) | ~6,800 |
| **[Apache Beam](https://github.com/apache/beam)** — Unified programming model for batch and streaming data processing pipelines. Runs on Spark, Flink, and Google Cloud Dataflow. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/beam?style=social&color=white)](https://github.com/apache/beam/stargazers) | ~8,500 |
| **[DuckDB](https://github.com/duckdb/duckdb)** — In-process analytical database. Fast OLAP queries on local files (Parquet, CSV, JSON). The "SQLite for analytics." MIT. | [![Stars](https://img.shields.io/github/stars/duckdb/duckdb?style=social&color=white)](https://github.com/duckdb/duckdb/stargazers) | ~25,000 |
| **[Apache Doris](https://github.com/apache/doris)** — MPP-based interactive SQL data warehousing for reporting and analysis. Real-time analytics on massive data. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/doris?style=social&color=white)](https://github.com/apache/doris/stargazers) | ~13,500 |
| **[StarRocks](https://github.com/StarRocks/starrocks)** — Next-generation data platform for sub-second analytics. MPP database with vectorized execution. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/StarRocks/starrocks?style=social&color=white)](https://github.com/StarRocks/starrocks/stargazers) | ~10,000 |
| **[Presto (prestodb)](https://github.com/prestodb/presto)** — Distributed SQL query engine for big data. Original Presto fork maintained by Facebook. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/prestodb/presto?style=social&color=white)](https://github.com/prestodb/presto/stargazers) | ~16,000 |

**Additional open-source options worth exploring:**

| Repo | Description |
|---|---|
| **[Apache Kylin](https://github.com/apache/kylin)** — Extreme OLAP engine for big data. Pre-computed cubes for sub-second queries on Hadoop. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/kylin?style=social&color=white)](https://github.com/apache/kylin/stargazers) |
| **[Apache Druid](https://github.com/apache/druid)** — Real-time analytics database for fast queries on event-driven data. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/druid?style=social&color=white)](https://github.com/apache/druid/stargazers) |
| **[Apache Pinot](https://github.com/apache/pinot)** — Real-time distributed OLAP datastore for user-facing analytics. Apache-2.0. | [![Stars](https://img.shields.io/github/stars/apache/pinot?style=social&color=white)](https://github.com/apache/pinot/stargazers) |

## 🤝 How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## ⚠️ Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud big data platforms handle potentially sensitive organizational data; ensure compliance with data protection regulations and internal security policies.
- **Open-source reality**: Cloud big data has one of the **most mature open-source ecosystems in data engineering**. **Apache Spark** remains the de facto standard for distributed data processing, **Apache Flink** leads in true stream processing, and **Trino** powers federated SQL queries across disparate sources. **Apache Iceberg** and **Delta Lake** have emerged as the open table format standards for lakehouses. However, **commercial platforms** (Databricks, Cloudera, Starburst) provide **managed infrastructure, enterprise SLAs, and unified governance** that open-source alternatives require significant operational investment to match. The open-source path is **genuinely viable** for organizations with strong data platform engineering capacity.
- **Pricing caveat**: All pricing figures above are **verified against cited search results** but may change without notice. Cloud infrastructure costs (compute, storage, networking) are typically billed separately and vary by region, instance type, and commitment level. Always request a formal quote for accurate budgeting.

---

**Made for data engineers, analytics engineers, platform teams, and data architects.**
Let's make cloud big data more open, scalable, and accessible.
