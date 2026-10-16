# India-Stocks-961-990-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 961 to 990)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-961-990-Historical-Data/
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

## 📦 Constituents (961 to 990)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 961 | `DHAMPURSUG` | Dhampur Sugar Mills Limited | `DHAMPURSUG.NS` |
| 962 | `DHANBANK` | Dhanlaxmi Bank Limited | `DHANBANK.NS` |
| 963 | `DHANUKA` | Dhanuka Agritech Limited | `DHANUKA.NS` |
| 964 | `DHARAN` | DHARAN INFRA-EPC LIMITED | `DHARAN.NS` |
| 965 | `DHARMAJ` | Dharmaj Crop Guard Limited | `DHARMAJ.NS` |
| 966 | `DHATRE` | Dhatre Udyog Limited | `DHATRE.NS` |
| 967 | `DHOOTTRANS` | Dhoot Transmission Limited | `DHOOTTRANS.NS` |
| 968 | `DHRUV` | Dhruv Consultancy Services Limited | `DHRUV.NS` |
| 969 | `DHUNINV` | Dhunseri Investments Limited | `DHUNINV.NS` |
| 970 | `DIACABS` | Diamond Power Infrastructure Limited | `DIACABS.NS` |
| 971 | `DIAMINESQ` | Diamines & Chemicals Limited | `DIAMINESQ.NS` |
| 972 | `DIAMONDYD` | Prataap Snacks Limited | `DIAMONDYD.NS` |
| 973 | `DICIND` | DIC India Limited | `DICIND.NS` |
| 974 | `DIFFNKG` | Diffusion Engineers Limited | `DIFFNKG.NS` |
| 975 | `DIGIDRIVE` | Digidrive Distributors Limited | `DIGIDRIVE.NS` |
| 976 | `DIGISPICE` | DiGiSPICE Technologies Limited | `DIGISPICE.NS` |
| 977 | `DIGITIDE` | Digitide Solutions Limited | `DIGITIDE.NS` |
| 978 | `DIGJAMLMTD` | Digjam Limited | `DIGJAMLMTD.NS` |
| 979 | `DISAQ` | Disa India Limited | `DISAQ.NS` |
| 980 | `DISHTV` | Dish TV India Limited | `DISHTV.NS` |
| 981 | `DIVGIITTS` | Divgi Torqtransfer Systems Limited | `DIVGIITTS.NS` |
| 982 | `DJML` | DJ Mediaprint & Logistics Limited | `DJML.NS` |
| 983 | `DLINKINDIA` | D-Link (India) Limited | `DLINKINDIA.NS` |
| 984 | `DMCC` | DMCC SPECIALITY CHEMICALS LIMITED | `DMCC.NS` |
| 985 | `DNAMEDIA` | Diligent Media Corporation Limited | `DNAMEDIA.NS` |
| 986 | `DODLA` | Dodla Dairy Limited | `DODLA.NS` |
| 987 | `DOLATALGO` | Dolat Algotech Limited | `DOLATALGO.NS` |
| 988 | `DOLLAR` | Dollar Industries Limited | `DOLLAR.NS` |
| 989 | `DOLLEX` | Dollex Agrotech Limited | `DOLLEX.NS` |
| 990 | `DOLPHIN` | Dolphin Offshore Enterprises (India) Limited | `DOLPHIN.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream DHAMPURSUG 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-961-990-Historical-Data/main/DHAMPURSUG/1m/2026/10/DHAMPURSUG_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
