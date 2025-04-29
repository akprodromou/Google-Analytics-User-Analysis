# Google Analytics User Behavior Analysis

## Project Overview

This project analyzes anonymized Google Analytics session data from a fictional e-commerce store, using SQL queries in BigQuery. The objective is to understand user behavior, traffic sources, engagement patterns, and key drivers of transactions and revenue.

## Dataset

- **Source:** `bigquery-public-data.google_analytics_sample.ga_sessions_20170801`
- **Scope:** One day of session data (August 1, 2017)
- **Fields:** Traffic source, device and browser information, geo-location, pageviews, transactions, revenue, user behavior (new vs returning), and e-commerce actions.

## Key Business Questions

- Which traffic sources bring the most users and/or revenue?
- What device types are most common among buyers?
- Are new users or returning users more likely to make a purchase?
- Which countries generate the most sessions or revenue?
- Can we predict which sessions are more likely to lead to a transaction?

## Methods

- SQL queries using CTEs, subqueries, aggregation functions, and array unnesting.
- Exploratory Data Analysis (EDA) through aggregation and descriptive statistics.
- Funnel exploration for conversion paths.

## Main Findings

### Traffic Sources
- **Direct traffic** generated the most sessions and revenue.
- **Mail.google.com** generated minor revenue.
- Most other sources (referral, organic, paid) generated little to no revenue.

### Device Analysis
- **Desktop devices** dominated sessions (~2/3 of all sessions).
- **Mobile and tablet users** represented the remaining third but showed high engagement.

### User Type Analysis
- **Returning visitors** converted 8.5 times more than new visitors.
- Returning visitors generated 11.3 times more revenue per session.

### Geographic Insights
- **United States** was the main market for both sessions and revenue.
- **Finland** had the highest conversion rate among smaller markets.

### Bounce and Landing Page Analysis
- Referral and organic mediums had the highest bounce rates (>60%).
- Specific landing pages had bounce rates exceeding 65%, suggesting UX or content alignment issues.

### Session Duration
- Higher session durations correlated with higher conversion probabilities.
- Sources like mail.google.com showed exceptional session engagement.

### Event and Funnel Analysis
- Higher event counts per session (especially "Add to Cart" and "Quickview Click") strongly correlated with transaction completion.
- Only 35% of users who interacted with a product added it to the cart, and 20% of those completed a purchase.

## Recommendations
- Strengthen **customer retention** strategies to maximize the value of returning visitors.
- Improve landing pages with high bounce rates through UX testing and content alignment.
- Optimize mobile and tablet shopping experiences.
- Target high-engagement sources and channels for future marketing efforts.
- Focus on reducing friction in the checkout process to increase cart-to-purchase conversion.

## Created using
- SQL (Google BigQuery)
- Jupyter Notebooks (with some Python for additional data exploration)
- Google Cloud Platform (BigQuery public datasets)

## Folder Structure

```bash
/
|-- notebooks/
|   |-- google_analytics_project.ipynb
|-- README.md
|-- requirements.txt
```

