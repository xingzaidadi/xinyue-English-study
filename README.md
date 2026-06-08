# Xinyue English Study

This repository tracks Xinyue's Cambridge English study plan, tasks, diagnostics, and future study-coach tooling.

## Current Goal

Build a steady home-study path from June 2026 through December 2026 for:

- A2 Key for Schools, commonly called KET for Schools
- B1 Preliminary for Schools, commonly called PET for Schools

The default strategy is:

1. Diagnose first, using official Cambridge-style tasks.
2. Prefer A2 Key for Schools first unless the diagnostic result clearly supports B1.
3. Protect interest and confidence before exam speed.
4. Review weekly, adjust monthly, and only register for an exam when readiness is visible.

## Repository Structure

```text
AGENTS.md                    Repository operating rules for Codex

plans/
  2026-study-plan.md        Full 2026 roadmap from June 8 to December 31

tasks/
  2026-task-list.md         Action checklist and recurring tasks

diagnostics/
  initial-diagnostic-table.md
  diagnostic-record-template.md
  results/

state/
  current-status.md         Current route, phase, and target
  current-week.md           This week's daily plan and completion status

logs/
  2026-06.md                Daily study log for June 2026

skills/
  ket-pet-study-coach/      Reusable study-coach workflow
```

Future additions:

```text
logs/
  2026-07.md
  2026-08.md
  ...

tools/
  Optional helper scripts for week creation or task lookup
```

## Operating Rhythm

- Update the plan when the target route changes.
- Update the task list every week.
- Keep diagnostic results separate from the plan so the plan stays readable.
- Use official Cambridge resources as the primary reference, and third-party resources only as supplements.

## Daily Use

On a new computer:

```powershell
git clone https://github.com/xingzaidadi/xinyue-English-study.git
cd xinyue-English-study
codex "Please follow AGENTS.md and tell me Xinyue's English task for today."
```

For everyday use after the repository already exists:

```powershell
cd xinyue-English-study
codex "Please follow AGENTS.md and tell me Xinyue's English task for today."
```

After the study session, report completion in natural language. Codex should update `state/current-week.md`, update the current month log under `logs/`, commit, and push.

## Official Resource Links

- A2 Key for Schools preparation: https://www.cambridgeenglish.org/exams-and-tests/qualifications/key/preparation/
- B1 Preliminary for Schools preparation: https://www.cambridgeenglish.org/exams-and-tests/qualifications/preliminary/preparation/
- Cambridge Test Your English: https://www.cambridgeenglish.org/test-your-english/
- Write & Improve: https://writeandimprove.com/
- Find an authorised exam centre: https://www.cambridgeenglish.org/find-a-centre/find-an-exam-centre/
