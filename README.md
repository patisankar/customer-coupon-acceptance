### Overview
This analysis explores customer coupon acceptance based on several factors, including weather conditions, coupon type, bar patronage, and restaurant traffic. The primary goal is to understand the conditional probabilities of a customer accepting a coupon under various scenarios and to visualize these relationships to provide actionable business insights.
[coab-notebook](https://colab.research.google.com/github/patisankar/customer-coupon-acceptance/blob/main/module5_dirver_coupon_eda.ipynb)
### Data Analysis Key Findings
The dataset initially contained a high percentage of missing values in the 'car' column (99.15%), which was subsequently dropped. Other columns like 'Bar', 'CoffeeHouse', 'CarryAway', 'RestaurantLessThan20', and 'Restaurant20To50' had smaller percentages of missing values that were filled using the mode.
Different coupon types have varying acceptance proportions, which were visualized.
Coupon acceptance rates vary by temperature and bar visit frequency, with detailed summaries and visualizations provided.
Specific driver groups, defined by combinations of bar visit frequency, age, passenger type, and occupation, show different bar coupon acceptance rates. For instance, drivers who visit bars more than once a month and are over 25 years old have a significantly higher bar coupon acceptance rate (around 71.36%) compared to other drivers (around 38.28%).
Complex multivariate conditions combining bar visits, passenger type, marital status, age, cheap restaurant frequency, and income can identify a specific group of drivers with a notably higher bar coupon acceptance rate (around 69.56%) compared to all other drivers (around 40.08%).
The analysis of numeric features showed varying mean values between accepted and rejected coupons and revealed correlations between certain distance-related features (toCoupon_GEQ5min, toCoupon_GEQ15min, toCoupon_GEQ25min).
Joint and conditional probability analysis between weather and coupon types revealed how the distribution of coupon types offered changes based on weather conditions and vice versa.
The conditional probability of coupon acceptance depends on both weather conditions and the specific coupon type offered.
#### Insights
The detailed analysis of bar coupon acceptance by various driver characteristics (frequency, age, passenger type, occupation, income) highlights specific segments of drivers who are more likely to accept bar coupons. This information can be used for targeted marketing campaigns.
Further investigation into the complex multivariate conditions could help refine driver segmentation and predict coupon acceptance with higher accuracy.
#### Overall trends
Weather's influence on acceptance: Weather significantly impacts customer behavior, with acceptance rates for certain offers changing based on conditions (e.g., sunny vs. rainy).
Distinct customer segments: Different bars attract customers with varying group sizes. This behavior is a strong indicator of potential business strategies and resource allocation.
Location-specific acceptance: Specific bar locations have unique acceptance patterns for particular group sizes.
#### Conditional probabilities
Weather and coupon usage: The probability of acceptance for a given coupon varies depending on the weather. This indicates an interaction effect, where the coupon's effectiveness is influenced by environmental factors.
Sunny weather boosts coffee house acceptance: In sunny weather, there is a significantly higher likelihood of customers visiting a coffee house. This suggests a strong correlation between sunny days and coffee house patronage.
Carryout vs. Take Away coupons: At less busy restaurants on sunny days, 'Carryout' coupons show a higher acceptance rate than 'Take Away' coupons.
### Analysis methods
**Histograms**: Used to visualize the distribution of a single variable, such as temperature or passanger count.
**Subplots**: Employed to compare different variables side-by-side (e.g., a histogram and a bar plot in the same figure).
**Density heatmaps**: Utilized to visualize the joint distribution of two variables (e.g., Bar and passanger count). Faceted heatmaps were used to incorporate a third variable (outcome).
**Correlation matrices**: Used to measure the pairwise correlation between multiple numerical columns, helping to identify potential linear relationships. Pearson and Spearman correlations were compared to understand the nature of the relationships.
**Contingency tables**: Used to calculate joint, marginal, and conditional probabilities for categorical variables.
### How to use this analysis
The insights from this analysis can help a business owner make data-driven decisions:
Targeted marketing: Focus specific coupon promotions based on weather forecasts and location-specific customer segments.
Resource allocation: Optimize staffing and resource distribution based on traffic patterns and typical customer group sizes for each location.
Operational strategy: Design bar layouts and services to cater to the predominant customer segment for each location.
