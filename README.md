<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Simple Calculator</title>
  <style>
    body {
      background: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
    }

    .calculator {
      background: #ffffff;
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    .display {
      width: 100%;
      height: 60px;
      background: #222;
      color: #fff;
      font-size: 2rem;
      border-radius: 8px;
      text-align: right;
      padding: 10px;
      box-sizing: border-box;
      margin-bottom: 15px;
    }

    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 60px);
      gap: 10px;
    }

    button {
      height: 60px;
      font-size: 1.5rem;
      border: none;
      border-radius: 8px;
      background: #e0e0e0;
      cursor: pointer;
      transition: 0.2s;
    }

    button:active {
      background: #c0c0c0;
    }

    .operator {
      background: #ffa500;
      color: white;
    }

    .equal {
      background: #00cc99;
      color: white;
      grid-column: span 2;
    }

    .clear {
      background: #ff4d4d;
      color: white;
      grid-column: span 2;
    }
  </style>
</head>
<body>

  <div class="calculator">
    <div class="display" id="display">0</div>
    <div class="buttons">
      <button class="clear" onclick="clearDisplay()">C</button>
      <button class="operator" onclick="appendValue('/')">÷</button>
      <button class="operator" onclick="appendValue('*')">×</button>

      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>
      <button class="operator" onclick="appendValue('-')">−</button>

      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>
      <button class="operator" onclick="appendValue('+')">+</button>

      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>
      <button onclick="appendValue('.')">.</button>

      <button onclick="appendValue('0')">0</button>
      <button class="equal" onclick="calculateResult()">=</button>
    </div>
  </div>

  <script>
    let display = document.getElementById('display');

    function appendValue(value) {
      if (display.innerText === '0') {
        display.innerText = value;
      } else {
        display.innerText += value;
      }
    }

    function clearDisplay() {
      display.innerText = '0';
    }

    function calculateResult() {
      try {
        display.innerText = eval(display.innerText);
      } catch {
        display.innerText = 'Error';
      }
    }
  </script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Simple Calculator</title>
  <style>
    body {
      background: #f0f0f0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: 'Segoe UI', sans-serif;
    }

    .calculator {
      background: #ffffff;
      padding: 20px;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    }

    .display {
      width: 100%;
      height: 60px;
      background: #222;
      color: #fff;
      font-size: 2rem;
      border-radius: 8px;
      text-align: right;
      padding: 10px;
      box-sizing: border-box;
      margin-bottom: 15px;
    }

    .buttons {
      display: grid;
      grid-template-columns: repeat(4, 60px);
      gap: 10px;
    }

    button {
      height: 60px;
      font-size: 1.5rem;
      border: none;
      border-radius: 8px;
      background: #e0e0e0;
      cursor: pointer;
      transition: 0.2s;
    }

    button:active {
      background: #c0c0c0;
    }

    .operator {
      background: #ffa500;
      color: white;
    }

    .equal {
      background: #00cc99;
      color: white;
      grid-column: span 2;
    }

    .clear {
      background: #ff4d4d;
      color: white;
      grid-column: span 2;
    }
  </style>
</head>
<body>

  <div class="calculator">
    <div class="display" id="display">0</div>
    <div class="buttons">
      <button class="clear" onclick="clearDisplay()">C</button>
      <button class="operator" onclick="appendValue('/')">÷</button>
      <button class="operator" onclick="appendValue('*')">×</button>

      <button onclick="appendValue('7')">7</button>
      <button onclick="appendValue('8')">8</button>
      <button onclick="appendValue('9')">9</button>
      <button class="operator" onclick="appendValue('-')">−</button>

      <button onclick="appendValue('4')">4</button>
      <button onclick="appendValue('5')">5</button>
      <button onclick="appendValue('6')">6</button>
      <button class="operator" onclick="appendValue('+')">+</button>

      <button onclick="appendValue('1')">1</button>
      <button onclick="appendValue('2')">2</button>
      <button onclick="appendValue('3')">3</button>
      <button onclick="appendValue('.')">.</button>

      <button onclick="appendValue('0')">0</button>
      <button class="equal" onclick="calculateResult()">=</button>
    </div>
  </div>

  <script>
    let display = document.getElementById('display');

    function appendValue(value) {
      if (display.innerText === '0') {
        display.innerText = value;
      } else {
        display.innerText += value;
      }
    }

    function clearDisplay() {
      display.innerText = '0';
    }

    function calculateResult() {
      try {
        display.innerText = eval(display.innerText);
      } catch {
        display.innerText = 'Error';
      }
    }
  </script>

</body>
</html>
