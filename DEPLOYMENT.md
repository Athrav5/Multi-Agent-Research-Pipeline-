# Deployment — Multi-Agent Research Pipeline

## Local

```bash
make install
make run
```

## Docker

```bash
docker build -t 05-multi-agent-research-pipeline .
docker run -p 8000:8000 --env-file .env 05-multi-agent-research-pipeline
```

## Production (illustrative)

Recommended deployment pattern:
1. Containerize with the included Dockerfile.
2. Deploy to Fly.io / Render / Railway.
3. Observe with OpenTelemetry → Arize Phoenix.
4. Alert on cost > 2× daily baseline.
5. Add a feature-flag kill switch.

## Cost budget
- Per-request cost target: $0.05 max
- Daily budget: $10
- Alert at 50%, 80%, 100% of budget

## Postmortem template

```markdown
# Postmortem — YYYY-MM-DD

## Summary
[One sentence.]

## Timeline
- HH:MM Detection
- HH:MM Mitigation
- HH:MM Resolution

## Root cause
[Technical.]

## Contributing factors
[Process / cultural.]

## Action items
- [ ] ...

## Lessons
[What we learned.]
```
