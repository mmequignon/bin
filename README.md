# bin
Some scripts I've made

###creagif

This script makes GIF animated screenshots.
Requirements: imagemagick, ffmpeg
It's bash written and work with ffmpeg and imagemagick.
In a first time, it'll make five screenshots per seconds using ffmpeg. And then, you will be able to cut undesirable parts, deleting the concerned pictures.
Once you have finished your modifications, imagemagick will merge png's in a single animated GIF file.

###screenmgr

This one allows you to manage your screens.
A little useless if you use a GUI, but useful if you are using a window manager like awesome, as I do.
First, you'll have to list your devices with the **-l** option, available screens will be displayed, HDMI2, for example.
Then, you can choose an action, connect, or disconnect.
If you want to use the screen as a cloned display :
**screenmgr -c HDMI2 --clone**
And if you want to disconnect it :
**screenmgr -d HDMI2**

Try screenmgr **-h** if you want to know more about the syntax and the different options
