# Tic-Tac-Toe

A two-player Tic-Tac-Toe game that runs in the browser, built with plain HTML, CSS and JavaScript. No frameworks or dependencies.

🎮 **Play it live:** [your-live-link-here](https://tic-tac-toe-mehex.vercel.app/)



## Features

- Two players take turns on a 3×3 board (O goes first, then X)
- Detects all 8 winning combinations (3 rows, 3 columns, 2 diagonals)
- Detects a draw when all 9 boxes are filled with no winner
- Shows a result message (winner or draw) with a **New Game** button
- **Reset Game** button to restart at any time
- Filled boxes are disabled, so a move can't be overwritten
- Responsive sizing using `vmin` units, so the board scales to the screen

## How to Play

1. Open the game. Player **O** starts.
2. Click an empty box to place your mark. Then it's X's turn.
3. Get three of your marks in a row, column or diagonal to win.
4. If all 9 boxes are filled and nobody has won, the game is a draw.
5. Click **New Game** (after a result) or **Reset Game** (any time) to play again.

## Tech Stack

| Area       | Technology         |
| ---------- | ------------------ |
| Structure  | HTML5              |
| Styling    | CSS3 (Flexbox)     |
| Game logic | Vanilla JavaScript |

## Project Structure

```
Tic-Tac-Toe/
├── index.html   # Page layout: board, result message, buttons
├── style.css    # Styling and responsive board sizing
├── script.js    # Game logic: turns, win check, draw check, reset
└── README.md
```

## How It Works

- The board is nine `<button class="box">` elements, read in order as positions 0 to 8.
- `turnO` tracks whose turn it is, and `count` tracks the number of moves played.
- `winPatterns` holds the 8 winning index combinations. After every move, `checkWinner()` compares the three boxes in each pattern.
- If a pattern matches, `showWinner()` displays the result and disables the board. If `count` reaches 9 with no winner, `gameDraw()` runs.
- `resetGame()` clears the board, resets `turnO` and `count`, and hides the result message.

## Run Locally

```bash
git clone https://github.com/geekymehex/Tic-Tac-Toe.git
cd Tic-Tac-Toe
```

Open `index.html` in your browser. No installation or build step is needed.

## Future Improvements

- [ ] Highlight the winning line
- [ ] Score counter across rounds
- [ ] Play against the computer (random moves first, then minimax)
- [ ] Let players choose X or O
- [ ] Show whose turn it is

## Author

**Mehefuj Mondol**
2nd year B.Tech (AI & ML), Ideal Institute of Engineering

- GitHub: [@geekymehex](https://github.com/geekymehex)
- LinkedIn: [your-profile](www.linkedin.com/in/mehefuj-mondol)

## License


## License

This project is open source under the [MIT License](LICENSE).
