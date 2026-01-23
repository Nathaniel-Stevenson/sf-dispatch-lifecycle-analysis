# sf-dispatch-lifecycle-analysis
# Overview
Dataset: https://catalog.data.gov/dataset/law-enforcement-dispatched-calls-for-service-real-time
# Header
Table: Incident Lifecycle Summary
- Each bin represents a different lifecycle path. 

- Lifecycles are derived using provided information: call type, whether an officer was onscene at time of initiation, and stage duration data. 

- The dataset includes calls, full dispatches, partial dispatch which appear to be process errors in that they do not give an accurate duration, officer initiated incidents.

- Call Only = Incident type provided by dataset
- Traffic Enforcement = Incident type provided by dataset
- On-view, no dispatch = Using on view Y or HSOC
- System timestamped = checks if there is no duration between different phases (like instant arrival time)
- Full dispatch = checks if all durations are not 0
- Other = does not meet any of these checks

Response time metrics will only be using lifecycles that are initiated by dispatch and follow the full process. Call only, officer initiated responses, and system timestamped incidents are excluded.

Table: Stage Durations by Dispatch Lifecycle

Lifecycle is a primary determiner of durations.

Table: Full Dispatched Incident Count by Hour

Table: Full Dispatched Incidents Duration Breakdown

Table: Duration Breakdown by Priority


# Limitations
- Many entries are missing enroute and close time, making any analysis of them impossible. ((These likely follow some pattern but more analysis is required)). 
