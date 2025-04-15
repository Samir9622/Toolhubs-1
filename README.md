<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ToolHub 1</title>
  <meta name="description" content="All-in-one free online tools - ToolHub 1" />
  <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@400;700&display=swap" rel="stylesheet">
  <style>
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
    header h1 {
      font-size: 3em;
      margin: 0;
      text-shadow: 2px 2px 4px #00000050;
    }
    header p {
      font-size: 1.4em;
      max-width: 800px;
      margin: 20px auto 0;
      line-height: 1.6;
    }
    .switch-section {
      text-align: center;
      margin: 20px 0;
    }
    select {
      font-size: 1em;
      padding: 10px;
      border-radius: 8px;
      border: 1px solid #ccc;
    }
    .tools-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 20px;
      padding: 40px 20px;
    }
    .tool-card {
      background: #ffffffcc;
      border: 2px solid #ddd;
      border-radius: 16px;
      padding: 20px;
      width: 260px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      transition: all 0.3s ease;
    }
    .tool-card:hover {
      transform: translateY(-6px) scale(1.03);
      background: #ffe;
      box-shadow: 0 6px 18px rgba(0, 0, 0, 0.15);
    }
    .tool-card h2 {
      color: #ff4e50;
      font-size: 1.3em;
      margin-bottom: 10px;
    }
    .tool-card p {
      font-size: 1em;
      color: #444;
    }
    .footer {
      text-align: center;
      padding: 30px;
      background: #fff;
      color: #666;
      font-size: 1em;
    }
    .ad-container {
      display: flex;
      justify-content: center;
      margin: 20px auto;
    }
    @media (max-width: 600px) {
      .tool-card {
        width: 90%;
      }
      header h1 {
        font-size: 2.2em;
      }
      header p {
        font-size: 1.1em;
      }
    }
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
      data-ad-client="ca-877348079981"
      data-ad-slot="ca-pub-9354903383"
      data-ad-format="auto"
      data-full-width-responsive="true"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>

  <section class="tools-grid">
    <div class="tool-card"><h2>Image Compressor</h2><p>Shrink images fast, smooth, and beautifully.</p></div>
    <div class="tool-card"><h2>Online Calculator</h2><p>Crunch numbers with ease and clarity.</p></div>
    <div class="tool-card"><h2>Stopwatch & Timer</h2><p>Track time with style and precision.</p></div>
    <div class="tool-card"><h2>QR Code Generator</h2><p>Create scannable codes instantly.</p></div>
    <div class="tool-card"><h2>Text Case Converter</h2><p>Flip between UPPER, lower, Proper, or Sentence case.</p></div>
    <div class="tool-card"><h2>Password Generator</h2><p>Create strong, secure, and unique passwords.</p></div>
    <div class="tool-card"><h2>Unit Converter</h2><p>Convert length, mass, volume, and more.</p></div>
    <div class="tool-card"><h2>Color Picker</h2><p>Pick and copy color hex codes instantly.</p></div>
    <div class="tool-card"><h2>Word Counter</h2><p>Count words, characters, and lines in real time.</p></div>
  </section>

  <div class="ad-container">
    <ins class="adsbygoogle"
      style="display:block"
      data-ad-client="877348079981"
      data-ad-slot="ca-pub-9055111364"
      data-ad-format="auto"
      data-full-width-responsive="true"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>

  <div class="footer">
    <p><strong>Click any tool above and start exploring!</strong><br>
    Bright. Bold. Beautiful. That’s <span style="color: #ff4e50;">ToolHubs-1</span>.</p>
  </div>

  <script>
    function switchTo
ol() {
      const selected = document.getElementById("toolSwitch").value;
      if (selected) window.location.href = selected;
    }
  </script>
</body>
</html>
