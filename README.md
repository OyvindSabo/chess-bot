# chess-bot
![Oyvind App Chess.jpg](https://cdn.steemitimages.com/DQmVVZFP7CeVukQVF6dBZ5HpqQDQynmPkhoJErhg5GxHncq/Oyvind%20App%20Chess.jpg)
### Introduction
This is a Chess game in which you play aginst the computer. Apart from the game logic, which uses the chess.js library, I've made everything myself, including the whole interface, and the AI.

### Getting started
Simply download the index.html file and open it in a browser. Alternatively, you can copy all the code in index.html into any JavaScript-compatible HTML editor, or you can simply play on https://oyvind.app/chess

![Chess-bot.jpg](https://cdn.steemitimages.com/DQmac3MZ9sJh6LozeWCsftwvajskKzRK6UxgxdrzqFE1Voy/Chess-bot.jpg)

### How to play
1. The simplest way is to first click the square from which you want to move, and then click the square you want to move to.
2. You can also move pieces by typing the move into the text input field below the board. The input field accepts Forsyth-Edwards Notation, as well as any command stating the square you're moving from and the square to which you want to move.

### How does it work
**Version 1**
- Minimax
- Alpha-beta pruning
- Evaluation: Aggregated value of pieces

**Version 2**
- Minimax
- Alpha-beta pruning
- Quiescence search
- Evaluation: Aggregated value of pieces

### How many moves ahead does the bot evaluate?
Right now, the bot thinks four moves ahead. The deeper the search, the more the alpha-beta comes into effect before searching deeper. I need to optimize the AI quite a bit before it's able to think further ahead. At the top of the chess-bot-x.html file, there is a line `let NUMBEROFPLYS = 4;` To make the bot search 6 moves forwards, simply change 4 to 6. I'm not quite sure, but the bot might only accept an even depth.
