# crosbylegal/redline-bench (GitHub) and crosbylegal/RedlineBench (Hugging Face dataset)

| | |
|---|---|
| Publisher | Crosby Legal |
| Licence | code MIT; dataset CC-BY-4.0 |
| Version read | GitHub commit b29d1113af5d98e2d577f4f17673ebb72834f107 (2026-10-02); Hugging Face dataset revision eee1b6790982ed1279e86bec7616b662a61993e6 (last modified 2026-06-18), read 2026-10-07 and rechecked 2026-10-20 |
| Entries in this release | 1 |

RedlineBench is 140 Harbor tasks (101 distinct input groups, 1,351 weighted pass/fail criteria) built from three simulated four-turn negotiations over three base contracts. The code, the judge and the `contract-redliner` skill are in the GitHub repository; the task data (input contract, grounding files, instruction, `rubrics.json`, reference redline `attorney_redlines.docx` and a copy of the verifier) is in the Hugging Face dataset. A submission must be a .docx with at least one tracked change or comment by the task's declared author (the author name the instruction assigns); each criterion is then graded PASS or FAIL by a three-model panel with strict majority.

## How corrections are accepted

Pull request on the GitHub repository (MIT). The same file is vendored in the Hugging Face dataset, which needs the same change.
