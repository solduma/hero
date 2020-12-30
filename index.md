<!doctype html>
<html lang="en">

<head>
  <meta charset="utf-8">
  <title>js-dos 6.22, Arkanoid</title>
  <script src="https://js-dos.com/6.22/current/js-dos.js"></script>
  <style>
    html, body, canvas, .dosbox-container {
      width: 100%;
      height: 100%;
      margin: 0;
      padding: 0;
      overflow: hidden;
    }
  </style>
</head>

<body>
  <canvas id="jsdos"></canvas>
  <button style="position: absolute; right: 1em; top: 1em;" onclick="ci.fullscreen()">Fullscreen</button>
  <script>
    Dos(document.getElementById("jsdos"), { 
      wdosboxUrl: "https://js-dos.com/6.22/current/wdosbox.js",
      cycles: 1000,
      autolock: true,
    }).ready(function (fs, main) {
      fs.extract("https://solduma.github.io/hero/src/hero.zip").then(function () {
        console.log('sdf');
        main(["-c", "cd hero", "-c", "HERO.COM"]).then(function (ci) {
          window.ci = ci;
        });
      });
    });
  </script>
</body>

</html>
