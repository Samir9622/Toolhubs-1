<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>ToolHub 1</title>
    <meta name="description" content="All-in-one free online tools - ToolHub 1" />
    <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* (Keep existing CSS styles the same) */
    </style>
    <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158" crossorigin="anonymous"></script>
</head>
<body>
    <header>
        <h1>Welcome to ToolHubs-1!</h1>
        <p>Your ultimate playground of <strong>smart, stylish & superfast tools</strong> — All in One Place!</p>
    </header>

    <div class="switch-section">
        <label for="toolSwitch">Select a Tool:</label>
        <select id="toolSwitch" onchange="switchTool()">
            <option value="">-- Choose Tool --</option>
            <option value="image-compressor.html">Image Compressor</option>
            <option value="online-calculator.html">Online Calculator</option>
            <option value="stopwatch-timer.html">Stopwatch & Timer</option>
            <option value="qr-code-generator.html">QR Code Generator</option>
            <option value="text-case-converter.html">Text Case Converter</option>
            <option value="password-generator.html">Password Generator</option>
            <option value="unit-converter.html">Unit Converter</option>
            <option value="color-picker.html">Color Picker</option>
            <option value="word-counter.html">Word Counter</option>
        </select>
    </div>

    <div class="ad-container">
        <ins class="adsbygoogle"
            style="display:block"
            data-ad-client="ca-pub-8773480799818158"
            data-ad-slot="9354903383"
            data-ad-format="auto"
            data-full-width-responsive="true"></ins>
        <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
    </div>

    <section class="tools-grid">
        <!-- Keep existing tool cards the same -->
    </section>

    <div class="ad-container">
        <ins class="adsbygoogle"
            style="display:block"
            data-ad-client="ca-pub-8773480799818158"
            data-ad-slot="9055111364"of 
            data-ad-format="auto"
            data-full-width-responsive="true"></ins>
        <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
    </div>

    <div class="footer">
        <p><strong>Click any tool above and start exploring!</strong><br>
        Bright. Bold. Beautiful. That’s <span style="color: #ff4e50;">ToolHubs-1</span>.</p>
    </div>

    <script>
        // Fixed switching function
        function switchTool() {
            const selector = document.getElementById("toolSwitch");
            const selectedValue = selector.value;
            if (selectedValue) {
                window.location.href = selectedValue;
            }
        }

        // Add click handlers to tool cards
        document.addEventListener('DOMContentLoaded', () => {
            const toolCards = document.querySelectorAll('.tool-card');
            const tools = [
                'image-compressor.html',
                'online-calculator.html',
                'stopwatch-timer.html',
                'qr-code-generator.html',
                'text-case-converter.html',
                'password-generator.html',
                'unit-converter.html',
                'color-picker.html',
                'word-counter.html'
            ];

            toolCards.forEach((card, index) => {
                card.style.cursor = 'pointer';
                card.addEventListener('click', () => {
                    window.location.href = tools[index];
                });
            });
        });

        // Initialize ads
        (adsbygoogle = window.adsbygoogle || []).push({});
    </script>
</body>
</html>
