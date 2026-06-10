---
marp: true
theme: default
paginate: true
html: true
header: 'HEIG-VD IST 2025/26 — Snowflake | Group A'
footer: 'Markaj Agron · Jorand Yuuta · Stampfli Nathan · Liao Pei-Wen · 12.06.2026'
size: 16:9
style: |
  @import url('https://fonts.googleapis.com/css2?family=Source+Serif+4:wght@400;600;700;900&family=Source+Code+Pro:wght@400;700&display=swap');

  :root {
    --bg:        #ffffff;
    --bg2:       #f4f4f5;
    --bg3:       #e4e4e7;
    --border:    #d1d5db;
    --blue:      #2563eb;
    --blue-dark: #1e3a8a;
    --teal:      #0891b2;
    --green:     #16a34a;
    --orange:    #ea580c;
    --red:       #dc2626;
    --yellow:    #ca8a04;
    --muted:     #6b7280;
    --text:      #09090b;
    --accent:    #29b6f6;
  }

  /* ── BASE ── */
  section {
    background: var(--bg);
    color: var(--text);
    font-family: 'Source Serif 4', serif;
    font-size: 21px;
    padding: 48px 68px 60px;
    line-height: 1.55;
  }

  /* ── HEADINGS ── */
  h1 {
    font-family: 'Source Serif 4', serif;
    font-size: 1.75em;
    font-weight: 900;
    color: var(--text);
    border-bottom: 3px solid var(--accent);
    padding-bottom: 0.2em;
    margin-top: 0;
    margin-bottom: 0.6em;
    letter-spacing: -0.03em;
    
  }

  h2 {
    font-family: 'Source Serif 4', serif;
    font-size: 0.95em;
    font-weight: 700;
    color: var(--blue);
    margin-bottom: 0.3em;
    margin-top: 0.9em;
    text-transform: uppercase;
    letter-spacing: 0.05em;
  }

  h3 {
    font-family: 'Source Code Pro', monospace;
    font-size: 1.0 em;
    font-weight: 700;
    color: var(--orange);
    margin-bottom: 0.25em;
    margin-top: 0.7em;
  }

  /* ── LISTS ── */
  ul, ol {
    padding-left: 1.4em;
    margin: 0.3em 0;
  }
  li {
    margin-bottom: 0.35em;
    color: var(--text);
  }
  li::marker { color: var(--accent); font-weight: 700; }
  li > ul > li::marker { color: var(--muted); }

  /* ── BLOCKQUOTE ── */
  blockquote {
    background: #e0f4fd;
    border-left: 4px solid var(--accent);
    border-radius: 0 4px 4px 0;
    padding: 0.6em 1em;
    margin: 0.9em 0 0;
    color: var(--blue-dark);
    font-family: 'Source Code Pro', monospace;
    font-size: 0.78em;
    line-height: 1.5;
  }
  blockquote > p { margin: 0; }

  /* ── INLINE CODE ── */
  code {
    background: var(--bg2);
    color: var(--teal);
    font-family: 'Source Code Pro', monospace;
    font-size: 0.8em;
    padding: 1px 6px;
    border-radius: 3px;
    border: 1px solid var(--border);
  }

  /* ── CODE BLOCKS ── */
  pre {
    background: #0f172a !important;
    border: none !important;
    border-left: 4px solid var(--accent) !important;
    border-radius: 4px !important;
    padding: 0.9em 1.1em !important;
    font-size: 0.7em !important;
    margin: 0.6em 0 !important;
  }
  pre code {
    background: transparent !important;
    border: none !important;
    padding: 0 !important;
    color: #e2e8f0 !important;
    font-size: 1em !important;
  }

  /* ── TABLES ── */
  table {
    width: 80%;
    margin: 0 auto;
    margin-top: 0.5em;
    font-size: 0.86em;
    border-collapse: collapse;
  }
  th {
    background: var(--accent);
    color: #040404;
    font-family: 'Source Serif 4', serif;
    font-weight: 700;
    font-size: 0.85em;
    padding: 0.55em 0.9em;
    border: none;
    text-align: left;
    text-transform: uppercase;
    letter-spacing: 0.04em;
  }
  td {
    padding: 0.45em 0.9em;
    border-bottom: 1px solid var(--border);
    color: var(--text);
    vertical-align: top;
    background: var(--bg);
  }
  tr:nth-child(even) td { background: var(--bg2); }
  tr:hover td { background: #e0f4fd; }

  /* ── LAYOUT HELPERS ── */
  .columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 1rem;
    margin-top: 0.4em;
  }
  .columns3 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1.4rem;
    margin-top: 0.4em;
  }

  .columns4 {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 1rem;
  margin-top: 0.4em;
  }

  .col-6-4 {
    display: grid;
    grid-template-columns: 6fr 4fr;
    gap: 2rem;
    margin-top: 0.4em;
  }

  .columns-tight {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.6rem;
  }

  /* ── CARD BOXES ── */
  .box, .box-ok, .box-warn, .box-info {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 4px;
    padding: 0.85em 1em;
    font-size: 0.82em;
    line-height: 1.5;
  }
  .box      { border-left: 4px solid var(--accent); }
  .box-ok   { border-left: 4px solid var(--green); }
  .box-warn { border-left: 4px solid var(--red); }
  .box-info { border-left: 4px solid var(--yellow); }

  /* ── BADGE / TAG ── */
  .tag {
    display: inline-block;
    background: var(--bg3);
    border-radius: 3px;
    font-family: 'Source Code Pro', monospace;
    font-size: 0.68em;
    padding: 2px 8px;
    color: var(--muted);
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin: 0 2px;
  }

  /* ── HEADER / FOOTER ── */
  header {
    font-family: 'Source Code Pro', monospace;
    font-size: 0.46em;
    color: var(--muted);
    border-bottom: 1px solid var(--border);
    padding-bottom: 4px;
    letter-spacing: 0.03em;
  }
  footer {
    font-family: 'Source Code Pro', monospace;
    font-size: 0.46em;
    color: var(--muted);
    border-top: 1px solid var(--border);
    padding-top: 4px;
    letter-spacing: 0.03em;
  }

  /* ── PAGE NUMBER ── */
  section::after {
    font-family: 'Source Code Pro', monospace;
    font-size: 0.46em;
    color: var(--border);
    content: attr(data-marpit-pagination) ' / ' attr(data-marpit-pagination-total);
  }

  /* ── TITLE SLIDE ── */
  section.title {
    background: #77d4ff;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 72px 80px;
    position: relative;
    overflow: hidden;
  }
  section.title::before {
    content: '';
    position: absolute;
    top: 0; left: 0;
    width: 6px; height: 100%;
    background: #0d1b2a;
  }
  section.title::after {
    content: '';
    position: absolute;
    bottom: -60px; right: -60px;
    width: 320px; height: 320px;
    border-radius: 50%;
    border: 40px solid rgba(255, 255, 255, 0.15);
  }
  section.title h1 {
    font-family: 'Source Serif 4', serif;
    font-size: 3.2em;
    font-weight: 900;
    border: none;
    padding: 0;
    margin-bottom: 0.1em;
    color: #0d1b2a;
    letter-spacing: -0.04em;
    text-transform: uppercase;
    line-height: 1.0;
  }
  section.title h2 {
    color: #0f172a;
    font-size: 1em;
    font-weight: 600;
    margin-top: 0;
    margin-bottom: 2.5em;
    text-transform: none;
    letter-spacing: 0;
  }
  section.title h2::before { content: ''; }
  section.title p {
    color: #ffffff;
    font-family: 'Source Code Pro', monospace;
    font-size: 0.70em;
    margin-top: 0;
    border-left: 2px solid #0b5da8;
    padding-left: 1em;
    line-height: 2;
  }
