# Customer Coupon Acceptance — Exploratory Analysis

### Overview
This analysis explores customer coupon acceptance based on several factors, including weather conditions, coupon type, bar patronage, and restaurant traffic. The primary goal is to understand the conditions under which customers accept coupons and to identify driver segments and contextual factors that influence acceptance rates.

Colab notebook: [module5_driver_coupon_eda.ipynb](https://colab.research.google.com/github/patisankar/customer-coupon-acceptance/blob/main/module5_dirver_coupon_eda.ipynb)

---

### Data Analysis — Key Findings
- The dataset initially contained a very high percentage of missing values in the `car` column (~99.15%), so that column was dropped. Several other columns (e.g., `Bar`, `CoffeeHouse`, `CarryAway`, `RestaurantLessThanX`) had missing data which were handled during preprocessing.
- Different coupon types show varying acceptance proportions; these were visualized and compared.
- Coupon acceptance rates vary by temperature and bar visit frequency; summaries and visualizations highlight these trends.
- Specific driver groups (defined by combinations of bar visit frequency, age, passenger type, and occupation) show different bar coupon acceptance rates. For example, drivers who visit bars frequently tend to accept bar coupons at different rates than infrequent visitors.
- Complex multivariate conditions combining bar visits, passenger type, marital status, age, cheap restaurant frequency, and income can identify groups with notably higher bar coupon acceptance rates.
- Numerical feature analysis revealed differences in mean values between accepted and rejected coupons and showed correlations among several distance-related features (e.g., toCoupon_GEQ5min, toCoupon_GEQ15min).
- Joint and conditional probability analyses between weather and coupon types reveal how the distribution of offered coupon types changes with weather and how acceptance probabilities depend on both weather and coupon type.

---

### Insights
- Detailed breakdowns of bar coupon acceptance by driver characteristics (frequency, age, passenger type, occupation, income) highlight segments more likely to accept offers.
- Further investigation into the identified multivariate conditions could refine driver segmentation and improve coupon acceptance prediction accuracy.

---

### Overall Trends
- Weather influence: Weather significantly affects customer behavior; acceptance rates for certain offers change depending on conditions (e.g., sunny vs. rainy).
- Distinct customer segments: Bars attract customers with varying group sizes, which is a useful indicator for marketing and resource allocation strategies.
- Location-specific acceptance: Certain bar locations exhibit unique acceptance patterns tied to typical group sizes and other local factors.

---

### Conditional Probabilities (selected)
- Weather and coupon usage: The probability of coupon acceptance varies with weather, indicating interaction effects between coupon type and environmental conditions.
- Sunny weather boosts coffee-house acceptance: Sunny days are associated with a higher likelihood of customers visiting coffee houses and accepting related coupons.
- Carryout vs. Take Away coupons: At less-busy restaurants on sunny days, "Carryout" coupons show a higher acceptance rate than "Take Away" coupons.

---

### Analysis Methods
- Histograms: Visualized distributions of single variables (e.g., temperature, passenger count).
- Subplots: Compared related visuals side-by-side (e.g., histogram with corresponding bar plot).
- Density heatmaps: Visualized joint distributions of two variables (e.g., `Bar` vs. passenger count), with faceting to incorporate outcome where useful.
- Correlation matrices: Measured pairwise correlations between numerical columns (Pearson and Spearman) to surface linear and monotonic relationships.
- Contingency tables: Calculated joint, marginal, and conditional probabilities for categorical variables to quantify relationships like coupon type vs. weather vs. acceptance.

---

### How to use this analysis
The insights from this analysis can help business owners and analysts make data-driven decisions:
- Targeted marketing: Tailor coupon promotions based on weather forecasts, customer segments, and location-specific patterns.
- Resource allocation: Optimize staffing and resources based on traffic patterns and typical customer group sizes per location.
- Operational strategy: Design bar and café services and layouts to better match predominant customer segments and maximize coupon effectiveness.

---
