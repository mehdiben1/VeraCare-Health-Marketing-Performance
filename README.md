# VeraCare Health Marketing Performance : 2019-2023

<details open>
  <summary>Table of Contents:</summary>
  
- [Project Background](#project-background)
- [Data Structure](#data-structure)
- [Executive Summary](#executive-summary)
- [Insights Deep Dive](#insights-deep-dive)
    - [Sales Trends](#Sales-Trends)
    - [Product Performance](#Product-Performance)
    - [Loyalty Program](#Loyalty-Program)
    - [Regional Comparisons](#Regional-Comparisons)
    - [Purchase platforms & Marketing Channel](#Purchase-platforms-&-Marketing-Channel)
      
- [Recommendations:](#Recommendations)

</details>

# Project Background:
**VeraCare Health** is a U.S.-based medical insurance company that has served **thousands of customers** nationwide since its founding in **2017**. As a mission-driven insurer, VeraCare focuses on making preventative care and personalized health coverage more accessible through flexible plan offerings and educational outreach. In 2019,the company expanded its acquisition strategy by launching a series of new campaign categories covering topics like wellness tips, the affordability of their plans, and preventative care. Their customers can sign up for 4 different plans - bronze, silver, gold, and platinum - each with different premiums and claim coverage rates.

Now that they’re strategizing their marketing budget for the forthcoming year, the company would like to attain a better understanding of the effectiveness of these various types of campaigns, and how they relate to signups and subsequent patient claims. 
The budget is allocated to drive two primary objectives: 
1.  to increase the number of customer signups.
2.  to raise awareness of VeraCare Health’s brand across the country.

So the goal of this project is to investigate the performance of marketing campaigns at VeraCare Health in order to surface recommendations on marketing budget allocation across future campaign categories.
**VeraCare Health**

# Data Structure:
The dataset consisted of **4 key tables**, provide a multi-angle view of marketing performance, customer acquisition and insurance utilization, with a total row count of **50K records**. Each table plays a distinct role in the analytical workflow:
- **Campaigns:** Contains campaign-level data such as campaign_category, campaign_type, cost, clicks, impressions, days_run, and the platform used.
- **Customers:** Stores customer-level records, including demographics (state), acquisition data (first_touch, signup_channel, campaign_id), and plan selection.
- **Claims:** Captures usage behavior including  claim_date, claim_amount, covered_amount, and product_name.
- **Date_Dim:** A time dimension used to filter and analyze trends by Date, Month, Day, and other time hierarchies.
  
Each row in the merged dataset represents a customer linked to a specific campaign, with the potential for associated claims.
The relationships between these tables are defined by keys **campaign_id** and **customer_id** as illustrated in the Entity Relationship Diagram (ERD) below:

![image](https://github.com/user-attachments/assets/f4f2e18f-84b5-4f66-84cc-3807ab4a71b9)


# Executive Summary

## Overview of Findings


# Insights Deep Dive
