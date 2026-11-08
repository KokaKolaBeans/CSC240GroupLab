# Answers to Questions

1. What’s the game?
   * Turn-based game featuring battle monsters(in the style of pokemon). The player will select active monster, and decide moves to use against opponent in effort to win battle.
   * Player wins when opposing monsters are all KOd. It is human vs. computer.
2. Problem statement:
   * Create the building blocks of a complex game displaying UI that enables move, monster selection and reflects current monster's health, opponent's health and available monster in player's/opponent's roster.
3. Structures → operations/Core V stretch
   Core:
   * Queue - Undo/Redo moves
   * Trees/Recursion - AI opponent
   * Array + HashTable - GameState
   Stretch(CFF):
   * Priority Heap - Turn order
   * 2D array - movable players in explorable space
4. Classes.
   * GameState class - representing and holding players, the turn, and current selected monster of players
   * Player class What’s the second class (at least), and what does each one represent?
   * AI DecisionTree class - tree of available options depending on game state(current health, number of monsters avail, opp health, opp. number of monsters avail, etc.)
5. Ownership.
   * Given both the turn-order structure and AI DecisionTree class hold Players, the GameState owns the Player objects, and AI DecisionTree only points at them. When a player is removed, the GameState pauses and asks to re-initialize, though in our game, the removal of monsters will be .. rare given the limited scope
