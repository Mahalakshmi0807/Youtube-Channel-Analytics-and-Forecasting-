<h1 align="center">🎥 YouTube Channel Analysis and Forecasting 📊</h1><p align="center">
  <b>Power BI Dashboard + Machine Learning Model</b> <br>
  Analyze, visualize, and forecast YouTube video performance using a 1000-row dataset with 20+ channel metrics.
</p>

---

## 📘 Project Overview

The **YouTube Channel Analysis and Forecasting** project combines **Power BI** and **Python** to perform data analysis, visualization, and predictive modeling on YouTube channel performance data.  
Using a dataset of **1000 videos** containing **20+ key metrics** such as *views, impressions, CTR, watch time, RPM, and estimated revenue*, this project helps creators understand what drives engagement and monetization — and forecast how future videos might perform.

---

## 🎯 Project Objectives

To build a real-time, interactive Power BI dashboard that helps YouTube creators analyze their video performance — including views, engagement, revenue, and audience behavior — and forecast future trends.

This dashboard converts raw YouTube data into insights that guide better content planning and growth strategies.
- To analyze YouTube video performance and identify key engagement factors.  
- To visualize content trends, traffic sources, and monetization metrics through Power BI.  
- To build a machine learning model that predicts video performance levels (Low, Medium, High).  
- To enable “what-if” forecasting for impressions and revenue growth.  
- To deliver real-time, interactive dashboards for data-driven decision-making.

---

## 🧾 Dataset Used

- **Dataset Name:**  https://github.com/Mahalakshmi0807/Youtube-Channel-Analytics-and-Forecasting-/blob/main/youtube_videos_1000.csv 
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

## Dashboard Screenshot 



## ❓ Business Questions / KPIs

The dashboard answers key business questions such as:
📊 What are the total views, likes, comments, and revenue?

🎯 What is the average engagement rate (likes + comments + shares ÷ views)?

🏆 Which are the Top 10 performing videos?

🧩 Which categories generate the most views and engagement?

🚦 Which traffic source brings the most audience?

📈 How have views and revenue changed month by month?

🔮 Can we forecast future views for the next few months?
 
🤩 Which traffic source contributes most to overall revenue?
   
🎥 How do Shorts compare with long-form videos in terms of views and monetization?  

💎 What is the relationship between impressions, CTR, and total views?  

🛍️ How does sponsorship impact engagement and revenue?  

📽️ What factors most influence high-performing videos (based on ML analysis)?

🔍 What if impressions increased by 10–30% — how much would revenue grow?

---

## ⚙️ Process 🔄 (Step-by-Step)

### 🪜 Step 1: Import the dataset

* Open **Power BI Desktop**
* Click **Get Data → Text/CSV → youtube_videos_1000.csv → Load**

---

### 🪜 Step 2: Data cleaning

* Change data types:

  * `published_date` → **Date**
  * `views`, `likes`, `comments`, `shares`, `revenue` → **Whole Number / Decimal**
* Rename columns for clarity if needed.

---

### 🪜 Step 3: Create DAX Measures

Go to **Modeling → New Measure** and add these formulas:

```dax
Total Views = SUM('youtube_videos_1000'[views])
Total Likes = SUM('youtube_videos_1000'[likes])
Total Comments = SUM('youtube_videos_1000'[comments])
Total Shares = SUM('youtube_videos_1000'[shares])
Total Revenue = SUM('youtube_videos_1000'[estimated_revenue_usd])

Engagement Rate =
DIVIDE(
    [Total Likes] + [Total Comments] + [Total Shares],
    [Total Views],
    0
)
```

---

### 🪜 Step 4: Create a Date Table

Go to **Modeling → New Table** and paste:

```dax
Date =
ADDCOLUMNS(
    CALENDAR(
        MIN('youtube_videos_1000'[published_date]),
        MAX('youtube_videos_1000'[published_date]) + 90
    ),
    "Year", YEAR([Date]),
    "Month", FORMAT([Date], "MMM"),
    "YearMonth", FORMAT([Date], "YYYY-MM")
)
```

Then:

* Go to **Model view**
* Connect `Date[Date]` → `youtube_videos_1000[published_date]`
* Right-click **Date Table** → Mark as Date Table → select `[Date]`

---

### 🪜 Step 5: Create Visuals

#### 🔹 KPIs (Cards)

* Total Views
* Total Likes
* Total Comments
* Engagement Rate (%)
* Total Revenue ($)

#### 🔹 Charts

1. **Bar Chart** → Top 10 videos by Views
2. **Pie Chart** → Views by Category
3. **Line Chart** → Views by Month (Date table)
4. **Donut Chart** → Traffic Source by Views
5. **Table** → All videos with columns:

   * Title
   * Category
   * Views
   * Likes
   * Comments
   * Estimated Revenue
   * Engagement Rate

#### 🔹 Forecast

* Select your **Views by Month** line chart
* Go to **Analytics Pane → Forecast → Add Forecast**
* Set Forecast length = 3 months

---

## 🧾 Dashboard Layout

| Section | Visual                                    | Purpose                          |
| ------- | ----------------------------------------- | -------------------------------- |
| Header  | Text “YouTube Channel Analysis Dashboard” | Title                            |
| Row 1   | KPI Cards                                 | Key performance metrics          |
| Row 2   | Bar + Pie Charts                          | Top videos + category comparison |
| Row 3   | Line + Donut Charts                       | Monthly trend + Traffic source   |
| Row 4   | Table                                     | Detailed video-level data        |
| Row 5   | Forecast                                  | Predict future performance       |

🎨 **Design tips:**

* Use white cards, light background, shadows
* Use red (YouTube color) for highlights
* Add YouTube logo on the top corner


---

## 🧠 Project Insights


After creating the dashboard, we can see:

1. 🔝 **Top 10 videos** bring almost **80% of total views**
2. 📚 **Educational videos** have the **highest engagement**
3. 💬 Higher likes and comments lead to **higher revenue**
4. 🌍 **Suggested Videos** and **YouTube Search** are main traffic sources
5. 📈 Forecast shows **steady growth** for next months
6. ⏱️ Shorter videos (under 5 mins) have **higher engagement rate**

We get the information that are,

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
| **Visualization** | Power BI |
| **Dashboard / BI** | Power BI Desktop & Service |
| **Environment** | Jupyter Notebook, VS Code |
| **Version Control** | Git, GitHub |


**Focus Areas:** Data Visualization • Predictive Analytics • Realtime Dashboards • BI Reporting  

---

## 📦 Deliverables

- 📘 `youtube_videos_1000.csv` — Dataset   
- 📊 `powerbi_blueprint.md` — Dashboard setup and DAX documentation  
- 🗂️ `presentation.pptx` — Final project slides  
- 📘 `README.md` — Full documentation  

---

## 🪄 Author
**Maha**  
📍 Villupuram, Tamil Nadu  
💼 Final Year BCA Student | MBA Aspirant | Data & Analytics Enthusiast  
📧 maharagupathi05@gmail.com

---

<p align="center">
🌟 <b>Transforming YouTube analytics into actionable insights using Data Science and Power BI.</b> 🌟
</p>
