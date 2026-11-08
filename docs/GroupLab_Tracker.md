# Group Lab Tracker

Shared progress tracker for the CSC-240 Group Lab, kept in the group repo so we both see the same state. Change it through a PR like any other file. Adrian maintains it with an AI wizard; see *AI Disclosure Log*.

Sources last read 2026-11-07:
- Group Lab PDF, modified 2026-11-07 13:29 (re-read after it changed; no dates moved)
- Course Schedule PDF, modified 2026-11-07 12:00

## 1. Timeline

Plan-to = the earlier of the two dates. ⚠️ = the PDFs disagree, so it's under *Open questions*.

| Item | Group Lab PDF | Schedule | Plan-to | Status |
|---|---|---|---|---|
| Proposal (ungraded, required) | Sun Nov 8 | Sun Nov 8 (Wk 12) | **Sun Nov 8** | 🟡 Kazim submitting |
| Group Log 1 | Sun Nov 8 (Wk 12) | Sun Nov 8 (Wk 12) | **Sun Nov 8** | ⬜ |
| Group Log 2 | Sun Nov 15 (Wk 13) | Sun Nov 15 (Wk 13) | Sun Nov 15 | ⬜ |
| Group Log 3 | Sun Nov 22 (Wk 14) | Sun Nov 22 (Wk 14) | Sun Nov 22 | ⬜ |
| Group AI Learning Transcript ⚠️ | Sun Nov 29 | Sun Nov 22 (Wk 14) | **Sun Nov 22** | ⬜ |
| Group Log 4 | Sun Nov 29 (Wk 15) | Sun Nov 29 (Wk 15) | Sun Nov 29 | ⬜ |
| Group Log 5 ⚠️ | Sun Dec 6 (Wk 16) | Sun Nov 29 (Wk 15) | **Sun Nov 29** | ⬜ |
| Design document (schedule only) ⚠️ | — | Sun Nov 29, and ≥24h before MOI2 slot | **Sun Nov 29** | ⬜ |
| Group Lab Final (40) ⚠️ | Sun Dec 6 | Sun Nov 29 (Wk 15) | **Sun Nov 29** | ⬜ |
| MOI2 booking opens (schedule only) | — | Tue Nov 17 | Nov 17 | ⬜ book early |
| Major Oral Inquiry 2 / defense ⚠️ | Dec 7–9 | Dec 1–4 | **Dec 1–4** | ⬜ |

Required meetings: Week 12 (plan & divide) ✅ Sat Nov 7 ~3 PM ET, iMessage, ~60 min; Week 15 (integrate & test) ⬜. Log both.

## 2. Team

| Name | Last name | GitHub | Areas (this week) | Contact |
|---|---|---|---|---|
| Adrian | Frimpong | frimmy | class to-do list; general game design (what Player encapsulates); proposal ideas | |
| Kazim | ? | ? | writes + submits proposal; specific game design; project file structure | |

Group is 2 members (Adrian + Kazim). ⚠️ The PDF says groups of 3–4, so this is under *Open questions*.
Repo owner `KokaKolaBeans`: presumably Kazim? Confirm.

## 3. Infrastructure (Step 1)

| Item | Status | Owner | Notes |
|---|---|---|---|
| Communication channel | ✅ iMessage | | The PDF recommends Discord/Slack, but any single place satisfies it |
| GitHub repo | ✅ created 2026-11-07 | KokaKolaBeans | https://github.com/KokaKolaBeans/CSC240GroupLab (public) |
| All members added as collaborators | ⬜ | KokaKolaBeans | 2026-11-07: frimmy's pending invite is for `KokaKolaBeans/CSC240Lab11` (wrong repo); still push:false on CSC240GroupLab. Stopgap under consideration: fork + PR from frimmy's fork. Adrian (frimmy) got a 403 on the collaborator list, so he probably has no push access yet |
| C++ `.gitignore` before first code | ⬜ | | not in repo yet |
| "No direct commits to main" agreed in writing | ⬜ | | |
| Branch protection on `main` | ⬜ | | not enabled (GitHub API 404) |
| Task board (To-Do / In Progress / Done / Blocked, named owners) | ⬜ | | README.MD holds this week's split for now |
| Style agreement | ⬜ | | |
| Trial PR (20 min, PDF recommends) | ⬜ | | |

## 4. Project

Source: [answers.md](answers.md) (Adrian, 2026-11-07).

