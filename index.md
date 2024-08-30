---
layout: base
title: Student Home 
description: Home Page
hide: true
---

# Lilian Wu Homepage

<style>
    /* Styles for Tic Tac Toe Game */
    .board {
        display: grid;
        grid-template-columns: repeat(3, 150px);
        gap: 5px;
        margin: 20px auto;
        align-items: center;
        justify-content: center;
        position: relative;
        top: -1050px;
        right: -400px;
    }
    .cell {
        width: 150px;
        height: 150px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 5em;
        cursor: pointer;
        border: 1px solid #333;
        border-color: #FF0000;
    }
    .title {
        margin-bottom: 20px;
        font-size: 4em;
        color: hotpink;
        text-align: center;
        font-family: cursive;
        position: relative;
        top: -800px;
        right: -400px;
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
        text-align: center;
        justify-content: center;
        align-items: center;
        font-family: Georgia, serif;
        position: relative;
        top: -980px;
        right: -400px;
    }
    .button:hover {
        background-color: hotpink;
        positive: relative;
        
    }
    .container-tic-tac-toe {
        text-align: center;
        margin-top: 20px;
        top: 1050px;
    }
    
    /* Existing styles */
    .container {
        width: 700px;
        height: 800px;
        background-color: #423275;
        margin: 0 auto;
        position: relative;
        right: -400px;
        top: 100px;
        color: #ab92fc;
        padding: 20px;
        font-family: serif;
        opacity: 0.6;
        font-size: 18px;
        line-height: 50px;
    }

    .image-container {
        display: inline-block;
        padding: 10px;
        border-radius: 30px;
        background: linear-gradient(270deg, #30e8b9, #e830a8, #82f186, #309de8, #e83030);
        background-size: 1000% 1000%;
        -webkit-animation: AnimationName 31s ease infinite;
        -moz-animation: AnimationName 31s ease infinite;
        animation: AnimationName 31s ease infinite;
        position: relative;
        top: -700px;
        left: 200px;
        transform: translateX(-50%);
    }

    @-webkit-keyframes AnimationName {
        0% { background-position: 0% 50% }
        50% { background-position: 100% 50% }
        100% { background-position: 0% 50% }
    }
    @-moz-keyframes AnimationName {
        0% { background-position: 0% 50% }
        50% { background-position: 100% 50% }
        100% { background-position: 0% 50% }
    }
    @keyframes AnimationName {
        0% { background-position: 0% 50% }
        50% { background-position: 100% 50% }
        100% { background-position: 0% 50% }
    }

    .image {
        display: block;
        border-radius: 24px;
        width: 420px;
        height: 400px;
    }

    #socials {
        display: flex;
        background-color: #423275;
        width: 450px;
        height: 100px;
        margin: 10px;
        position: relative;
        top: -600px;
        left: -30px;
        opacity: 0.6;
        justify-content: center;
        align-items: center;
    }
</style>

<body>
    <!-- Homepage content -->
    <div class="container">
        <p>Hi! My name is Lilian Wu and I'm currently a junior in Del Norte High School. I took CSSE last year and am now taking CSA to gain a deeper understanding about Java. In my free time, I enjoy playing tennis, playing piano, playing with my cats, cooking, and improving my skill set.  In the future, I'm passionate about STEM and look forward to pursuing a career in this field, as I love learning and solving problems.</p>
    </div>
    <div class="image-container">
        <img id="image" src="images/IMG_5299.png" alt="Me and my friend" class="image">
    </div>
    
    <div id="socials">
        <p><a href="https://github.com/LiliWuu"><img src="images/github.png" width="100" height="100"></a></p>
        <p><a href="https://www.instagram.com/lilianw.w/"><img src="images/instagram.png" width="100" height="80"></a></p>
        <p><a href="https://www.youtube.com/@lilianw6836"><img src="images/youtube.png" width="80" height="100"></a></p>
    </div>

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
