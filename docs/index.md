# Continuous Intelligence

This site provides documentation for this project.
Use the navigation to explore module-specific materials.

## How-To Guide

Many instructions are common to all our projects.

See
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- **Project Instructions** - instructions specific to this module
- **Your Files** - how to copy the example and create your version
- **Glossary** - project terms and concepts

## Additional Resources

## Custom Project

### Dataset
ALong with the existing dataset that consisted of requests, errors, total_latency_ms, error_rate, avg_latency_ms  and throughput, I added two new fields quarter (from Q1 to Q4) and system_name (to identify the system for which the metrics were generated)to the database.

### Signals
1. I added two new  derived signals to understand the system behaviour:
Weighted Load Index:
This field combines the metrics from requests and error and weights them by multiplying the requests*1  and errors*5, to analyse the impact of errors on system load.
2. I added a classification signal for each row based on the calculated metrics from the weighted load index.

### Experiments
I added two new fields (Quarter and System)and updated the select to include these fields in the final output. I experimented by creating new expressions, adding them to a newly created dataframe and calling the fields in the final select.

### Results
My custom project shows that Q1 and Q2 had a higher load for System B and C. In Q3 the overall load was low and Q4 showed a mixed behavior of moderate load.

### Interpretation
(Describe what this means for your system - provide the business intelligence you gained)
Based on the custom project results, since Q1 and Q2 had a higher load index, they require more capacity planning and monitoring of the error so there is a improvement in performance. Based on System trends, System C needs more improvement as it had higher load and higher errors. The addition of quarter and system_name helped to drill down to more details and helped in bringing more business solutions.

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)
