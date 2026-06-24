# ❌ Tic-Tac-Toe Game in Java ⭕

A lightweight, high-performance **Tic-Tac-Toe** game built using **Core Java**. This project showcases clean object-oriented programming (OOP) principles, comprehensive input validation, and a sleek, interactive Command-Line Interface (CLI).

---

## 🚀 Features

* **Interactive Local Multiplayer:** Pass-and-play mode for 2 players.
* **Smart Input Validation:** Prevents illegal moves, accidental overwrites, and invalid inputs.
* **Dynamic Board Rendering:** Real-time updates to the grid layout in the console.
* **Automated Win & Draw Detection:** Instant evaluation of rows, columns, and diagonals.

---

## 🛠️ Tech Stack & Requirements

* **Language:** Java 17 or higher (compatible with Java 8+)
* **Environment:** Command Line / Terminal
* **Compiler/IDE:** Any IDE (IntelliJ IDEA, Eclipse, VS Code) or standard JDK CLI tools

---

## 🏁 Getting Started

Follow these simple steps to download, compile, and run the game on your local machine.

### Prerequisites
Ensure you have the Java Development Kit (JDK) installed. Check your version by running:
```bash
java -version
```

### 1. Clone the Repository
```bash
git clone https://github.com
cd tic-tac-toe-java
```

### 2. Compile the Source Code
Navigate to your source directory and compile the `.java` files:
```bash
javac src/*.java -d bin
```

### 3. Run the Game
Execute the compiled bytecode using the terminal:
```bash
java -cp bin Main
```

---

## 🎮 How To Play

1. The game initializes a fresh `3x3` grid mapped out by cell numbers `1-9`.
2. **Player 1 (X)** and **Player 2 (O)** take alternating turns.
3. When prompted, type a number from `1` to `9` to select your target square:

```text
 1 | 2 | 3 
-----------
 4 | 5 | 6 
-----------
 7 | 8 | 9 
```

4. The first player to align three matching symbols horizontally, vertically, or diagonally wins!
5. If all 9 cells fill up without a winner, the game declares a tie.

---

## 📝 Roadmap / Future Enhancements

- [ ] **GUI Upgrade:** Transition from CLI to a graphical layout using Java Swing or JavaFX.
- [ ] **Scoreboard System:** Track player wins, losses, and ties across multiple rounds.
