<!DOCTYPE html>
<html>
  <head>
    <title>Animated Name</title>
    <style>
      #name {
        font-size: 48px;
        color: #000;
        text-align: center;
        animation: pulse 1s infinite;
      }

      @keyframes pulse {
        0% {
          transform: scale(1);
        }
        50% {
          transform: scale(1.2);
        }
        100% {
          transform: scale(1);
        }
      }
    </style>
  </head>
  <body>
    <div id="name"></div>
    <script>
      const name = "Your Name";
      const textColor = "#000"; // change to your preferred text color
      const fontSize = "48px"; // change to your preferred font size
      const animationDuration = "1s"; // change to your preferred animation duration
      const animationDelay = "0.1s"; // change to your preferred animation delay

      const nameDiv = document.querySelector("#name");
      nameDiv.style.color = textColor;
      nameDiv.style.fontSize = fontSize;
      nameDiv.style.animationDuration = animationDuration;

      for (let i = 0; i < name.length; i++) {
        const char = name.charAt(i);
        const span = document.createElement("span");
        span.textContent = char;
        span.style.animationDelay = `${i * parseFloat(animationDelay)}s`;
        nameDiv.appendChild(span);
      }
    </script>
  </body>
</html>
