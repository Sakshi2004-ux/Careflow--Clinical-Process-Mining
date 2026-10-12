# INFOTACT SOLUTIONS INTERNSHIP — GROUP 9

> **TEAM = Together, Everyone, Achieves, More.**  
> *Many hands make light work.*

# CareFlow — First 2 Weeks Plan

## Project Overview

For the first two weeks, our goal is to build a strong foundation for CareFlow while all four members work in parallel. We will follow the project's intended sequence: event-log engineering with BigQuery and dbt, alongside process mining with PM4Py and dashboard development in Power BI.

**Team members:** Satyam, Vansh, Sakshi, and Tushar  
**Start date:** 13 October 2026  
**Target completion for Weeks 1–2:** 26 October 2026  
**Mid-review window:** 27–30 October 2026

---

## Week 1: Dataset Understanding and Project Setup

**Goal:** Understand Dataset 2, prepare the development environment, define the event-log schema, and start initial analysis.

### Day 1 — 13 October: Team Kickoff and Repository Setup
- **Satyam:** Review the dataset columns and structure.
- **Vansh:** Set up the project folder structure and explore BigQuery/dbt requirements.
- **Sakshi:** Understand process mining and the CareFlow problem statement.
- **Tushar:** Research Power BI process visuals and draft dashboard sections.
- **All:** Create/confirm individual GitHub repositories, branches as required, and the task-distribution document.

### Day 2 — 14 October: Dataset Quality and Schema
- **Satyam:** Check nulls, duplicates, data types, and timestamp validity.
- **Vansh:** Design the raw table schema.
- **Sakshi:** Verify event ordering within each case and understand activity sequences.
- **Tushar:** Define preliminary KPIs and required dashboard fields.

### Day 3 — 15 October: Exploratory Analysis
- **Satyam:** Prepare a data-quality summary.
- **Vansh:** Test data-loading options and draft the first dbt model.
- **Sakshi:** Calculate activity frequencies, cases per activity, and events per case using Python.
- **Tushar:** Sketch the Power BI dashboard wireframe.

### Day 4 — 16 October: Initial Implementation
- **Satyam:** Investigate unusual records and missing values.
- **Vansh:** Begin loading the raw data into BigQuery, subject to access and setup.
- **Sakshi:** Analyze elapsed time between consecutive activities.
- **Tushar:** Identify suitable charts for activity volumes, delays, and patient journeys.

### Day 5 — 17 October: Standardization and First Findings
- **Satyam:** Finalize the data-quality report.
- **Vansh:** Standardize column names and data types in the initial transformation model.
- **Sakshi:** Identify frequent transitions and potentially slow transitions.
- **Tushar:** Refine the dashboard layout and KPI definitions.

### Day 6 — 18 October: Initial Integration
- **Satyam:** Cross-check the data-quality findings.
- **Vansh:** Test the transformation output and add basic dbt tests where possible.
- **Sakshi:** Convert a sample of the standardized event data into PM4Py format.
- **Tushar:** Prepare sample visuals using the available exploratory results.

### Day 7 — 19 October: Week 1 Review
- Review the data-quality report and dataset source status.
- Confirm the agreed event-log schema.
- Check that GitHub contains genuine contributions from each member.
- Review the initial Python analysis, pipeline setup, and dashboard wireframe.
- List blockers and set Week 2 priorities.

### Week 1 Deliverables
- [ ] Dataset profile and documented data-quality checks.
- [ ] Individual GitHub repository setup and initial commits.
- [ ] Agreed event-log schema.
- [ ] Initial BigQuery/dbt setup or documented setup blockers.
- [ ] Python exploratory notebook with preliminary findings.
- [ ] Power BI wireframe and agreed KPI list.

---

## Week 2: Event-Log Transformation and Process Discovery

**Goal:** Create a standardized event log, discover process paths in the data, and begin connecting analytical results to the dashboard.

### Day 8 — 20 October: Finalize the Event-Log Structure
- **Satyam:** Recheck data consistency and record unresolved limitations.
- **Vansh:** Continue building dbt staging and standardized models.
- **Sakshi:** Prepare the event log with case ID, activity, and timestamp for PM4Py.
- **Tushar:** Set up the initial Power BI report pages.

