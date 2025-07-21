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
- [Presentation Sample](#Presentation-Sample)
- [Appendix](#Appendix)

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

<img width="900" height="504" alt="image" src="https://github.com/user-attachments/assets/9da8d1c5-d1e9-4063-b935-3a08e2a04a13" />


# Insights Deep Dive

## 1. Signup rate:

- Across campaign categories, **Health for All campaigns had the best-performing signup rate (2.08%)** and the second-highest number of signups (3.5K).
- Among the platforms, social media had the highest number of signups and a **slightly higher signup rate of 0.23%.**
- **Within Email, Health for All campaigns far outperformed** other campaign categories at a 3.72% signup rate compared to <0.06% for other categories.

<img width="815" height="327" alt="image" src="https://github.com/user-attachments/assets/75dc2a6f-bc7a-4da0-adc8-68caf83f9260" />



## 2. Cost per signup:

- Across campaign categories, **Coverage Matters campaigns had by far the lowest cost per signup ($0.65)**, with Golden Years Security performing the worst in terms of cost and volume.
- **TV signups had the highest cost but also the lowest volume**, this may be related to poor attribution abilities for this channel.
- **Email and SEO both have similar costs per signups** ($4.04 and $5.24).

<img width="848" height="333" alt="image" src="https://github.com/user-attachments/assets/ca0062c5-0b30-48c1-a246-52736c6a72fb" />


## 3. Click through rate:

- Across campaign categories, **Health For All had a high CTR (25.48%), which was more than double the average.** Family Plans had CTRs of near zero.
- **Email also outperformed other channels in terms of CTR (16.71%)**, though the number of impressions was third-lowest (2M).
- **Within Email, Health for All campaigns have the highest CTR at nearly 50%.**

<img width="802" height="332" alt="image" src="https://github.com/user-attachments/assets/6b93248c-614e-4ba8-9e15-d65fc6c451eb" />


## 4. Cost per impression:

- Across categories, **cost per impression was similar for Coverage Matters, Family Coverage Plan, Tailored Health Plans** campaigns ($0.003-$0.004).
- Note that while Health For All had the highest CTR, this category had the highest impression cost ($0.025).
- Social media had **the lowest cost per impression and the second highest clickthrough rate** after the mail platform. In contrast, **TV had the highest cost per impression with a click-through rate of 0%.**

<img width="810" height="336" alt="image" src="https://github.com/user-attachments/assets/f897f495-a625-4508-ae7c-2f5cd8c58d09" />


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


# Presentation Sample:
The PowerPoint presentation presenting the above insights and recommendations for the marketing team can be found [here](https://github.com/mehdiben1/VeraCare-Health-Marketing-Performance/blob/main/Presentation/VeraCare%20Health%20Presentation.pdf). Some highlights are shown below:

<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/0ee8d59a-ec13-4924-b944-5df628dd94aa" />
<img width="1920" height="1080" alt="8" src="https://github.com/user-attachments/assets/2f5fa850-957d-46e3-95a3-0d145ac6bcf7" />
<img width="1920" height="1080" alt="13" src="https://github.com/user-attachments/assets/5dfc5287-fa50-4949-b66a-d9f6ca3124ab" />
<img width="1920" height="1080" alt="VeraCare Health Presentation" src="https://github.com/user-attachments/assets/9966215f-0d67-4cc8-b312-622302349ae3" />

# Appendix:

- For more details about the dataset and the data cleaning process check out [the Dataset Summary & Issue Log ](https://github.com/mehdiben1/VeraCare-Health-Marketing-Performance/blob/main/Scope%20of%20work%20%26%20Issues%20log/Data%20Cleaning%20Process%20-%20VeraCare%20Health%20Data%20set.pdf)

  
- Check out the full Power Bi report [here](https://github.com/mehdiben1/VeraCare-Health-Marketing-Performance/blob/main/Power%20Bi%20Dashboard/VeraCare%20Health.pbix))
