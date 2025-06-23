# Descriptive Analytics: Analysis of the Second-Hand Car Market

## Project Overview

This project explores the pricing dynamics of the second-hand car market, specifically Ford Fiestas listed on Auto Trader UK. By combining descriptive statistics, hypothesis testing, correlation analysis, and regression modeling, the analysis aims to understand which factors most strongly drive price, and whether local market pricing aligns with national trends.

---

## Dataset Description

- **Source:** Web-scraped from Auto Trader UK
- **Sample:** ~100 Ford Fiesta listings (2020–2023 registrations), local area
- **Key variables:** Price, mileage, engine size, registration year, transmission, fuel type, number of doors, additional features

---

## Exploratory Data Analysis & Visualization

### Engine Size Distribution

![Histogram of Engine Size](images/Histogramofengine.jpg)

*Interpretation:*  
Most Ford Fiestas in this sample are equipped with 1.0-litre engines, with smaller clusters at 1.1 and 1.5 litres. This concentration helps explain why price and performance are relatively consistent for the bulk of the sample.

---

### Relationship Between Price and Registration Year

![Scatter Plot: Price vs Year](images/Scatterplot.jpg)

*Interpretation:*  
As expected, newer vehicles command higher prices. 2023 models are typically the most expensive, while 2020 and 2021 cars are less expensive. Notably, there is some price volatility among 2022 models, likely reflecting differences in condition, features, or mileage.

---

### Price by Number of Doors

![Boxplot: Price by Doors](images/Boxplot.jpg)

*Interpretation:*  
Five-door Fiestas tend to be pricier and show less price variation than three-door models, possibly due to greater practicality and demand.

---

## Descriptive Statistics

![Descriptive Statistics](images/Discriptivestatistics.jpg)

*Interpretation:*  
- The median price is £14,692, with the average price slightly lower due to a handful of cheaper, older models.
- Engine sizes are tightly clustered around 1.0–1.1L.
- Mileage shows a typical spread from 9,000–19,000 miles, with outliers at both extremes.

---

## Confidence Intervals for Mileage

![Confidence Interval](images/Confidenceinterval.jpg)
![Confidence Interval 2](images/confidenceinterval2.jpg)
![Confidence Interval 3](images/confidenceinterval3.jpg)

*Interpretation:*  
Most cars in this local sample have driven 9,000 to 19,000 miles. The confidence interval for mean mileage (95%) helps quantify the expected spread and supports reliable comparison across models and segments.

---

## Hypothesis Testing: Fuel Type and Mileage

![Independent Sample Test](images/Independentsampletest.jpg)
![Independent Sample Test 2](images/independentsampletest2.jpg)
![T-TEST](images/T-TEST.jpg)
![ANOVA Table](images/ANOVA.jpg)

*Interpretation:*  
Independent samples t-tests and ANOVA suggest there is no statistically significant difference in average mileage between different fuel types (p = 0.256). Although petrol and hybrid/diesel cars show a small difference in means, it’s not strong enough to rule out chance.

---

## Comparison with National Market Trends

![Comparison with Market Trends](images/comparisionwithmarkettrends.jpg)

*Interpretation:*  
The mean price for local Fiestas (£14,229) matches closely with the UK national mean (£14,180). Statistical tests (p = 0.852) confirm no significant price difference, supporting the idea that local pricing is representative of the broader UK market.

---

## Correlation Analysis

![Correlation Table](images/correlation.jpg)

*Interpretation:*  
- **Price** increases with engine size (r = 0.345) and registration year (r = 0.211)
- **Price** decreases as mileage increases (r = -0.265)
- Other variables, such as doors and transmission, show weaker relationships with price.

---

## Regression Modeling

**Model Summary:**  
![Model Summary](images/modelsummary.jpg)  
**Regression Coefficients:**  
![Coefficients Table](images/Coefficients.jpg)  
**Regression Output:**  
![Regression Output](images/regression.jpg)

*Interpretation:*  
The multiple linear regression model explains about 24.5% of the variation in car price (R² = 0.245). Engine size and registration year are statistically significant predictors (p < 0.05). Mileage has a negative effect, as expected, but is less significant when controlling for other factors.

---

## Residual Analysis

![Residual Statistics](images/Residualstatistics.jpg)
![Residual Scatterplot](images/Residualscatterplot.jpg)
![Histogram of Residuals](images/Histogramofresiduals.jpg)
![Durbin Watson Statistic](images/Durbinwatsonstatistics.jpg)

*Interpretation:*  
- Residuals are mostly centered around zero, suggesting the model fits the data reasonably well.
- The residual scatterplot shows a few outliers, where the model underestimates or overestimates the true price.
- The Durbin-Watson statistic (~2.1) confirms no autocorrelation in the residuals, a sign of good model reliability.

---

## Key Takeaways

- **Price drivers:** Engine size, registration year, and mileage are the most influential factors for Ford Fiesta pricing.
- **Market alignment:** Local pricing closely mirrors the national average, supporting market-wide pricing strategies.
- **Model reliability:** The model performs well for most listings, though some outliers remain. Dealers can use these insights to fine-tune their pricing for maximum competitiveness.

---

## Reference

[Auto Trader UK](https://www.autotrader.co.uk)

---

*For full details, see the report and statistical output in this repository.*
