# PROCESS.md

Short, distilled log. One line per entry. Update at the end of each milestone.

## Setup
Not set up yet. Planned: Python venv in `backend/.venv`, Node 20 for the frontend,
AWS CLI configured with a limited IAM user or SSO (not root).

## Decisions
- Keep S3 private and use presigned URLs, so the bucket is never public.
- Fargate task in a public subnet with no NAT Gateway, to avoid roughly US$33/month.
- Smallest Fargate size (0.25 vCPU, 0.5 GB) to keep cost down.
- Use moto to fake S3 in unit tests, so tests run offline.
- Keep three docs: CLAUDE.md (standing instructions), PROCESS.md (distilled log), PROMPTS.md (raw archive).

## Log
- 2026-11-26: repo created (Meetbels/AOLabs-Images), connected to Claude, docs files initialised, CLAUDE.md moved to repo root so Claude Code auto-loads it. Next: scaffold backend, `/health` endpoint, first pytest, debugger config.
