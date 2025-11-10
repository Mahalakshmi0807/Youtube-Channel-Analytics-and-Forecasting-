# Youtube-Channel-Analytics-and-Forecasting-
This project,YouTube Channel Analysis and Forecasting,combines Power BI and Python to analyze,visualize,and predict YouTube video performance.It provides insights for audience engagement and monetization.The objective is to help creators identify the factors that lead to high-performing videos and forecast future success based on historical data.
<h1 align="center">🎥 YouTube Channel Analysis and Forecasting 📊</h1>

<p align="center">
  <b>Power BI Dashboard + Machine Learning Model</b> <br>
  Analyze, visualize, and forecast YouTube video performance using a 1000-row dataset with 20+ channel metrics.
</p>

---

## 📘 Project Overview

The **YouTube Channel Analysis and Forecasting** project combines **Power BI** and **Python** to perform data analysis, visualization, and predictive modeling on YouTube channel performance data.  
Using a dataset of **1000 videos** containing **20+ key metrics** such as *views, impressions, CTR, watch time, RPM, and estimated revenue*, this project helps creators understand what drives engagement and monetization — and forecast how future videos might perform.

---

## 🎯 Project Objectives

- To analyze YouTube video performance and identify key engagement factors.  
- To visualize content trends, traffic sources, and monetization metrics through Power BI.  
- To build a machine learning model that predicts video performance levels (Low, Medium, High).  
- To enable “what-if” forecasting for impressions and revenue growth.  
- To deliver real-time, interactive dashboards for data-driven decision-making.

---

## 🧾 Dataset Used

- **Dataset Name:** `youtube_videos_1000.csv`  
- **Rows:** 1000  **Columns:** 20+  **Primary Key:** `video_id`  

| Column Name | Description |
|--------------|-------------|
| `video_id` | Unique video identifier (Primary Key) |
| `upload_date` | Date when video was uploaded |
| `category` | Type of content (Education, Gaming, Tech, etc.) |
| `video_length_sec` | Duration of video in seconds |
| `views` | Total number of views |
| `likes`, `comments`, `shares` | Engagement metrics |
| `impressions` | How many times the video was shown |
| `ctr_percent` | Click-through rate (%) |
| `avg_view_duration_sec` | Average viewing time per user |
| `watch_time_hours` | Total watch time in hours |
| `estimated_revenue_usd` | Estimated ad revenue |
| `rpm_usd` | Revenue per 1,000 views |
| `traffic_source_primary` | Primary source of traffic (Search, Suggested, Shorts, etc.) |
| `subs_gained` | Subscribers gained from video |
| `contains_sponsor` | Whether the video is sponsored |
| `is_shorts_video` | 1 = Shorts video |
| `is_monetized` | Whether video is eligible for ads |

---

## ❓ Business Questions / KPIs

The dashboard answers key business questions such as:

1. Which content categories attract the highest number of views and engagement?  
2. Which traffic source contributes most to overall revenue?  
3. How do Shorts compare with long-form videos in terms of views and monetization?  
4. What is the relationship between impressions, CTR, and total views?  
5. How does sponsorship impact engagement and revenue?  
6. What factors most influence high-performing videos (based on ML analysis)?  
7. What if impressions increased by 10–30% — how much would revenue grow?

---

## 🔄 Process Workflow

1. **Data Preprocessing (Python):**  
   - Cleaned missing values, standardized formats, and removed duplicates.  
   - Created new features — *engagement rate, watch rate, views per minute, title length, etc.*

2. **Exploratory Data Analysis (EDA):**  
   - Used Python (Pandas, Matplotlib, Seaborn) to identify trends and correlations.  
   - Examined patterns between category, traffic source, and engagement metrics.

3. **Feature Engineering:**  
   - Derived new columns to enhance model accuracy (RPM ratio, average view duration, etc.)

4. **Machine Learning Modeling:**  
   - Built **Random Forest** and **XGBoost** models to predict video performance category (Low / Medium / High).  
   - Evaluated model using Accuracy, F1-score, RMSE, and feature importance via SHAP.

5. **Power BI Dashboard Creation:**  
   - Designed an interactive Power BI dashboard using cleaned dataset.  
   - Created KPI cards, charts, and forecasting visualizations with DAX measures.  
   - Integrated a **What-If Simulator** for revenue prediction.

---

## 📊 Power BI Dashboard Components

### **Dashboard Pages**
1. **Overview Page**
   - KPI Cards: Total Views, Total Revenue, Avg RPM, Engagement Rate  
   - Time Series: Views and Revenue over time  
   - Combo Chart: Revenue vs RPM Trend

2. **Content Performance Page**
   - Donut Charts:  
     - Views Share by Category  
     - Revenue Share by Traffic Source  
     - Shorts vs Long-form Views Split  
   - Bar Chart: Category vs Estimated Revenue  
   - Scatter Plot: Views vs Watch Rate (size = Subs Gained)

3. **Model Insights Page**
   - Predictions Table (Low / Medium / High)  
   - Confusion Matrix for model accuracy  
   - Feature Importance Bar Chart (Top 10 factors influencing performance)

4. **Forecast & What-If Page**
   - Impression % Increase Slider  
   - Adjusted Revenue Card and Comparison Chart

---

## 🧠 Project Insights

- **Education and Tech** categories generated the highest total views and revenue.  
- **Suggested and Browse** traffic sources were the most effective for audience reach.  
- **Shorts videos** gained more views but had lower RPM compared to long-form content.  
- Videos with **higher CTR and average view duration** performed significantly better.  
- **Sponsorship** had a mixed impact — slightly higher views but inconsistent RPM.  
- **Machine Learning results** showed that *impressions, watch rate, and engagement* were top predictors of success.  
- **What-if analysis** revealed that a 20% increase in impressions could raise estimated revenue by ~18%.

---

## 💡 Conclusion

The **YouTube Channel Analysis and Forecasting** project demonstrates how data analytics, visualization, and machine learning can work together to improve decision-making in digital media.  
By leveraging **Power BI dashboards** and **predictive models**, creators can identify what drives success, optimize upload strategies, and plan future content more effectively.  

This project not only enhances analytical skills but also showcases the integration of **business intelligence tools with AI-driven forecasting** — turning YouTube data into actionable insights for channel growth.

---

## ⚙️ Tools and Technologies

| Category | Tools / Libraries |
|-----------|------------------|
| **Data Cleaning & Analysis** | Python, Pandas, NumPy |
| **Visualization** | Power BI, Matplotlib, Seaborn |
| **Machine Learning** | Scikit-learn, XGBoost, SHAP |
| **Dashboard / BI** | Power BI Desktop & Service |
| **Environment** | Jupyter Notebook, VS Code |
| **Version Control** | Git, GitHub |

---

## 📦 Deliverables

- 📘 `youtube_videos_1000.csv` — Dataset  
- 🧮 `01_EDA_and_FeatureEngineering.ipynb` — Data exploration notebook  
- 🤖 `02_Modeling_Predict_Views.ipynb` — Machine learning notebook  
- 📊 `powerbi_blueprint.md` — Dashboard setup and DAX documentation  
- 🗂️ `presentation.pptx` — Final project slides  
- 📘 `README.md` — Full documentation  

---

## 🪄 Author
**Maha**  
📍 Villupuram, Tamil Nadu  
💼 Final Year BCA Student | MBA Aspirant | Data & Analytics Enthusiast  
📧 [your-email@example.com]

---

<p align="center">
🌟 <b>Transforming YouTube analytics into actionable insights using Data Science and Power BI.</b> 🌟
</p>
