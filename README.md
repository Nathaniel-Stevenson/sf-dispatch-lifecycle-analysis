# sf-dispatch-lifecycle-analysis
# Overview
Dataset: https://catalog.data.gov/dataset/law-enforcement-dispatched-calls-for-service-real-time
# Header
Table: Incident Lifecycle Summary
- Each bin represents a different lifecycle path. 

- Lifecycles are derived using provided information: call type, whether an officer was onscene at time of initiation, and stage duration data. 

- The dataset includes calls, full dispatches, partial dispatch which appear to be process errors in that they do not give an accurate duration, officer initiated incidents. 

- Incidents that do not have full information provided are labled "Missing Info" and excluded from this analysis

Table: Stage Durations by Dispatch Lifecycle

- Total Time (Sum of Medians) is used in place of MEDIAN of DER Total Time due to an error in Excel. 

# Limitations
- Many entries are missing enroute and close time, making any analysis of them impossible. ((These likely follow some pattern but more analysis is required)). 
- In analysis using table: Stage Durations by Dispatch Lifecycle, Total Time (Sum of Medians) is used in place of MEDIAN of DER Total Time due to an error in Excel. This is not the correct metric to use, as it can differ from the sum.
