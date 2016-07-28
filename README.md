# online-videostream-processing
I'm testing an online processing video stream which include transcoding, image processing (face recognition) in realtime. 

HTTP and websocket server are written in GO, video decoding and encoding library are written in C utilizing ffmpeg (libavcoded, libavutil, and libswscale), image processing library using OpenCV with python binding, and web client decoder to view the processed video is using jsmpeg library which written in javascript.

Video will be streamed using h264 to http server to be decoded to PPM (portable pixmap format) and processed. The processed image then encoded to MPEG1 and broadcasted through websocket connection to connected client(s). 

## Dependencies
This project using several dependencies as follows:
- ffmpeg
- jsmpeg
- OpenCV version >3

## How To Build

## How To Run