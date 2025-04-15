<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ToolHub - All-in-One Online Tools</title>
    <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Base Styles */
        body {
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: #f0f2f5;
            color: #333;
            line-height: 1.6;
        }

        header {
            background: linear-gradient(145deg, #f9d423, #ff4e50);
            padding: 60px 20px;
            text-align: center;
            color: #fff;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.2);
            margin-bottom: 30px;
        }

        /* Tool Selector */
        .tool-selector {
            max-width: 300px;
            margin: 20px auto;
            padding: 15px;
        }

        #toolSwitch {
            width: 100%;
            padding: 12px;
            border-radius: 8px;
            border: 2px solid #ff4e50;
            font-size: 16px;
            background: white;
        }

        /* Tool Sections */
        .tool-section {
            max-width: 800px;
            margin: 30px auto;
            padding: 25px;
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            display: none;
            animation: fadeIn 0.3s ease;
        }

        .tool-section.active-tool {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Ad Containers */
        .ad-container {
            margin: 20px auto;
            text-align: center;
            padding: 10px;
        }

        /* Tool Elements */
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
            margin: 10px 5px;
        }

        .result-output {
            margin-top: 20px;
            padding: 15px;
            background: #f8f9fa;
            border-radius: 8px;
            word-break: break-word;
        }
    </style>
    <!-- AdSense Script -->
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158" crossorigin="anonymous"></script>
</head>
<body>
    <header>
        <h1>ToolHub Pro</h1>
        <p>Your Ultimate Online Toolbox</p>
    </header>

    <!-- Top Ad -->
    <div class="ad-container">
        <ins class="adsbygoogle"
             style="display:block"
             data-ad-client="ca-pub-8773480799818158"
             data-ad-slot="3941204223"
             data-ad-format="auto"
             data-full-width-responsive="true"></ins>
    </div>

    <div class="tool-selector">
        <select id="toolSwitch" onchange="showTool(this.value)">
            <option value="">Select a Tool</option>
            <option value="password-generator">Password Generator</option>
            <option value="case-converter">Text Case Converter</option>
            <option value="word-counter">Word Counter</option>
            <option value="color-picker">Color Picker</option>
            <option value="image-compressor">Image Compressor</option>
        </select>
    </div>

    <!-- Tools Sections -->
    <div id="password-generator" class="tool-section">
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

    <div id="case-converter" class="tool-section">
        <h2>🔄 Text Case Converter</h2>
        <textarea id="case-input" class="tool-input" rows="5" placeholder="Enter text..."></textarea>
        <button onclick="convertCase('upper')" class="tool-button">UPPERCASE</button>
        <button onclick="convertCase('lower')" class="tool-button">lowercase</button>
        <button onclick="convertCase('proper')" class="tool-button">Proper Case</button>
        <div id="case-output" class="result-output"></div>
    </div>

    <div id="word-counter" class="tool-section">
        <h2>📝 Word Counter</h2>
        <textarea id="word-input" class="tool-input" rows="5" placeholder="Start typing..."></textarea>
        <div class="result-output">
            Words: <span id="word-count">0</span> | 
            Characters: <span id="char-count">0</span>
        </div>
    </div>

    <div id="color-picker" class="tool-section">
        <h2>🎨 Color Picker</h2>
        <input type="color" id="color-input" value="#ff4e50" class="tool-input">
        <div class="result-output" id="color-hex">Hex: #ff4e50</div>
    </div>

    <div id="image-compressor" class="tool-section">
        <h2>🖼️ Image Compressor</h2>
        <input type="file" id="image-input" accept="image/*" class="tool-input">
        <canvas id="image-canvas" style="display:none;"></canvas>
        <div id="compressed-image" class="result-output"></div>
    </div>

    <!-- Bottom Ad -->
    <div class="ad-container">
        <ins class="adsbygoogle"
             style="display:block"
             data-ad-client="ca-pub-8773480799818158"
             data-ad-slot="9505617632"
             data-ad-format="auto"
             data-full-width-responsive="true"></ins>
    </div>

    <script>
        // Tool Visibility Control
        function showTool(toolId) {
            document.querySelectorAll('.tool-section').forEach(tool => {
                tool.classList.remove('active-tool');
            });
            if (toolId) {
                document.getElementById(toolId).classList.add('active-tool');
                window.scrollTo({
                    top: document.getElementById(toolId).offsetTop - 100,
                    behavior: 'smooth'
                });
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
                password += chars[Math.floor(Math.random() * chars.length)];
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
            const text = this.value.trim();
            document.getElementById('word-count').textContent = 
                text ? text.split(/\s+/).length : 0;
            document.getElementById('char-count').textContent = text.length;
        });

        // Color Picker
        document.getElementById('color-input').addEventListener('input', function() {
            document.getElementById('color-hex').textContent = `Hex: ${this.value.toUpperCase()}`;
        });

        // Image Compressor
        document.getElementById('image-input').addEventListener('change', function(e) {
            const file = e.target.files[0];
            if (!file) return;

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
                        <a href="${compressed}" download="compressed.jpg" class="tool-button">
                            Download Compressed Image
                        </a>`;
                };
            };
            reader.readAsDataURL(file);
        });

        // Initialize Ads
        document.addEventListener('DOMContentLoaded', () => {
            // Show default tool
            showTool('password-generator');
            
            // Load ads
            (adsbygoogle = window.adsbygoogle || []).push({});
            (adsbygoogle = window.adsbygoogle || []).push({});
        });
    </script>
</body>
</html>
