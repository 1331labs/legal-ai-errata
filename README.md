# Lexspring Legal AI Errata Repo

By 1331 Labs. Sam Redlich, contributor.

Corrections to published legal AI artifacts: benchmark rubrics and gold answers, legal skills and plugins, and contract templates.

Each entry sets out the defects found in one public file or task, quotes the artifact at a fixed commit, quotes the governing source from its official publisher, and gives the correction as replacement text or a patch. Every correction is also offered to the artifact's maintainers through the channel their repository provides, and the entry links to that pull request or issue once it is open.

## This release

16 corrections to 8 repositories from 6 publishers.

| Publisher | Artifact | Kind | Corrections |
|---|---|---|---|
| Harvey | [harvey-labs](targets/harveyai-harvey-labs/TARGET.md) | Benchmark rubrics | 5 |
| Harvey | [biglaw-bench](targets/harveyai-biglaw-bench/TARGET.md) | Benchmark gold answers | 1 |
| LegalQuants | [lq-plugin-oss](targets/legalquants-lq-plugin-oss/TARGET.md) | Legal skills and reference files | 3 |
| LegalQuants | [lq-ai](targets/legalquants-lq-ai/TARGET.md) | Legal skills | 1 |
| Anthropic | [claude-for-legal](targets/anthropics-claude-for-legal/TARGET.md) | Legal plugins | 2 |
| General Legal | [legal-templates](targets/general-legal-legal-templates/TARGET.md) | Contract templates | 2 |
| Thomson Reuters | [cocobench-sample](targets/thomsonreuters-cocobench-sample/TARGET.md) | Benchmark tasks | 1 |
| Crosby Legal | [redline-bench](targets/crosbylegal-redlinebench/TARGET.md) | Benchmark harness | 1 |

The corrections are set out one by one in [RELEASE-01.md](RELEASE-01.md). The full list is in [REGISTER.md](REGISTER.md) and, as data, in [REGISTER.csv](REGISTER.csv).

The counts say where corrections were found among the files that were read. They are not a measure of any publisher's quality and they do not support a comparison between publishers: the artifacts differ in size by orders of magnitude and were not read to the same depth.

## What counts as a correction here

An entry is included only where the defect is objective and has one correct answer that a maintainer can check without taking anyone's word for it:

- **A rule stated wrongly.** A rubric, skill or template states a statutory amount, deadline, citation or requirement that differs from the text of the governing source in force on the date the artifact's own facts require. Example: a rubric criterion that requires a 15-day challenge period where the governing rule gives 30 days.
- **An authority that is not what the artifact says it is.** A citation that resolves to a withdrawn opinion, a different paper, or a provision that does not contain the quoted words.
- **A rubric or gold answer that contradicts its own source documents.** The task file says one thing and the criterion that grades it requires another.
- **A required term missing.** A template or checklist omits a term that the governing regulation requires an agreement of that kind to contain.
- **Code that cannot do what the task requires.** Shown by a run that anyone can repeat.

Points that turn on contract construction, drafting preference, or a view about how a benchmark ought to be designed are outside this release.

## Reading an entry

Each entry is a markdown file under `targets/<artifact>/findings/`.

| Section | Content |
|---|---|
| Front matter | Identifier, artifact, location (file, line, criterion or section), defect class, severity, status, and the dates the correction was filed, first answered and resolved |
| Defect | What the artifact says, what is correct, and the effect on a user of the artifact or on scoring |
| Evidence | Exact quotations from the artifact with path and line, and from the governing source with its URL |
| Proposed correction | Old text and new text for every place that states the defect; a patch file where the licence permits a derivative |
| Verification notes | What was opened and compared, the upstream commit at which the passage was confirmed unchanged, and the sources |
| Objections considered | The strongest objections a maintainer could raise, and the answer to each from the record |
| Upstream tracker | Where present, related issues and pull requests in the publisher's repository |

### Severity

| Level | Meaning |
|---|---|
| high | A correct answer is scored wrong, or a competent user of the artifact is led to a wrong result on a point that changes an outcome |
| medium | A real defect whose effect is limited or conditional |
| low | A wrong citation, date or restatement with no effect on a result |

### Status

| Status | Meaning |
|---|---|
| ready-to-file | Verified as described below; not yet offered upstream |
| filed | Pull request or issue open with the publisher; the entry links to it |
| acknowledged | The publisher has replied |
| merged | The publisher has applied the correction |
| declined | The publisher has declined the correction; the entry records the reason given |
| withdrawn | The entry was wrong; it stays in the register with the reason |

### Dates

| Field | Meaning |
|---|---|
| `filed_on` | The day the issue or pull request was opened with the publisher |
| `first_response_on` | The day of the first comment, review, label or state change by a publisher maintainer. Automated checks and bots do not count |
| `resolved_on` | The day the correction was merged, declined or superseded |

The dates are read from the publisher's tracker and updated in the register as they occur. Time from `filed_on` to `first_response_on` is recorded for each entry; it is reported as the fact it is, per entry, and is not aggregated into a comparison between publishers.

## What each entry contains

1. **The artifact.** Every quotation matches the file character for character at the commit recorded in the artifact's `TARGET.md`, and the entry gives the date on which the passage was confirmed unchanged at the repository's head.
2. **The governing source.** Every rule, amount, deadline and citation is quoted from its official publisher (for example the eCFR, the Federal Register, the issuing court or agency, a legislature's own site), with the URL. Where an official site could not be reached and an official bulk copy was used instead, the entry says so.
3. **The date.** The provision is shown to be in force on the date the artifact's own facts require, not only today.
4. **The arithmetic.** Every date, count and sum in an entry is recomputed.
5. **Objections.** Each entry states the strongest objections a maintainer could raise (another criterion, instruction or document that resolves the point, a reading or an effective date under which the artifact is right, or an intentional error the task wants caught) and answers them.
6. **The correction.** The proposed text agrees with every other place in the same task, skill or document that states the same fact, so that the correction does not leave the artifact inconsistent with itself. Patches apply cleanly to the repository's head.
7. **Earlier reports.** Where an issue or pull request in the publisher's repository already touches the same defect, the entry names it.

## Limits

- Nothing here is legal advice. The entries concern the text of published artifacts.
- The entries do not assess any publisher's products, services or people.
- An entry reflects the artifact at the recorded commit and the law on the recorded date. Both change.
- Synthetic task documents sometimes contain errors on purpose, for the solver to catch. An entry is recorded only where the rubric rewards the error instead of its correction.

## Reporting an error in this repository

Open an issue citing the entry identifier. An entry shown to be wrong is marked `withdrawn` with the reason and stays in the register.

## Credit and licence

Lexspring Legal AI Errata Repo by 1331 Labs. Sam Redlich, contributor.

Quotations from the artifacts and patch files derived from them remain under each artifact's own licence, recorded in its `TARGET.md`. Where an artifact has no licence permitting derivatives, the correction is given as old and new text and no patch is supplied.
