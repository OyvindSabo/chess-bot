# chess-bot
![Oyvind App Chess.jpg](https://cdn.steemitimages.com/DQmVVZFP7CeVukQVF6dBZ5HpqQDQynmPkhoJErhg5GxHncq/Oyvind%20App%20Chess.jpg)
### Introduction
This is a Chess game in which you play aginst the computer. Apart from the game logic, which uses the chess.js library, I've made everything myself, including the whole interface, and the AI.

### Getting started
Simply copy all the code from interface.html into a JavaScript-compatible HTML file, or you can play on https://oyvind.app/chess

![Chess-bot.jpg](https://cdn.steemitimages.com/DQmac3MZ9sJh6LozeWCsftwvajskKzRK6UxgxdrzqFE1Voy/Chess-bot.jpg)

### How to play
1. The simplest way is to first click the square from which you want to move, and then click the square you want to move to.
2. You can also move pieces by typing the move into the text input field below the board. The input field accepts Forsyth-Edwards Notation, as well as any command stating the square you're moving from and the square to which you want to move.

### How does it work
The bot uses the Minimax algorithm with alpha-beta pruning. The evaluation of the board takes into account all of your pieces' value, as well as the number of possible moves you can do, thus favoring positions in the center of the board.

### How many moves ahead does the bot evaluate?
Right now, the bot thinks two moves ahead, so it's pretty easy to beat. The alpha-beta pruning doesn't come into effect before searching deeper. I need to optimize the AI quite a bit before it's able to think further ahead within reasonable time. In the interface.html file, in the makeBotMove function, there is a line `const bestMove = findBestMove(2, chess, true)` To make the bot search 4 moves forwards, simply change 2 to 4. I'm not quite sure, but the bot might only accept an even depth.
