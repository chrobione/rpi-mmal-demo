Simple Raspberry Pi MMAL project

* main.c - just displays camera preview until ctrl-c
* still_capture.c - captures  still jpeg image with text overlay
* video_record.c  - records video with text overlay, outputs h264

        -t 3 - record 3 seconds of video
        -s "camera 1" - overlay text

Build
-----
0. Install pre-required packages
   
        $ sudo apt-get install cmake libopencv-dev


1. Place  Raspberry Pi userland project in /home/pi/src/raspberrypi/userland
    
        $ mkdir -p /home/pi/src/raspberrypi
        $ cd /home/pi/src/raspberrypi
        $ git clone --depth 1 https://github.com/raspberrypi/userland.git


2. Build pre-required libraries
    
        $ make -C /opt/vc/src/hello_pi/libs/vgfont
    

3. Build project 

        $ mkdir build
        $ cd build
        $ cmake ../
        $ make 
    
    
<img src="http://i.imgur.com/r7HOAVA.jpg"/>
