<!DOCTYPE html>
<html>
  <head>
    <title>My Name Animation</title>
    <style>
      #name {
        font-size: 48px;
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
    <div id="name">Haze Morales</div>
    <script>
      const name = document.querySelector("#name");
      const text = name.textContent;
      name.innerHTML = "";

      for (let i = 0; i < text.length; i++) {
        const char = text.charAt(i);
        const span = document.createElement("span");
        span.textContent = char;
        span.style.animationDelay = `${i * 0.1}s`;
        name.appendChild(span);
      }
    </script>
  </body>
</html>