---

<!-- _class: title -->
<!-- _paginate: false -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Snowflake
## Cloud Data Platform for Swiss SMEs

<p>HEIG-VD IST 2025/26<br>Markaj Agron · Jorand Yuuta · Stampfli Nathan · Liao Pei-Wen<br>12.06.2026, 16:30 - 16:42</p>

---

# Agenda

<div class="columns4">

<div class="box">

## 01
### Business Scenario
SwissBike SA challenges

</div>

<div class="box">

## 02
### What is Snowflake?
A quick introduction

</div>

<div class="box">

## 03
### Architecture
How Snowflake is built

</div>

<div class="box">

## 04
### Workflow
How data moves through the platform

</div>

</div>

<div class="columns4" style="margin-top: 1rem">

<div class="box">

## 05
### Characteristics
Storage, scalability & recovery

</div>

<div class="box">

## 06
### Vendor Lock-in
Multi-cloud, but at what cost?

</div>

<div class="box">

## 07
### Cost Scenario
Real numbers for a Swiss SME

</div>

<div class="box">

## 08
### Demo
SwissBike SA use case

</div>

</div>

<div class="columns4" style="margin-top: 1rem">

<div class="box">

## 09
### Pros & Cons
Strengths and limitations

</div>

<div class="box">

## 10
### Recommendation
When should a SME use Snowflake?

