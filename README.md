# 🏠 Airbnb Sydney Pricing & Host Strategy Analysis

## 📊 Overview
This project explores how machine learning and data mining techniques can help Airbnb hosts in Sydney optimise their pricing strategies and identify what makes a successful host. Sydney’s Airbnb market is highly competitive, and success relies on more than just offering a property—it requires strategic pricing, guest satisfaction, and smart listing management. This report combines predictive modelling and host classification to provide actionable insights for Airbnb hosts and property investors.

---

## 🎯 Objectives
- Predict Airbnb daily rental prices based on listing attributes.
- Identify key predictors of guest pricing willingness.
- Define and classify the "Best Hosts" using performance indicators.
- Discover common behaviours of successful hosts using pattern mining.
- Recommend strategies to improve host performance and revenue.

---

## 🔍 Problem Context
In a crowded market with fluctuating demand, hosts must set prices that attract guests while maintaining profitability. Similarly, understanding what makes a host successful is key for property investors seeking sustainable returns. This project addresses:
- **What is the optimal rental price for an Airbnb in Sydney?**
- **What differentiates high-performing (best) hosts from average ones?**
- **How can hosts optimise pricing and improve guest satisfaction simultaneously?**

---

## 📁 Methodology Summary

### 🧠 Predictive Modelling
- **Target Variable**: Daily rental price (log-transformed)
- **Data Source**: Inside Airbnb (Sydney listings)
- **Models Evaluated**:
  - ElasticNet
  - k-Nearest Neighbours (k-NN)
  - Random Forest
  - Gradient Boosting
  - Support Vector Regression (SVR)
  - **XGBoost** (Best performer)
  - Stacking Ensemble

| Model           | RMSE  | R²    |
|----------------|-------|-------|
| **XGBoost**     | 0.417 | 0.786 |
| Random Forest   | 0.419 | 0.780 |
| SVR             | 0.463 | 0.731 |
| Model Stacking  | 0.458 | 0.737 |
| k-NN            | 0.500 | 0.686 |
| ElasticNet      | 0.544 | 0.629 |

### 🔑 Key Insights from Price Prediction
- **Room Type**: Most influential predictor (entire homes/apartments priced higher).
- **Guest Capacity**: Larger spaces attract higher rates.
- **Amenities**: More bathrooms and quality features justify higher pricing.
- **Location**: Premium suburbs (e.g., Sydney CBD, Mosman) attract higher rates.
- **Dynamic Pricing**: Seasonality and event data drive optimised pricing.

---

## 🧩 Data Mining: What Are the Best Hosts Doing?

### 🏅 Defining "Best Hosts"
Based on high-performing characteristics:
- **Superhost Status**
- **Average Review Score ≥ 4.7**
- **Response Rate ≥ 90%**
- **Top 20% in Price/Revenue**

### 🔍 Classification Model (Random Forest)
- **Goal**: Predict whether a host is "Best" or "Average"
- **Performance**: High accuracy, precision, and recall
- **Key Predictors**:
  - Superhost status (most important)
  - Average review score
  - Availability (days listed)
  - Price
  - Response rate
  - Minimum nights
  - Neighbourhood

### 📊 Generalised Sequential Pattern (GSP) Analysis
Top-performing hosts consistently:
- Have Superhost status
- Respond promptly
- Price listings in premium ranges
- Offer flexible booking (low min nights, long max stays)
- Operate in premium suburbs with longer average stays

---

## 📈 Strategic Insights for Hosts & Investors

### 🎯 Superhost Status & Guest Trust
- Superhosts earn ~15% more due to better visibility and trust.
- They maintain review scores > 4.8 and response rates > 90%.
- Average availability: 182 days.

### 🧮 Occupancy vs Satisfaction
- Superhosts: Lower occupancy (58%) but higher reviews (4.51)
- Non-Superhosts: Higher occupancy (66%) but lower reviews (3.36)
- Insight: Prioritise **guest experience over mass bookings** to build reputation.

### 💰 Dynamic Pricing in High-Demand Areas
- Top 20% priced listings earn ~30% more revenue.
- Sydney CBD average: AUD 605/night vs AUD 320 in budget areas.
- Key: **Match price to quality, season, and location.**

### 🏡 Flexible Availability Boosts Bookings
- High-rated hosts (avg. review ≥ 4.8) see 25% more bookings.
- Flexible stays attract a broader market (short stays + families).
- Top listings: 85% average occupancy vs. 60% for low-rated ones.

---

## ✅ Recommendations

1. **Prioritise Superhost Status**  
   Improve guest experience, respond quickly, and aim for top reviews.

2. **Implement Smart Dynamic Pricing**  
   Use pricing tools and market data to adjust for seasonality and events.

3. **Offer Flexible Booking Options**  
   Lower minimum stays and longer availability windows can increase reach.

4. **Focus on Review Quality Over Quantity**  
   Enhance guest satisfaction to drive return bookings and build loyalty.

5. **Invest in High-Value Locations**  
   Premium neighbourhoods consistently yield higher revenue potential.

---

## 📚 Tools & Libraries Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn
- XGBoost
