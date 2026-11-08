# Group Lab Kickoff: Adrian + Kazim

## Deadlines (plan to the earlier date when the course docs disagree)

| Due | What | Who |
|---|---|---|
| **Sun Nov 8** | Proposal (one page) | Kazim submits |
| **Sun Nov 8** | Group Log 1 | each of us, separately |
| Sun Nov 15 | Group Log 2 | each |
| Tue Nov 17 | Major Oral 2 booking opens, so book early | each |
| Sun Nov 22 | Group Log 3 | each |
| **Sun Nov 22** ⚠️ | Group AI Learning Transcript (lab PDF says Nov 29) | together |
| **Sun Nov 29** ⚠️ | Group Lab Final + design doc (lab PDF says Dec 6) | together |
| Sun Nov 29 | Group Logs 4 and 5 (schedule puts both in Wk 15) | each |
| **Dec 1–4** ⚠️ | Major Oral 2: you defend the *whole* project, including parts you didn't write (lab PDF says Dec 7–9) | each |

⚠️ = the lab PDF and the course schedule disagree. Adrian is asking the instructor.

## Setup checklist (Step 1)

- [x] Channel: iMessage
- [x] Repo created: KokaKolaBeans/CSC240GroupLab
- [ ] **Invite `frimmy` as collaborator** (Settings → Collaborators). Commits must come from each of our own accounts. Owner: KokaKolaBeans
- [ ] Add a C++ `.gitignore` (build outputs, `*.o`, executables, `*.dSYM/`, `.vscode/` if wanted) **before any code**
- [ ] Agree in writing (reply "agreed" here): **no direct commits to `main`**. Every change goes branch → PR → teammate review → merge
- [ ] Turn on branch protection for `main`: require a PR and 1 approval
- [ ] Task board: GitHub Projects with To-Do / In Progress / Done / Blocked, every card has an owner
- [ ] Style agreement (see below)
- [ ] Trial PR: each of us opens and reviews one tiny PR this week (~20 min)

## Style agreement (fill in together; it follows the Oakton C++ Coding Conventions)

- Class names: ___  Functions/members: ___  Constants: ___
- Indentation: ___ spaces; brace style: ___
- Header comment per file: ___
- Pre/postcondition comment format on every public function: ___
- File naming (`.h` / `.cpp` pairs): ___

## How every task flows

```
git checkout main
git pull
git checkout -b feature-<task>
# work, commit small
git push -u origin feature-<task>
```
Then on GitHub: **Compare & pull request**, request the other person as reviewer.

**Review norm:** the reviewer asks one "walk me through this" or "why this approach?" question in the PR comments, and the author answers there. The rubric scores review quality from those comments, and it's how each of us learns the code we'll be questioned on.

## Meetings (both must be logged)

- Week 12: plan & divide (date: ___)
- Week 15: integrate & test (date: ___)

## Group Log template (each of us submits our own, every week)

```
Week [N] — Group Log
Member: [Name]
Date/time of group meeting: [date and platform]
Duration: [minutes]

What I contributed this week:
What I reviewed or learned from my group:
Am I blocked? If yes, what is the blocker:
One thing I would change about our team workflow:
```
