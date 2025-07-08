# 📊 Simple Linear Regression Analysis of Temperature's Effect on Groundwater Level in Riau

## 🧠 Overview

This project investigates the **influence of temperature on groundwater level (GWL)** in **Riau Province, Indonesia**, using **Simple Linear Regression** with **R programming**. It serves as a statistical analysis exercise and environmental study relevant to **data science** and **hydrological impact analysis**.

---

## 🎯 Objective

To determine whether temperature significantly impacts groundwater level fluctuations in Riau, using historical data and visual/statistical interpretation.

---

## 🗂️ Project Structure

```
C:\analisis-gwl-riau
├── data.csv                   # Dataset containing temperature and GWL values
├── R.Rmd                     # R markdown file for reproducible analysis
├── README.md                 # This documentation
```

---

## 🧰 Tools and Libraries Used

* **R** / **RStudio** (IDE)
* **ggplot2** – for data visualization
* **lmtest** – for hypothesis testing (e.g., Breusch-Pagan test)
* **stats** – for regression modeling and correlation

> 

---

## 📈 Analysis Summary

> **"Simple Linear Regression Analysis of the Effect of Temperature on Groundwater Level (GWL) in Riau Province, Indonesia."**

### 📌 Data Highlights:

* Source: Secondary climate data of Riau Province (2019)
* Variables: Temperature (Suhu) and Groundwater Level (GWL)

### 🔍 Key Results:

* **Pearson correlation coefficient**: r = 0.035 (very weak)
* **Regression Equation**: `GWL = 29.45 + 1.11 * Suhu`
* **R-squared**: Small value indicating low explanatory power
* **Significance**: Model is statistically significant (p-value < 0.05)

---

## 📦 Key Code Steps (in R.Rmd)

```r
# Load libraries
library(ggplot2)
library(lmtest)

# Import data
data <- read.csv("data.csv")

# Build regression model
model <- lm(GWL ~ Suhu, data = data)
abline(model, col = "red")
summary(model)

# Pearson correlation
cor(data$Suhu, data$GWL)

# R-squared value
summary(model)$r.squared
```

---

## 🧠 Credits

Created by **Farrel Julio Akbar** and team
📍 Case Study: **Riau, Indonesia**
📘 Based on coursework: *Advanced Data Science (ADS)*
