---
layout: base
title: Student Home 
description: Home Page
hide: true
---

# Lilian Wu Homepage

<style>

    .board {
        display: grid;
        grid-template-columns: repeat(3, 150px);
        gap: 5px;
        margin: 20px auto;
        justify-content: center;
    }
    .cell {
        width: 150px;
        height: 150px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 5em;
        cursor: pointer;
        border: 1px solid #e0d6ff;
    }
    .title {
        margin-bottom: 20px;
        font-size: 4em;
        color: hotpink;
        text-align: center;
        font-family: cursive;
    }
    .button {
        padding: 10px 30px;
        font-size: 1.5em;
        color: white;
        background-color: teal;
        border: none;
        border-radius: 30px;
        cursor: pointer;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        transition: background-color 0.3s ease;
        font-family: Georgia, serif;
        display: inline-block;
        margin-top: 20px;
    }
    .button:hover {
        background-color: hotpink;
    }
    .container-tic-tac-toe {
        text-align: center;
    }

</style>

<body>
    <!-- Tic Tac Toe Game -->
    <h1 class="title">Tic Tac Toe</h1>
    <div class="board">
        <div class="cell" id="cell-0" onclick="handleCellClick(0)"></div>
        <div class="cell" id="cell-1" onclick="handleCellClick(1)"></div>
        <div class="cell" id="cell-2" onclick="handleCellClick(2)"></div>
        <div class="cell" id="cell-3" onclick="handleCellClick(3)"></div>
        <div class="cell" id="cell-4" onclick="handleCellClick(4)"></div>
        <div class="cell" id="cell-5" onclick="handleCellClick(5)"></div>
        <div class="cell" id="cell-6" onclick="handleCellClick(6)"></div>
        <div class="cell" id="cell-7" onclick="handleCellClick(7)"></div>
        <div class="cell" id="cell-8" onclick="handleCellClick(8)"></div>
    </div>
    <div class="container-tic-tac-toe">
        <label class="button" onclick="resetGame()">Reset Game</label>
    </div>

    <script>
        // JavaScript for Tic Tac Toe Game
        let board = ["", "", "", "", "", "", "", "", ""];
        let currentPlayer = "X";
        let gameActive = true;

        function handleCellClick(clickedCellIndex) {
            if (!gameActive || board[clickedCellIndex] !== "") return;
            board[clickedCellIndex] = currentPlayer;
            document.getElementById(`cell-${clickedCellIndex}`).innerText = currentPlayer;
            checkWinner();
            currentPlayer = currentPlayer === "X" ? "O" : "X";
        }

        function checkWinner(clickedCellIndex) {
            const winningCombinations = [
                [0, 1, 2], [3, 4, 5], [6, 7, 8], // Rows
                [0, 3, 6], [1, 4, 7], [2, 5, 8], // Columns
                [0, 4, 8], [2, 4, 6]             // Diagonals
            ];
            for (let i = 0; i < winningCombinations.length; i++) {
                const [a, b, c] = winningCombinations[i];
                if (board[a] && board[a] === board[b] && board[a] === board[c]) {
                    gameActive = false;
                    alert(`Player ${currentPlayer} wins!`);
                    return;
                }
            }
            if (!board.includes("")) {
                gameActive = false;
                alert("It's a draw!");
            }
        }

        function resetGame() {
            board = ["", "", "", "", "", "", "", "", ""];
            currentPlayer = "X";
            gameActive = true;
            for (let i = 0; i < 9; i++) {
                document.getElementById(`cell-${i}`).innerText = "";
            }
        }
    </script>
</body>
