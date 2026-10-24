# 📖 Data Dictionary — `Road_Accident_Data.xlsx`

Sheet: `Data` · 307,973 rows × 21 columns · One row = one reported road accident.

| # | Column | Type | Description | Example |
|---|---|---|---|---|
| 1 | `Accident_Index` | Text | Unique identifier for the accident record | `BS0000001` |
| 2 | `Accident Date` | Date | Date the accident occurred | `2021-01-01` |
| 3 | `Day_of_Week` | Text | Day of the week the accident occurred | `Thursday` |
| 4 | `Junction_Control` | Text | How the junction (if any) was controlled | `Give way or uncontrolled` |
| 5 | `Junction_Detail` | Text | Type of junction at/near the accident site | `T or staggered junction` |
| 6 | `Accident_Severity` | Text | Severity classification of the accident | `Slight`, `Serious`, `Fatal` (also contains 49 mislabeled `Fetal` rows — see README data-quality note) |
| 7 | `Latitude` | Decimal | Latitude of the accident location | `51.512273` |
| 8 | `Light_Conditions` | Text | Lighting conditions at the time of the accident | `Daylight`, `Darkness - lights lit` |
| 9 | `Local_Authority_(District)` | Text | Local authority/district where the accident occurred | `Kensington and Chelsea` |
| 10 | `Carriageway_Hazards` | Text | Any hazard present on the carriageway | `None`, `Other object on road` |
| 11 | `Longitude` | Decimal | Longitude of the accident location | `-0.201349` |
| 12 | `Number_of_Casualties` | Integer | Number of casualties in the accident | `1` |
| 13 | `Number_of_Vehicles` | Integer | Number of vehicles involved | `2` |
| 14 | `Police_Force` | Text | Police force that recorded the accident | `Metropolitan Police` |
| 15 | `Road_Surface_Conditions` | Text | Condition of the road surface | `Dry`, `Wet or damp`, `Frost or ice` |
| 16 | `Road_Type` | Text | Type of road where the accident occurred | `Single carriageway`, `Roundabout` |
| 17 | `Speed_limit` | Integer | Posted speed limit (mph) at the accident location | `30` |
| 18 | `Time` | Time | Time of day the accident occurred | `15:11` |
| 19 | `Urban_or_Rural_Area` | Text | Whether the accident occurred in an urban or rural area | `Urban`, `Rural` |
| 20 | `Weather_Conditions` | Text | Weather at the time of the accident | `Fine no high winds`, `Raining no high winds` |
| 21 | `Vehicle_Type` | Text | Type of vehicle(s) involved | `Car`, `Taxi/Private hire car` |

## Value distributions (full dataset)

**Accident_Severity**
- Slight: 263,280 (85.5%)
- Serious: 40,740 (13.2%)
- Fatal: 3,904 (1.3%)
- Fetal *(typo, treat as Fatal)*: 49 (<0.1%)

**Urban_or_Rural_Area**
- Urban: 198,532 (64.5%)
- Rural: 109,441 (35.5%)

**Road_Type (top 5)**
- Single carriageway: 230,612
- Dual carriageway: 45,467
- Roundabout: 20,929
- One way street: 6,197
- Slip road: 4,768

**Light_Conditions**
- Daylight: 227,286
- Darkness - lights lit: 60,093
- Darkness - no lighting: 16,528
- Darkness - lighting unknown: 2,924
- Darkness - lights unlit: 1,142

**Day_of_Week**
- Friday: 50,529 · Tuesday: 46,386 · Wednesday: 46,381 · Thursday: 45,649 · Monday: 43,918 · Saturday: 41,566 · Sunday: 33,544

**Road_Surface_Conditions**
- Dry: 208,967 · Wet or damp: 81,796 · Frost or ice: 12,078 · Snow: 4,758 · Flood over 3cm deep: 374
