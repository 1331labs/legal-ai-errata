# harveyai/harvey-labs

| | |
|---|---|
| Publisher | Harvey |
| Licence | MIT |
| Version read | commit 5dc79a9b1323b4aef2d3d5d922735d304dd71361 (committed 2026-10-06); entries rechecked at 97810facfd447317b57f6dd02a1469561c573d79 on 2026-10-20; patches rebased and rechecked at 81d6a31b22d7c9f661cda4770cffcc12a5735dc2 on 2026-10-23 |
| Entries in this release | 5 |

Harvey LAB (Legal Agent Benchmark) is a public repository of 2,010 `task.json` files in 27 top-level task folders, each with instructions and an inline rubric of equally weighted pass/fail criteria (`id`, `title`, `match_criteria`, and `deliverables` in most tasks); most tasks also carry synthetic source documents. By default two LLM judges (`claude-sonnet-4-6` and `gpt-5.5`) each grade every criterion against its `match_criteria`, and a task scores only if every criterion passes (docs/eval-strategies.md).

## How corrections are accepted

Pull request. CONTRIBUTING.md accepts task and rubric corrections, asks for small focused pull requests and for the offline task integrity tests to be run first. CHANGELOG.md requires a dataset entry in the same pull request.
