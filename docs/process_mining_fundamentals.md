# Day 1: Understanding Process Mining

## 1. Objective
To understand the fundamentals of process mining, its role in data analytics, and its application to the CareFlow — Clinical Pathway Process Mining project.

## 2. What is Process Mining?
Process mining is a data analytics technique that uses event logs to discover, analyze, and improve real-world business processes. It helps reconstruct the actual sequence of activities, identify process variations, and investigate potential bottlenecks.

## 3. Types of Process Mining

- **Process Discovery:** Reconstructs the actual process from recorded event data.
- **Conformance Checking:** Compares observed process behavior against an expected or reference process.
- **Process Enhancement:** Enriches process analysis using additional information such as timestamps, waiting intervals, and resource details.

## 4. Understanding Event Logs
An event log records activities associated with individual process instances. In CareFlow, each case represents a recorded patient journey, and each event represents an activity within that journey.

Important event-log attributes include:

- **Case ID:** Identifies a patient journey.
- **Activity:** Describes the recorded event.
- **Timestamp:** Records when the event occurred.
- **Event Index:** Helps establish the event sequence within a case.
- **Next Activity:** Records the subsequent activity.
- **Elapsed to Next (min):** Records the elapsed interval to the next activity.
- **Resource and Department:** Provide information about the assigned resource and department.
- **Status:** Records the event status.

## 5. CareFlow Problem Understanding
CareFlow aims to analyze Emergency Room patient pathways and investigate potential operational bottlenecks. Traditional dashboards often summarize performance using averages, whereas process mining helps reveal the actual sequences of activities and variations between patient journeys.

The analysis will focus on understanding patient pathways, activity transitions, elapsed times, and repeated activities that may indicate areas for further investigation.

## 6. Planned Technology Stack
- **Google BigQuery:** Storage and SQL-based analysis of event data.
- **dbt:** Data transformation, standardization, and testing.
- **Python and PM4Py:** Process discovery and process analysis.
- **Power BI:** Visualization of process insights and operational metrics.

## 7. Key Learnings
1. Process mining relies on event logs to reconstruct actual process behavior.
2. Case ID, activity, and timestamp are fundamental attributes for process analysis.
3. Patient journeys may vary in activity sequence and duration.
4. Long elapsed intervals and repeated activities can highlight potential bottlenecks, but do not independently establish their causes.
5. Event ordering and data quality must be validated before conducting process discovery.
6. Dataset assumptions and provenance should be documented before drawing real-world conclusions.

## 8. Next Steps
- Verify event ordering within each case.
- Check chronological consistency of timestamps.
- Validate the Next Activity column against the next recorded event.
- Inspect individual patient activity sequences.
- Document validation results before proceeding to process discovery.
