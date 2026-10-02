# GridHack (2012 Edition)

A Flash game I made in 2012, originally released on Newgrounds and Kongregate. Flash Player is
long gone, so this copy runs in the browser on [Ruffle](https://ruffle.rs), a Flash Player emulator.

**Play: https://mopierotti.github.io/grid-hack-game-2012/**

Needs a desktop browser (tested in Chrome and Firefox) and a keyboard. It loads on phones and
tablets, but you can't play it there without a hardware keyboard.

Gameplay recording: [gameplay.mp4](gameplay.mp4)

## Controls

> **Tip:** hold **Shift** while pressing an arrow key to move two spaces at once. The game
> itself never mentions this.

| Key | Action |
|---|---|
| Arrow keys | Move |
| Shift + arrow key | Move two spaces at once |
| A / S (later D / F) | Switch color |
| R | Restart level |
| M | Mute |

The in-game **How to Play** screen covers the rest.

## Play offline

The game has to be served over HTTP; browsers won't run Ruffle from a double-clicked `index.html`.
With Python 3 installed (macOS, Linux, or Windows):

```
python3 -m http.server 8765 --directory web
```

Then open http://localhost:8765/.

## What's changed since 2012

The SWF has a few small patches so it runs cleanly today: a grid-rendering fix for Ruffle, the
defunct analytics call and outbound links removed, and a bundled monospace font for the terminal
text. Gameplay is unchanged.

## Credits and third-party components

- Music used with permission; artists are credited in the game's About screen.
- [Ruffle](https://github.com/ruffle-rs/ruffle) (MIT / Apache-2.0), in `web/ruffle/`.
- [IBM Plex Mono](https://github.com/IBM/plex) (SIL Open Font License 1.1), in `web/fonts/`.
- The game itself bundles Box2D, the Flint particle system, and TweenLite, compiled in 2012.
