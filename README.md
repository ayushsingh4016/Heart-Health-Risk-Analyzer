# Heart-Health-Risk-Analyzer
The Heart Health Risk Analyzer is an interactive Power BI dashboard that helps visualize potential risk factors leading to heart disease. This project uses a real-world dataset to showcase how data can be leveraged for preventive healthcare insights using data analytics and storytelling.

✅ Built to impress recruiters, healthcare professionals, and data enthusiasts with clean visuals, tooltips, KPIs, and meaningful interactions.

📊 Dashboard Features
🔹 Feature	💬 Description
KPI Cards	Total Heart Disease Cases, Avg. Cholesterol, Avg. Age, % Risk
Age vs Heart Disease	Clustered Column Chart showing high-risk age groups
Chest Pain Type Analysis	Breakdown by types like ASY, NAP, etc.
Gender Distribution	Donut chart with % Male vs Female
Exercise-Induced Angina	Impact visualized via stacked bars
Blood Pressure Category	Heart disease count by BP category
Tooltips	Hover over KPIs to view Min/Max/Std Dev of Cholesterol
Slicers	Interactive filters for Sex, Chest Pain Type, and Age Groups

🧠 Skills Applied
📊 Power BI

🧮 DAX Calculations

🧼 Data Cleaning & Modeling

🎨 UI/UX Design

📌 Tooltip Integration

📂 Report Navigation & Drillthroughs

🧾 Sample DAX Measures Used
DAX
Copy
Edit
Total Heart Cases = CALCULATE(COUNTROWS(HeartData), HeartData[HeartDisease] = 1)

% Heart Disease Risk = DIVIDE([Total Heart Cases], COUNTROWS(HeartData))

Avg Cholesterol (Heart Patients) = 
CALCULATE(
    AVERAGE(HeartData[Cholesterol]),
    HeartData[HeartDisease] = 1
)

Age Group = 
SWITCH(
    TRUE(),
    HeartData[Age] < 40, "Under 40",
    HeartData[Age] >= 40 && HeartData[Age] <= 55, "40 - 55",
    HeartData[Age] > 55 && HeartData[Age] <= 70, "56 - 70",
    HeartData[Age] > 70, "70+",
    "Unknown"
)
📂 Dataset Source
📥 Heart Failure Prediction Dataset
📎 Source: Kaggle – Link
📌 Contains: Age, Sex, Chest Pain Type, Cholesterol, Resting BP, Exercise Angina, etc.


📊 Dashboard Format: .pbix (Power BI Desktop)

🚀 What I Learned
How to use KPIs & tooltips for real-world healthcare data

Importance of slicers & filters for dashboard storytelling

Designing clean & professional dashboards for recruiters

Using DAX effectively to create dynamic groupings and stats
