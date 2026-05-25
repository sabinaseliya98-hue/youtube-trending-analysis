# YouTube Trending Videos — Data Cleaning & Analysis

## Project Overview
This project performs data cleaning and exploratory analysis on the 
US YouTube Trending Videos dataset using Microsoft Excel. The goal 
was to identify data quality issues, clean the dataset, and extract 
meaningful insights about trending video patterns.

## Tools Used
- Microsoft Excel
  - Pivot Tables
  - COUNTIF, COUNTBLANK, AVERAGE, MEDIAN
  - Conditional Formatting
  - Text to Columns
  - Remove Duplicates

## Dataset
- Source: [Kaggle — YouTube Trending Videos](https://www.kaggle.com/datasets/datasnaek/youtube-new)
- Country: United States (USvideos.csv)
- Original Rows: 40,949
- Clean Rows after deduplication: 6,282
- Total Columns: 16

## Data Quality Issues Found

| # | Column | Problem | Action Taken |
|---|---|---|---|
| 1 | video_id | 397 invalid #NAME! entries | Left as is — removed in deduplication |
| 2 | trending_date | Wrong format (YY.DD.MM) | Fixed using Text to Columns |
| 3 | publish_time | Complex timestamp format | Excluded — not needed |
| 4 | tags | Messy mixed language values | Excluded — not needed |
| 5 | video_id | 34,667 duplicate rows (84.6%) | Removed duplicates |

## Missing Values Summary

| Column | Blank Count |
|---|---|
| video_id | 0 |
| trending_date | 0 |
| title | 0 |
| channel_title | 0 |
| category_id | 0 |
| views | 0 |
| likes | 0 |
| dislikes | 0 |
| comment_count | 0 |

## Key Findings

- **Top 3 Categories:** Entertainment, Music, Howto & Style
- **Average Views:** 752,097 — skewed high by viral outliers
- **Median Views:** 271,274 — more realistic performance benchmark
- **Most Viral Video:** 39,349,927 views
- **Outlier Videos:** 432 videos (6.9%) with views above 2,256,291
- **Key Insight:** Average views is 3x higher than median — indicating 
  a small number of viral videos significantly skew the data

## Business Recommendations

1. Use **median views** instead of average for realistic benchmarking
2. Treat viral outlier videos separately in engagement analysis
3. Focus content strategy on **Entertainment and Music** — highest trending categories
4. Map category IDs to category names for better readability in reporting

## Dashboard Preview
![Dashboard](screenshots/conditional_formatting.png)

## Project Structure
youtube-trending-analysis/
│
├── USvideos.csv                   ← Raw dataset
├── YouTube_Analysis.xlsx          ← Cleaned Excel workbook
├── Data_Quality_Report.pdf        ← 1 page data quality report
├── README.md                      ← Project documentation
└── screenshots/
    └── conditional_formatting.png ← Outliers highlighted in red

## What I Learned
- How to identify and handle duplicate data
- How to fix date formatting issues using Text to Columns
- How mean vs median reveals outliers in data
- How to use conditional formatting to visually highlight outliers
- How to build a frequency table using COUNTIF
- How to write a professional data quality report

## Connect With Me
- LinkedIn: https://www.linkedin.com/in/sabina-neva-4638423b5/
- GitHub: https://github.com/sabinaseliya98-hue
