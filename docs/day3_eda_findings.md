# Day 3 — Exploratory Data Analysis

## Objective
Explore the CareFlow event log to understand activity frequencies, patient journey patterns, and recorded transition durations.

## 1. Dataset Overview
- Total patient cases: 1,428
- Average events per case: 6.90
- Minimum events per case: 6
- Maximum events per case: 9

## 2. Patient Journey Distribution
- 6 events: 685 cases
- 7 events: 371 cases
- 8 events: 200 cases
- 9 events: 172 cases

## 3. Common Patient Pathways
- Most frequent pathway: Standard pathway ending in inpatient ward handover without CT imaging — 457 cases.
- Pathway ending in ward handover after CT imaging — 247 cases.
- Pathway ending in outpatient discharge without CT imaging — 228 cases.
- Pathway involving CT imaging, specialist consultation, and ICU transfer — 200 cases.
- Cases containing a recorded laboratory re-draw pathway: 172.

## 4. Transition-Time Analysis
Record the overall mean, median, maximum, and activity-level transition durations from the actual notebook output.

## 5. Key Observations
- The most frequent exact pathway accounts for approximately 32.0% of cases.
- Seven pathway patterns account for all 1,428 cases in the current analysis.
- Laboratory re-draw events occur in approximately 12.0% of cases.
- Recorded transition durations require further interpretation before being described as waiting times or confirmed bottlenecks.

## 6. Limitations
These findings are descriptive. They do not establish why pathways differ or prove that any activity causes a particular outcome.
