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


# CareFlow – Process Mining & Analytics

## Overview
This module analyzes clinical event logs using Python and PM4Py to discover patient pathways, identify repeated activities, and examine transition times.

## Dataset Summary
- Total events: 9,855
- Unique patient cases: 1,428
- Unique activities: 11
- Unique journey patterns: 7

## Process Mining
- Prepared and validated the event log.
- Discovered the process tree using PM4Py.
- Generated a Petri net process model.
- Evaluated the discovered model using token-based replay fitness and precision.

## Key Findings
- 172 cases (12.04%) contain a specimen re-draw loop.
- 8,427 transitions have recorded elapsed-time values.
- 13 distinct activity transitions were analyzed.
- Five candidate bottleneck transitions were identified for further investigation.

## Evaluation
- Token-based replay fitness: 100%
- Process model precision: 0.8804

## Output Files
- `careflow_process_tree.txt`
- `careflow_process_model.pnml`
- `careflow_petri_net.png`
- `careflow_analytical_summary.csv`

## Tools & Technologies
Python, Pandas, PM4Py, Google Colab

## Limitations
The findings describe the available dataset. Candidate bottlenecks require further investigation, and observed associations do not establish causation. The real-world provenance and interpretation of elapsed-time fields should be verified.
