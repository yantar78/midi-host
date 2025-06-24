
<a href="https://yantar78.github.io/midi-host/joytouchbytouch_Joy.mid" download>joytouchbytouch</a>

<head>
  <meta charset="UTF-8">
  <title>Проигрыватель MIDI</title>
  <script src="https://yantar78.github.io/midi-host/joytouchbytouch_Joy.mid"></script>
</head>
<body>
 
  <button onclick="playMIDI()">▶ Играть MIDI</button>

  <script>
    function playMIDI() {
      MIDI.loadPlugin({
        soundfontUrl: "./soundfont/",
        instrument: "acoustic_grand_piano",
        onsuccess: function() {
          MIDI.Player.loadFile("joytouchbytouch_Joy.mid", MIDI.Player.start);
        }
      });
    }
  </script>
</body>
</html>
