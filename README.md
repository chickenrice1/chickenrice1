<!DOCTYPE html>
<html lang="en">
- 👋 Hi, I’m @chickenrice1
- 👀 I’m interested in guitar and coding, although im not very good at coding.
- 🌱 I’m currently learning russian and spanish!
- 💞️ I’m looking to collaborate on... right here! mention me and we can work on a game together.
- 📫 How to reach me no email just here on github :)
- 😄 Pronouns: im a microwave, my pronouns are brrrrrrr/beeep beeepbeeep (he/him)
- ⚡ Fun fact: idk get to know me outside of here and im a pretty cool guy :]

<!---
chickenrice1/chickenrice1 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Guessing Game</title>
</head>
<body>
    <h1>Number Guessing Game</h1>
    <p>I've picked a number between 1 and 100. Can you guess it?</p>
    
    <input type="number" id="guessInput" placeholder="Enter your guess">
    <button onclick="checkGuess()">Guess</button>
    
    <p id="result"></p>
    
    <script>
        const numberToGuess = Math.floor(Math.random() * 100) + 1;
        let attempts = 0;

        function checkGuess() {
            const guess = Number(document.getElementById("guessInput").value);
            attempts++;

            let resultMessage = "";

            if (guess < numberToGuess) {
                resultMessage = "Too low! Try again.";
            } else if (guess > numberToGuess) {
                resultMessage = "Too high! Try again.";
            } else {
                resultMessage = `Congratulations! You've guessed the number in ${attempts} attempts.`;
            }

            document.getElementById("result").innerText = resultMessage;
        }
    </script>
</body>
</html>
