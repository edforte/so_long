# so_long

A small 2D top-down game in C built with the [MiniLibX](https://github.com/42Paris/minilibx-linux) graphics library. Project of the 42 Common Core.

The player collects every item on the map and then reaches the exit, with a move counter shown in the terminal.

## Features

- Map loading from `.ber` files with full validation: rectangular shape, closed walls, exactly one player and one exit, at least one collectible
- **Path-finding check** (flood fill) that rejects maps where items or the exit are unreachable
- Sprite-based rendering with custom XPM assets
- Clean exit on `ESC` or window close, without memory leaks

## Build & run

Requires Linux with X11 development libraries.

```bash
make
./so_long maps/mappa.ber
```

## Controls

| Key | Action |
| --- | --- |
| `W` `A` `S` `D` | Move |
| `ESC` | Quit |

## What I learned

Event-driven game loops, 2D rendering, input validation and flood-fill path finding in C.
