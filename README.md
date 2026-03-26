# Applicant Behavior Analysis

> An end-to-end web analytics project that simulates and analyzes how applicants interact with Internee.pk — tracking user behavior across a 6-stage application funnel, identifying drop-off bottlenecks, and delivering actionable conversion insights using Python and SQL-style queries.

\---

## Overview

This project was completed as part of a **Data Analyst Internship at** [**Internee.pk**](https://internee.pk). The goal was to analyze how applicants interact with the Internee.pk platform — from their first visit to final application submission — and identify exactly where and why users drop off during the process.

This type of analysis is called **funnel analysis** or **conversion rate optimization (CRO)** and is one of the most valuable skills in product analytics, growth analytics, and UX research. Companies like Google, Meta, and every major e-commerce platform use this exact methodology to improve their user experience.

\---

## Objectives

* ✅ Simulate realistic applicant behavior data across **6 funnel stages**
* ✅ Track user behavior including page visits, application flow, and exit points
* ✅ Use **SQL-style queries with pandas** to extract meaningful insights
* ✅ Identify the **biggest bottleneck** where applicants drop off
* ✅ Analyze behavior by **device type**, **traffic source**, and **internship category**
* ✅ Deliver a **5-panel professional dashboard** with business recommendations

\---

## Dataset

The dataset was **custom-built** to simulate real-world applicant session data across 4 months.

|Column|Description|
|-|-|
|`session\_id`|Unique ID for each user session|
|`user\_id`|Unique user identifier|
|`age\_group`|Age bracket of the applicant|
|`device\_type`|Device used (Mobile / Desktop / Tablet)|
|`traffic\_source`|How the user found the site (Google, LinkedIn, Social Media, etc.)|
|`homepage\_visited`|1 = visited homepage, 0 = did not|
|`listings\_browsed`|1 = browsed internship listings|
|`detail\_page\_viewed`|1 = opened a specific internship detail page|
|`registration\_attempted`|1 = attempted to register or sign in|
|`form\_started`|1 = started filling the application form|
|`application\_submitted`|1 = successfully submitted an application|
|`time\_on\_\*\_sec`|Time spent (in seconds) on each page|
|`exit\_page`|The last page the user visited before leaving|
|`visit\_date`|Date of the session|
|`internship\_category`|Department the internship belongs to|

**Dataset Stats:**

* Total Sessions: **210 rows**
* Date Range: January 2024 — April 2024
* Devices: Mobile, Desktop, Tablet
* Traffic Sources: Google Search, LinkedIn, Social Media, Direct, Email
* Departments: Data Science, Software Engineering, Marketing, Finance, HR

\---

## Tech Stack

|Tool|Purpose|
|-|-|
|**Python 3.8+**|Core programming language|
|**Pandas**|Data loading, SQL-style querying, aggregation|
|**Matplotlib**|Chart creation and multi-panel dashboard|
|**Seaborn**|Enhanced chart aesthetics|
|**Google Colab**|Cloud-based notebook environment|

\---

## Project Structure

```
applicant-behavior-analysis/
│
├── Applicant\_Behavior\_Analysis.ipynb    # Main Google Colab notebook
├── applicant\_behavior.csv               # Raw dataset (210 sessions)
├── behavior\_analysis\_results.csv        # Enriched output with completion labels
├── funnel\_summary.csv                   # Funnel conversion table
├── behavior\_dashboard.png               # 5-panel visualization dashboard
└── README.md                            # Project documentation (you are here)
```

\---

## Application Funnel

The project tracks users across these 6 stages of the Internee.pk application journey:

```
Homepage Visit
      ↓ (\~72% proceed)
Browse Listings
      ↓ (\~58% proceed)
View Internship Detail
      ↓ (\~41% proceed)
Register / Sign In
      ↓ (\~29% proceed)
Fill Application Form       ← Biggest drop-off point
      ↓ (\~18% proceed)
Application Submitted  
```

> Each stage is tracked as a binary column (1 = completed, 0 = dropped off). This structure mirrors exactly how Google Analytics and product analytics tools like Mixpanel and Amplitude track user funnels in real products.

\---

## How to Run

### Option 1 — Google Colab (Recommended)

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Click **File → Upload Notebook** and upload `Applicant\_Behavior\_Analysis.ipynb`
3. Upload `applicant\_behavior.csv` using the 📁 left sidebar
4. Click **Runtime → Run All**
5. All charts and results will generate automatically

### Option 2 — Run Locally

**1. Clone this repository**

```bash
git clone https://github.com/YOUR\_USERNAME/applicant-behavior-analysis.git
cd applicant-behavior-analysis
```

**2. Install dependencies**

```bash
pip install pandas matplotlib seaborn
```

**3. Launch the notebook**

```bash
jupyter notebook Applicant\_Behavior\_Analysis.ipynb
```

\---

## Results \& Visualizations

### Funnel Conversion Summary

|Stage|Users|Conversion Rate|
|-|-|-|
|Homepage Visit|210|100%|
|Browse Listings|\~152|\~72%|
|View Detail Page|\~122|\~58%|
|Registration|\~86|\~41%|
|Started Form|\~61|\~29%|
|**Submitted**|**\~38**|**\~18%**|

> \*Exact numbers depend on dataset. Run the notebook to see your results.\*

### Dashboard Preview

The project generates a **5-panel visual dashboard** including:

* **Horizontal Funnel Chart** — Users at each stage with conversion rates labeled
* **Pie Chart** — Distribution of exit pages (where users leave)
* **Bar Chart** — Conversion rate by traffic source (color-coded by performance)
* **Grouped Bar Chart** — Completed vs dropped off by device type
* **Horizontal Bar Chart** — Submitted applications by internship department

\---

## Key Insights \& Recommendations

|#|Insight|Recommendation|
|-|-|-|
|1|Only \~18% of visitors complete an application|Set a 25%+ conversion target and A/B test the form|
|2|The application form is the biggest drop-off point|Reduce fields, add a progress bar, enable "Save \& Continue Later"|
|3|LinkedIn drives the highest quality traffic|Increase LinkedIn marketing investment|
|4|Mobile users have the highest drop-off rate|Audit and optimize the form for mobile screens|
|5|Data Science receives the most applications|Feature it prominently on the homepage|

\---

## Author

**Ayna Khan**
Data Analyst Intern — Internee.pk