</div>

<div></div>
<div></div>

</div>

---

# Scenario / Challenges

<div class="columns-tight">

<div>

## SwissBike SA

SwissBike SA is a Swiss SME selling bicycles and accessories online:

- **~50 employees**, IT handled by generalists
- **~1,500 orders/month**
- currently **10 analytics users**
- Collect data **across disconnected systems**( E-commerce, ERP, CRM and Marketing tools)


</div>

<div>

## Challenges

- **No dedicated data engineer**
- Data is scattered across **multiple systems**
- Analytics rely on **manual Excel** exports
- **More users** need access to analytics
- **Growing data volume** with no scalable storage strategy
- **Budget** constraints

</div>

</div>

<div class="box-info">

### Key Question

How can SwissBike **centralize** its data, **scale** analytics and stay within **budget** **without a dedicated data team** ? 

</div>

---

# What Does Snowflake Solve?

<style scoped>
th { background: var(--accent); color: #0d1b2a; }
.table-center { display: flex; justify-content: center; }
.table-center table { width: 90%; margin-top: 0.5em; }

</style>

<div class="table-center">

| SME Pain Point | Snowflake Solution | Covered In |
|----------------|-------------------|------------|
| User increase | Add Virtual Warehouses without touching storage | Architecture |
| No data engineer | No infra to maintain| Architecture |
| Data volume growing, query speed slower | Storage layer scales independently + Micro-partitions + pruning skip irrelevant data | Architecture + Storage |
| Milti disconnected systems, no single source of truth | Snowpipe centralizes all sources | Workflow + Vendor lockin|
| Manual CSV exports, reports 1 week stale | Automated ingestion, always up to date | Workflow + + Vendor lockin|
| Budget sensitive | Pay only when warehouse is running | Cost Scenario |

</div>

<br>

<div class="box-info">

### Bottom Line

Snowflake is not the cheapest option but for a Swiss SME outgrowing Excel, it **removes the need for a data engineering team entirely**.

</div>

---

# Architecture : Independent Scaling & Query Performance

<div class="columns">
<div>

###  Hybrid Model = Shared-disk + Shared-nothing + MPP

## Cloud Services
- Always on, managed by Snowflake (Query opt, metadata, auth)
- **Free** under 10% of daily compute usage

## Compute (Virtual Warehouses)
- 24h query result **cache** &rarr; free repeated queries 
- **Auto scale** up/down, pause when idle
- Trade off : Cold start 2-3s

## Storage
- Decoupled from compute &rarr; pay separately
- Trade off : **Egress costs** when different regions
<br>


</div>
<div>

<!-- <img src="imgs/architecture.png" width="100%"> -->
<img src="imgs/archi_multi_cluster.png" width="90%">

### Key insight:
Scale independently + Query without conflict, no duplication

### Trade off:
Layer separation adds overhead for small frequent transactions (`INSERT`, `UPDATE` slower than PostgreSQL)
</div>
</div>

---
# Storage: Columnar, Partitioned & Protected

<div class="columns">
<div>

## Data Types
- **Structured** + **Semi-structured** 
- **Unstructured** → PDF, images via staged storage — limited query support

## Micro-partitions
- Auto-split into **columnar chunks** (50–500MB)
- Metadata per partition &rarr; **pruning skips irrelevant data at query time**
- **Clustering keys** — optional, co-locates frequent query columns for large tables

## Data Protection
- **Time Travel** — query or restore data up to 90 days
- **Fail-safe** — 7-day recovery after Time Travel expires, managed by Snowflake

</div>
<div>

<img src="imgs/storage.png" width="80%">


### Key Advantage
- Mainain query speed as data grow &rarr; prune+cluster 
- Storage cost stays low &rarr; columnar compression


### Trade-off
Egress costs apply when extracting data out &rarr; keep compute and storage in same region


</div>
</div>

---

# Workflow

*SwissBike SA centralizes data from multiple business systems into Snowflake to generate business insights.*

<div class="columns-tight">

<div>

## Data Sources

- E-commerce platform
- ERP system
- CRM system
- Marketing tools
- CSV / API imports

<br>

## Data Ingestion

- Batch imports
- Connectors
- External stages
- Semi-structured formats (JSON, Parquet)

</div>

<div>

## Snowflake Processing

- Centralized storage
- Automatic compression
- Micro-partitioning
- Query optimization
- MPP execution via Virtual Warehouses

<br>

## Outputs

- SQL analytics
- Dashboards (Power BI, Tableau)
- Reports
- Machine learning datasets

</div>

</div>


---
# Vendor Lock-in: Multi-cloud, But At What Cost?



<div class="columns">
<div>

## Portable
- Runs on AWS, Azure, GCP : no vendor dependency
- Standard ANSI SQL : queries portable 
- Open ingestion formats — Parquet, JSON, CSV


<style scoped>
th { background: var(--accent); color: #0d1b2a; }
table { font-size: 0.72em; width: 95%; }
td, th { padding: 0.3em 0.6em; }
</style>
## Proprietary Features
| Feature | Lock-in Risk | Mitigation |
|---------|-------------|------------|
| Time Travel | no equivalent elsewhere | Use for recovery only |
| Zero-Copy Clone | proprietary syntax | Document dependencies |
| Data Sharing | partner Snowflake account | Export via open formats |
| Snowpipe | proprietary ingestion | Replace with Airbyte or `COPY INTO` |

</div>
<div>

## Migration Cost If You Leave

- Rebuild all ingestion pipelines
- Recreate security policies & role hierarchy
- Re-implement Time Travel logic elsewhere
- Export all data — **egress costs apply**

<div class="box-warn">

### Real Risk for SME
No data engineer :  proprietary features get adopted without governance, migration cost grows silently over time.

</div>

<div class="box-info">

### Mitigation Strategy
Prefer ANSI SQL + open formats where possible. Use Snowflake-specific features consciously, not by default.

</div>

</div>
</div>

---
# Cost Scenario: SwissBike SA


<div class="columns">
<div>

<style scoped>
th { background: var(--accent); color: #0d1b2a; }
table { font-size: 0.72em; width: 95%; }
td, th { padding: 0.3em 0.6em; }
</style>

## SwissBike Assumptions
- 500 GB stored data
- 1 X-Small Warehouse, Standard edition
- 10h/week warehouse usage
- Region: AWS EU Zurich (**Swiss nDSG**)
- Snowflake CoWork enabled

## How Snowflake Charges

| Layer | Unit | When Charged | EU Zurich |
|-------|------|-------------|-----------|
| Cloud Services | Credits | Free under 10% of compute | ~$0 for SME |
| Compute | Credits/second | Warehouse running only | $3.10/credit |
| Storage | GB/month | Always, 24/7 | $26.95/TB |


</div>

<div>

## Calculation
`10h/week × 4.3 weeks × 1 credit/h × $3.10 = $133/month`
`0.5 TB × $26.95 = $13.48/month`


| Component | Monthly Cost |
|------------|-------------:|
| Compute (XS Warehouse) | $133.30 |
| Snowflake CoWork | $123.08 |
| Snowflake Cortex AI | $5.78 |
| Storage (500 GB, EU Zurich) | $13.48 |
| **Total** | **$275.64** |


<div class="box">

### Cost Observations
- CoWork + Cortex AI = **$128/month — 46% of total bill**
- Storage is cheap, compute dominates
- Without auto-suspend: 24/7 running (40h/week)= ~$520/month instead of $133/month


</div>

</div>
</div>

---

# Demo

---

# Pros & Cons

<div class="columns">

<div>

<div class="box-ok">

## Pros

- High scalability
- MPP architecture
- Excellent concurrency
- Minimal administration
- Strong security
- Time Travel & Fail-safe
- Zero-Copy Clone
- Multi-cloud support

</div>

</div>

<div>

<div class="box-warn">

## Cons

- Consumption-based pricing
- Cost monitoring required
- Vendor lock-in
- Cloud dependency
- Not optimized for OLTP
- Learning curve

</div>

</div>

</div>

> Snowflake offers strong analytical capabilities and scalability, but requires active cost management and acceptance of some vendor dependency.

---

# Recommendation

<div class="columns">

<div>

## Recommended For

✓ SMEs needing centralized analytics

✓ Companies expecting significant data growth

✓ Organizations with multiple teams accessing data

✓ Businesses seeking low operational overhead

</div>

<div>

## Not Recommended For

✗ Small transactional applications (OLTP)

✗ Organizations requiring full infrastructure control

✗ Businesses with very limited cloud adoption

</div>

</div>

<div class="box-info" style="margin-top:1rem;">

### Final Assessment

Snowflake is an excellent analytical platform for growing SMEs.

Its strongest advantages are scalability, MPP processing, concurrency and operational simplicity.

However, organizations should carefully monitor costs and consider the long-term impact of vendor lock-in.

</div>

---

# References

- https://www.snowflake.com/en/blog/5-reasons-to-love-snowflakes-architecture-for-your-data-warehouse/
