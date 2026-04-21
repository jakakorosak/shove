# Shove

A two-player strategy board game played on a square grid. Players take turns placing and pushing slabs, trying to achieve one of three winning conditions.

## Rules

### Overview
Two players — White and Black — take turns on a configurable square grid (default 6×6). Each player starts with a reserve of slabs (default 18).

### Turn structure
Each turn consists of two mandatory steps. Inability to complete either is an immediate loss.

1. **Place** — take a slab from your reserve and place it on any empty square not orthogonally adjacent to an opponent slab
2. **Move** — slide one of your slabs one square orthogonally (up, down, left, right). If the destination is occupied, a push occurs

### Pushing
A push moves the entire contiguous line of slabs one square in the direction of travel. It is legal if the last slab has room and your pushing power meets or exceeds the opponent slabs in the line.

**Pushing power** = the moving slab + all your slabs anywhere in the line ahead + all your slabs contiguously behind the moving slab. Your own slabs in the line offer no resistance.

### Removal
- **Pushed off the edge** — returned to owner's reserve
- **Isolation** — after every move, any slab that had a neighbour before the move but has none after is returned to reserve. A player may deliberately isolate their own slab as a tactical choice.

### Winning
Win conditions are checked after placement and after every move:

1. **No legal turn** — opponent cannot place (reserve empty or all squares adjacent to your slabs) or cannot move any slab
2. **Board clear** — after a push, opponent has zero slabs on the board
3. **Connection** — your slabs form a single orthogonally connected region covering at least half the squares of the board

### Notation
Each turn is two tokens separated by a space. Coordinates are `col,row` numbered from 1. White and black share a numbered line separated by `|`.

```
1.  3,4 2,4-2,5  |  5,6 4,6-4,5
2.  1,2 3,2-3,3  |  6,6 5,6-5,5
```

## Configuration
Before starting, set board size (4×4 to 12×12) and slabs per player.

## Mobile
On touchscreen devices, tap a slab to select it then swipe in the direction you want to move.