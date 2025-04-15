<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="ToolHubs-1 - All-in-One Free Online Tools Hub"/>
  <title>ToolHubs-1 | All-in-One Tools</title>
  <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@400;700&display=swap" rel="stylesheet"/>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f0f2f5;
      color: #333;
    }

    header {
      background: linear-gradient(145deg, #f9d423, #ff4e50);
      padding: 60px 20px 30px;
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

    .ads-container {
      margin: 20px auto;
      display: flex;
      justify-content: center;
    }

    .tool-selector {
      text-align: center;
      margin: 40px 0 20px;
    }

    .tool-selector select {
      font-size: 1.1em;
      padding: 10px 20px;
      border-radius: 10px;
      border: 2px solid #ccc;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
      cursor: pointer;
    }

    .tool-section {
      display: none;
      padding: 20px;
    }

    .tool-section.active {
      display: block;
    }

    .tool-card {
      background: #ffffffcc;
      border: 2px solid #ddd;
      border-radius: 16px;
      padding: 20px;
      width: 90%;
      max-width: 600px;
      margin: 0 auto 40px;
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
      font-size: 1.5em;
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

    @media (max-width: 600px) {
      .tool-card {
        width: 95%;
      }

      header h1 {
        font-size: 2.2em;
      }

      header p {
        font-size: 1.1em;
      }
    }
  </style>

  <!-- Google AdSense -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158"
     crossorigin="anonymous"></script>
</head>
<body>

<header>
  <h1>Welcome to ToolHubs-1!</h1>
  <p>Your ultimate playground of <strong>smart, stylish & superfast tools</strong> — All in One Place!</p>
</header>

<!-- Top Ad Unit -->
<div class="ads-container">
  <ins class="adsbygoogle"
       style="display:block"
       data-ad-client="877348079981"
       data-ad-slot="ca-pub-"9354903383"
       data-ad-format="auto"
       data-full-width-responsive="true"></ins>
  <script>
       (adsbygoogle = window.adsbygoogle || []).push({});
  </script>
</div>

<!-- Tool Selector -->
<div class="tool-selector">
  <label for="tool-select"><strong>Select a Tool:</strong></label>
  <select id="tool-select">
    <option value="image-compressor">Image Compressor</option>
    <option value="calculator">Online Calculator</option>
    <option value="timer">Stopwatch & Timer</option>
    <option value="qr-code">QR Code Generator</option>
    <option value="text-case">Text Case Converter</option>
    <option value="password">Password Generator</option>
    <option value="unit-converter">Unit Converter</option>
    <option value="color-picker">Color Picker</option>
    <option value="word-counter">Word Counter</option>
  </select>
</div>

<!-- Tool Sections -->
<div id="image-compressor" class="tool-section active">
  <div class="tool-card">
    <h2>Image Compressor</h2>
    <p>Shrink images fast, smooth, and beautifully.</p>
  </div>
</div>

<div id="calculator" class="tool-section">
  <div class="tool-card">
    <h2>Online Calculator</h2>
    <p>Crunch numbers with ease and clarity.</p>
  </div>
</div>

<div id="timer" class="tool-section">
  <div class="tool-card">
    <h2>Stopwatch & Timer</h2>
    <p>Track time with style and precision.</p>
  </div>
</div>

<div id="qr-code" class="tool-section">
  <div class="tool-card">
    <h2>QR Code Generator</h2>
    <p>Create scannable codes instantly.</p>
  </div>
</div>

<div id="text-case" class="tool-section">
  <div class="tool-card">
    <h2>Text Case Converter</h2>
    <p>Flip between UPPER, lower, Proper, or Sentence case.</p>
  </div>
</div>

<div id="password" class="tool-section">
  <div class="tool-card">
    <h2>Password Generator</h2>
    <p>Create strong, secure, and unique passwords.</p>
  </div>
</div>

<div id="unit-converter" class="tool-section">
  <div class="tool-card">
    <h2>Unit Converter</h2>
    <p>Convert length, mass, volume, and more.</p>
  </div>
</div>

<div id="color-picker" class="tool-section">
  <div class="tool-card">
    <h2>Color Picker</h2>
    <p>Pick and copy color hex codes instantly.</p>
  </div>
</div>

<div id="word-counter" class="tool-section">
  <div class="tool-card">
    <h2>Word Counter</h2>
    <p>Count words, characters, and lines in real time.</p>
  </div>
</div>

<!-- Bottom Ad Unit -->
<div class="ads-container">
  <ins class="adsbygoogle"
       style="display:block"
       data-ad-client="877348079981"
       data-ad-slot="ca-pub-9055111364"
       data-ad-format="auto"
       data-full-width-responsive="true"></ins>
  <script>
       (adsbygoogle = window.adsbygoogle || []).push({});
  </script>
</div>

<div class="footer">
  <p><strong>Click any tool above and start exploring!</strong><br>
  Bright. Bold. Beautiful. That’s <span style="color: #ff4e50;">ToolHubs-1</span>.</p>
</div>

<script>
  const selector = document.getElementById('tool-select');
  const sections = document.querySelectorAll('.tool-section');

  selector.addEventListener('change', function () {
    const selected = this.value;
    sections.forEach(section => {
      section.classList.toggle('active', section.id === selected);
    });
  });
</script>

</body>
</html>
