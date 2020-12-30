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
