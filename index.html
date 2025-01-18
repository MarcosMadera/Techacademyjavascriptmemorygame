<!DOCTYPE html>
<html>
<head>
    <title>Memory Game</title>
    <style>
        /* Styling for the overall body of the page, setting the font and text alignment */
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }

        /* Styling for the game board, using a grid layout to arrange cards */
        #gameBoard {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 25px;
            width: 600px;
            margin: 20px auto;
        }

        /* Basic styling for each card, including size and 3D perspective for flipping effect */
        .card {
            width: 112px;
            height: 150px;
            perspective: 1000px;
            position: relative;
        }

        /* Styling for the inner part of the card, including transition for the flip effect */
        .cardInner {
            position: relative;
            width: 100%;
            height: 100%;
            text-align: center;
            transition: transform 0.6s;
            transform-style: preserve-3d;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }

        /* Special styling for flipped cards to rotate them 180 degrees */
        .card.flipped .cardInner {
            transform: rotateY(180deg);
        }

        /* Styling for the front and back of each card, including visibility and alignment */
        .cardFront, .cardBack {
            position: absolute;
            width: 100%;
            height: 100%;
            backface-visibility: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            border-radius: 10px;
        }

        /* Specific styling for the front and back sides of the card */
        .cardFront {
            background-color: orange;
        }
        .cardBack {
            background-color: darkblue;
            color: white;
            transform: rotateY(180deg);
            font-size: 93px;
        }

        /* Styling for matched cards with animation effect */
        .matched {
            animation: matchAnimation 0.5s;
            background-color: green;
            border-radius: 10px;
        }

        /* Keyframe animation for matched cards, giving them a pulsing effect */
        @keyframes matchAnimation {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.2); }
        }

        /* Styling for the attempt counter displayed below the game board */
        #attemptCounter {
            margin-bottom: 20px;
        }

        /* Initial styling for the reset button, hidden until the game ends */
        #resetButton {
            display: none;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div id="gameBoard"></div>
    <div id="attemptCounter">Attempts Remaining: 8</div>
    <button id="resetButton" onclick="resetGame()">Play Again</button>

    <script>
        // Initialization of the game symbols, attempt counter, and other state variables
        const symbols = ["♣", "♥", "♠", "♦"];
        let attempts = 8;
        let matches = 0;
        let flippedCards = [];
        let lockBoard = false;
        const gameBoard = document.getElementById('gameBoard');
        const attemptCounter = document.getElementById('attemptCounter');
        const resetButton = document.getElementById('resetButton');

        // Function to set up the game by creating cards and arranging them on the game board
        function setupGame() {
            let deck = [...symbols, ...symbols];
            deck.sort(() => 0.5 - Math.random());
            deck.forEach(symbol => {
                const card = document.createElement('div');
                card.classList.add('card');
                card.dataset.symbol = symbol;

                const cardInner = document.createElement('div');
                cardInner.classList.add('cardInner');

                const cardFront = document.createElement('div');
                cardFront.classList.add('cardFront');

                const cardBack = document.createElement('div');
                cardBack.classList.add('cardBack');
                cardBack.textContent = symbol;

                cardInner.appendChild(cardFront);
                cardInner.appendChild(cardBack);
                card.appendChild(cardInner);

                card.addEventListener('click', flipCard);
                gameBoard.appendChild(card);
            });
        }

        // Function to handle the card flip action
        function flipCard() {
            if (lockBoard) return;
            if (this.classList.contains('flipped')) return;
            this.classList.add('flipped');
            if (!flippedCards[0]) {
                flippedCards[0] = this;
            } else {
                flippedCards[1] = this;
                checkForMatch();
            }
        }

        // Function to check if the flipped cards are a match
        function checkForMatch() {
            if (flippedCards[0].dataset.symbol === flippedCards[1].dataset.symbol) {
                disableCards();
            } else {
                unflipCards();
            }
        }

        // Function to disable cards that are matched and update game state
        function disableCards() {
            flippedCards.forEach(card => {
                card.classList.add('matched');
                card.removeEventListener('click', flipCard);
            });
            resetBoard();
            matches++;
            attempts--;
            attemptCounter.textContent = `Attempts Remaining: ${attempts}`;
            checkGameEnd();
        }

        // Function to flip the cards back if they are not a match
        function unflipCards() {
            lockBoard = true;
            setTimeout(() => {
                flippedCards.forEach(card => {
                    card.classList.remove('flipped');
                });
                resetBoard();
                attempts--;
                attemptCounter.textContent = `Attempts Remaining: ${attempts}`;
                checkGameEnd();
            }, 1000);
        }

        // Function to reset the board for the next turn
        function resetBoard() {
            flippedCards = [];
            lockBoard = false;
        }

        // Function to check if the game has ended and handle the end-of-game scenarios
        function checkGameEnd() {
            if (matches === 4) {
                setTimeout(() => {
                    if (confirm("You win! Play again?")) {
                        resetGame();
                    }
                }, 500);
            } else if (attempts === 0) {
                setTimeout(() => {
                    if (confirm("Game Over! You lose. Play again?")) {
                        resetGame();
                    }
                }, 500);
            }
        }

        // Function to reset the game and start a new round
        function resetGame() {
            gameBoard.innerHTML = '';
            attemptCounter.textContent = 'Attempts Remaining: 8';
            attempts = 8;
            matches = 0;
            setupGame();
        }

        // Initial call to set up the game when the page loads
        setupGame();
    </script>
</body>
</html>


