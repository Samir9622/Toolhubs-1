<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <meta name="description" content="ToolHubs-1 - All-in-One Free Online Tools Hub"/>
  <title>ToolHubs-1 | All-in-One Tools</title>
  <link href="https://fonts.googleapis.com/css2?family=Segoe+UI:wght@400;700&display=swap" rel="stylesheet"/>

  <!-- Google AdSense -->
  <script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8773480799818158" crossorigin="anonymous"></script>

  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(145deg, #fceabb, #f8b500);
      color: #333;
    }

    header {
      background: linear-gradient(145deg, #ff416c, #ff4b2b);
      padding: 60px 20px 30px;
      text-align: center;
      color: #fff;
      border-radius: 0 0 25px 25px;
      box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
    }

    header h1 {
      font-size: 3em;
      margin: 0;
      text-shadow: 2px 2px 5px #00000055;
    }

    header p {
      font-size: 1.4em;
      max-width: 800px;
      margin: 20px auto 0;
      line-height: 1.6;
    }

    .switcher {
      text-align: center;
      margin: 40px auto 20px;
      padding: 20px;
      background: #fff8e1;
      border-radius: 15px;
      max-width: 320px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }

    select {
      font-size: 1.2em;
      padding: 12px 20px;
      border-radius: 10px;
      border: 2px solid #ff9800;
      background: #fffef7;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      cursor: pointer;
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
      margin-top: 20px;
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

      .switcher {
        max-width: 90%;
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>Welcome to ToolHubs-1!</h1>
    <p>Your ultimate playground of <strong>smart, stylish & superfast tools</strong> — All in One Place!</p>
  </header>

  <div class="switcher">
    <label for="toolSelect"><strong>Select a Tool:</strong></label><br><br>
    <select id="toolSelect" onchange="navigateToTool()">
      <option value="">-- Choose Tool --</option>
      <option value="image-compressor">Image Compressor</option>
      <option value="online-calculator">Online Calculator</option>
      <option value="stopwatch-timer">Stopwatch & Timer</option>
      <option value="qr-code-generator">QR Code Generator</option>
      <option value="text-case-converter">Text Case Converter</option>
      <option value="password-generator">Password Generator</option>
      <option value="unit-converter">Unit Converter</option>
      <option value="color-picker">Color Picker</option>
      <option value="word-counter">Word Counter</option>
    </select>
  </div>

  <!-- Top AdSense Unit -->
  <div style="text-align: center; margin: 20px 0;">
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="877348079981"
         data-ad-slot="9354903383"
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

  <!-- Bottom AdSense Unit -->
  <div style="text-align: center; margin: 40px 0;">
    <ins class="adsbygoogle"
         style="display:block"
         data-ad-client="877348079981"
         data-ad-slot-"9055111364"
         data-ad-format="auto"
         data-full-width-responsive="true"></ins>
    <script>(adsbygoogle = window.adsbygoogle || []).push({});</script>
  </div>

  <div class="footer">
    <p><strong>Click any tool above or select from the dropdown!</strong><br>
    Bright. Bold. Beautiful. That’s <span style="color: #ff4e50;">ToolHubs-1</span>.</p>
  </div>

  <script>
    function n
avigateToTool() {
      const tool = document.getElementById('toolSelect').value;
      if (tool) {
        window.location.href = tool + '.html';
      }
    }
  </script>

</body>
</html>
