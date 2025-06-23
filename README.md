# Descriptive Analytics: Analysis of the Second-Hand Car Market

## Project Overview

This project provides a detailed statistical analysis of the UK second-hand car market, focusing on the Ford Fiesta. The goal is to understand key drivers of price and build a regression model for accurate market estimation, using a real-world sample of ~100 cars scraped from Auto Trader.

---

## Dataset Description

- **Source:** Auto Trader UK (scraped web data)
- **Sample:** ~100 Ford Fiesta cars (2020–2023), local market
- **Main Variables:**
  - Price
  - Mileage
  - Engine size
  - Registration year
  - Transmission
  - Fuel type
  - Number of doors
  - Additional equipment/features

---

## Data Visualization

### Histogram of Engine Size

The majority of Ford Fiestas have 1.0-litre engines, with smaller clusters at 1.1 and 1.5 litres.

![Histogramofengine](images/Histogramofengine.jpg)

---

### Scatter Plot: Price vs Registration Year

Newer (2023) vehicles are more expensive; older cars (2020, 2021) are cheaper. Price volatility exists for 2022 registrations.

![Scatter Plot: Price vs Year](images/scatter_price_year.png)

---

### Boxplot: Price by Number of Doors

Five-door models are pricier and more stable in price than three-door models.

![Boxplot: Price by Doors](images/boxplot_price_doors.png)

---

## Advanced Statistical Analysis

### Descriptive Statistics

- Median price: £14,692 (higher than mean due to some cheaper cars)
- Engine size clusters at 1.05L (mostly 1L engines)
- Sample dominated by new cars, driving up the average price

---

### Confidence Interval for Mileage

- Most cars: 9,000–19,000 miles (median ≈ 13,500)
- Mean inflated by outliers (average ≈ 15,722 miles)

---

### Hypothesis Testing: Fuel Type & Mileage

**Null hypothesis:** No difference in average mileage between fuel types  
- Fuel type 1: avg ≈ 11,341 miles  
- Fuel type 2: avg ≈ 16,052 miles  
- **p-value = 0.256:** Not statistically significant  
- Effect size suggests a small practical difference

---

### Comparison with UK Market Trends

- Local mean price: £14,229  
- National mean: £14,180  
- **p-value = 0.852:** No significant price difference
- Local prices align with the UK market

---

### Correlation Analysis

- Price ↑ with engine size (0.345)
- Price ↓ with higher mileage (−0.265)
- Newer year ↑ price (0.211)

---

### Regression Model

The regression explains 24.5% of price variation:
> **Price = −20735.04 + (8280.28 × Engine Size in Litres) + (1028.13 × Registration Year) − (0.039 × Mileage)**

- **Engine size and registration year:** Strongest predictors (p < 0.05)
- **Mileage:** Negative effect, but less significant alone

---

### Residual Analysis

**Residual scatterplot and histogram:**
- Residuals mostly centered around zero, indicating good model fit
- Some outliers (model underestimates price for some cars)
- Durbin-Watson ≈ 2.1 (no autocorrelation)

![Residual Scatterplot](images/resid_scatter.png)
![Residual Histogram](images/resid_hist.png)

---

## Key Takeaways

- **Main price drivers:** Engine size, registration year, mileage
- **Local prices:** Align with UK national trends
- **Model performance:** Good fit for most cars; some outliers
- **Dealers:** Can use this model for strategic, competitive pricing

---

## Reference

[Auto Trader UK](https://www.autotrader.co.uk)

---

*For details, see the full report and code in this repository.*

