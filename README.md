# sf-dispatch-lifecycle-analysis
## Overview
This project uses Law Enforcement Dipatched Calls for Service (Real Time) dataset published by the City of San Francisico to analyze lifeycycles and response times of law enforcement incidents. 

This analysis focuses on distinguishing lifecycle paths and evaluating response behavior for only incidents that follow a complete dispatch initiated process. Incidents that do not follow standard dispatch workflow are excluded.

Dataset: https://catalog.data.gov/dataset/law-enforcement-dispatched-calls-for-service-real-time

## Findings
Table: Incident Lifecycle Summary
Each bin represents a different lifecycle path. Lifeycycle paths are decided using call type metadata, officer-initiated indicators, ordering of timestamps across dispatch stages, and so on. Incidents are classified whether they represent a full dispatch workflow, and officer initiated event, a call only, or system timestamping. 

Response time metrics will only be using lifecycles that are initiated by dispatch and follow the full process. Incidents that are call only, officer initiated , and system timestamped incidents are excluded from stage duration analysis later.

Table: Stage Durations by Dispatch Lifecycle

Lifecycle is a primary determiner of stage durations. Incidents that do not have a full dispatch cycle have durations that are either zero or do not follow a logical progression. This validates the need to exclude lifecycles that do not follow full dispatch process. 

Table: Full Dispatched Incident Count by Hour

Responses that follow full dispatch procedure are consistent throughout the day, with an increase during daytime hours and decrease during nighttime hours. There are no concentrations of high volume. Durations of stages do not align with hourly incident count, suggesting that call volume by hour is not a primary driver to stage durations.

Table: Full Dispatched Incidents Duration Breakdown by Hour

Stage duration and Total Times show variability hour to hour, but the variability is irregular and there is no hour of day pattern. Hour of day is not a primary determiner of durations.

Table: Full Dispatched Incidents Duration Breakdown by Priority 

Response timing varies meaningfully by priority. Highest priority incidents are dispatched substantially faster and remain longer after an officer arrives onscene. Lower priority incidents have long dispatch delays but resolve much faster when the officer is onscene. Travel time is similar across all priorities, indiciating that priority affects decision making in dispatch and time resources needed to close, not unit travel time. This leads to differences in total durations being driven primarily by dispatch delay, secondarily by time to resolve from when officer arrives onscene. 

# Limitations
- Analysis relies on median durations, variability within priority or lifecycles not captured
