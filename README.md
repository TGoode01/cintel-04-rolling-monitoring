# cintel-04-rolling-monitoring

[![Python 3.14+](https://img.shields.io/badge/python-3.14%2B-blue?logo=python)](#)
[![MIT](https://img.shields.io/badge/license-see%20LICENSE-yellow.svg)](./LICENSE)

> Professional Python project for continuous intelligence.

Continuous intelligence systems monitor data streams, detect change, and respond in real time.
This course builds those capabilities through working projects.

In the age of generative AI, durable skills are grounded in real work:
setting up a professional environment,
reading and running code,
understanding the logic,
and pushing work to a shared repository.
Each project follows the structure of professional Python projects.
We learn by doing.

## This Project

This project introduces **rolling monitoring**.

The goal is to copy this repository,
set up your environment,
run the example analysis,
and explore how system metrics change over time.

You will run the example pipeline, read the code,
and make small modifications to understand
how rolling windows help smooth short-term variation and
reveal trends in time-series data.

## Data

The example pipeline reads time-series system metrics from:

`data/system_metrics_timeseries_case.csv`

Each row represents one observation at a specific timestamp.
The pipeline computes rolling averages for requests, errors, and latency, then saves the monitoring results as an artifact.

## Working Files

You'll work with just these areas:

- **data/** - it starts with the data
- **docs/** - tell the story
- **src/cintel/** - where the magic happens
- **pyproject.toml** - update authorship & links
- **zensical.toml** - update authorship & links

## Instructions

Follow the [step-by-step workflow guide](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/) to complete:

1. Phase 1. **Start & Run**
2. Phase 2. **Change Authorship**
3. Phase 3. **Read & Understand**
4. Phase 4. **Modify**
5. Phase 5. **Apply**

## Challenges

Challenges are expected.
Sometimes instructions may not quite match your operating system.
When issues occur, share screenshots, error messages, and details about what you tried.
Working through issues is part of implementing professional projects.

## Success

After completing Phase 1. **Start & Run**, you'll have your own GitHub project, running on your machine, and running the example will print out:

```shell
========================
Pipeline executed successfully!
========================
```

And a new file named `project.log` will appear in the project folder.

## Command Reference

The commands below are used in the workflow guide above.
They are provided here for convenience.

Follow the guide for the **full instructions**.

<details>
<summary>Show command reference</summary>

### In a machine terminal (open in your `Repos` folder)

After you get a copy of this repo in your own GitHub account,
open a machine terminal in your `Repos` folder:

```shell
# Replace username with YOUR GitHub username.
git clone https://github.com/tgoode01/cintel-04-rolling-monitoring

cd cintel-04-rolling-monitoring
code .
```

### In a VS Code terminal

```shell
uv self update
uv python pin 3.14
uv sync --extra dev --extra docs --upgrade

uvx pre-commit install
git add -A
uvx pre-commit run --all-files

uv run python -m cintel.rolling_monitor_case

uv run ruff format .
uv run ruff check . --fix
uv run zensical build

git add -A
git commit -m "update"
git push -u origin main
```

</details>

## Notes

- Use the **UP ARROW** and **DOWN ARROW** in the terminal to scroll through past commands.
- Use `CTRL+f` to find (and replace) text within a file.

## Change Summary

### What I Changed
I improved the rolling monitoring pipeline by adding new metrics and extending the analysis logic.I introduced things like:
- error_rate
- avg_latency (total latency dvided by requests)

---

### Why I Made the Change
The original pipeline focused only on raw counts (requests, errors, and latency), which limited insight into system performance.

These changes were made to:
- Improve understanding of system reliability (error rate)
- Measure efficiency more accurately (average latency)
- Identify trends over time using smoothed rolling metrics instead of noisy raw values

---

### What I Observed After Running the Project
After running the updated pipeline, several patterns became clearer:
- Error rates increased during periods of higher request volume
- Rolling error rate revealed a gradual upward trend that was not obvious in raw data
- Average latency increased alongside higher traffic levels

Overall, the system showed signs of performance lowering under heavier load, and the rolling metrics made these trends easier to detect and interpret.
