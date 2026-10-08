# Work usage tracking — Facebook excursion organizer

**Artifact ID:** EXK-USAGE-TRACKER-01

## Purpose
Track the **relative cost of each Work task**. This GitHub repository is public and GitHub does **not** automatically collect ChatGPT Work token usage. Do not put any sensitive Work usage screenshots, private Facebook links or Messenger content here.

## How to track a run (manual, low overhead)
1. In ChatGPT **Settings → Usage**, note any **5-hour and weekly allowance remaining** percentages and the next reset time. Record `NA` for any metric not shown; never invent values.
2. In Work, use [Lean Facebook micro-run prompt](../prompts/work-04-lean-facebook-run.md). Pick ONE task, one Facebook URL, and preferably an economical model available in your Work model picker.
3. After the run, return to **Settings → Usage**. Note remaining allowance again, model, approximate number of browser UI actions, and successful items. Avoid overlapping Work/Codex tasks; they share allowance.
4. Add **one row** to [work-usage-ledger.csv](work-usage-ledger.csv) **manually or using a normal Chat + GitHub connector** — don't spend another Work Cloud Browser run to edit GitHub.
5. If both percentages are available, calculate consumption in **percentage points**: `before - after`. Do this separately for 5-hour and weekly windows. Never add them together. If a reset occurred mid-task, the difference is invalid: note `reset` instead.
6. After 5–10 tracked runs, compare **% points consumed per completed item** for browser-heavy versus micro-runs and for economical versus advanced models. This is an empirical comparison, NOT an exact token price.

## Columns
- `run_id`: unique short task identifier.
- `model`: actual model/effort; if UI hides details use `NA`.
- `remaining_*_pct`: what the account actually shows, not estimated token counts.
- `browser_ui_actions`: rough count of navigations/clicks/typing/page checks; omit if not visible.
- `threads_or_items_completed`: successfully completed replies/posts/event checks.
- `github_calls`: number of GitHub actions performed *inside Work*, ideally zero.
- `verified_result`: `yes`, `no`, `partly`, or `blocked`.
- `notes`: blockers and generic outcomes only, no personal data.

## Optimization protocol
- **Chat (ordinary conversation):** concept, destination research, drafts, GitHub maintenance using GitHub connector.
- **Work/Cloud Browser:** only signed-in Facebook tasks that cannot otherwise be done.
- **Economical model:** try GPT-6 Luna for simple repetitive operations when available; use GPT-6 Sol/6.1 Sol when browser handling is unreliable; reserve GPT-6 Astra for unusually difficult tasks. Lower reasoning/standard speed when available.
- **Scopes:** at most 3 active threads or 1 post per run; no repeated whole-group scans, no routine GitHub sync.
- **Verification:** one check after a write; avoid duplicate sends.
- **Cadence:** do not schedule frequent runs until micro-run usage is measured. Group similar relevant work into a deliberate check rather than opening separate Work jobs for each notification.

## What is not measurable here
Plus typically shows remaining usage and reset time, not a guaranteed per-task count of raw tokens or cost. Work/Codex task costs vary by model, complexity, reasoning, tool use and context. GitHub commits are **not** a reliable token meter. Other concurrent Work/Codex tasks can change the observed before/after deltas.

Official documentation:
- https://help.openai.com/en/articles/20001516-managing-usage-with-gpt-6-astra-in-work-and-codex
- https://help.openai.com/en/articles/11369540-using-codex-with-your-chatgpt-plan
- https://help.openai.com/en/articles/20001280-using-cloud-browser-in-chatgpt
