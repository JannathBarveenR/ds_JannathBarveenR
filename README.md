# Crypto Trading & Market Sentiment Analysis — Data Science Assignment

**Jannath Barveen R**

## Project Folder
`ds_JannathBarveenR`

---

##  Project Structure
```
ds_JannathBarveenR/
│
├── csv_files/
│   ├── historical_data.csv
│   ├── fear_greed_index.csv
│   ├── merged_data.csv
│   ├── daily_summary.csv
│   └── sentiment_trend.csv
│
└── outputs/
    ├── leverage_by_sentiment.png
    ├── daily_trade_value_vs_sentiment.png
    └── sentiment_trend_chart.png
```

---

##  Objective
This project analyzes cryptocurrency trading activity together with global market sentiment (Fear & Greed Index).  
The goal is to understand whether trader behavior changes depending on market sentiment.

---

##  Input Files
| File | Description |
|------|-------------|
| `historical_data.csv` | Actual trade-level crypto trading data |
| `fear_greed_index.csv` | Global market sentiment index |

---

##  Data Processing Steps

### **1 Preprocessing**
- Converted timestamps  
- Extracted clean date format  
- Standardized sentiment dataset dates  
- Cleaned column names  
- Ensured both datasets use the same `date`

### **2 Merging Datasets**
Merged both datasets using:

```python
merged_df = pd.merge(trader_df, sentiment_df, on="date", how="left")
```

This produced the master file: **merged_data.csv**

---

##  Generated Output Files

### **merged_data.csv**
Combined trading + sentiment dataset.

### **daily_summary.csv**
Contains:
- average execution price  
- total trade value  
- total trades  
- average sentiment value  
- sentiment label  

### ** sentiment_trend.csv**
Contains:
- sentiment value  
- sentiment classification  
- 7‑day Moving Average (SMA7)  

---

##  Visualizations
Saved in `/outputs/` folder:
- leverage_by_sentiment.png  
- daily_trade_value_vs_sentiment.png  
- sentiment_trend_chart.png  

---

##  Key Insights (Examples)
- Trading activity tends to increase during **Fear** phases.  
- Sentiment SMA7 shows clear long‑term market mood patterns.  
- High-value trades are more frequent in **neutral-to-fear** zones.  

---

##  How to Run the Project
1. Upload both input CSV files  
2. Run preprocessing  
3. Merge datasets  
4. Generate summary files  
5. Generate charts  

All outputs will automatically be created inside:

```
ds_JannathBarveenR/csv_files/
ds_JannathBarveenR/outputs/
```

---

##  Conclusion
This assignment showcases:
- Data cleaning  
- Feature engineering  
- Time series analysis  
- Merging multiple datasets  
- Visualizing trends  
- Generating organized project output files  
