# Process Discovery in CareFlow

## What is Process Discovery?

Process Discovery is a process mining technique used to understand how a business process actually works by analysing event logs.

In CareFlow, each patient journey consists of multiple activities performed during a hospital visit, such as:

- ED Registration & Triage
- Initial Physician Assessment
- Blood Sample Collection
- Laboratory Testing
- Diagnostic Imaging
- Treatment
- Patient Discharge or Transfer

Each activity is recorded with a timestamp and a case identifier.

Process discovery analyses these recorded events to identify the actual sequence of activities, possible variations in patient journeys, repeated activities, and different process paths.

**In CareFlow:** Process discovery helps reconstruct patient pathways from event log data and understand how patients move through the hospital workflow.

---

## 1. What is Inductive Miner?

Inductive Miner is a process discovery algorithm used to automatically discover a process model from an event log.

It analyses the order of activities in recorded cases and identifies common patterns and relationships between activities.

The algorithm recursively divides the event log into smaller parts and discovers the process structure. It produces a structured model called a **Process Tree**.

### Why use Inductive Miner in CareFlow?

- Identifies the common sequence of hospital activities.
- Detects different patient journey variations.
- Identifies optional activities and repeated steps.
- Produces a structured process model that can be converted into a Petri Net.

The discovered model provides an overview of how patient pathways are organised in the available event log.

---

## 2. Sequence, XOR, AND and Loop Operators

Inductive Miner uses different operators to represent relationships between activities.

### A. Sequence (→)

Sequence represents activities that occur one after another in a particular order.

**Example:**

ED Registration → Physician Assessment → Blood Collection → Laboratory Testing

This means the activities follow the specified order.

### B. XOR (Exclusive Choice)

XOR represents a choice between alternative paths. Only one of the alternatives is followed in a particular execution of that choice.

**Example:**

After treatment, a patient may follow one of these paths:

- Discharge to Outpatient Care
- Inpatient Ward Bed Handover
- Direct ICU Bed Transfer

A particular patient follows one of these alternatives.

### C. AND (Parallel)

AND represents activities that can occur in parallel rather than requiring one fixed order.

**Example:**

Two hospital activities may be carried out independently during the same stage of a patient journey.

The AND operator represents parallel behaviour in the process model.

### D. Loop (⟳)

A Loop represents a process that can repeat an activity or group of activities.

**Example:**

Blood Collection → Laboratory Testing → Specimen Re-draw → Blood Collection

If a blood sample is rejected, the collection and testing process may need to be repeated.

**Note:** These operators describe the structural patterns that a process discovery algorithm can identify. Their presence in a model does not automatically establish the clinical reason behind a patient's pathway.

---

## 3. What is a Petri Net?

A Petri Net is a mathematical and graphical model used to represent processes and the flow of activities within them.

It helps describe how a process moves from one state to another.

A Petri Net consists of places, transitions, arcs and tokens.

In process mining, Petri Nets are useful for representing discovered workflows and analysing how activities are connected.

**In CareFlow:** A Petri Net represents the discovered patient journey and provides a formal model that can be used for further process analysis.

---

## 4. Places, Transitions, Arcs and Tokens

A Petri Net consists of four important elements:

### A. Places (○)

Places represent the states or conditions of a process.

They are represented by circles.

**Example:** A patient waiting for a laboratory test.

### B. Transitions (▭)

Transitions represent activities or actions performed during a process.

They are represented by rectangles.

**Example:** Blood Collection or Laboratory Testing.

### C. Arcs (→)

Arcs are directed connections between places and transitions.

They define the flow of the process and indicate how one step is connected to another.

### D. Tokens (●)

Tokens represent the current state or position of the process within the Petri Net.

A token moves through the net when a transition fires, provided its required input conditions are satisfied.

**Simple example:**

A token in the place representing a patient waiting for a blood test can move through the Blood Collection transition when that transition is enabled.

Together, these components represent the flow and execution of a process.

---

## 5. How CareFlow Converts a Process Tree into a Petri Net

CareFlow uses PM4Py to discover a process tree from the patient event log and convert that process tree into a Petri Net.

The workflow consists of the following steps:

