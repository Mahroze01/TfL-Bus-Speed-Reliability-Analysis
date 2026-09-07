# TfL Bus Speed & Reliability Analysis

## Project Overview

This project analyses Transport for London (TfL) bus speed data to identify routes and reporting periods associated with slower or more variable bus performance.

The project uses Power BI and Power Query to transform and analyse historical TfL bus speed data across multiple years, creating an interactive dashboard that highlights potential areas for further investigation.

The analysis focuses on a practical business question:

> **Which bus routes and reporting periods show slower or more inconsistent bus speed patterns, and where should further investigation be prioritised?**

---

## Business Problem

Bus performance can vary significantly between routes and over time. Identifying routes with consistently low speeds or high levels of variation can help transport planners determine where further investigation may be required.

This project aims to answer:

- Which bus routes have the lowest average speeds?
- How do these routes perform across different years?
- How does average bus speed change over time?
- Which routes experience the greatest variation in speed?
- Where could further operational investigation be prioritised?

The purpose of this analysis is to identify patterns and potential areas for investigation rather than establish the causes of changes in bus speed.

---

## Dashboard

<img width="1322" height="746" alt="Dashboard" src="https://github.com/user-attachments/assets/920cccb4-708b-413f-9622-06eb5a46522a" />


The Power BI dashboard provides an overview of:

- Overall average bus speed
- 10 slowest bus routes
- Yearly comparison of slow-performing routes
- Average bus speed trends by reporting period
- 10 most variable bus routes

---

## Key Findings

### Overall Bus Speed

The overall average bus speed across the analysed data is approximately:

**10.3 mph**

This provides a benchmark for comparing performance across routes and reporting periods.

### Slowest Bus Routes

The dashboard identifies the 10 routes with the lowest average bus speeds.

These routes can be used as a starting point for further investigation into potential operational or network-related factors affecting bus performance.

### Performance Over Time

Average bus speed fluctuates across reporting periods rather than remaining constant.

The trend analysis highlights periods where network-wide average speed increases or decreases, providing opportunities for further investigation.

### Year-on-Year Comparison

Comparing the slowest routes across different years helps identify whether lower performance is relatively consistent or varies over time.

### Most Variable Routes

A speed range measure was used to identify routes with the greatest difference between their highest and lowest recorded speeds.

**Route 399** stands out as having substantially higher speed variation than the other routes highlighted in the analysis.

---

## Business Recommendations

Based on the analysis, several actions could be considered:

### 1. Investigate consistently slow routes

Routes that repeatedly appear among the slowest could be prioritised for further investigation into factors such as congestion, road conditions, bus-stop activity and network characteristics.

### 2. Investigate highly variable routes

Routes with large differences between their highest and lowest recorded speeds could be examined to understand the reasons behind their variation.

### 3. Monitor performance trends

Reporting-period trends could be monitored to identify recurring periods of declining bus speeds.

### 4. Combine with additional datasets

The analysis could be strengthened by combining bus speed data with:

- Traffic congestion data
- Roadworks and road closure data
- Passenger demand
- Bus-stop locations
- Timetable adherence
- Journey-time data
- Weather conditions
- Traffic incidents

This would allow the analysis to move from identifying **where performance changes** to investigating **why performance changes**.

---

## Tools & Technologies

- **Power BI** – Dashboard development and data visualisation
- **Power Query** – Data cleaning and transformation
- **DAX** – Measures and analytical calculations
- **Excel** – Source data
- **GitHub** – Project documentation and version control

---

##  Data Preparation

Power Query was used to prepare the TfL data for analysis.

Key transformation steps included:

1. Importing annual TfL bus speed datasets
2. Removing unnecessary rows and columns
3. Standardising column names
4. Reshaping reporting-period data
5. Combining multiple years into a single dataset
6. Creating Year and Period Number fields
7. Creating a Reporting Period field
8. Handling invalid or missing observations
9. Creating analytical measures in Power BI

---

##  Key Metrics

### Average Bus Speed

``` DAX
Average Bus Speed =
AVERAGE('Bus Speed Data'[Mean Bus Speed])

Maximum Bus Speed =
MAX('Bus Speed Data'[Mean Bus Speed])

Minimum Bus Speed =
MIN('Bus Speed Data'[Mean Bus Speed])

Speed Range =
[Maximum Bus Speed] - [Minimum Bus Speed]




