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

- [Suggested Datasets](https://denisecase.github.io/pro-analytics-02/reference/datasets/cintel/)

## Custom Project

### Dataset
This dataset is used to monitor system behavior and analyze performance trends over time.It contains a time series type of system. This performs metrics collected at regular intervals.

### Signals
I created additional signals to improve monitoring:
- **error_rate** = errors ÷ requests
- **avg_latency** = total latency ÷ requests
- **rolling error_rate** (moving average to a more Specefic window)

### Experiments
I modified the pipeline by updating the logic used for monitoring.

### Results
- Error rates increased during periods of higher request volume.
- Rolling error rate revealed a clearer upward trend in failures over time.
- Average latency increased alongside traffic, indicating slower response times under load,
- The rolling metrics made it easier to identify patterns that were less obvious in the raw data.

### Interpretation
The results suggest that system performance degrades as demand increases. Higher request volumes are associated with both increased error rates and longer response times, indicating potential scalability or resource limitations.