1. **Event Log Preparation:** Patient event data is prepared with case identifiers, activity names and timestamps.
2. **Process Discovery:** Inductive Miner analyses the event log and discovers the process structure.
3. **Process Tree Generation:** The discovered process is represented as a Process Tree containing operators such as Sequence, XOR, AND and Loop.
4. **Petri Net Conversion:** The Process Tree is converted into a Petri Net.
5. **Visualization:** The Petri Net is visualized to understand the discovered process flow.

### Process Flow

Event Log → Inductive Miner → Process Tree → Petri Net → Process Analysis

The Process Tree provides a structured representation of the discovered process, while the Petri Net provides a formal model of its execution flow.

---

## 6. Python Implementation Using PM4Py

PM4Py is an open-source Python library used for process mining. It provides functions for process discovery, process model conversion, visualization and conformance checking.

The following implementation demonstrates how a prepared event log can be used to discover a Process Tree and convert it into a Petri Net.

### Step 1: Install PM4Py

```bash
pip install pm4py
```

### Step 2: Prepare the Event Log

The event log must contain three important attributes:

- `case:concept:name` – Identifies the patient case.
- `concept:name` – Represents the activity performed.
- `time:timestamp` – Records when the activity occurred.

```python
import pandas as pd
import pm4py

# Load the standardized event log
df = pd.read_csv("careflow_standardized_event_log.csv")

# Select the required columns
event_log = df[["Case ID", "Activity", "Timestamp"]].copy()

# Rename columns according to PM4Py conventions
event_log = event_log.rename(columns={
    "Case ID": "case:concept:name",
    "Activity": "concept:name",
    "Timestamp": "time:timestamp"
})

# Convert timestamps into datetime format
event_log["time:timestamp"] = pd.to_datetime(
    event_log["time:timestamp"],
    utc=True
)

# Sort events chronologically within each case
event_log = event_log.sort_values(
    ["case:concept:name", "time:timestamp"]
)

print(event_log.head())
```

### Step 3: Discover the Process Tree Using Inductive Miner

```python
# Discover the process tree
process_tree = pm4py.discover_process_tree_inductive(event_log)

# Display the discovered process tree
print(process_tree)
```

This step applies the Inductive Miner algorithm to identify the process structure from the event log.

### Step 4: Convert the Process Tree into a Petri Net

```python
# Convert the process tree into a Petri Net
net, initial_marking, final_marking = pm4py.convert_to_petri_net(
    process_tree
)
```

The conversion produces:

- `net`: The Petri Net containing places, transitions and arcs.
- `initial_marking`: The initial state of the process.
- `final_marking`: The expected final state of the process.

### Step 5: Visualize the Petri Net

```python
# Visualize the discovered Petri Net
pm4py.view_petri_net(
    net,
    initial_marking,
    final_marking
)
```

The visualization helps understand the relationships and flow between activities in the discovered process model.

---

## 7. How the Discovered Model Supports Further Analysis

The discovered process model provides a foundation for several important process mining activities in CareFlow.

### A. Understanding Patient Pathways

The model helps identify the different sequences of activities followed by patients during their hospital visits.

### B. Identifying Process Variations

Different patients may follow different pathways depending on their requirements and outcomes. The model helps represent these variations.

### C. Bottleneck Analysis

The event log can be analysed to calculate the time between consecutive activities.

These transition durations help identify potentially time-consuming stages in the patient journey.

For example, a longer duration between Laboratory Testing and Diagnostic Imaging may indicate a stage that requires further investigation.

### D. Conformance Checking

Conformance checking compares the recorded patient journeys with the discovered process model.

It helps evaluate whether the observed event sequences follow the behaviour represented by the model.

### E. Process Performance Analysis

The discovered model can be combined with event timestamps and other event-log attributes to study:

- Patient journey duration
- Activity frequency
- Transition duration
- Process variations
- Repeated activities
- Potential bottlenecks

### Conclusion

Process Discovery is an important part of the CareFlow project because it transforms raw patient event logs into a structured representation of hospital workflows.

By using Inductive Miner and Petri Nets through PM4Py, CareFlow can reconstruct patient pathways and establish a foundation for bottleneck analysis, conformance checking and process performance evaluation.
