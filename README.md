## Clustering Data to Unveil Maji Ndogo's Water Crisis (Part 2)

---

### Table of Contents
1. [Project Overview](#project-overview)  
2. [Sources of Data](#sources-of-data)  
3. [Data Cleaning](#data-cleaning)  
   - [1. Cleaning the Data](#1-cleaning-the-data)  
   - [2. Analyzing Locations](#2-analyzing-locations)  
   - [3. Diving into the Sources](#3-diving-into-the-sources)  
   - [4. Start of a Solution](#4-start-of-a-solution)  
   - [5. Analyzing Queues](#5-analyzing-queues)  
4. [Insights](#insights)  
5. [Recommendations](#recommendations)  

---

### Project Overview
In this second phase of the integrated project, we take a deeper analytical dive into Maji Ndogo’s water crisis. By leveraging a wide range of analytical functions, including advanced window functions, we aim to extract actionable insights from the data tables.

Our objectives include:
- Deepening our exploration of the dataset to reveal hidden patterns and trends.  
- Moving beyond isolated figures to identify meaningful clusters and groupings.  
- Gaining a panoramic view by clustering data, allowing us to uncover broader narratives.  
- Unveiling hidden correlations embedded within the dataset.  
- Paying close attention to the varied data structures. Although challenging, these structures are rich in insight and potential.  

As we refine and process the data, we reveal deeper layers of understanding critical for data-driven decision-making.

---

### Sources of Data
- `md_water_services`

---

### Data Cleaning

#### 1. Cleaning the Data
Before conducting meaningful analysis, we performed initial cleaning tasks:
- **Added Missing Emails:** The employee table lacked email addresses, which are needed for sharing reports. We updated the table to include them.  
- **Standardized Phone Numbers:** Phone numbers were stored as inconsistent strings. We cleaned and reformatted them for consistency and accuracy.  

#### 2. Analyzing Locations
The location data revealed that most water sources are located in small, rural communities scattered across Maji Ndogo. By counting records per province, we confirmed that all regions were fairly represented in the survey.

**Key insights from the location table:**
1. The entire country was thoroughly canvassed, reflecting the actual situation on the ground.  
2. Approximately 60% of water sources are in rural communities, a crucial factor when prioritizing infrastructure planning and interventions.

#### 3. Diving into the Sources
The breakdown of water source usage showed:
- 43% of residents rely on shared taps, with about 2,000 people sharing one on average.  
- 31% have in-home water taps, but 45% of these are non-functional. The issue lies in the infrastructure (treatment plants, pipes, reservoirs), not the taps themselves.  
- 18% use wells, but only 28% of these (4,916 out of 17,383) are clean, posing health risks.  

This highlights significant inequality in water access and infrastructure reliability.

#### 4. Start of a Solution
To begin solving Maji Ndogo’s water issues, we must prioritize high-impact interventions. A logical first step is to fix the sources that affect the greatest number of people.

**We proposed a query to rank water source types by total number of users.**  
For example:
- Shared taps, serving 43% of people, should be fixed first.  
- Wells are widely used but often contaminated; cleaning and treating them is essential.  
- Fixing shared infrastructure (e.g., treatment plants or main pipelines) can restore multiple sources at once.

#### 5. Analyzing Queues
Queue analysis uncovered distinct usage patterns:
1. Mondays have the longest queues, both in the morning and evening, as people stock up after the weekend.  
2. Wednesdays have lower average wait times, except in the evening.  
3. Saturdays show the longest queue durations, possibly due to people fetching water for the upcoming week.  
4. Sundays have the shortest queues, reflecting cultural norms that prioritize family and religious observance.

---

### Insights
From the cleaned and analyzed data, we extracted the following key insights:
1. A majority of water sources are located in rural areas.  
2. 43% of residents use shared taps; on average, 2,000 people share one tap.  
3. 31% have in-home infrastructure, but 45% of those systems are non-functional.  
4. 18% rely on wells, but only 28% of those wells provide clean water.  
5. Citizens spend over 120 minutes on average in water queues.  
6. Queue trends:  
   - Longest on Saturdays  
   - Peak in mornings and evenings  
   - Shortest on Wednesdays and Sundays  

---

### Recommendations

#### Strategic Plan Overview

1. **Prioritize High-Impact Fixes**
   - Start with shared taps, as they serve the largest number of people.  
   - Address contamination in wells with filtration systems (UV or reverse osmosis).  
   - Fix existing infrastructure (pipes, pumps, reservoirs) to reduce waiting times and restore access.  

2. **Focus on Rural Areas**
   - Most sources are rural, requiring logistical planning for difficult terrains, limited labor, and transportation challenges.  

---

#### Practical Solutions

1. **For River-Dependent Communities**
   - Deploy water trucks temporarily while initiating well-drilling operations as a long-term solution.  

2. **For Wells**
   - Install UV filters for biological contamination.  
   - Use reverse osmosis filters for polluted sources.  
   - Investigate root causes of contamination for sustainable remediation.  

3. **For Shared Taps**
   - Use queue data to deploy additional water tankers on high-demand days.  
   - Install extra taps in high-usage areas to meet the UN-recommended 30-minute maximum wait time.  

4. **For Low-Queue Shared Taps**
   - In-home tap installation is resource-intensive and better suited for long-term plans, especially when queue times are already acceptable.  

5. **Infrastructure Repair**
   - Fixing a single reservoir or pipeline can restore multiple sources.  
   - Further analysis is needed to identify the most commonly affected areas.  

