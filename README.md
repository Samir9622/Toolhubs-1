<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ToolHubs-1</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background: #f5f5f5; text-align: center; }
    .header { background: linear-gradient(to right, #ffa726, #fb8c00); padding: 20px; color: white; border-radius: 0 0 10px 10px; }
    .tools-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px; padding: 20px; }
    .tool-card { background: white; border-radius: 12px; padding: 20px; cursor: pointer; box-shadow: 0 2px 6px rgba(0,0,0,0.1); }
    .tool-section { display: none; padding: 20px; background: white; margin: 10px auto; border-radius: 12px; max-width: 800px; box-shadow: 0 2px 6px rgba(0,0,0,0.1); }
    .tool-section.active { display: block; }
    button { margin: 4px; padding: 10px 15px; font-size: 16px; }
  </style>
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158" crossorigin="anonymous"></script>
</head>
<body>
  <div class="header">
    <h2>Welcome to ToolHubs-1!</h2>
    <p>Your ultimate playground of smart, stylish & superfast tools — All in One Place!</p>
  </div>
  

  <ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-9354903383" data-ad-slot="2486822494" data-ad-format="auto" data-full-width-responsive="true"></ins>
  <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>

  <div class="tools-grid">
    <div class="tool-card" onclick="switchTool('compressor')">Image Compressor</div>
    <div class="tool-card" onclick="switchTool('calculator')">Online Calculator</div>
  </div>

  <div id="compressor" class="tool-section active">
    <h3>Image Compressor</h3>
    <input type="file" id="imgInput" accept="image/*" /><br><br>
    <canvas id="canvas" style="max-width:100%; display:none;"></canvas><br><br>
    <button onclick="compressImage()">Compress</button>
    <a id="downloadLink" style="display:none;" download="compressed.jpg">Download Image</a>
  </div>

  <div id="calculator" class="tool-section">
    <h3>Online Calculator</h3>
    <input type="text" id="calcDisplay" readonly style="width: 200px; font-size: 1.2em;" /><br><br>
    <div>
      <button onclick="appendCalc('1')">1</button>
      <button onclick="appendCalc('2')">2</button>
      <button onclick="appendCalc('3')">3</button>
      <button onclick="appendCalc('+')">+</button><br>
      <button onclick="appendCalc('4')">4</button>
      <button onclick="appendCalc('5')">5</button>
      <button onclick="appendCalc('6')">6</button>
      <button onclick="appendCalc('-')">-</button><br>
      <button onclick="appendCalc('7')">7</button>
      <button onclick="appendCalc('8')">8</button>
      <button onclick="appendCalc('9')">9</button>
      <button onclick="appendCalc('*')">*</button><br>
      <button onclick="appendCalc('0')">0</button>
      <button onclick="appendCalc('.')">.</button>
      <button onclick="calculateResult()">=</button>
      <button onclick="appendCalc('/')">/</button><br>
      <button onclick="clearCalc()">C</button>
    </div>
  </div>

  <ins class="adsbygoogle" style="display:block" data-ad-client="ca-pub-9055111364" data-ad-slot="2486822494" data-ad-format="auto" data-full-width-responsive="true"></ins>
  <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>

  <script>
    function switchTool(id) {
      document.querySelectorAll('.tool-section').forEach(sec => sec.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }

    function compressImage() {
      const input = document.getElementById("imgInput");
      if (!input.files.length) return alert("Upload an image first!");
      const file = input.files[0];
      const reader = new FileReader();
      reader.onload = function (e) {
        const img = new Image();
        img.src = e.target.result;
        img.onload = function () {
          const canvas = document.getElementById("canvas");
          const ctx = canvas.getContext("2d");
          const scale = 0.5;
          canvas.width = img.width * scale;
          canvas.height = img.height * scale;
          ctx.drawImage(img, 0, 0, canvas.width, canvas.height);
          canvas.style.display = "block";
          canvas.toBlob(function (blob) {
            const link = document.getElementById("downloadLink");
            link.href = URL.createObjectURL(blob);
            link.style.display = "inline-block";
          }, "image/jpeg", 0.7);
        };
      };
      reader.readAsDataURL(file);
    }

    function appendCalc(val) {
      document.getElementById("calcDisplay").value += val;
    }

    function clearCalc() {
      document.getElementById("calcDisplay").value = "";
    }

    function calculateResult() {
      try {
        const result = eval(document.getElementById("calcDisplay").value);
        document.getElementById("calcDisplay").value = result;
      } catch {
        alert("Invalid Expression");
      }
    }
  </script>
</body>
</html>
