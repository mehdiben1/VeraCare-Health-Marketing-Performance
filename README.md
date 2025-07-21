# VeraCare Health Marketing Performance : 2019-2023

<details open>
  <summary>Table of Contents:</summary>
  
- [Project Background](#project-background)
- [Data Structure](#data-structure)
- [Executive Summary](#executive-summary)
- [Insights Deep Dive](#insights-deep-dive)
    - [Signup rate](#Signup-rate)
    - [Cost per signup](#Cost-per-signup)
    - [Click through rate](#Click-through-rate)
    - [Cost per impression](#Cost-per-impression)
      
- [Recommendations](#Recommendations)

</details>

# Project Background:
**VeraCare Health** is a U.S.-based medical insurance company that has served **thousands of customers** nationwide since its founding in **2017**. As a mission-driven insurer, VeraCare focuses on making preventative care and personalized health coverage more accessible through flexible plan offerings and educational outreach. In 2019,the company expanded its acquisition strategy by launching a series of new campaign categories covering topics like wellness tips, the affordability of their plans, and preventative care. Their customers can sign up for 4 different plans - bronze, silver, gold, and platinum - each with different premiums and claim coverage rates.

Now that they’re strategizing their marketing budget for the forthcoming year, the company would like to attain a better understanding of the effectiveness of these various types of campaigns, and how they relate to signups and subsequent patient claims. 
The budget is allocated to drive two primary objectives: 
1.  to increase **the number of customer signups.**
2.  to raise **awareness of VeraCare Health’s brand across the country.**

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
Our analysis of VeraCare Health’s historical marketing campaign data reveals these key insights:

- The average signup rate across all campaigns is 0.18%, with top-performing campaigns achieving **over 11× this rate.**
- Cost per impression (CPI) varies widely — **from as low as $0.01 to over $0.15** — indicating significant disparities in awareness efficiency.
- **Social Media** and **Email** platforms generate the highest number of signups **(7610 & 4130)**, while **TV campaigns** show poor performance **(494 signup)** despite high cost.
- Signup activity shows significant geographic variation, with some states demonstrating much higher campaign engagement than others which represents a potential opportunity for targeted marketing.

These insights highlight the potential to optimize marketing budget allocation by prioritizing high-conversion campaigns and platforms.

# Insights Deep Dive

## 1. Signup rate:

- Across campaign categories, **Health for All campaigns had the best-performing signup rate (2.08%)** and the second-highest number of signups (3.5K).
- Among the platforms, social media had the highest number of signups and a **slightly higher signup rate of 0.23%.**
- **Within Email, Health for All campaigns far outperformed** other campaign categories at a 3.72% signup rate compared to <0.06% for other categories.


## 2. Cost per signup:

- Across campaign categories, **Coverage Matters campaigns had by far the lowest cost per signup ($0.65)**, with Golden Years Security performing the worst in terms of cost and volume.
- **TV signups had the highest cost but also the lowest volume**, this may be related to poor attribution abilities for this channel.
- **Email and SEO both have similar costs per signups** ($4.04 and $5.24).


## 3. Click through rate:

- Across campaign categories, **Health For All had a high CTR (25.48%), which was more than double the average.** Family Plans had CTRs of near zero.
- **Email also outperformed other channels in terms of CTR (16.71%)**, though the number of impressions was third-lowest (2M).
- **Within Email, Health for All campaigns have the highest CTR at nearly 50%.**



## 4. Cost per impression:

- Across categories, **cost per impression was similar for Coverage Matters, Family Coverage Plan, Tailored Health Plans** campaigns ($0.003-$0.004).
- Note that while Health For All had the highest CTR, this category had the highest impression cost ($0.025).
- Social media had **the lowest cost per impression and the second highest clickthrough rate** after the mail platform. In contrast, **TV had the highest cost per impression with a click-through rate of 0%.**



# Recommendations:
Based on the insights and findings above, we would recommend the following:

## 1. Increase Signups:

- **Prioritize campaigns in the Health for All category** and campaigns that are run on email, as these not only have the highest signup rate but also the lowest cost per signup.
- **Reallocate TV budget to email campaigns**, as TV has the highest cost per signup but the lowest signup rate among all platforms.
- **Within email campaigns, consider removing the other categories** (Preventative Care News, Summer Wellness Tips, and Benefit Updates) and prioritizing Health for All + Email

## 2. Increase Brand Awareness:

- **Prioritize campaigns run on email and Social Media**, as these have high click through rate and low cost per impression, respectively.
- **Remove the TV campaign**, as it had the highest CPI and a CTR of 0%, indicating it was ineffective platform for generating awareness.
- **Continue investing in Health For All campaigns** for their high CTR, but investigate specific drivers for high impression cost.
- **Reallocate TV budget to Mail**, as impression costs are similar but CTR is almost 16x higher.


