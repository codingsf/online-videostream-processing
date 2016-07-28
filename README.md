# online-videostream-processing
Experimenting online video stream processing which include transcoding, image processing (face recognition) in realtime, instead performing the frame processing locally

HTTP and websocket server are written in GO, video decoding and encoding library are written in C utilizing ffmpeg (libavcoded, libavutil, and libswscale), image processing library using OpenCV with python binding, and web client decoder to view the processed video is using jsmpeg library which written in javascript.

Video will be streamed using h264 to http server, decoded to PPM (portable pixmap format) and processed. The processed image then encoded to MPEG1 and broadcasted through websocket connection to connected client(s). 

## Dependencies
This project using several dependencies as follows:
- [Go](https://golang.org/) version >1.5
- [ffmpeg](http://ffmpeg.org)
- [jsmpeg](https://github.com/phoboslab/jsmpeg)
- [OpenCV](http://opencv.org/) version >3

## How To Install
Make sure that you have installed Golang, ffmpeg and OpenCV locally. 

You can find the steps to compile and install ffmpeg in this link <https://trac.ffmpeg.org/wiki/CompilationGuide>.

I'm using anaconda to install OpenCV on my machine <https://www.continuum.io/downloads> and run 'conda install opencv'. Or you can download form http://opencv.org/downloads.html

To build and install online-videostream-processing:
```
make
make install
make clean
```
## How To Run
Running the server
```
./server
```
Open cam and stream to endpoint
```
./cam-stream.sh
```

Open client.html to see the live stream of the processed image
