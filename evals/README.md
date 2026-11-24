# Evals for Multi-Agent Research Pipeline

## Methodology
1. Golden dataset — `golden.jsonl` contains test cases with inputs and expected outputs/rubrics.
2. Eval runner — `eval_runner.py` loads the dataset, runs the agent, and scores outputs.
3. Report — prints a summary and writes a JSON artifact for CI.

## Metrics
- `report_quality_score`
- `citation_accuracy`
- `iteration_count`
- `cost_per_report`

## Running
```bash
make eval
```

## Adding cases
Append JSONL records with an id, input, and expected rubric.

## CI integration
Run `make eval` in your CI workflow and fail the build when the pass rate is below the configured threshold.
