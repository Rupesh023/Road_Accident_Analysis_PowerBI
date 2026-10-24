# 🚦 Road Accident Analysis (UK, 2021–2022)

An end-to-end **Power BI** project analysing 300K+ UK road traffic accident records to uncover patterns in accident severity, location, timing, and road/weather conditions — built to support road-safety planning and resource allocation.



---

## 📌 Project Overview

This repository contains a Power BI dashboard built on a real-world UK road accident dataset (2021–2022). The report is designed as a single, data-dense **executive summary page** that lets a road-safety analyst or policymaker quickly answer:

- How many accidents and casualties happened this year, and how does that compare to the previous year?
- How severe are accidents (Fatal / Serious / Slight) and how is that trending month over month?
- Where do accidents cluster geographically (urban vs. rural, and on the map)?
- What conditions (lighting, road type) are most associated with casualties?

> 📎 The original raw dataset and the `.pbix` Power BI file are both included in this repo so the project can be reproduced or extended end-to-end.

---


## 🎯 Objectives

1. Consolidate raw, row-level accident data into a clean analytical model.
2. Build KPI cards for at-a-glance monitoring (total accidents, total casualties, casualties by severity).
3. Compare the current year's casualty trend against the prior year on a monthly basis.
4. Break down casualties by **urban/rural split**, **lighting conditions**, and **road type**.
5. Plot accident locations geographically using latitude/longitude.
6. Make the report interactive via slicers so users can filter by relevant dimensions.

---

## 🗂️ Repository Structure

```
Road-Accident-Analysis/
│
├── reports/
│   └── Road_Accident_Analysis.pbix     # Power BI report (data model + dashboard)
│
├── data/
│   └── Road_Accident_Data.xlsx         # Raw source dataset (307,973 records)
│
├── docs/
│   └── data-dictionary.md              # Column-by-column explanation of the dataset
│
├── images/
│   └── dashboard-preview.png           # (Add your own) screenshot of the report
│
├── README.md                           # You are here
├── LICENSE                             # MIT License
└── .gitignore                          # Ignores Power BI temp/lock files
```

---

## 📊 Dataset

| | |
|---|---|
| **Source file** | `Road_Accident_Data.xlsx` |
| **Records** | 307,973 accident rows |
| **Columns** | 21 |
| **Time period** | 1 Jan 2021 – 31 Dec 2022 |
| **Granularity** | One row per reported accident |
| **Geography** | United Kingdom (police-force & local-authority level, with lat/long) |

Full column-level documentation is in **[`docs/data-dictionary.md`](docs/data-dictionary.md)**. In short, each row captures: when and where the accident happened, how severe it was, how many people/vehicles were involved, and the environmental conditions at the time (light, weather, road surface, speed limit, junction type, road type).

### ⚠️ Known data-quality notes
- `Accident_Severity` contains 49 rows labelled **`Fetal`**, which is almost certainly a data-entry typo for **`Fatal`**. These were kept as-is in the raw file for transparency but should be corrected (or merged into `Fatal`) before any severity-based analysis — this is called out explicitly so the fix is auditable.
- A small number of geographic fields (lat/long) are missing for a handful of records and are excluded automatically by the map visual.

---

## 🧮 Key Insights

*(Computed directly from the dataset — these are the numbers the dashboard surfaces.)*

- **307,973 accidents** were recorded across the two-year period, resulting in **417,883 total casualties**.
- **Severity split:** Slight – 85.5% (263,280) · Serious – 13.2% (40,740) · Fatal – 1.3% (3,904).
- **Urban vs. Rural:** 64.5% of accidents occurred in **urban** areas vs. 35.5% in **rural** areas — but rural accidents tend to skew more severe, a common pattern driven by higher speeds.
- **Road type:** Single carriageways account for ~75% of all accidents (230,612), followed by dual carriageways (~15%) and roundabouts (~7%).
- **Lighting:** ~74% of accidents happened in **daylight**, with ~20% occurring in darkness (lit or unlit roads combined).
- **Day of week:** **Friday** is the highest-accident day (50,529), while **Sunday** is the lowest (33,544) — consistent with higher weekday/commute traffic volume.
- **Vehicle type:** **Cars** are involved in the vast majority of accidents (239,794), followed by goods vans and motorcycles.
- **Weather:** Most accidents (~79%) happen in fine weather with no high winds — a reminder that *volume of driving* in good conditions outweighs the per-trip risk of bad weather.

---

## 📈 Dashboard Walkthrough

The report is a single interactive page containing:

| Visual | Purpose |
|---|---|
| **KPI Cards** – Total CY Accidents, Total CY Casualties, Fatal/Serious/Slight Casualties | Instant headline numbers for the current year |
| **Area Chart** – CY Casualties vs. PY Casualties (Monthly Trend) | Year-over-year trend comparison to spot seasonal spikes |
| **Donut Chart** – Casualties by Urban/Rural | Geographic split of casualty severity |
| **Donut Chart** – Casualties by Light Conditions | Impact of visibility on casualty counts |
| **Bar Chart** – Casualties by Road Type | Which road types are riskiest |
| **Map** – Casualties by Location | Geospatial clustering of accidents (lat/long) |
| **Slicer(s)** | Lets the viewer filter the whole page by key dimensions |

---

## 🛠️ Tools & Skills Used

- **Power BI Desktop** — data modeling, DAX measures, and dashboard design
- **Microsoft Excel** — source data (raw export)
- **DAX** — current year / prior year comparison measures, severity splits
- **Data visualization** — cards, donut charts, area chart, bar chart, map, slicers
- **GitHub** — version control & project documentation

---

## 🚀 How to Use This Project

1. **Clone the repo**
   ```bash
   git clone https://github.com/<your-username>/Road_Accident_Analysis_PowerBI.git
   cd Road_Accident_Analysis_PowerBI
   ```
2. **Open the report**
   - Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free, Windows only).
   - Open `reports/Road_Accident_Analysis.pbix`.
3. **Refresh the data (optional)**
   - If you update `data/Road_Accident_Data.xlsx`, go to **Home → Refresh** in Power BI Desktop to pull in the changes.
4. **Explore**
   - Use the slicer(s) and click into chart segments to cross-filter the whole page.

---

## 🔭 Future Scope

- Add more report pages: a **time/hour-of-day heatmap**, a **vehicle-type deep dive**, and a **junction/speed-limit risk analysis** page.
- Publish the report to the **Power BI Service** and embed a live link/screenshot here.
- Automate data refresh via **Power BI Gateway** if connected to a live data source.
- Clean the `Fetal` → `Fatal` typo and other data-quality issues at the source and re-publish.

---

## 👤 Author

**[Your Name]**
📧 rupeshkumar230201@gmail.com · 🔗 [LinkedIn](www.linkedin.com/in/rupesh-kumar-0056351ba) · 🐙 [GitHub](https://github.com/Rupesh023)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). The dataset is used for educational/portfolio purposes.
