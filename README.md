# Tic-Tac-Tow
✨ Features
🎮 Two-player local play: take turns on the same device
🏆 Automatic winner detection across all 8 winning lines (3 rows, 3 columns, 2 diagonals)
🤝 Draw detection when all 9 cells are filled with no winner
🔄 Reset Game button to restart at any time
🆕 New Game button on the result screen after a win or draw
🔒 Move protection: a filled cell is disabled, so it can't be overwritten
📱 Responsive layout using vmin units, so it scales on phones, tablets and desktops
🪶 Zero dependencies: no frameworks, no build step, no installs
🕹️ How to Play
O always goes first, then players alternate with X.
Click any empty cell to place your mark.
The first player to get three in a row (horizontally, vertically or diagonally) wins.
If all nine cells fill up with no winner, the game is a draw.
Click New Game (or Reset Game at any time) to play again.
🗂️ Project Structure
.
├── index.html   # Markup, styles and game logic, all in one file
└── README.md
Inside index.html:
Section	Purpose
<style>	Layout, colours and responsive sizing
Markup	Game board (9 buttons), result message and controls
<script>	Turn handling, win/draw detection and reset logic
🧠 How It Works
Turn tracking. A boolean turnO flips after every move to decide whether the next mark is O or X. A count variable tracks how many moves have been played, which is how a draw is detected.
Win detection. The board is a list of nine cells indexed 0–8. All eight winning combinations are stored in a winPatterns array:
js
const winPatterns = [
  [0, 1, 2], [3, 4, 5], [6, 7, 8],   // rows
  [0, 3, 6], [1, 4, 7], [2, 5, 8],   // columns
  [0, 4, 8], [2, 4, 6],              // diagonals
];
After each move, checkWinner() loops through these patterns and checks whether all three cells are non-empty and identical.
End of game. When someone wins or the board fills up, the remaining cells are disabled and a result message with a New Game button appears.
🛣️ Ideas for the Future
 Score tracking across multiple rounds
 Single-player mode with a computer opponent (random, then minimax)
 Highlight the winning line
 Choose who goes first
 Dark / light theme toggle
 Sound effects and subtle animations
 Keyboard accessibility improvements
🤝 Contributing
Contributions, issues and feature requests are welcome!
Fork the project
Create your feature branch (git checkout -b feature/amazing-feature)
Commit your changes (git commit -m "Add amazing feature")
Push to the branch (git push origin feature/amazing-feature)
Open a Pull Request
<div align="center">
Built with ❤️ by Ojashree
If you enjoyed this project, consider giving it a ⭐ on GitHub!
</div>
