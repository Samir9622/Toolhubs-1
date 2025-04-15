<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToolHubs 1 - All-in-One Tools</title>
    <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@400;700&display=swap" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/npm/qrcode-generator/qrcode.min.js"></script>
    <style>
        /* Base Styles */
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f0f2f5;
            color: #333;
        }

        header {
            background: linear-gradient(145deg, #f9d423, #ff4e50);
            padding: 60px 20px;
            text-align: center;
            color: #fff;
            border-radius: 0 0 20px 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
        }

        /* Tool Grid & Cards */
        .tools-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 20px;
            padding: 40px 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .tool-card {
            background: #ffffffcc;
            border: 2px solid #ddd;
            border-radius: 16px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .tool-card:hover {
            transform: translateY(-6px) scale(1.03);
            background: #ffe;
            box-shadow: 0 6px 18px rgba(0, 0, 0, 0.15);
        }

        /* Tool Content Styles */
        .tool-content {
            max-width: 800px;
            margin: 30px auto;
            padding: 20px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            display: none;
        }

        .active-tool {
            display: block;
        }

        /* Common Form Elements */
        .tool-input, select {
            width: 100%;
            padding: 12px;
            margin: 10px 0;
            border: 1px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
        }

        .tool-button {
            background: #ff4e50;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            transition: background 0.3s;
            margin: 5px;
        }

        .tool-button:hover {
            background: #ff3638;
        }

        .result-output {
            margin-top: 20px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 8px;
            word-break: break-all;
        }

        /* Ad Containers */
        .ad-container {
            text-align: center;
            margin: 20px auto;
            padding: 10px;
        }
    </style>
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-877348079981"
            crossorigin="anonymous"></script>
</head>
<body>
    <header>
        <h1>Welcome to ToolHubs-1!</h1>
        <p>Your ultimate playground of <strong>smart, stylish & superfast tools</strong> — All in One Place!</p>
    </header>

<!-- Top Ad Unit -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158" crossorigin="anonymous"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-8773480799818158"
     data-ad-slot="3941204223"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>(adsbygoogle = window.adsbygoogle || []).push({});</script>


    <div class="switch-section">
        <label for="toolSwitch">Select a Tool:</label>
        <select id="toolSwitch" onchange="showTool(this.value)">
            <option value="">-- Choose Tool --</option>
            <option value="password-generator">Password Generator</option>
            <option value="case-converter">Text Case Converter</option>
            <option value="word-counter">Word Counter</option>
            <option value="color-picker">Color Picker</option>
            <option value="image-compressor">Image Compressor</option>
            <option value="calculator">Calculator</option>
            <option value="stopwatch">Stopwatch</option>
            <option value="qr-generator">QR Generator</option>
            <option value="unit-converter">Unit Converter</option>
        </select>
    </div>

    <!-- Tools Content -->
    <div id="password-generator" class="tool-content">
        <h2>🔒 Password Generator</h2>
        <input type="number" id="pass-length" value="12" min="8" max="50" class="tool-input">
        <div>
            <label><input type="checkbox" id="uppercase" checked> Uppercase</label>
            <label><input type="checkbox" id="numbers" checked> Numbers</label>
            <label><input type="checkbox" id="symbols" checked> Symbols</label>
        </div>
        <button onclick="generatePassword()" class="tool-button">Generate</button>
        <div id="password-result" class="result-output"></div>
    </div>

    <div id="case-converter" class="tool-content">
        <h2>🔄 Text Case Converter</h2>
        <textarea id="case-input" class="tool-input" rows="5" placeholder="Enter text..."></textarea>
        <button onclick="convertCase('upper')" class="tool-button">UPPERCASE</button>
        <button onclick="convertCase('lower')" class="tool-button">lowercase</button>
        <button onclick="convertCase('proper')" class="tool-button">Proper Case</button>
        <div id="case-output" class="result-output"></div>
    </div>

    <div id="word-counter" class="tool-content">
        <h2>📝 Word Counter</h2>
        <textarea id="word-input" class="tool-input" rows="5" placeholder="Start typing..."></textarea>
        <div class="result-output">
            Words: <span id="word-count">0</span> | 
            Characters: <span id="char-count">0</span>
        </div>
    </div>

    <div id="color-picker" class="tool-content">
        <h2>🎨 Color Picker</h2>
        <input type="color" id="color-input" value="#ff4e50" class="tool-input">
        <div class="result-output" id="color-hex">Hex: #ff4e50</div>
    </div>

    <div id="image-compressor" class="tool-content">
        <h2>🖼️ Image Compressor</h2>
        <input type="file" id="image-input" accept="image/*" class="tool-input">
        <canvas id="image-canvas" hidden></canvas>
        <div id="compressed-image" class="result-output"></div>
    </div>

    <div id="calculator" class="tool-content">
        <h2>🧮 Calculator</h2>
        <input type="text" id="calc-display" class="tool-input" readonly>
        <div class="calculator-buttons">
            <!-- Calculator buttons would be added here -->
        </div>
    </div>

    <!-- Bottom Ad Unit -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158" crossorigin="anonymous"></script>
<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-8773480799818158"
     data-ad-slot="9505617632"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>
<script>(adsbygoogle = window.adsbygoogle || []).push

    <script>
        // Tool Switching Logic
        function showTool(toolId) {
            document.querySelectorAll('.tool-content').forEach(tool => {
                tool.style.display = 'none';
            });
            if (toolId) {
                document.getElementById(toolId).style.display = 'block';
                window.scrollTo(0, document.getElementById(toolId).offsetTop - 100);
            }
        }

        // Password Generator
        function generatePassword() {
            const length = document.getElementById('pass-length').value;
            const uppercase = document.getElementById('uppercase').checked;
            const numbers = document.getElementById('numbers').checked;
            const symbols = document.getElementById('symbols').checked;
            
            let chars = 'abcdefghijklmnopqrstuvwxyz';
            chars += uppercase ? 'ABCDEFGHIJKLMNOPQRSTUVWXYZ' : '';
            chars += numbers ? '0123456789' : '';
            chars += symbols ? '!@#$%^&*()_+' : '';
            
            let password = '';
            for (let i = 0; i < length; i++) {
                password += chars.charAt(Math.floor(Math.random() * chars.length));
            }
            document.getElementById('password-result').textContent = password;
        }

        // Case Converter
        function convertCase(type) {
            const text = document.getElementById('case-input').value;
            let result = '';
            switch(type) {
                case 'upper': result = text.toUpperCase(); break;
                case 'lower': result = text.toLowerCase(); break;
                case 'proper': 
                    result = text.toLowerCase().replace(/\b\w/g, c => c.toUpperCase());
                    break;
            }
            document.getElementById('case-output').textContent = result;
        }

        // Word Counter
        document.getElementById('word-input').addEventListener('input', function() {
            const text = this.value;
            document.getElementById('word-count').textContent = 
                text.trim().split(/\s+/).filter(word => word.length > 0).length;
            document.getElementById('char-count').textContent = text.length;
        });

        // Color Picker
        document.getElementById('color-input').addEventListener('input', function() {
            document.getElementById('color-hex').textContent = `Hex: ${this.value.toUpperCase()}`;
        });

        // Image Compressor
        document.getElementById('image-input').addEventListener('change', function(e) {
            const file = e.target.files[0];
            const reader = new FileReader();
            reader.onload = function(event) {
                const img = new Image();
                img.src = event.target.result;
                img.onload = function() {
                    const canvas = document.getElementById('image-canvas');
                    const ctx = canvas.getContext('2d');
                    canvas.width = img.width;
                    canvas.height = img.height;
                    ctx.drawImage(img, 0, 0);
                    const compressed = canvas.toDataURL('image/jpeg', 0.7);
                    document.getElementById('compressed-image').innerHTML = `
                        <a href="${compressed}" download="compressed.jpg">
                            Download Compressed Image
                        </a>`;
                };
            };
            reader.readAsDataURL(file);
        });

        // Initialize Ads
        (adsbygoogle = window.adsbygoogle || []).push({});
    </script>
</body>
</html>
