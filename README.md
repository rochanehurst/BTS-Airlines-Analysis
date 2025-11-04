# ✈️ US Airline Performance Analysis (April 2025)

A comprehensive data analysis project examining US domestic flight performance using Bureau of Transportation Statistics (BTS) data. This project explores delay patterns, airline performance metrics, and operational insights across 583,950 flights.

## 📊 Project Overview

This analysis investigates on-time performance across US airlines, examining factors that contribute to delays and identifying patterns in airline operations. The project combines data cleaning, exploratory analysis, and interactive visualizations to provide actionable insights into the aviation industry.

**Key Findings:**
- 19.86% of flights experienced significant delays (>15 minutes)
- Late aircraft delays are the primary cause of disruptions (39.5% of total delay time)
- Friday shows the highest average delays across all airlines
- Significant performance variance exists between carriers (16.32% - 26.91% delay rates)

## 🛠️ Technologies Used

- **Python 3.13**
- **Pandas & NumPy** - Data manipulation and analysis
- **Matplotlib & Seaborn** - Statistical visualizations
- **Folium** - Interactive geospatial mapping
- **Jupyter Notebook** - Interactive development environment

## 📁 Project Structure

```
├── BTS-Airline-DataCleaning.ipynb    # Data preprocessing and cleaning
├── BTS-Airline-EDA.ipynb             # Exploratory data analysis
├── data/
│   ├── T_ONTIME_REPORTING.csv        # Raw BTS dataset
│   ├── bts_airline_clean.csv         # Cleaned dataset
│   └── airports.csv                  # Airport metadata with coordinates
└── README.md
```

## 🔍 Analysis Highlights

### 1. Data Cleaning & Preprocessing
- Handled 583,950 flight records with 21+ features
- Filled missing delay values (carrier, weather, NAS, security, late aircraft)
- Removed 2,512 duplicate records
- Converted date/time fields to appropriate data types
- Created categorical delay classifications (Early, On Time/Minor, Delayed, Severe Delay)
- Standardized column naming conventions to snake_case

### 2. Key Metrics Analyzed

**Delay Categories:**
- **Early:** Arrival < 0 minutes
- **On Time/Minor:** 0-15 minutes late
- **Delayed:** 15-60 minutes late
- **Severe Delay:** >60 minutes late

**Airlines Analyzed:** AA, AS, B6, DL, F9, G4, HA, MQ, NK, OH, OO, UA, WN, YX (14 carriers)

### 3. Major Insights

#### Airline Performance
- **Most Reliable:** YX (16.32% delay rate)
- **Least Reliable:** F9 (26.91% delay rate)
- Median delays range from -8 to -2 minutes across carriers
- Mean delays significantly higher due to extreme outliers

#### Delay Causes Breakdown
| Cause | Avg Contribution |
|-------|------------------|
| Late Aircraft | 39.5% |
| Carrier Issues | 32.8% |
| NAS (Air Traffic) | 22.3% |
| Weather | 5.5% |
| Security | 0.2% |

#### Temporal Patterns
- **Worst Day:** Friday (highest average delays)
- **Best Day:** Saturday (lowest average delays)
- Delays tend to compound throughout the week

#### Airport Performance
- **Top Problem Airports (Origin):** DDC, FAY, HTS showed highest average delays
- **Top Problem Airports (Destination):** FAY, VCT, HOB experienced worst arrival delays
- Interactive heatmap visualization reveals geographic delay hotspots

## 📈 Visualizations

The project includes multiple visualization types:
- Bar charts comparing airline performance metrics
- Distribution plots showing delay patterns
- Box plots revealing delay variability by carrier
- Correlation heatmaps identifying delay factor relationships
- Line graphs tracking weekly delay trends
- Interactive Folium heatmap displaying geographic delay concentrations
- Donut charts breaking down delay cause contributions

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn folium kaggle
```

### Running the Analysis
1. Clone this repository
2. Download the BTS dataset (or use Kaggle API as shown in notebook)
3. Run `BTS-Airline-DataCleaning.ipynb` first
4. Then run `BTS-Airline-EDA.ipynb` for visualizations

### Data Source
Data sourced from the Bureau of Transportation Statistics (BTS) On-Time Performance dataset for April 2025. Airport coordinate data obtained from Kaggle.

## 💡 Key Takeaways for Travelers

Based on this analysis:
- **Choose Saturday flights** for best on-time performance
- **Avoid Fridays** when booking if punctuality is critical
- **YX, B6, and NK** show the most consistent on-time records
- **Late aircraft cascading delays** are the #1 controllable factor
- **Geographic clusters** exist where delays are more common

## 🎯 Skills Demonstrated

- Large-scale data cleaning and preprocessing (500K+ records)
- Exploratory Data Analysis (EDA) best practices
- Statistical analysis and hypothesis testing
- Data visualization and storytelling
- Geospatial data integration and mapping
- Python programming for data science
- Jupyter Notebook documentation

## 📝 Future Enhancements

- [ ] Time series forecasting for delay prediction
- [ ] Machine learning classification model for delay risk
- [ ] Expand analysis to multiple months/years for trend analysis
- [ ] Route-specific delay analysis
- [ ] Weather data integration for deeper weather delay insights
- [ ] Interactive dashboard using Plotly Dash or Streamlit

## 📧 Contact

**Rochane Hurst**

Feel free to reach out if you have questions about this analysis or would like to discuss data science opportunities!

---

*This project demonstrates proficiency in Python, data analysis, statistical visualization, and the ability to extract actionable insights from large datasets.*
