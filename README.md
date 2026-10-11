# CareFlow — Clinical Pathway Process Mining

## Project Overview

CareFlow is a healthcare operations analytics project focused on understanding patient journeys in hospital Emergency Rooms (ERs). It uses process mining to discover actual patient pathways, identify operational bottlenecks, analyze waiting times, and investigate repeated activities.

## Problem Statement

Traditional dashboards report average waiting times but may not reveal the sequence of events responsible for delays. CareFlow aims to reconstruct patient journeys from timestamped event logs and help identify areas where hospital workflows can be improved.

## Project Objectives

- Prepare and validate chronological hospital event logs.
- Discover actual patient pathways using process mining.
- Identify repeated activities and potential bottlenecks.
- Calculate transition times between activities.
- Compare actual pathways against expected workflows.
- Present operational insights through an interactive dashboard.

## Planned Technology Stack

- Python — data generation and analysis
- Google BigQuery — data storage and SQL analytics
- dbt — data cleaning and transformation
- PM4Py — process mining
- Microsoft Power BI — visualization and reporting

## Initial Event Log Structure

| Field | Description |
|---|---|
| Case_ID | Identifies a patient visit |
| Activity_Name | Activity performed during the visit |
| Timestamp | Time associated with the event |

## Planned Project Structure

```text
CareFlow-Clinical-Process-Mining/
├── data/
├── notebooks/
├── src/
├── sql/
├── dbt_project/
├── dashboard/
├── docs/
└── README.md
```

## Project Status

Initial setup and requirement analysis in progress. Dataset selection, data preparation, process discovery, bottleneck analysis, and dashboard development will follow.

## Data Privacy

The project will use suitable public or synthetic data for development. No identifiable real patient information should be committed to this repository.

## Team

Data Analytics Internship — Infotact Solutions
