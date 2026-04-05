# ♟️ Vanilla JavaScript Chess Game

A clean and interactive chess game built from scratch using **Vanilla JavaScript**, focusing on core game logic and chess engine fundamentals.

---

## 🚀 Features

* ♟️ Fully functional chessboard (8x8 grid)
* 🔄 Turn-based gameplay (White vs Black)
* 🎯 Legal move generation for all pieces:

  * Pawn
  * Knight
  * Bishop
  * Rook
  * Queen
  * King
* 🚫 Illegal moves are prevented (king cannot move into check)
* ⚠️ Check detection
* 🏁 Checkmate detection (game ends when checkmate occurs)
* ✨ Interactive UI with move highlighting

---

## 🧠 Project Motivation

This project was built to deeply understand:

* Game state management
* Algorithmic thinking
* Rule-based systems
* Building a simple chess engine from scratch

Rather than relying on libraries, all logic — including movement rules and checkmate detection — was implemented manually.

---

## 🏗️ Tech Stack

* **JavaScript (Vanilla)**
* **HTML5**
* **CSS3**

No frameworks or external libraries were used.

---

## ⚙️ How It Works

### 🧩 Board Representation

The chessboard is represented as a **2D array**:

```js
board[y][x]
```

Each cell contains either:

* A piece (e.g. `"w_king"`, `"b_pawn"`)
* Or `null`

---

### ♟️ Move Generation

Each piece has its own movement logic implemented in:

```js
getMoves(x, y)
```

This function generates **pseudo-legal moves** (ignores check).

---

### 🛡️ Legal Move Validation

To ensure valid gameplay:

```js
getLegalMoves(x, y)
```

* Simulates each possible move
* Checks if the king would be in check
* Filters out illegal moves

---

### ⚠️ Check Detection

```js
isCheck(color)
```

Determines whether a king is under attack by:

* Finding the king’s position
* Checking if any opponent piece can reach it

---

### 🏁 Checkmate Detection

```js
isCheckmate(color)
```

A player is in checkmate if:

* Their king is in check
* AND they have no legal moves left

---

## 🎮 How to Play

1. Click on a piece (only current player's pieces are selectable)
2. Valid moves will be highlighted
3. Click a highlighted square to move
4. Game automatically switches turns
5. Game ends when a checkmate is detected

---

## 🧪 Possible Improvements

* ♜ Castling
* ♟️ En passant
* 👑 Pawn promotion
* 🤖 AI opponent (Minimax algorithm)
* 🔊 Sound effects & animations
* ♻️ Undo/Redo functionality

---

## 📌 Future Goals

* Implement a basic AI opponent using Minimax
* Improve performance and code structure
* Convert the project into a React-based application
