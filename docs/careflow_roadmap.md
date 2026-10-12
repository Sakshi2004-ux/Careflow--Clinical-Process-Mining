INFOTACT SOLUTIONS INTERNSHIP – GROUP 9 
TEAM = Together, Everyone, Achieves, More.
 Many hands make light work.
CareFlow — First 2 Weeks Plan
For the first two weeks, our goal is to build a strong foundation for CareFlow while all four members work in parallel. We'll follow the project's intended sequence: event-log engineering with BigQuery and dbt, alongside process mining with PM4Py and dashboard development in Power BI. 
PROJECT.pdf
The plan below is organized by day, so your team can use it as an execution checklist.
Week 1: Dataset understanding and project setup
Goal: Understand Dataset 2, prepare the development environment, define the event-log schema, and start initial analysis.
Suggested duration: Days 1–7

Day 1
Team kickoff and repository setup
•	Satyam: Review the dataset columns and structure.
•	Vansh: Set up the project folder structure and explore BigQuery/dbt requirements.
•	Sakshi: Understand process mining and the CareFlow problem statement.
•	Tushar: Research Power BI process visuals and draft dashboard sections.
•	All: Create the new GitHub repository, individual branches, and task-distribution document.
Day 2
Dataset quality and schema
•	Satyam: Check nulls, duplicates, data types, and timestamp validity.
•	Vansh: Design the raw table schema.
•	Sakshi: Verify event ordering within each case and understand the activity sequence.
•	Tushar: Define preliminary KPIs and required dashboard fields.
Day 3
Exploratory analysis
•	Satyam: Prepare a data-quality summary.
•	Vansh: Test data loading options and draft the first dbt model.
•	Sakshi: Calculate activity frequencies, cases per activity, and events per case using Python.
•	Tushar: Sketch the Power BI dashboard wireframe.
Day 4
Initial implementation
•	Satyam: Investigate unusual records and missing values.
•	Vansh: Begin loading the raw data into BigQuery, subject to access and setup.
•	Sakshi: Analyze elapsed time between consecutive activities.
•	Tushar: Identify suitable charts for activity volumes, delays, and patient journeys.
Day 5
Standardization and first findings
•	Satyam: Finalize the data-quality report.
•	Vansh: Standardize column names and data types in the initial transformation model.
•	Sakshi: Identify frequent transitions and potentially slow transitions.
•	Tushar: Refine the dashboard layout and KPI definitions.
Day 6
Initial integration
•	Satyam: Cross-check the data-quality findings.
•	Vansh: Test the transformation output and add basic dbt tests where possible.
•	Sakshi: Convert a sample of the standardized event data into PM4Py format.
•	Tushar: Prepare sample visuals using the available exploratory results.
Day 7
Week 1 review
•	Review the data-quality report and dataset source status.
•	Confirm the agreed event-log schema.
•	Check that GitHub contains genuine contributions from each member.
•	Review the initial Python analysis, pipeline setup, and dashboard wireframe.
•	List blockers and set Week 2 priorities.

Week 1 deliverables
By the end of Week 1, aim to have:
•	Dataset profile and documented data-quality checks.
•	GitHub repository, branches, and initial commits.
•	Agreed event-log schema.
•	Initial BigQuery/dbt setup or documented setup blockers.
•	Python exploratory notebook with preliminary findings.
•	Power BI wireframe and agreed KPI list.

Week 2: Event-log transformation and process discovery
Goal: Create a standardized event log, discover the actual process paths in the data, and begin connecting the analytical results to the dashboard.
Suggested duration: Days 8–14

Day 8
Finalize the event-log structure
•	Satyam: Recheck data consistency and record any unresolved limitations.
•	Vansh: Continue building dbt staging and standardized models.
•	Sakshi: Prepare the event log with case ID, activity, and timestamp for PM4Py.
•	Tushar: Set up the initial Power BI report pages.
Day 9
Validate transformations and event sequences
•	Satyam: Compare raw and transformed record counts.
•	Vansh: Add transformation tests for required fields and data types.
•	Sakshi: Validate chronological ordering and case-level activity sequences.
•	Tushar: Prepare initial activity-frequency and transition-time charts.
Day 10
Discover the process model
•	Satyam: Investigate any records that fail validation.
•	Vansh: Run and document the transformation pipeline.
•	Sakshi: Use PM4Py to discover an initial process model or directly-follows graph.
•	Tushar: Explore how to present the process map in Power BI.
Day 11
Analyze patient-flow patterns
•	Satyam: Review data-quality exceptions that could affect the results.
•	Vansh: Improve transformation reliability and documentation.
•	Sakshi: Examine common pathways, activity loops, and differences between cases.
•	Tushar: Build preliminary visuals for activity counts and elapsed times.
Day 12
Validate analytical findings
•	Satyam: Cross-check suspicious or unexpected sequences against the raw data.
•	Vansh: Verify the standardized output against the agreed schema.
•	Sakshi: Calculate average, median, and percentile transition times; investigate possible bottlenecks.
•	Tushar: Integrate available metrics into the report.
Day 13
End-to-end integration
•	Satyam: Sign off on data-quality checks or document remaining issues.
•	Vansh: Test the raw-to-transformed data workflow.
•	Sakshi: Export the process-discovery outputs and document findings.
•	Tushar: Connect the available data and metrics to Power BI.
•	All: Review integration issues together.
Day 14
Week 2 review and next-phase planning
•	Confirm that the standardized event log is usable.
•	Review the discovered process map.
•	Identify the strongest candidate bottlenecks and validate their evidence.
•	Review dashboard progress and pipeline reliability.
•	Plan Week 3 bottleneck calculations and dashboard development.
Week 2 deliverables
•	Standardized event log suitable for process mining.
•	Tested initial dbt transformation models.
•	Initial PM4Py process map.
•	Patient-flow and transition-time analysis.
•	Preliminary Power BI report.
•	Week 2 integration and progress report.


Date	Main task / milestone
13 Oct (Tue)	Team kickoff, GitHub setup, task distribution
14 Oct (Wed)	Dataset quality checks and schema
15 Oct (Thu)	Exploratory analysis and dashboard KPIs
16 Oct (Fri)	Data loading and transition-time analysis
17 Oct (Sat)	Data standardization and preliminary findings
18 Oct (Sun)	PM4Py sample, dbt tests, dashboard wireframe
19 Oct (Mon)	Week 1 review and deliverables checkpoint
20 Oct (Tue)	dbt transformations and process discovery
21 Oct (Wed)	Validate transformed data and event sequences
22 Oct (Thu)	Generate the initial process map
23 Oct (Fri)	Analyze patient-flow patterns
24 Oct (Sat)	Investigate potential bottlenecks
25 Oct (Sun)	Integrate pipeline, process map, and dashboard
26 Oct (Mon)	Week 2 completion checkpoint


