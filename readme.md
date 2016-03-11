This was the first experiment I did with Ken Shirrif's Infrared Remote Control Library for the Arduino. 

The circuit uses a TSOP382 IR photo sensor to receive the codes from the Clarion remote controller I had lying around.  Once the code is received the program then decides which tone to play.  In this example I have 8 tones set up, middle c through middle b.  For added fun and visual effects I turn on a led for each of the notes as they are played.

Here is a short video of a few notes being played on the Arduino.  Below the video is the code along with some instructions on how to modify the library so it will work with the tone() function.

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/8W6UCkx7llQ/0.jpg)](http://www.youtube.com/watch?v=8W6UCkx7llQ)

If you try to use this you will need to install the Arduino library written by Ken Shirrif.  You will also need to modify the library so that it uses TIMER1 instead of TIMER2 because TIMER2 is used by the tone() function. 

First, go to Libraries\Documents\Arduino\libraries\IRremote , the files for the library would be there.
In IRremoteInt.h, at line 194 you need to uncomment the IR_USE_TIME1 line and comment out the IR_USE_TIMER2

Now if your using codebender you will need to upload the modified version of Ken Shirrif's library to your personal libraries so that when compiling it will user your modified version rather than the default version that is allready registered with codebender.



[Source Code.](https://github.com/driewe/IRMusic/blob/master/sourcecode/IR_Music.ino)
