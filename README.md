# 🌾  Seasonal-Agriculture-Performance-Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA) and Statistical Analysis** on farm-level agricultural data.

The dataset contains **4,000 farm records** covering different crops, states, districts, and seasons. The analysis focuses on understanding patterns associated with:

- 🌱 Crop Yield
- 💰 Revenue and Profitability
- 💧 Water Usage and Water Efficiency
- 🌦️ Environmental Conditions
- 🧪 Resource Usage
- 🐛 Disease and Pest Risk

The project uses Python-based data analysis and statistical techniques to identify meaningful patterns and compare agricultural performance across crops, seasons, and states.

---

## 🎯 Objectives

The main objectives of this project are:

1. Understand the structure and quality of the agricultural dataset.
2. Clean and validate the data.
3. Analyze agricultural performance across different seasons.
4. Compare crop performance across seasons.
5. Compare state-level performance across seasons.
6. Identify profitable crop-season combinations.
7. Analyze water usage and water efficiency.
8. Study relationships between agricultural variables using correlation analysis.
9. Apply statistical tests to determine whether differences between groups are significant.
10. Generate insights that can support agricultural decision-making.

---

## 📊 Dataset

The dataset contains **4,000 records and 28 variables**.

### Dataset Dimensions

- **Rows:** 4,000
- **Columns:** 28
- **States:** 8
- **Districts:** 10
- **Crops:** 8
- **Seasons:** 3
- **Irrigation Methods:** 4

### Crops

- Wheat
- Maize
- Pulses
- Rice
- Cotton
- Chilli
- Groundnut
- Sugarcane

### Seasons

- Kharif
- Rabi
- Zaid

### States

- Andhra Pradesh
- Maharashtra
- Telangana
- Karnataka
- Gujarat
- Tamil Nadu
- Punjab
- Madhya Pradesh

---

## 🗂️ Important Variables

| Variable | Description |
|---|---|
| `Farm_ID` | Unique farm identifier |
| `State` | State where the farm is located |
| `District` | District where the farm is located |
| `Crop` | Crop cultivated |
| `Season` | Agricultural season |
| `Farm_Area_Hectares` | Farm area in hectares |
| `Rainfall_mm` | Rainfall received |
| `Avg_Temperature_C` | Average temperature |
| `Humidity_pct` | Relative humidity |
| `Sunlight_Hours_Day` | Average daily sunlight |
| `Soil_pH` | Soil pH |
| `Soil_Moisture_pct` | Soil moisture percentage |
| `Nitrogen_kg_ha` | Nitrogen usage |
| `Phosphorus_kg_ha` | Phosphorus usage |
| `Potassium_kg_ha` | Potassium usage |
| `Irrigation_Method` | Irrigation method used |
| `Fertilizer_kg_ha` | Fertilizer usage |
| `Pesticide_Litre_ha` | Pesticide usage |
| `Seed_Quality_Score` | Seed quality score |
| `Yield_Tonnes_Ha` | Crop yield per hectare |
| `Production_Tonnes` | Total production |
| `Market_Price_INR_Tonne` | Market price |
| `Total_Cost_INR` | Total production cost |
| `Revenue_INR` | Total revenue |
| `Profit_INR` | Total profit |
| `Water_Used_m3` | Water consumed |
| `Water_Efficiency_t_per_1000m3` | Yield per 1,000 m³ of water |
| `Disease_Pest_Risk_pct` | Disease/pest risk percentage |

---

# 🔎 Analysis Performed

## 1. Data Understanding

The dataset was inspected to understand:

- Dataset dimensions
- Column names
- Data types
- Numerical variables
- Categorical variables
- Unique values
- Basic statistical properties

---

## 2. Data Cleaning

The following data-quality checks were performed:

- Missing-value detection
- Missing-value treatment
- Duplicate row detection
- Duplicate `Farm_ID` detection
- Numerical range validation
- Financial consistency validation
- Production consistency validation

### Missing Values

Initially, missing values were found in:

- `Rainfall_mm`
- `Soil_Moisture_pct`
- `Yield_Tonnes_Ha`

After cleaning, the final dataset contained **no missing values**.

There were also:

- No duplicate rows
- No duplicate Farm IDs
- No invalid values in the checked ranges

---

# 📈 Exploratory Data Analysis

The project analyzes agricultural performance from multiple perspectives.

### Season-wise Analysis

The following metrics were compared across Kharif, Rabi, and Zaid:

