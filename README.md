<head>
  <meta content="never" name="referrer">
  <title>MHDTVPLAY.NET | Watch Your Favourite Indian TV Channels Anytime Anywher</title>
  <meta name="robots" content="noindex" />
  <link rel="stylesheet" type="text/css" href="/clap.css">
  <script src="//cdn.jsdelivr.net/npm/@clappr/player@0.4.0/dist/clappr.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/mux.js@5.6.7/dist/mux.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/level-selector@latest/dist/level-selector.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/clappr-chromecast-plugin@latest/dist/clappr-chromecast-plugin.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/clappr-pip@latest/dist/clappr-pip.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/clappr-playback-rate-plugin@latest/dist/clappr-playback-rate-plugin.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/shaka-player@2.5.10/dist/shaka-player.compiled.min.js"></script>
  <script src="//cdn.jsdelivr.net/gh/clappr/dash-shaka-playback@latest/dist/dash-shaka-playback.external.min.js"></script>
  <script src="//cdn.jsdelivr.net/npm/cdnbye-shaka@latest"></script>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.0/jquery.min.js"></script>
  <script disable-devtool-auto src='https://cdn.jsdelivr.net/npm/disable-devtool@latest'></script>
  <style>
    .player-poster[data-poster] {
      background-size: cover;
    }

    body {
      margin: 0;
      padding: 0;
    }
  </style>
</head>
<div id="player"></div>
<script>
  var player = new Clappr.Player({
    source: 'https://bpprod5linear.akamaized.net/bpk-tv/irdeto_com_Channel_252/output/manifest.mpd',
    mimeType: 'application/dash+xml',
    height: '100%',
    width: '100%',
    autoPlay: true,
    plugins: [LevelSelector, DashShakaPlayback, Clappr.MediaControl],
    events: {
      onReady: function() {
        var plugin = this.getPlugin('click_to_pause');
        plugin && plugin.disable();
      },
    },
    chromecast: {
      appId: '9DFB77C0',
      contentType: 'video/mp4',
    },
    shakaConfiguration: {
      drm: {
        clearKeys: {
          '6a9e4204f3f8577ebf6e79b3b18573f8': '49d1acc1dc6426331da6d0a0ff4e67a7'
        }
      },
    },
    shakaOnBeforeLoad: function(shaka_player) {},
    parentId: '#player'
  });
</script>
