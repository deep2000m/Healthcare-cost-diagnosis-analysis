# 🏥 Healthcare Data Analysis & Billing Insight Dashboard

## 📘 Project Overview

This project focuses on analyzing hospital data to uncover trends in diagnoses, medication utilization, insurance behavior, and billing anomalies. The goal is to support cost optimization, resource planning, and data-driven operational decisions.

Developed using Power BI, the dashboard enables dynamic exploration of hospital performance across clinical, financial, and temporal dimensions. Stakeholders can interactively slice the data by diagnosis, insurer, time period, test results, and medication to gain deeper operational and strategic insights.

___________________________

## 📊 Key Dashboard Highlights

![Image](https://github.com/user-attachments/assets/ab220e96-da8f-4b14-ba0b-912ec57625fe)

The dashboard enables filtering, comparison, and drill-down views across the following domains:

✅ Diagnosis Prevalence

💊 Medication Demand Patterns

💸 Billing Trends & Anomalies

🏥 Hospital Performance by ALOS & Cost

📆 Monthly Admission Patterns

🏦 Insurance Provider Utilization

🧪 Test Result Outcomes vs. Billing

> 🎛 Interactive charts and slicers allow stakeholders to explore hidden patterns and detect inefficiencies or operational

___________________________

## 🔎 Key Insights

1. *Most Common Diagnosis*: Arthritis is the most frequently diagnosed condition.

2. *ALOS*: The average length of stay is 16 days.

3. *Billing Cost Drivers*:
   - Obesity-related patients have the *highest average billing amount*.
   - Top hospitals report average billing between ₹51,000 and ₹52,000.

4. *Insurance*: Cigna is the most frequently used insurance provider, followed by Blue Cross.

5. *Test Results: "Inconclusive" results are linked to the **highest average billing*, indicating potential inefficiencies.

6. *Medication Demand*: Lipitor is in high demand; Ibuprofen is also frequently used.

7. *Correlation Insights*:
   - Stay duration vs. patient age: -0.0082 (negligible)
   - Stay duration vs. billing: -0.0056 (negligible)

8. *Admissions by Month: Significant spike from **May to September*.

___________________________

## ❓ Exploratory Questions

### 1. Why is Cigna the most frequently used insurance provider?

Cigna appears as the *most commonly used insurance provider* in the dataset, maintaining the top spot in terms of claim volume across multiple hospitals.

Key factors that may explain this dominance:

- *Extensive hospital network*: Cigna may have contracts with a broader range of in-network hospitals, making it the default option for patients.
- *Patient preference or employer sponsorship*: If a significant portion of patients are covered through employer health plans, Cigna could be the standard provider in those networks.
- *Higher claim acceptance rate*: Hospitals and patients may prefer Cigna due to quicker reimbursements or fewer claim denials.
- *Historic affiliation with top-performing hospitals*: Some of the highest-billing hospitals may have long-term partnerships with Cigna, reinforcing its usage.

> 🔍 Conclusion: Cigna’s consistent presence across high-billing hospitals and departments may be a result of strong payer-provider relationships, wide coverage, and possibly fewer administrative rejections.

---

### 2. Why do "Inconclusive" test results lead to the highest average billing amount?

The analysis revealed that patients with *inconclusive test results* had the *highest average billing amount*, exceeding those with positive or negative results.

Possible explanations include:

- *Repeat testing and extended diagnostics*: When results are inconclusive, hospitals often run additional tests, extending the length of stay and driving up costs.
- *Specialist referrals*: Inconclusive findings may lead to consultations with neurologists, radiologists, or other specialists, increasing procedural billing.
- *Overtesting or protocol inefficiency*: Some facilities may lack efficient diagnostic paths, leading to a loop of tests with no clear outcome — a potential flag for operational inefficiency.
- *Billing loopholes*: There’s a possibility that inconclusive results are being used as a billing code for extended procedures without clear clinical justification.

> 🔍 Conclusion: Inconclusive results may be symptomatic of diagnostic inefficiencies or strategic testing behaviors. This warrants *policy-level review* to minimize unnecessary cost buildup while maintaining diagnostic integrity.

___________________________


##💡 Recommendations

1. Prioritize targeted care pathways and resource planning for patients aged 50+.

2. Strengthen partnerships with BlueCross and other secondary insurers to optimize claim cycles.

3. Investigate high billing tied to inconclusive test results to rule out fraud or diagnostic inefficiencies.

4. Ensure inventory readiness for high-demand medications like Lipitor and Ibuprofen.

5. Prepare for seasonal demand spikes (May–September) with proactive capacity and staffing planning.

___________________________

## 📊 Detailed Visual Analysis

### C1. Diagnosis & ALOS
Arthritis is the most commonly diagnosed condition.
ALOS stands at ~16 days.
![Image](https://github.com/user-attachments/assets/b229da33-71e3-4414-b9ad-7d366a7a4652)


### C2. Test Results vs. Billing
"Inconclusive" test results correlate with the *highest billing*, indicating inefficiency or anomaly.

![Image](https://github.com/user-attachments/assets/e2d9a64d-cd3b-4c77-ac6f-608eb724d5eb)



### C3. Insurance & Medication Demand
Cigna dominates the insurance market. 
Lipitor and Ibuprofen are top-demand medications.
![Image](https://github.com/user-attachments/assets/e8765c9a-274f-4a28-8963-0e5876562f42)



### C4. Monthly Admission Trend
Noticeable spike in admissions between *May and September* each year.
![Image](https://github.com/user-attachments/assets/41109325-5534-450a-b185-8f64376f47fa)




___________________________

# 💼 Tools & Tech

- *Power BI* (dashboard and data modeling)
- Excel (ETL and data prep)
- DAX (custom measures and KPIs)

___________________________

### Key formulae and calculation (most relevant ones)

**Mostcommon = 
VAR summarytable =
    SUMMARIZE(
        healthcare_dataset,
        healthcare_dataset[Medical Condition],
        "countmedicalcondition", COUNTROWS(healthcare_dataset)
    )
VAR maxcount = MAXX(summarytable, [countmedicalcondition])
RETURN
    CALCULATE(
        MAX(healthcare_dataset[Medical Condition]),
        FILTER(summarytable, [countmedicalcondition] = maxcount)
    )**


___________________________

# 📈 Analytical Techniques

Aggregation and filtering by diagnosis, test result, and insurer

Correlation analysis (Pearson)

Custom measures for ALOS, average billing, and demand frequency

Identification of high-impact cost drivers

___________________________

# ✅ Summary

This project demonstrates the use of healthcare data analytics to derive operational and clinical insights. With a focus on real-world metrics such as length of stay, billing variance, and diagnostic efficiency, the dashboard is designed to support stakeholders in hospital administration, clinical quality teams, and insurance coordination.

____________________________

# 🚀 How to Use

1. Download the .pbix file from this repository.
2. Open it using Power BI Desktop (free from Microsoft).
3. Explore the dashboard
4. No installation or code setup is required — just open and explore.
> 💡 Tip: Use “Focus Mode” in Power BI to expand visuals for deeper analysis.


📬 Contact

Created by: Deepak Das
📧  deepakdas909@gmail.com
🔗 Portfolio: 
💼  Linkdin
