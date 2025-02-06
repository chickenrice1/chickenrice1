# Simple Timer
```markdown
Here’s an example of a simple timer using HTML and JavaScript:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Timer</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
        #timer { font-size: 3em; margin-bottom: 20px; }
        button { margin: 5px; padding: 10px 20px; font-size: 1em; }
    </style>
</head>
<body>
    <div id="timer">00:00:00</div>
    <button onclick="startTimer()">Start</button>
    <button onclick="stopTimer()">Stop</button>
    <button onclick="resetTimer()">Reset</button>
    <script>
        let timer, h = 0, m = 0, s = 0, running = false;
        const updateDisplay = () => document.getElementById('timer').textContent = 
            `${h < 10 ? "0" : ""}${h}:${m < 10 ? "0" : ""}${m}:${s < 10 ? "0" : ""}${s}`;

        const updateTimer = () => { if (++s === 60) { s = 0; if (++m === 60) { m = 0; h++; } } updateDisplay(); }
        const startTimer = () => { if (!running) running = true, timer = setInterval(updateTimer, 1000); }
        const stopTimer = () => { running = false; clearInterval(timer); }
        const resetTimer = () => { running = false; clearInterval(timer); h = m = s = 0; updateDisplay(); }

        window.onload = startTimer;
    </script>
</body>
</html> 
