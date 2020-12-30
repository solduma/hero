<html lang="en-us">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
    <title>js-dos api</title>
    <style type="text/css">
      .dosbox-container { width: 1024px; height: 768px; }
      .dosbox-container > .dosbox-overlay { background: url(https://js-dos.com/cdn/digger.png); }
    </style>
  </head>
  <body>
    <div id="dosbox"></div>
    <br/>
    <button onclick="dosbox.requestFullScreen();">Make fullscreen</button>
    
    <script type="text/javascript" src="https://js-dos.com/cdn/js-dos-api.js"></script>
    <script type="text/javascript">
      var dosbox = new Dosbox({
        id: "dosbox",
        onload: function (dosbox) {
          dosbox.run("https://github.com/solduma/hero/blob/main/src/hero.zip?raw=true", "./HERO.COM");
        },
        onrun: function (dosbox, app) {
          console.log("App '" + app + "' is runned");
        }
      });
    </script>
  </body>
</html>

