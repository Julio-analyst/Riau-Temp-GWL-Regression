# 📊 Simple Linear Regression: Impact of Temperature on Groundwater Level in Riau

> A statistical data science case study using R to explore environmental trends.

---

## 📌 Overview

This project investigates the relationship between **temperature** and **groundwater level (GWL)** in **Riau Province, Indonesia**, using **Simple Linear Regression** in R. It serves as a statistical case study and environmental analysis that intersects **climate science** and **data analytics**.

---

## 🔗 Data Source

- Climate and hydrological data from Riau Province (2019), sourced from open-access academic datasets
- Variables: `Suhu` (temperature), `GWL` (groundwater level)

---

## 📊 Objective

To evaluate whether variations in temperature significantly impact groundwater levels in Riau through regression modeling, correlation analysis, and hypothesis testing.

---

## 📁 Project Structure

```
└️ analisis-gwl-riau/
   ├─ data.csv               # Dataset with temperature and GWL
   ├─ R.Rmd                 # R Markdown for reproducible analysis
   └─ README.md             # Project documentation
```

---

## 🛠️ Tools & Libraries

- **R** & **RStudio**
- `ggplot2` – Visualization
- `lmtest` – Regression diagnostics (e.g., Breusch-Pagan Test)
- `stats` – Linear regression model

---

## 📈 Key Results

- **Pearson correlation coefficient**: **r = 0.035** → very weak correlation
- **Regression model**: `GWL = 29.45 + 1.11 * Suhu`
- **R-squared**: very low → temperature is not a strong explanatory variable
- **p-value < 0.05** → model statistically significant despite weak fit

---

## 📊 Visual Output

| Scatter Plot & Regression Line | Residual Diagnostic |
|-------------------------------|----------------------|
| ![regression_plot](images/regression_plot.png) | ![residual_plot](images/residual_plot.png) |

---

## 📝 Sample Code (R)

```r
# Load libraries
library(ggplot2)
library(lmtest)

# Import data
data <- read.csv("data.csv")

# Regression model
model <- lm(GWL ~ Suhu, data = data)
summary(model)

# Correlation
cor(data$Suhu, data$GWL)

# Plot
ggplot(data, aes(x = Suhu, y = GWL)) +
  geom_point() +
  geom_smooth(method = "lm", se = FALSE, color = "red")

# R-squared
summary(model)$r.squared
```

---

## 👨‍💼 Skills Demonstrated

- Statistical Modeling (Simple Linear Regression)
- Correlation Analysis & R-squared Interpretation
- Exploratory Data Analysis (EDA)
- Residual Diagnostics (Breusch-Pagan)
- Reproducible Research using R Markdown

---

## 📚 References & Docs

- [R stats::lm() Documentation](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/lm.html)
- [ggplot2 Guide](https://ggplot2.tidyverse.org/)
- [lmtest Package on CRAN](https://cran.r-project.org/web/packages/lmtest/index.html)

---

## 📝 License

MIT License  
© 2025 Julio-analyst

---

## 📬 Contact

- 🌐 [LinkedIn](https://www.linkedin.com/in/farrel-julio-427143288)  
- 📂 [Portfolio (Notion)](https://linktr.ee/Julio-analyst)  
- ✉️ farelrel12345@gmail.com
