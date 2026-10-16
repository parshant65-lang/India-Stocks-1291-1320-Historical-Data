# India-Stocks-1291-1320-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 1291 to 1320)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-1291-1320-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (1291 to 1320)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 1291 | `ICEMAKE` | Ice Make Refrigeration Limited | `ICEMAKE.NS` |
| 1292 | `ICIL` | Indo Count Industries Limited | `ICIL.NS` |
| 1293 | `ICRA` | ICRA Limited | `ICRA.NS` |
| 1294 | `IDEAFORGE` | Ideaforge Technology Limited | `IDEAFORGE.NS` |
| 1295 | `IFBAGRO` | IFB Agro Industries Limited | `IFBAGRO.NS` |
| 1296 | `IFBIND` | IFB Industries Limited | `IFBIND.NS` |
| 1297 | `IFGLEXPOR` | IFGL Refractories Limited | `IFGLEXPOR.NS` |
| 1298 | `IGARASHI` | Igarashi Motors India Limited | `IGARASHI.NS` |
| 1299 | `IGCL` | Indogulf Cropsciences Limited | `IGCL.NS` |
| 1300 | `IGPL` | IG Petrochemicals Limited | `IGPL.NS` |
| 1301 | `IIFLCAPS` | IIFL Capital Services Limited | `IIFLCAPS.NS` |
| 1302 | `IITL` | Industrial Investment Trust Limited | `IITL.NS` |
| 1303 | `IKIO` | IKIO Technologies Limited | `IKIO.NS` |
| 1304 | `IL&FSENGG` | IL&FS Engineering and Construction Company Limited | `IL&FSENGG.NS` |
| 1305 | `IL&FSTRANS` | IL&FS Transportation Networks Limited | `IL&FSTRANS.NS` |
| 1306 | `IMAGICAA` | Imagicaaworld Entertainment Limited | `IMAGICAA.NS` |
| 1307 | `IMFA` | Indian Metals & Ferro Alloys Limited | `IMFA.NS` |
| 1308 | `IMPAL` | India Motor Parts and Accessories Limited | `IMPAL.NS` |
| 1309 | `INA` | Insolation Energy Limited | `INA.NS` |
| 1310 | `INCREDIBLE` | INCREDIBLE INDUSTRIES LIMITED | `INCREDIBLE.NS` |
| 1311 | `INDBANK` | Indbank Merchant Banking Services Limited | `INDBANK.NS` |
| 1312 | `INDGN` | Indegene Limited | `INDGN.NS` |
| 1313 | `INDIAGLYCO` | India Glycols Limited | `INDIAGLYCO.NS` |
| 1314 | `INDIANCARD` | Indian Card Clothing Company Limited | `INDIANCARD.NS` |
| 1315 | `INDIANHUME` | Indian Hume Pipe Company Limited | `INDIANHUME.NS` |
| 1316 | `INDIASHLTR` | India Shelter Finance Corporation Limited | `INDIASHLTR.NS` |
| 1317 | `INDIGOPNTS` | Indigo Paints Limited | `INDIGOPNTS.NS` |
| 1318 | `INDIQUBE` | Indiqube Spaces Limited | `INDIQUBE.NS` |
| 1319 | `INDNIPPON` | India Nippon Electricals Limited | `INDNIPPON.NS` |
| 1320 | `INDOAMIN` | Indo Amines Limited | `INDOAMIN.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream ICEMAKE 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-1291-1320-Historical-Data/main/ICEMAKE/1m/2026/10/ICEMAKE_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
