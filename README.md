# Madrid Housing Market Analysis: The Sunlight Premium & Diminishing Returns

An econometric analysis and data visualization project investigating the structural and environmental drivers of property valuations in the Madrid housing market. Utilizing an R-based analytic pipeline, this project models how physical attributes (such as built surface area and room counts) and orientation metrics control market pricing.

---

## 🚀 Key Analytical Themes

* **The Sunlight Premium**: Quantifies and visualizes the valuation spread commanded by south-facing residential real estate properties relative to other orientations.
* **Diminishing Returns with Scale**: Models the non-linear relationship between property square footage and market valuation, testing whether increments in asset size add value at a decreasing rate.
* **Multivariate Valuation Controls**: Employs multiple ordinary least squares (OLS) linear regressions to isolate the individual value contributions of rooms, built area, orientation profiles, and cross-variable interaction parameters.

---

## 🛠️ Econometric Modeling Framework

The script computes and benchmarks five distinct linear statistical models to identify structural patterns:

### 1. Simple Linear Model
$$Price = \beta_0 + \beta_1(\text{Size}) + \epsilon$$

### 2. Full Multiple Regression Model
$$Price = \beta_0 + \beta_1(\text{Size}) + \beta_2(\text{South Facing}) + \beta_3(\text{Rooms}) + \epsilon$$

### 3. Sunlight Premium Model
$$Price = \beta_0 + \beta_1(\text{Size}) + \beta_2(\text{South Facing}) + \epsilon$$

### 4. Polynomial (Quadratic) Model
$$Price = \beta_0 + \beta_1(\text{Size}) + \beta_2(\text{Size}^2) + \epsilon$$

### 5. Interaction Model
$$Price = \beta_0 + \beta_1(\text{Size}) + \beta_2(\text{Orientation}) + \beta_3(\text{Size} \times \text{Orientation}) + \epsilon$$

---

## 🖥️ Project Setup & Execution

### System Requirements
* **R Language Environment** (v4.0.0 or higher recommended)
* **Required Packages**: `tidyverse`, `ggplot2` (v3.4.0+ required for optimal execution formatting), and `readr`.

### Execution
1. Ensure your source data matrix (`houses_Madrid.csv`) is placed directly within your active working directory.
2. Execute the complete script from an R console or an integrated IDE like RStudio:
   ```R
   source("Madrid Housing Anlysis.R")
