# FFMPEG-Camera-Streams
ffmpeg files to stream RTSP-based camera feeds to HTTP

Usage:
For more than four cameras you can copy the files increasing the number corresponding to the cameras that are installed.

Each file requires a configuration file corresponding to the camera RTSP feed.

E.g. stream1.conf should contain an RTSP URL that corresponds to the camera. Camera documentation will
describe the format.  One example is shown here:

```
rtsp://username:password@XXX.XXX.XXX.XXX:YYY/video.mjpeg?channel=1&stream=0
```

The mosaic configuration file, mosaic_inputs.conf uses a similar format except needs a prefix on each line for each camera:

```
-i rtsp://username:password@XXX.XXX.XXX.XXX:YYY/video.mjpeg?channel=1&stream=0
-i rtsp://username:password@XXX.XXX.XXX.XXX:YYY/video.mjpeg?channel=2&stream=0
-i rtsp://username:password@XXX.XXX.XXX.XXX:YYY/video.mjpeg?channel=3&stream=0
-i rtsp://username:password@XXX.XXX.XXX.XXX:YYY/video.mjpeg?channel=4&stream=0
```
