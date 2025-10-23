# Customer Coupon Acceptance — Exploratory Analysis

### Overview
This analysis explores customer coupon acceptance based on several factors, including weather conditions, coupon type, bar patronage, and restaurant traffic. The primary goal is to understand the conditions under which customers accept coupons and to identify driver segments and contextual factors that influence acceptance rates.

Colab notebook: [module5_driver_coupon_eda.ipynb](https://colab.research.google.com/github/patisankar/customer-coupon-acceptance/blob/main/module5_dirver_coupon_eda.ipynb)

---

## Data Quality & Preprocessing Findings
- The dataset initially contained a very high percentage of missing values in the `car` column (~99.15%), so that column was dropped. Several other columns (e.g., `Bar`, `CoffeeHouse`, `CarryAway`, `RestaurantLessThan20`) had missing data which were handled by filling with mode values during preprocessing.

## Bar Coupon Acceptance Patterns

### Overall Performance:
- **Bar coupon acceptance rate**: 41% (lowest among all coupon types)
- **Best performing coupons**: 
  - Carry out & Take away: 73.55% acceptance (highest)
  - Restaurant(<20): 70.71% acceptance
  - Coffee House: 49.93% acceptance (most volume)

### Critical Success Factors:

#### 1. Bar Visit Frequency Impact:
- **4-8 times/month**: 63.76% acceptance (highest)
- **1-3 times/month**: 62.19% acceptance
- **Never visit bars**: 53.21% acceptance (lowest)
- Different coupon types show varying acceptance proportions across all frequency groups

#### 2. Demographic & Behavioral Insights:
- **Age factor**: Drivers >25 who visit bars >1/month show **62.15% acceptance** vs **55.35%** for others
- **Multi-factor targeting**: Drivers who visit bars >1/month + not traveling with kids + not in farming/fishing/forestry occupations show **62.21% acceptance**
- Specific driver groups defined by combinations of bar visit frequency, age, passenger type, and occupation show distinctly different bar coupon acceptance rates

#### 3. Environmental Factors:
- **Temperature dependency**: 80°F weather shows **60.03% acceptance** vs ~53% for other temperatures
- **Weather patterns**: Sunny weather dominates coupon distribution (79% of all coupons)
- Weather significantly affects customer behavior; acceptance rates for certain offers change depending on conditions

### Multivariate Condition Analysis:
- Complex multivariate conditions combining bar visits, passenger type, marital status, age, cheap restaurant frequency, and income can identify groups with notably higher bar coupon acceptance rates
- Drivers satisfying specific combined conditions show **62.21% acceptance** vs **54.46%** for others

### Numerical Feature Analysis:
- Numerical feature analysis revealed differences in mean values between accepted and rejected coupons
- Correlations exist among distance-related features (e.g., toCoupon_GEQ5min, toCoupon_GEQ15min show 0.32 moderate correlation)
- These distance factors show minimal contribution to overall acceptance patterns

## Weather & Coupon Type Interactions

### Joint and Conditional Probability Insights:
- Joint and conditional probability analyses between weather and coupon types reveal how the distribution of offered coupon types changes with weather
- **Sunny weather boosts coffee-house acceptance**: Sunny days are associated with higher likelihood of customers visiting coffee houses (87% of coffee house coupons distributed on sunny days)
- **Weather-coupon interaction**: The probability of coupon acceptance varies with weather, indicating interaction effects between coupon type and environmental conditions
- **Carryout optimization**: "Carryout & Take Away" coupons show higher acceptance rates than other types, especially on sunny days

## Customer Segmentation Insights

### High-Value Segments Identified:
- Drivers visiting bars 4-8 times monthly
- Age >25 with moderate bar visiting habits  
- Non-agricultural occupations traveling without children
- Those targeted during warmer weather (80°F)

### Distinct Customer Patterns:
- Bars attract customers with varying group sizes, which is a useful indicator for marketing and resource allocation strategies
- Location-specific acceptance: Certain customer segments exhibit unique acceptance patterns tied to typical group sizes and behavioral factors

## Analysis Methods Applied
- **Histograms**: Visualized distributions of single variables (e.g., temperature, passenger count)
- **Subplots**: Compared related visuals side-by-side (e.g., histogram with corresponding bar plot)
- **Correlation matrices**: Measured pairwise correlations between numerical columns to surface linear relationships
- **Contingency tables**: Calculated joint, marginal, and conditional probabilities for categorical variables to quantify relationships like coupon type vs. weather vs. acceptance
- **Interactive visualizations**: Used Plotly for enhanced user experience and pattern identification

## Strategic Business Applications

### How to Use This Analysis:
The insights from this analysis can help business owners and analysts make data-driven decisions:

- **Targeted marketing**: Tailor coupon promotions based on weather forecasts, customer segments, and location-specific patterns
- **Resource allocation**: Optimize staffing and resources based on traffic patterns and typical customer group sizes per location  
- **Operational strategy**: Design bar and café services and layouts to better match predominant customer segments and maximize coupon effectiveness
- **Segmentation refinement**: Further investigation into the identified multivariate conditions could refine driver segmentation and improve coupon acceptance prediction accuracy