### Day 9 — 21 October: Validate Transformations and Event Sequences
- **Satyam:** Compare raw and transformed record counts.
- **Vansh:** Add transformation tests for required fields and data types.
- **Sakshi:** Validate chronological ordering and case-level activity sequences.
- **Tushar:** Prepare initial activity-frequency and transition-time charts.

### Day 10 — 22 October: Discover the Process Model
- **Satyam:** Investigate records that fail validation.
- **Vansh:** Run and document the transformation pipeline.
- **Sakshi:** Use PM4Py to discover an initial process model or directly-follows graph.
- **Tushar:** Explore how to present the process map in Power BI.

### Day 11 — 23 October: Analyze Patient-Flow Patterns
- **Satyam:** Review data-quality exceptions that could affect the results.
- **Vansh:** Improve transformation reliability and documentation.
- **Sakshi:** Examine common pathways, activity loops, and differences between cases.
- **Tushar:** Build preliminary visuals for activity counts and elapsed times.

### Day 12 — 24 October: Validate Analytical Findings
- **Satyam:** Cross-check suspicious or unexpected sequences against the raw data.
- **Vansh:** Verify the standardized output against the agreed schema.
- **Sakshi:** Calculate average, median, and percentile transition times; investigate possible bottlenecks.
- **Tushar:** Integrate available metrics into the report.

### Day 13 — 25 October: End-to-End Integration
- **Satyam:** Sign off on data-quality checks or document remaining issues.
- **Vansh:** Test the raw-to-transformed data workflow.
- **Sakshi:** Export process-discovery outputs and document findings.
- **Tushar:** Connect available data and metrics to Power BI.
- **All:** Review integration issues together.

### Day 14 — 26 October: Week 2 Review and Next-Phase Planning
- Confirm that the standardized event log is usable.
- Review the discovered process map.
- Identify candidate bottlenecks and validate the evidence.
- Review dashboard progress and pipeline reliability.
- Plan Week 3 bottleneck calculations and dashboard development.

### Week 2 Deliverables
- [ ] Standardized event log suitable for process mining.
- [ ] Tested initial dbt transformation models.
- [ ] Initial PM4Py process map.
- [ ] Patient-flow and transition-time analysis.
- [ ] Preliminary Power BI report.
- [ ] Week 2 integration and progress report.

---

## Calendar at a Glance

| Date | Day | Main Task / Milestone |
|---|---|---|
| 13 October | Tuesday | Team kickoff, GitHub setup, and task distribution |
| 14 October | Wednesday | Dataset quality checks and schema |
| 15 October | Thursday | Exploratory analysis and dashboard KPIs |
| 16 October | Friday | Data loading and transition-time analysis |
| 17 October | Saturday | Data standardization and preliminary findings |
| 18 October | Sunday | PM4Py sample, dbt tests, and dashboard wireframe |
| 19 October | Monday | Week 1 review and deliverables checkpoint |
| 20 October | Tuesday | dbt transformations and process discovery |
| 21 October | Wednesday | Validate transformed data and event sequences |
| 22 October | Thursday | Generate the initial process map |
| 23 October | Friday | Analyze patient-flow patterns |
| 24 October | Saturday | Investigate potential bottlenecks |
| 25 October | Sunday | Integrate pipeline, process map, and dashboard |
| 26 October | Monday | Week 2 completion checkpoint |
| 27–30 October | Tuesday–Friday | Mid-review window: final checks, fixes, and presentation/viva preparation |

---

## Important Notes

1. Dataset 2 is being used provisionally while its original source is being verified.
2. Keep the raw dataset unchanged; perform cleaning and transformations in separate outputs.
3. Treat long transitions and repeated activities as potential bottlenecks to investigate, not proof of a cause.
4. If BigQuery or dbt access is delayed, continue local Python analysis and document the blocker.
5. Each member should document their actual contribution and follow the team's GitHub and internship tracking requirements.
6. The mid-review is scheduled within **27–30 October 2026**; confirm the exact appointment with the internship coordinator.

**Team principle:** Work in parallel, communicate regularly, and integrate progress throughout the project.
