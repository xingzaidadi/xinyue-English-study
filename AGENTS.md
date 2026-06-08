# AGENTS.md

## Project Purpose

This repository manages Xinyue's Cambridge English study plan, diagnostic workflow, daily tasks, completion logs, and study-coach skill.

The learner is an 11-year-old Grade 4 student preparing for A2 Key for Schools and possibly B1 Preliminary for Schools.

## Default Workflow

When the user asks for today's English task:

1. Run `git pull` if network and credentials are available.
2. Read `state/current-status.md`.
3. Read `state/current-week.md`.
4. Read the current month log under `logs/`.
5. Use `plans/2026-study-plan.md` only when the current status or week plan is unclear.
6. Give today's task in Chinese.
7. Keep the task list short, concrete, and executable.
8. Ask the user to report completion, score, time spent, child mood, and any visible difficulty.

When the user reports completion:

1. Update the relevant day in `state/current-week.md`.
2. Append or update the daily entry in `logs/YYYY-MM.md`.
3. Record task completion, score, time spent, mood, and error causes.
4. Adjust tomorrow's task only when the evidence supports it.
5. Commit and push the change to GitHub.

When the user asks for a weekly plan:

1. Review `state/current-status.md`.
2. Review the latest month log.
3. Follow the current route in `plans/2026-study-plan.md`.
4. Create or update `state/current-week.md`.
5. Keep one no-test day.
6. Commit and push the change to GitHub.

When the user asks for diagnostic analysis:

1. Read `diagnostics/initial-diagnostic-table.md` for process.
2. Read the relevant completed record under `diagnostics/results/`.
3. Apply the route rules in the diagnostic file.
4. Recommend one of: foundation-first, A2 Key for Schools first, direct B1 Preliminary for Schools, or delay exam decision.
5. Update `state/current-status.md` only after the user agrees with the route decision.

## Study Rules

- Prefer 35-50 minutes on normal weekdays.
- Keep one no-test day per week.
- Do not over-schedule because the learner is still in primary school.
- If emotional load is high for two consecutive study days, reduce difficulty for the next session.
- Use official Cambridge resources as primary materials when doing diagnosis or exam-style practice.
- Do not introduce full mock tests too early.
- Do not change the long-term route unless diagnostic evidence or repeated weekly records support the change.

## Logging Rules

Use the current month file under `logs/`.

Each daily entry should include:

- Date.
- Planned tasks.
- Completed tasks.
- Time spent.
- Scores or output, if any.
- Error causes.
- Child mood.
- Parent notes.
- Tomorrow adjustment.

Use simple factual language. Do not turn logs into long essays.

## Git Rules

- Before editing, check `git status --short`.
- Do not overwrite user changes.
- Commit related updates together.
- Use concise commit messages, for example:
  - `Update 2026-06-10 study log`
  - `Plan week of 2026-06-10`
  - `Record initial diagnostic result`
- Push after committing when credentials allow it.

## File Map

- `plans/2026-study-plan.md`: yearly roadmap.
- `tasks/2026-task-list.md`: high-level task checklist.
- `diagnostics/initial-diagnostic-table.md`: diagnostic execution guide.
- `diagnostics/diagnostic-record-template.md`: record template for one diagnostic run.
- `diagnostics/results/`: completed diagnostic records.
- `state/current-status.md`: current route, stage, and active target.
- `state/current-week.md`: this week's executable plan and completion status.
- `logs/YYYY-MM.md`: monthly daily records.
- `skills/ket-pet-study-coach/`: reusable study-coach skill.
