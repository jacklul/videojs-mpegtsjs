```html
<link href="https://cdn.jsdelivr.net/npm/video.js/dist/video-js.min.css" rel="stylesheet" />
<script src="https://cdn.jsdelivr.net/npm/video.js/dist/video.min.js" type="text/javascript"></script>

<link href="https://cdn.jsdelivr.net/npm/videojs-mobile-ui/dist/videojs-mobile-ui.min.css" rel="stylesheet">
<script src="https://cdn.jsdelivr.net/npm/videojs-mobile-ui/dist/videojs-mobile-ui.min.js" type="text/javascript"></script>

<script src="https://cdn.jsdelivr.net/npm/mpegts.js/dist/mpegts.min.js" type="text/javascript"></script>

<script src="https://cdn.jsdelivr.net/gh/jacklul/videojs-mpegtsjs@master/videojs-mpegts.js" type="text/javascript"></script>

<script type="text/javascript">
    if (window.mpegts) {
        mpegts.LoggingControl.applyConfig({
            enableDebug: false,
            enableVerbose: false,
            enableInfo: false,
            enableWarn: false,
            enableError: true,
        });
    }
    
    var player = videojs('video', {
        suppressNotSupportedError: true,
        mpegtsjs = {
            mediaDataSource: {
                type: 'mpegts',
                isLive: true,
                cors: true,
                withCredentials: false
            },
            config: {
                enableWorker: true,
                enableWorkerForMSE: true,
            }
        }
    });
</script>
```
