# Group Lab Proposal: Monster Battle Game

**Group:** Adrian Frimpong, Kazim TODO(group: last name)
**Submitted by:** Kazim, on behalf of the group

## Topic and problem statement

**Topic #3: Gaming.**

A turn-based, human-vs-computer battle game featuring monsters, in the style of Pokémon. The player selects an active monster and decides which moves to use against the opponent. The player wins when all of the opponent's monsters are KO'd.

Problem: create the building blocks of a complex game, with a UI that enables move and monster selection and reflects the current monster's health, the opponent's health, and the monsters available in each roster.

> **TODO(group):** The PDF says the project must "go beyond reimplementing a lab." Consider adding one sentence on the *structural* challenge, for example what the AI opponent has to decide, or what undo has to restore.

## Data structures and the operation each serves

| Structure | Serves | Status |
|---|---|---|
| Stack | Undo / redo of moves: undo returns the most recent move first | Core (changed from queue during planning) |
| Tree + recursion | AI opponent: a decision tree of options based on game state (current health, monsters available, opponent health, opponent monsters available) | Core |
| Hash table | Game state: keys `player`, `computer`, `moves` | Core. Tentative; may change if it doesn't fit |
| Array | Each side's monster slots (stored under the `player`/`computer` keys) | Core |
| Priority heap | Turn order | Stretch (Creative Final Feature candidate) |
| 2D array | Movable players in an explorable space | Stretch |

## Object classes

- **GameState:** represents and holds the players, the turn, and a pointer to each player's currently selected monster. Owns the Player objects.
- **Player:** a human or computer side. Owns its Monster objects. **TODO(group):** anything else a Player holds.
- **AIDecisionTree:** a tree of the options available given the game state. Points at Players; doesn't own them.
- **Monster:** a battle monster with health, moves and KO state. Owned by its Player; GameState only points at the selected one.

Ownership: GameState owns the Player objects, and AIDecisionTree only points at them. When a player is removed, GameState pauses and asks to re-initialize.

When a monster is KO'd it isn't deleted. GameState drops its pointer to it, and the Player keeps ownership.

## Initial task division

| Member | Week of Nov 7 |
|---|---|
| Adrian | To-do list of classes; general game design (what the Player class encapsulates); ideas for the proposal |
| Kazim | Write and submit the final proposal; specific game design (what kind of game, what players do); set up the project file structure |

## Repository and communication

- **GitHub:** https://github.com/KokaKolaBeans/CSC240GroupLab
- **Communication:** iMessage group chat

---

## Before submitting (delete this section first)

- [ ] Kazim agrees with the planning changes Adrian answered for him (stack for undo, Monster class owned by Player, KO handling, hash-table keys)
- [ ] Fill in Kazim's last name
- [ ] Optional: one sentence on the structural challenge in the problem statement
