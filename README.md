# 🏥 US Healthcare RCM: Operations Command Center & SLA Analytics

### 📌 Project Overview
This end-to-end business intelligence project simulates a 30-day operational environment for a US Healthcare Revenue Cycle Management (RCM) floor. The objective was to diagnose SLA breaches, track A/R inventory flow, and identify specific agent retraining needs by connecting production data with HR roster metrics.

### 🛠️ Tech Stack Used
*   **Microsoft Excel:** Data generation, power query cleaning, and macro automation.
*   **MS SQL Server:** Advanced querying, CTEs, Window Functions for rolling trends, and root-cause analysis.
*   **Power BI:** Relational data modeling (Star Schema), DAX measure creation, and interactive executive dashboarding.

### 📊 The Business Problem
The operations floor was experiencing intermittent Turnaround Time (TAT) breaches across three core queues (Charge Entry, Payment Posting, Denial Management). Leadership lacked visibility into whether SLA misses were driven by poor individual agent performance, high floor shrinkage, or unexpected A/R volume spikes.

### 💡 The Solution & Insights
1.  **The Agent Coaching Matrix:** Built a SQL script and Power BI Scatter Plot to isolate agent performance into 4 quadrants. Instantly identified agents (e.g., EMP045) operating with high AHT and low quality (<90%) for targeted side-by-side coaching.
2.  **Shrinkage Correlation:** Modeled a 1-to-Many relational database to accurately track individual agent shrinkage against scheduled hours, providing a true root cause for production dips.
3.  **Rolling 7-Day Backlog Trend:** Utilized SQL Window Functions (`AVG() OVER`) to track A/R inventory flow, smoothing out daily variances to give the VP of Operations a clear trendline of the department's backlog health.

### 📁 Repository Contents
*   `Raw_Data/`: CSV files representing 30 days of production, roster, and inventory logs.
*   `SQL_Scripts/`: Advanced queries used for data extraction and SLA logic.
*   `Dashboard/`: The Power BI `.pbix` file and PDF export of the final Command Center.
