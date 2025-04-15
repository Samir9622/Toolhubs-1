<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ToolHubs1</title>
  <style>
    body { font-family: sans-serif; background: #f8fafa; margin: 0; padding: 0; }
    .container { padding: 20px; max-width: 1200px; margin: 0 auto; }
    h1 { color: #2d60d1; text-align: center; }
    .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 16px; margin-top: 20px; }
    .card { background: #fff; padding: 16px; border-radius: 8px; box-shadow: 0 2px 8px rgba(0,0,0,0.1); cursor: pointer; text-align: center; }
    .tool-content { display: none; padding: 20px; background: white; border-radius: 10px; margin-top: 20px; }
    .tool-active { display: block; }
    footer { text-align: center; margin-top: 40px; color: #666; }
    input, button, textarea { margin: 10px 0; padding: 8px; width: 100%; max-width: 300px; }
  </style>
</head>
<body>
  <div class="container">
    <h1>ToolHubs1</h1>
    <p style="text-align: center">All-in-One Utility Tools at Your Fingertips</p>

    <div class="grid">
      <div class="card" onclick="showTool('image-compressor')">Image Compressor</div>
      <div class="card" onclick="showTool('calculator')">Online Calculator</div>
      <div class="card" onclick="showTool('stopwatch-timer')">Stopwatch & Timer</div>
      <div class="card" onclick="showTool('qr-generator')">QR Code Generator</div>
      <div class="card" onclick="showTool('text-case')">Text Case Converter</div>
      <div class="card" onclick="showTool('password-gen')">Password Generator</div>
      <div class="card" onclick="showTool('unit-converter')">Unit Converter</div>
      <div class="card" onclick="showTool('color-picker')">Color Picker</div>
      <div class="card" onclick="showTool('word-counter')">Word Counter</div>
    </div>

    <div id="image-compressor" class="tool-content">
      <h2>Image Compressor</h2>
      <input type="file" id="image-input" accept="image/*">
      <canvas id="preview-canvas"></canvas>
      <button onclick="compressImage()">Compress</button>
    </div>

    <div id="calculator" class="tool-content">
      <h2>Calculator</h2>
      <input type="text" id="calc-display" readonly>
      <div id="calc-buttons"></div>
    </div>

    <div id="stopwatch-timer" class="tool-content">
      <h2>Stopwatch & Timer</h2>
      <button onclick="startStopwatch()">Start</button>
      <button onclick="stopStopwatch()">Stop</button>
      <button onclick="resetStopwatch()">Reset</button>
      <p id="stopwatch-display">00:00:00</p>
    </div>

    <div id="qr-generator" class="tool-content">
      <h2>QR Code Generator</h2>
      <input type="text" id="qr-input" placeholder="Enter text or URL">
      <div id="qr-code"></div>
    </div>

    <div id="text-case" class="tool-content">
      <h2>Text Case Converter</h2>
      <textarea id="text-case-input"></textarea>
      <button onclick="convertCase('upper')">UPPERCASE</button>
      <button onclick="convertCase('lower')">lowercase</button>
      <button onclick="convertCase('capitalize')">Capitalize</button>
      <textarea id="text-case-output"></textarea>
    </div>

    <div id="password-gen" class="tool-content">
      <h2>Password Generator</h2>
      <input type="number" id="pass-length" placeholder="Length (e.g. 12)">
      <button onclick="generatePassword()">Generate</button>
      <input type="text" id="password-output" readonly>
    </div>

    <div id="unit-converter" class="tool-content">
      <h2>Unit Converter</h2>
      <input type="number" id="unit-input" placeholder="Enter value">
      <select id="unit-from">
        <option value="km">Kilometer</option>
        <option value="m">Meter</option>
      </select>
      <select id="unit-to">
        <option value="m">Meter</option>
        <option value="km">Kilometer</option>
      </select>
      <button onclick="convertUnit()">Convert</button>
      <input type="text" id="unit-result" readonly>
    </div>

    <div id="color-picker" class="tool-content">
      <h2>Color Picker</h2>
      <input type="color" id="color-input">
      <input type="text" id="color-value" readonly>
    </div>

    <div id="word-counter" class="tool-content">
      <h2>Word Counter</h2>
      <textarea id="word-input" placeholder="Type or paste text..."></textarea>
      <p id="word-count">Words: 0</p>
    </div>

    <footer>© 2025 ToolHub by Samir Dey. All rights reserved.</footer>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
  <script>
    function showTool(toolId) {
      document.querySelectorAll('.tool-content').forEach(el => el.classList.remove('tool-active'));
      document.getElementById(toolId).classList.add('tool-active');
    }

    function compressImage() {
      const input = document.getElementById('image-input');
      const canvas = document.getElementById('preview-canvas');
      const file = input.files[0];
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          const img = new Image();
          img.onload = function() {
            canvas.width = img.width / 2;
            canvas.height = img.height / 2;
            const ctx = canvas.getContext('2d');
            ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
          }
          img.src = e.target.result;
        }
        reader.readAsDataURL(file);
      }
    }

    const calcDisplay = document.getElementById("calc-display");
    const calcButtons = ["7","8","9","/","4","5","6","*","1","2","3","-","0",".","=","+"];
    const buttonContainer = document.getElementById("calc-buttons");
    let current = "";
    calcButtons.forEach(btn => {
      const b = document.createElement("button");
      b.textContent = btn;
      b.onclick = () => {
        if (btn === "=") {
          current = eval(current);
        } else {
          current += btn;
        }
        calcDisplay.value = current;
      };
      buttonContainer.appendChild(b);
    });

    let stopwatchInterval, stopwatchTime = 0;
    function updateStopwatch() {
      let hrs = Math.floor(stopwatchTime / 3600), min = Math.floor((stopwatchTime % 3600) / 60), sec = stopwatchTime % 60;
      document.getElementById("stopwatch-display").textContent = `${hrs.toString().padStart(2,'0')}:${min.toString().padStart(2,'0')}:${sec.toString().padStart(2,'0')}`;
    }
    function startStopwatch() {
      stopwatchInterval = setInterval(() => { stopwatchTime++; updateStopwatch(); }, 1000);
    }
    function stopStopwatch() { clearInterval(stopwatchInterval); }
    function resetStopwatch() { stopwatchTime = 0; updateStopwatch(); }

    document.getElementById('qr-input').addEventListener('input', () => {
      const qrCode = document.getElementById("qr-code");
      qrCode.innerHTML = "";
      new QRCode(qrCode, document.getElementById("qr-input").value);
    });

    function convertCase(type) {
      const input = document.getElementById("text-case-input").value;
      let output = "";
      if (type === "upper") output = input.toUpperCase();
      else if (type === "lower") output = input.toLowerCase();
      else output = input.replace(/\b\w/g, c => c.toUpperCase());
      document.getElementById("text-case-output").value = output;
    }

    function generatePassword() {
      const length = document.getElementById("pass-length").value;
      const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()";
      let pass = "";
      for (let i = 0; i < length; i++) pass += chars.charAt(Math.floor(Math.random() * chars.length));
      document.getElementById("password-output").value = pass;
    }

    function convertUnit() {
      const value = parseFloat(document.getElementById("unit-input").value);
      const from = document.getElementById("unit-from").value;
      const to = document.getElementById("unit-to").value;
      let result = value;
      if (from === "km" && to === "m") result = value * 1000;
      else if (from === "m" && to === "km") result = value / 1000;
      document.getElementById("unit-result").value = result;
    }

    document.getElementById("color-input").addEventListener("input", (e) => {
      document.getElementById("color-value").value = e.target.value;
    });

    document.getElementById("word-input").addEventListener("input", () => {
      const text = document.getElementById("word-input").value.trim();
      const count = text ? text.split(/\s+/).length : 0;
      document.getElementById("word-count").textContent = `Words: ${count}`;
    });

    showTool('image-compressor');
  </script>
</body>
</html>
