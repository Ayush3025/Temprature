# Temprature

# HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <div class="input-container">
            <label for="celsius">Celsius:</label>
            <input type="number" id="celsius" placeholder="Enter temperature in Celsius">
        </div>
        <div class="result">
            <p>Fahrenheit: <span id="fahrenheit">-</span></p>
        </div>
        <button id="convertBtn">Convert</button>
    </div>
    <script src="script.js"></script>
</body>
</html>

# CSS

body {
    font-family: Arial, sans-serif;
    background-color: #f2f2f2;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
}

.container {
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    text-align: center;
    padding: 20px;
}

h1 {
    font-size: 24px;
}

.input-container {
    margin: 20px 0;
}

label {
    font-weight: bold;
}

input {
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 5px;
    width: 100%;
}

.result {
    margin-top: 10px;
    font-weight: bold;
}

button {
    background-color: #007BFF;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

# Javascript


document.addEventListener("DOMContentLoaded", function () {
    const celsiusInput = document.getElementById("celsius");
    const fahrenheitResult = document.getElementById("fahrenheit");
    const convertBtn = document.getElementById("convertBtn");

    convertBtn.addEventListener("click", function () {
        const celsiusValue = parseFloat(celsiusInput.value);
        if (!isNaN(celsiusValue)) {
            const fahrenheitValue = (celsiusValue * 9/5) + 32;
            fahrenheitResult.textContent = fahrenheitValue.toFixed(2);
        } else {
            alert("Please enter a valid number for Celsius.");
        }
    });
});

