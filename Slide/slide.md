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
    text-transform: uppercase;
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
    font-size: 0.82em;
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
    width: 100%;
    font-size: 0.86em;
    border-collapse: collapse;
    margin-top: 0.5em;
  }
  th {
    background: var(--text);
    color: #ffffff;
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
    gap: 2rem;
    margin-top: 0.4em;
  }
  .columns3 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1.4rem;
    margin-top: 0.4em;
  }
  .col-6-4 {
    display: grid;
    grid-template-columns: 6fr 4fr;
    gap: 2rem;
    margin-top: 0.4em;
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

<div class="columns3">
<div class="box">

## 01
### Architecture
How Snowflake is built internally

</div>
<div class="box">

## 02
### Workflow
How data moves through the platform

</div>
<div class="box">

## 03
### Characteristics
Storage, versioning, concurrency

</div>
</div>

<div class="columns3" style="margin-top: 1.2rem">
<div class="box">

## 04
### Vendor Lock-in
Multi-cloud, but at what cost?

</div>
<div class="box">

## 05
### Cost Scenario
Real numbers for a Swiss SME

</div>
<div class="box">

## 06
### Demo + Recommendations
Live example & when to use it

</div>
</div>

---

# Architecture

<div class="columns">
<div>

## Multi-cluster shared data Architecture 

### Cloud Services
- Query optimization, metadata, auth
- Always on, managed by Snowflake

### Compute (Virtual Warehouses)
- Independent compute clusters
- Scale up/down, pause when idle

### Storage
- Compressed columnar micro-partitions (50–500MB) 
- Decoupled from compute &rarr; pay separately
<br>

## Hybrid Model
### Shared-disk + Shared-nothing + MPP


</div>
<div>

<!-- <img src="imgs/architecture.png" width="100%"> -->
<img src="imgs/archi_multi_cluster.png" width="100%">

> **Key insight:** Scale each side independently &rarr; multiple warehouses can query the same data simultaneously without conflict + no data duplication

</div>
</div>

---

# Storage


<div class="columns">
<div>

## Data Types
- **Structured** → CSV, tables, relational data
- **Semi-structured** → JSON, Avro, Parquet via `VARIANT` type
- **Unstructured** → files (PDF, images) via staged storage — limited query support

<br>

## Micro-partitions
- Auto-split into 50–500MB columnar chunks
- Metadata per partition → partition pruning at query time
- No manual indexing needed

</div>
<div>

<img src="imgs/storage.png" width="100%">

> **Critical:** egress costs apply when extracting data out

</div>
</div>





---

# Workflow

---

# Key Characteristics

---

# Vendor Lock-in

---

# Cost Scenario

---

# Demo

---

# Pros & Cons — Recommendations

---

# References

- https://www.snowflake.com/en/blog/5-reasons-to-love-snowflakes-architecture-for-your-data-warehouse/
