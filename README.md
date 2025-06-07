# 🩺 BI Performance Dashboard – Power BI/ SQL/ Python

This dashboard is a comprehensive performance tracker for PrEP (Pre-Exposure Prophylaxis) program participants, offering visibility into patient engagement, appointment adherence, prescription fills, medication types, and overall care continuity.

![Sample_8_page-0001](https://github.com/user-attachments/assets/94415b5a-e7be-448f-8208-2b426f6e6ee2)
![Sample_8_page-0002](https://github.com/user-attachments/assets/d0533dc5-bf48-43bd-8258-66904b612efc)
![Sample_8_page-0003](https://github.com/user-attachments/assets/6b050566-b848-45d4-b286-bcc07738ae44)
![Sample_8_page-0004](https://github.com/user-attachments/assets/b9a5d403-bbea-410c-919d-724bf9d6cfee)

---

## 🔍 Purpose

The primary goal of this dashboard is to:
- Monitor **patient lifecycle** from first appointment to medication fill and follow-up.
- Identify trends in **appointment completion, dropouts, and medication reversals**.
- Track **prescription shipment wait times**, drug adherence, and fill percentages.
- Enable clinics and providers to **optimize care engagement strategies**.

---

## 🎯 Business Impact

- Tracked **9,960 total MRNs**, identifying **5,621 dropouts** and **4,339 in-care patients**.
- Improved visibility on **first filled rates post-appointment**, enabling targeted re-engagement.
- Reduced medication fill delays by surfacing issues in **shipment wait times** (e.g., 531 days peak delay).
- Supported clinical outreach by highlighting **reverse fill trends** in the first three prescriptions.
- Informed leadership with data slices by **clinic, provider, zip code, age, and gender**.

---

## 🛠️ How It Was Created

### 📊 Power BI
- Connected to patient records and pharmacy datasets.
- Created interactive visuals:
  - Appointment status over time
  - Prescription fill patterns
  - Reversal statistics
  - Drug types (e.g., % on **Descovy**)
  - Fill shipment wait time averages
- Filters included: year, quarter, month, age group, clinic, gender, provider, and location
- DAX used for calculating:
  - Fill % after appointment
  - Reversal counts
  - Dropout vs. in-care segmentations
  - Average engagement duration per patient

---

### 🐍 Python Integration (Preprocessing + Analytics)

Python was used for **data wrangling** and **enrichment** before loading into Power BI.

Tasks handled by Python:
- Filled missing values in appointment/fill dates.
- Grouped patients by drug type and computed % on Descovy.
- Calculated average time to fill and engagement duration.
- Flagged anomalies (e.g., extreme shipment delays > 300 days).

---

## 📌 Key Insights
- 80%+ fill rate after completed appointments in recent years (post-2022)
- Avg. fill shipment delay is around 50 days, with historical spikes up to 531 days
- Descovy remains the most prescribed drug in 2024 (~71% of first fills)
- Reversals in the first three fills increased in 2023 compared to prior years
- 5,621 out of 9,960 MRNs dropped care — highlighting the need for re-engagement protocols
- Consistent drop in first completed appointments during 2020 (COVID effect)

---

## 🧰 Tools Used
- Power BI:	Interactive dashboard and filtering
- Excel / CSV:	Raw source data from clinics and pharmacies
- MySQL: Data Table extract, views creation, CTEs
- Python (pandas, numpy)	Preprocessing, anomaly detection, cohort analysis