- Topic: #3 Gaming: turn-based, human-vs-computer monster battle game (Pokémon-style genre; use original monsters/moves). Win = all opponent monsters KO'd.
- Problem statement: building blocks of a complex game; UI for move and monster selection, showing health and rosters. TODO(group): add the structural challenge so it goes beyond a lab.
- Core structures: Stack → undo/redo (most recent first); Tree + recursion → AI opponent; HashTable (keys player/computer/moves) + Array (monster slots) → GameState. Hash table is tentative: open Q on whether 3 fixed keys justify hashing (rubric 3.1 "appropriately and efficiently")
- Stretch / CFF candidates: Priority heap → turn order; 2D array → explorable space
- Classes: GameState (owns Players; points at selected monsters), Player (owns its Monsters), Monster (health, moves, KO state), AIDecisionTree (points at Players)
- Ownership/removal: GameState owns Players; AI tree only points at them. Player removal → pause and re-init. Monster KO → not deleted; GameState drops its pointer, Player keeps ownership. Open Q: do AI tree nodes also point at monsters?

## 5. Phase status

- **Phase 0 Setup & Proposal:** proposal draft ready pending Kazim's agreement + submit; setup checklist open. Drafts: `GroupLab_Proposal.md` (4 open questions for Kazim), `GroupLab_Kickoff.md` (for iMessage)
- Phase 1 Build & Group Log: Week 12 entry drafted for Adrian
- Phase 2 Group AI Transcript: not started
- Phase 3 CFF: not started
- Phase 4 Final package: not started
- Phase 5 Defense prep: not started

## 6. Group Log

| Week | Adrian | Kazim |
|---|---|---|
| 12 (Nov 8) | 🟡 [drafted](logs/Week12_GroupLog_Frimpong.md) | ⬜ |
| 13 (Nov 15) | ⬜ | ⬜ |
| 14 (Nov 22) | ⬜ | ⬜ |
| 15 (Nov 29) | ⬜ | ⬜ |
| 16 / 15b | ⬜ | ⬜ |

## 7. Decisions & changes from proposal

- 2026-11-07: Undo/redo structure changed queue → stack (undo returns most recent first). Monster added as a class owned by Player; GameState holds pointers only. Hash table keyed player/computer/moves (tentative). Adrian answered on Kazim's behalf; Kazim to confirm.
- 2026-11-07: Workflow change idea (Adrian): track tasks with GitHub Issues. Feeds critical-thinking Q5.
- 2026-11-07: Topic #3 Gaming: monster battle game. Turn-order heap and 2D explorable map moved to stretch/CFF.

## 8. Open questions for instructor

1. Group AI Transcript: Nov 29 (Group Lab PDF) or Nov 22 (Schedule, Week 14)?
2. Group Lab Final: Dec 6 (Group Lab PDF) or Nov 29 (Schedule, Week 15)?
3. MOI2: Dec 7–9 (Group Lab PDF) or Dec 1–4 (Schedule)?
4. Group Log 5: Week 16 (Dec 6) or Week 15 alongside Log 4 (Schedule)?
5. Our group has 2 members; the PDF says 3–4. Is that expected, or will someone be added?
6. Is the Schedule's "Design document (Nov 29)" the same as `GroupLab_Specifications.pdf`?

## 9. AI Disclosure Log

| Date | Tool | What was asked | What was done with it |
|---|---|---|---|
| 2026-11-07 | Claude Code (group-lab-wizard) | Reconcile Group Lab PDF and Schedule deadlines; read-only audit of the group repo | Built this tracker's timeline and setup checklist |
| 2026-11-07 | Claude Code (group-lab-wizard) | Assemble Adrian's answers into the proposal's 5-bullet format; flag gaps as questions | Draft `GroupLab_Proposal.md` given to Kazim; group content is the group's own words |
| 2026-11-07 | Claude Code (group-lab-wizard) | Setup checklist, timeline and workflow summary from the Group Lab PDF | `GroupLab_Kickoff.md` shared in iMessage |
| 2026-11-07 | Claude Code (group-lab-wizard) | Ask questions about undo order, KO ownership, Monster class, hash-table keys; fold the group's answers into the proposal | Group changed queue → stack and added Monster ownership rules (decisions are the group's) |
| 2026-11-07 | Claude Code (group-lab-wizard) | Put Adrian's Week 12 log answers into the PDF template | `logs/Week12_GroupLog_Frimpong.md` |
