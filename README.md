# Rock, Paper, Scissors Game

A simple and interactive **Rock, Paper, Scissors** game built with JavaScript.  
You play against the computer, and the first to reach **3 points** wins the match.

This project practices DOM manipulation, event handling, conditional logic, and dynamic UI updates.

---

## Demo

The interface includes:

- A large heading at the top.
- A collapsible **Rules to the game** section.
- Player score and computer score displayed side-by-side.
- Three buttons for choosing:
  - **Rock**
  - **Paper**
  - **Scissors**
- A results message showing:
  - Round winner
  - What beat what
- A final winner message once someone reaches 3 points.
- A **Play again?** button that resets the game.

---

## Game Rules

- **Rock beats Scissors**
- **Scissors beat Paper**
- **Paper beats Rock**
- Choosing the same option results in a **tie** (no points awarded).
- First to **3 points** wins the entire game.

---

## Tech Stack

- **HTML** – Layout for rules, buttons, scores, and results.
- **CSS** – Styling for layout, colors, buttons, and responsiveness.
- **JavaScript** – Game logic, random computer choices, scoring, and UI interaction.

---

## Features

- Computer chooses randomly each round.
- Real-time score updates for both player and computer.
- Round result messages (e.g., *"Player wins! Rock beats Scissors"*).
- Game ends at 3 points:
  - Shows the winner message.
  - Hides option buttons.
  - Displays **Play again?** button.
- Full game reset using the reset button.
- Mobile-friendly layout.

---

## How It Works (JavaScript Breakdown)

### 1. Random Computer Choice

```js
function getRandomComputerResult() {
  const options = ["Rock", "Paper", "Scissors"];
  const randomIndex = Math.floor(Math.random() * options.length);
  return options[randomIndex];
}
2. Determine Round Winner
js
Copy code
function hasPlayerWonTheRound(player, computer) {
  return (
    (player === "Rock" && computer === "Scissors") ||
    (player === "Scissors" && computer === "Paper") ||
    (player === "Paper" && computer === "Rock")
  );
}
3. Score Tracking & Round Resolution
playerScore and computerScore start at 0

getRoundResults():

Updates scores

Returns the appropriate round message

4. Updating the UI
Updates score spans

Writes round result text

Checks for game end:

Shows winner message

Shows reset button

Hides R/P/S buttons

5. Resetting the Game
js
Copy code
function resetGame() {
  playerScore = 0;
  computerScore = 0;

  // Reset UI elements...
}
How to Run
Clone the repo:

bash
Copy code
git clone https://github.com/SharpSanders/rock-paper-scissor.git
cd rock-paper-scissor
Open the game:

Double-click index.html
or

Use Live Server inside VS Code

That’s it—everything runs client-side.

Project Structure
text
Copy code
rock-paper-scissor/
├── index.html     # Markup for UI and game elements
├── styles.css     # Styling and layout
└── script.js      # Game logic, score handling, and UI updates
What I Practiced
Game-state management in JavaScript

Using event listeners for button interactions

Updating DOM elements in real time

Conditional branching for game logic

UI feedback messages and layout

Future Improvements
Add image icons for Rock, Paper, Scissors

Add sound effects for button clicks and wins

Add animations for winning/losing rounds

Add keyboard shortcuts (R, P, S)

Add a scoreboard that tracks wins/losses across sessions (localStorage)

Author
Created by Trevyn Sanders.