# Yuu_
UKK RPL 2024/2025

# UKK PADA HARI JUM'AT PADA TANGGAL 21 FEB 2025

# codingan kalkulator
<!DOCTYPE html>
<html>
  <head>
    <title>Kalkulator</title>
    <style type="text/css">
      body {
        font-family: Sans-Serif;
        text-align: center;
      }
      .calculator {
        width: 250px;
        padding: 15px;
        background-color: pink;
        border: 2px solid black;
        margin: 60px auto;
      }
      input {
        width: 90%;
        height: 40px;
        font-size: 20px;
        margin-bottom: 10px;
        border-width: 2px;
      }
      button {
        width: 50px;
        height: 50px;
        font-size: 20px;
        margin-bottom: 5px;
        margin-right: 5px;
        background-color: skyblue;
        color: hotpink;
        border: none;
        cursor: pointer;
      }
      button:hover {
        background-color: white;
      }
    </style>
  </head>
  <body>
    <div class="calculator">
      <input type="text" id="display" readonly>
      <br>
      <button onclick="angka('9')">9</button>
      <button onclick="angka('8')">8</button>
      <button onclick="angka('7')">7</button>
      <button onclick="angka('+')">+</button>
      <br>
      <button onclick="angka('6')">6</button>
      <button onclick="angka('5')">5</button>
      <button onclick="angka('4')">4</button>
      <button onclick="angka('-')">-</button>
      <br>
      <button onclick="angka('3')">3</button>
      <button onclick="angka('2')">2</button>
      <button onclick="angka('1')">1</button>
      <button onclick="angka('*')">*</button>
      <br>
      <button onclick="angka('0')">0</button>
      <button onclick="angka('.')">.</button>
      <button onclick="hapus()">C</button>
      <button onclick="angka('/')">÷</button>
      <br>
      <button onclick="hasil()" style="width: 90%">=</button>
    </div>
    <script type="text/javascript">
      function angka(value) {
        let display = document.getElementById('display');
        
        // Cegah duplikasi titik dalam angka
        if (value === '.' && display.value.includes('.')) {
          return;
        }
        
        display.value += value;
      }

      function hapus() {
        document.getElementById('display').value = '';
      }

      function hasil() {
        let display = document.getElementById('display');
        try {
          display.value = eval(display.value);
        } catch {
          display.value = 'Error';
        }
      }
    </script>
  </body>
</html>
