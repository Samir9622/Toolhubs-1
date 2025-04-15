<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>ToolHubs1</title>
  <style>
    /* Base styles (same as before) */
    body { font-family: sans-serif; background: #f8fafa; margin: 0; padding: 0; }
    .container { padding: 20px; max-width: 1200px; margin: 0 auto; }
    h1 { color: #2d60d1; text-align: center; }
    .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(240px, 1fr)); gap: 16px; margin-top: 20px; }

    /* Tool switching system */
    .tool-content { display: none; padding: 20px; background: white; border-radius: 10px; margin-top: 20px; }
    .tool-active { display: block; }
  </style>
</head>
<body>
  <div class="container">
    <h1>ToolHubs1</h1>
    <p style="text-align: center">All-in-One Utility Tools at Your Fingertips</p>

    <div class="grid">
      <!-- Tools now load in-page -->
      <div class="card" onclick="showTool('image-compressor')">
        <div>Image Compressor</div>
        <p>Reduce image size without losing quality.</p>
      </div>

      <div class="card" onclick="showTool('calculator')">
        <div>Online Calculator</div>
        <p>Perform quick and accurate calculations.</p>
      </div>

      <!-- Add more tool cards following the same pattern -->
    </div>

    <!-- Tool Containers -->
    <div id="image-compressor" class="tool-content">
      <h2>Image Compressor</h2>
      <input type="file" id="image-input" accept="image/*">
      <canvas id="preview-canvas"></canvas>
      <button onclick="compressImage()">Compress</button>
    </div>

    <div id="calculator" class="tool-content">
      <h2>Calculator</h2>
      <input type="text" id="calc-display" readonly>
      <div class="calc-buttons">
        <!-- Calculator buttons would go here -->
      </div>
    </div>

    <!-- Add more tool containers -->
    
    <footer>
      © 2025 ToolHub by Samir Dey. All rights reserved.
    </footer>
  </div>

  <script>
    // Tool switching logic
    function showTool(toolId) {
      document.querySelectorAll('.tool-content').forEach(el => {
        el.classList.remove('tool-active');
      });
      document.getElementById(toolId).classList.add('tool-active');
    }

    // Basic Image Compressor logic
    function compressImage() {
      const input = document.getElementById('image-input');
      const canvas = document.getElementById('preview-canvas');
      const file = input.files[0];
      
      if (file) {
        const reader = new FileReader();
        reader.onload = function(e) {
          const img = new Image();
          img.onload = function() {
            canvas.width = img.width;
            canvas.height = img.height;
            const ctx = canvas.getContext('2d');
            ctx.drawImage(img, 0, 0);
            // Add compression logic here
          }
          img.src = e.target.result;
        }
        reader.readAsDataURL(file);
      }
    }

    // Initialize first tool
    showTool('image-compressor');
  </script>
</body>
</html>
