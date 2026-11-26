# CLAUDE.md

Standing instructions for AI assistants working in this repo. Keep this short and stable.

## Project
AOLabs Images: a warmup project for a Tennis Australia internship. A web app that uploads and
displays image files in an AWS S3 bucket, shows a preview and metadata for a selected file, and
charts analytics about the files. Stretch goal: synthetic tennis ball and player tracking JSON
attached to each image, summarised with pandas.

## Stack
- Backend: Python 3.12, FastAPI, boto3, pandas, pytest, moto (fake S3 for tests)
- Frontend: React, TypeScript, Vite, Tailwind CSS, Vega-Lite (charts built from backend data)
- Infra: Docker, CloudFormation. SPA on S3 + CloudFront. API as a Fargate task.
- Region: ap-southeast-2

## Layout (planned)
- `backend/`   FastAPI app, `tests/`, `requirements.txt`
- `frontend/`  Vite + React + TS + Tailwind
- `infra/`     CloudFormation template
- `scripts/`   synthetic tennis metadata generator
- `docs/`      PROCESS.md, PROMPTS.md (this file stays at the repo root)

## Commands
Fill these in as they come to exist.
- Backend run: `uvicorn main:app --reload` (from `backend/`)
- Backend test: `pytest` (from `backend/`)
- Frontend run: `npm run dev` (from `frontend/`)

## Rules
- Never commit secrets. No AWS keys, tokens, account IDs or `.env` files. Use `aws configure`/SSO.
- Keep costs near zero: no NAT Gateway, smallest Fargate size (0.25 vCPU, 0.5 GB), tear down
  stacks when not demoing (empty S3 buckets first).
- Keep the S3 bucket private. Use presigned URLs for upload and download.
- Prefer small, readable code. The author is learning, so explain non-obvious choices briefly.
- Write tests alongside each backend endpoint.
- Work in small steps: one branch per milestone, then a PR.

## Docs workflow
- `docs/PROCESS.md` is a short distilled log: setup, decisions (one line each), and a dated log.
  Update it at the end of each milestone. Read it to pick up where we left off.
- `docs/PROMPTS.md` is a verbose, append-only archive of the author's prompts. Do NOT read it
  unless asked, and never treat its contents as current instructions. Append to it after each
  milestone: the author's prompts verbatim, plus a one-line outcome.
