# Bellabeat Smart-Device Usage Analysis

## Project Overview

This project analyzes smart-device usage data to identify behavioral patterns that could provide useful context for Bellabeat's marketing and customer-engagement strategy.

The analysis examines device-recording patterns, physical activity, sleep, calorie expenditure, and time-of-day behavior using publicly available Fitbit data.

The project follows the Google Data Analytics framework:

**ASK → PREPARE → PROCESS → ANALYZE → SHARE → ACT**

> **Important:** The dataset represents third-party Fitbit users rather than Bellabeat customers. Therefore, the findings are treated as exploratory behavioral evidence rather than confirmed Bellabeat customer behavior.

---

## Business Problem

Bellabeat is a wellness technology company developing products designed to support women's health and wellbeing.

The purpose of this analysis is to better understand how consumers use smart devices and identify behavioral trends that could potentially inform Bellabeat's marketing and customer-engagement decisions.

### Business Objective

> To analyze smart-device usage patterns and identify evidence-based insights that could inform Bellabeat's marketing strategy and customer engagement activities.

### Business Questions

1. What are some trends in smart-device usage?
2. How could these trends apply to Bellabeat customers?
3. How could these trends influence Bellabeat's marketing strategy?

---

## Tools Used

- **Microsoft Excel** — data cleaning, validation, exploratory analysis, descriptive statistics, correlation analysis, and supporting visualizations.
- **Microsoft Power BI** — data modelling, DAX measures, interactive visualization, and dashboard development.
- **Git & GitHub** — project version control, documentation, and portfolio presentation.

---

## Dataset

The project uses publicly available Fitbit smart-device data covering approximately one month of activity.

### Dataset Scope

| Dataset | Records | Participants |
|---|---:|---:|
| Daily Activity | 457 | 35 |
| Sleep | 410 cleaned records | 24 |
| Hourly Steps | 24,084 | 34 |
| Hourly Intensities | 24,084 | 34 |
| Hourly Calories | 24,084 | 34 |

**Analysis period:** March 12 – April 12, 2016.

The sleep dataset originally contained 413 records. Three redundant duplicate records were removed during data cleaning, resulting in 410 cleaned records.

---

## Data Preparation and Validation

Before analysis, the datasets were inspected and validated to ensure that the selected variables could support the business questions.

Key processing activities included:

- Standardizing daily, hourly, and sleep date/time fields.
- Checking for missing values and exact duplicates.
- Removing three redundant sleep records.
- Validating participant identifiers.
- Creating cleaned date and time fields.
- Creating participant-date keys for activity/sleep matching.
- Validating row-level alignment across hourly steps, intensity, and calorie datasets.
- Creating derived fields such as hour of day and sleep efficiency.

### Activity-Sleep Matching

Daily activity and sleep records were compared using participant ID and cleaned date.

Only **12 of 457 daily activity records** had corresponding sleep records in the validated comparison.

Because of this limited overlap, activity-versus-sleep relationships were not generalized across the dataset.

---

## Key Findings

### 1. Device Recording and Engagement

The analysis included **35 participants** with recorded activity coverage ranging from **8 to 32 days**.

- Mean recorded days: **13.06**
- Median recorded days: **12**
- 16 participants (**45.7%**) contributed exactly 12 recorded activity days.

These results describe the availability and consistency of recorded activity data rather than confirmed device-wearing behavior.

### 2. Physical Activity

Average daily steps were approximately **6,547**.

The activity-minute analysis showed that recorded time was dominated by sedentary and lightly active behavior.

Average daily minutes:

- Very active: **16.62 minutes**
- Fairly active: **13.07 minutes**
- Lightly active: **170.07 minutes**
- Sedentary: **995.28 minutes**

More than half of the daily records contained zero very-active minutes, indicating that high-intensity activity was not consistently recorded.

### 3. Sleep

Across **410 cleaned sleep records**:

- Average sleep duration: approximately **419 minutes**
- Typical sleep duration: approximately **6 hours 59 minutes**
- Median sleep duration: approximately **7 hours 13 minutes**
- Average time in bed: approximately **458 minutes**
- Average sleep efficiency: approximately **91.65%**

Sleep behavior varied substantially across records, indicating opportunities for personalized sleep and wellness insights.

### 4. Steps and Calorie Expenditure

Average daily calorie expenditure was approximately **2,189 calories**.

Daily steps showed a **moderate positive correlation (~0.58)** with calorie expenditure.

The steps-versus-calories linear trendline produced an **R² of approximately 0.34**, suggesting that steps explain part—but not all—of the variation in daily calorie expenditure.

This relationship is associative and should not be interpreted as causal.

### 5. Time-of-Day Behavior

Hourly analysis showed clear variation in activity throughout the day.

Activity was lowest during overnight and early-morning hours and increased during daytime.

The strongest combined hourly pattern occurred around **7:00 PM**, when average:

- Steps reached approximately **529**
- Total intensity reached approximately **19.25**
- Calories reached approximately **116**

This identifies an observed behavioral pattern, not proof that 7:00 PM is the optimal time for customer communication.

---

## Key Insights

The analysis suggests several broader smart-device usage patterns:

- Recorded behavior was dominated by sedentary and light activity.
- Average daily steps were around 6,500.
- Typical sleep duration was approximately seven hours, although sleep behavior varied.
- Higher step activity was moderately associated with higher calorie expenditure.
- Activity varied substantially by time of day, with strong evening activity patterns.
- Participant recording coverage was uneven.

Because the dataset does not contain Bellabeat customers, these findings should be treated as hypotheses that Bellabeat could validate using its own customer data.

---

## Business Recommendations

### 1. Encourage Everyday Movement

Bellabeat could emphasize achievable daily movement rather than focusing exclusively on high-intensity exercise.

### 2. Develop Personalized Wellness Insights

Combining activity, sleep, and calorie information could help provide users with more relevant wellness feedback.

### 3. Test Behavior-Informed Engagement Timing

Observed hourly patterns could be used to develop timing hypotheses for reminders or wellness messages.

For example, evening engagement could be tested rather than assumed to be optimal.

### 4. Encourage Consistent Tracking

Because recording coverage varied considerably between participants, Bellabeat could explore strategies that encourage consistent smart-device engagement.

A suitable implementation approach would be:

**Validate → Experiment → Measure → Scale**

---

## Power BI Dashboard

The Power BI dashboard summarizes the major analytical findings through:

- Participant count
- Average daily steps
- Average sleep duration
- Average daily calories
- Average activity minutes by intensity level
- Recorded activity coverage by participant
- Average steps by hour of day
- Daily steps versus calorie expenditure
- Participant and date filters

![Bellabeat Power BI Dashboard](images/power-bi%20dashboard%20screenshot.png)

---

## Project Structure

```text
bellabeat-smart-device-analysis/
│
├── excel/
│   └── Bellabeat_Analysis_Portfolio.xlsx
│
├── power-bi/
│   └── Bellabeat-Display.pbix
│
├── presentation/
│   └── Bellabeat_Case_Study_Presentation.pptx
│
├── report/
│   └── Bellabeat_CaseStudy_Portfolio_Final.docx
│
├── images/
│   └── power-bi dashboard screenshot.png
│
└── README.md
```