- Yield
- Production
- Revenue
- Cost
- Profit
- Water usage
- Water efficiency
- Disease/pest risk
- Environmental conditions
- Resource usage

### Crop-wise Analysis

Crop-level performance was analyzed using:

- Average yield
- Revenue
- Profit
- Water efficiency
- Seasonal performance

### State-wise Analysis

States were compared based on:

- Yield
- Profit
- Revenue
- Water efficiency
- Seasonal performance
- Disease/pest risk

---

# 🌱 Crop × Season Analysis

A detailed comparison was performed between crops and seasons.

This analysis identifies:

- Best season for each crop
- Highest-yielding crop in each season
- Most profitable crop-season combination
- Lowest-performing crop-season combination
- Water-efficient crop-season combinations
- Revenue differences between crop-season combinations

### Key Findings

- **Kharif produced the highest average yield for every crop.**
- **Sugarcane had the highest average yield across seasons.**
- **Sugarcane + Kharif** had the highest average yield: **53.46 tonnes/ha**.
- **Sugarcane + Kharif** had the highest average profit: **₹1,000,790.81**.
- **Sugarcane + Kharif** also had the highest water efficiency: **36.00 tonnes/1,000 m³**.
- **Rice + Zaid** had the lowest average profit: **-₹227,239.34**.

---

# 🗺️ State × Season Analysis

State and season interactions were analyzed to identify regional differences.

The analysis determines:

- Best season by yield for each state
- Best season by profit for each state
- Best-performing state in each season
- Revenue differences
- Water-efficiency differences

### Key Findings

Highest average yield by season:

| Season | State | Average Yield |
|---|---|---:|
| Kharif | Karnataka | 6.46 tonnes/ha |
| Rabi | Punjab | 8.61 tonnes/ha |
| Zaid | Karnataka | 6.62 tonnes/ha |

Highest average profit by season:

| Season | State | Average Profit |
|---|---|---:|
| Kharif | Gujarat | ₹217,051.33 |
| Rabi | Punjab | ₹169,294.52 |
| Zaid | Punjab | ₹62,109.69 |

---

# 🔗 Correlation Analysis

Correlation analysis was performed to identify relationships between important agricultural variables.

### Correlation with Yield

| Variable | Correlation with Yield |
|---|---:|
| Water Efficiency | 0.913 |
| Profit | 0.488 |
| Water Used | 0.386 |
| Nitrogen | 0.053 |
| Rainfall | 0.031 |

### Correlation with Profit

| Variable | Correlation with Profit |
|---|---:|
| Water Efficiency | 0.489 |
| Yield | 0.488 |
| Water Used | 0.190 |
| Rainfall | 0.108 |
| Soil Moisture | 0.091 |

### Important Note

`Water_Efficiency_t_per_1000m3` is mathematically derived from yield and water usage. Therefore, its strong correlation with yield is expected and **should not be interpreted as an independent causal relationship**.

Similarly, variables such as profit, revenue, production, and water efficiency are derived metrics and should be interpreted carefully in correlation analysis.

---

# 📊 Statistical Analysis

Statistical tests were used to determine whether observed differences between seasons were statistically significant.

## One-Way ANOVA

ANOVA was performed for:

- Yield
- Profit
- Water Efficiency

| Metric | F-statistic | p-value | Result |
|---|---:|---:|---|
| Yield | 1.5439 | 0.213678 | Not significant |
| Profit | 34.2918 | 1.71 × 10⁻¹⁵ | Significant |
| Water Efficiency | 6.9483 | 0.000972 | Significant |

This indicates that season had a statistically significant effect on **profit** and **water efficiency**, while the ANOVA did not detect a significant difference in mean yield.

---

## Kruskal-Wallis Test

Because variables such as yield and profit showed strong skewness and extreme values, the non-parametric Kruskal-Wallis test was also performed.

| Metric | H-statistic | p-value |
|---|---:|---:|
| Yield | 68.7131 | 1.20 × 10⁻¹⁵ |
| Profit | 101.9261 | 7.36 × 10⁻²³ |
| Water Efficiency | 56.8115 | 4.61 × 10⁻¹³ |

The results indicate statistically significant differences in the distributions across seasons.

### Statistical Interpretation

There is a discrepancy between ANOVA and Kruskal-Wallis for yield:

- ANOVA: **Not significant**
- Kruskal-Wallis: **Significant**

This is likely influenced by the strong skewness and extreme values in the yield data. Therefore, yield differences should be interpreted using robust/non-parametric methods rather than relying only on ANOVA.

---

# 🔬 Two-Way ANOVA

Two-way ANOVA was used to study:

- State
- Season
- State × Season interaction

### Yield

- State: Not significant
- Season: Not significant
- **State × Season: Significant (p = 0.04594)**

This indicates that the effect of season on yield varies depending on the state.

### Profit

- State: Not significant
- **Season: Significant**
- State × Season: Not significant

### Water Efficiency

- State: Not significant
- **Season: Significant**
- State × Season: Not significant

Overall, **season was an important factor for profit and water efficiency**, while the **State × Season interaction was significant for yield**.

---

# 💡 Key Insights

The major findings from the analysis are:

1. **Kharif was the strongest overall season** in terms of average profit and water efficiency.
2. Kharif had an average profit of approximately **₹178,914.65**.
3. Kharif had the highest average water efficiency of approximately **5.89 tonnes/1,000 m³**.
4. **Sugarcane was the highest-yielding crop** across all seasons.
5. **Sugarcane + Kharif** was the strongest crop-season combination based on yield, profit, revenue, and water efficiency.
6. **Zaid showed the lowest overall profitability**, with an average profit of approximately **-₹24,804.82**.
7. Season significantly affected **profit and water efficiency**.
8. State alone did not show a statistically significant effect on profit or water efficiency.
9. The **State × Season interaction significantly affected yield**.
10. Water efficiency showed a strong mathematical relationship with yield, but this should not be interpreted as causal because water efficiency is derived from yield and water usage.

---

# 🛠️ Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Statsmodels

### Development Environment

- **Google Colab**

---

# 📚 Statistical Techniques Used

- Descriptive Statistics
- GroupBy Analysis
- Correlation Analysis
- Pearson Correlation
- One-Way ANOVA
- Two-Way ANOVA
- Kruskal-Wallis Test
- Tukey HSD Post-Hoc Test
- Effect Size Analysis
- Interaction Analysis

---

# 🚀 Future Scope

The project can be extended into a complete agricultural decision-support system.

### Machine Learning

- Crop yield prediction
- Profit prediction
- Water requirement prediction
- Disease/pest risk prediction

### Smart Agriculture

- Irrigation recommendations
- Water optimization
- Crop recommendation
- Soil-based crop selection
- Weather-based farming recommendations

### Real-Time Data

The system could be integrated with:

- Weather APIs
- IoT soil sensors
- Satellite imagery
- Live market prices

### Interactive Applications

The analysis could be converted into an interactive application using:

- Streamlit
- Power BI
- Tableau

### AI Agricultural Assistant

A future version could use an AI assistant to provide recommendations based on:

- Location
- Crop
- Soil conditions
- Weather
- Water availability
- Market prices
- Historical farm performance

---

# 👥 Potential End Users

### Farmers

Can use the insights to compare crops, seasons, profitability, and water efficiency.

### Agricultural Departments

Can analyze regional and seasonal agricultural patterns for planning and policy decisions.

### Agronomists and Researchers

Can study relationships between environmental conditions, resources, crop performance, and profitability.

### Agribusinesses and Consultants

Can use crop-season and regional profitability insights for planning and investment decisions.

---

# ⚠️ Limitations

- The analysis is based on the available dataset and its recorded variables.
- Correlation does not imply causation.
- Several financial and efficiency variables are derived from other variables.
- Extreme values and skewed distributions affect some statistical tests.
- The dataset may not capture all real-world agricultural factors.
- Statistical relationships identified in this dataset may not generalize to all farming regions.

---

# 🏁 Conclusion

This project provides a comprehensive analysis of agricultural farm data using **Exploratory Data Analysis and Statistical Methods**.

The analysis identifies important differences between crops, states, and seasons and highlights the role of seasonal conditions in agricultural profitability and water efficiency.

Overall, **Kharif performed strongly across multiple metrics**, while **Sugarcane consistently emerged as the highest-performing crop**, particularly in the Kharif season.

The statistical analysis further demonstrates that **season has a significant effect on profit and water efficiency**, while the interaction between state and season significantly affects yield.

The project provides a foundation for developing future **machine-learning models, smart irrigation systems, crop recommendation systems, dashboards, and AI-powered agricultural decision-support tools**.

---

## 👨‍💻 Author

P Durgashyamanth

Agricultural Data Analysis Project
