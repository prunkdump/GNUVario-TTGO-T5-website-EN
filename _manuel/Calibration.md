---
step: 6
title: Manual
description: Calibration
---

**It is important to calibrate the accelerometers**

The GnuVario-E incorporates an accelerometer, which must be calibrated.

**Procédure:**

Since version 0.10.2 of the webserver, the calibration procedure is simplified. 

{% include manuelimg.md name="calibrationweb1EN.jpg" %}

**1.** From the web server, "SD card" tab or directly on the SD card, check that the variocal.cfg file is the blank file available in the RootSD folder.

{% highlight shell_session %}
Blank variocal.cfg file 

[VERSION=1.0]

/* Calibration */
[VERTACCEL_GYRO_CAL_BIAS_00=0x00]
[VERTACCEL_GYRO_CAL_BIAS_01=0x00]
[VERTACCEL_GYRO_CAL_BIAS_02=0x00]
[VERTACCEL_GYRO_CAL_BIAS_03=0x00]
[VERTACCEL_GYRO_CAL_BIAS_04=0x00]
[VERTACCEL_GYRO_CAL_BIAS_05=0x00]
[VERTACCEL_GYRO_CAL_BIAS_06=0x00]
[VERTACCEL_GYRO_CAL_BIAS_07=0x00]
[VERTACCEL_GYRO_CAL_BIAS_08=0x00]
[VERTACCEL_GYRO_CAL_BIAS_09=0x00]
[VERTACCEL_GYRO_CAL_BIAS_10=0x00]
[VERTACCEL_GYRO_CAL_BIAS_11=0x00]
[VERTACCEL_ACCEL_CAL_BIAS_00=0]
[VERTACCEL_ACCEL_CAL_BIAS_01=0]
[VERTACCEL_ACCEL_CAL_BIAS_02=0]
[VERTACCEL_ACCEL_CAL_SCALE=0]
[VERTACCEL_MAG_CAL_BIAS_00=0]
[VERTACCEL_MAG_CAL_BIAS_01=0]
[VERTACCEL_MAG_CAL_BIAS_02=0]
[VERTACCEL_MAG_CAL_PROJ_SCALE=-16689]
[VERTACCEL_ACCEL_CAL_BIAS_MULTIPLIER=6]
[VERTACCEL_MAG_CAL_BIAS_MULTIPLIER=4]

{% endhighlight %}


**2.** Delete the "RECORD00.CAL file if it is present. 

**3.** Restart the vario then perform the calibration manipulation:  

Enter calibration mode by pressing the right button at start-up (at the time of the init screen).
You have a few seconds to place the vario flat and press the center button. 

To be optimal, the calibration should not be done on a north/south axis. If you know where north is, try shifting the vario 45 ° from north (when it is flat on the table)     

**Wait for the 3 beeps** then start rotating the vario in all directions using a support (cardboard, book) to stabilize it on its edge.
You must do about 5 to 6 moves per side while waiting for the beep between each move
The more measurements you take, the more accurate the calibration will be.
**ATTENTION it is essential not to forget any face**     

At the end, press the left button of the vario for at least two seconds to complete the calibration. The vario restarts.   

<iframe width="560" height="315" src="https://www.youtube.com/embed/6yxoZcxxzVY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>


**4.** Return to the web server then go to the "Configuration" tab, then "CALIBRATION" 

{% include manuelimg.md name="calibrationweb3EN.jpg" %}

Press "Start the generation of the calibration file". The RECORD00.CAL file created during the calibration phase is sent to a remote server which calculates the correct values and updates the Variocal.cfg file.

If the message "Calculation of the calibration file OK appears, it means that everything has gone well. Your vario is calibrated.

{% include manuelimg.md name="calibrationweb2EN.jpg" %}


**If the semi-automatic procedure above does not work, you can calculate the calibration values with a python script.**


**1.** On Windows, install the [Python](https://www.python.org/downloads/) programm . Make sure to check the **add Python x.x to PATH** option.

{% include manuelimg.md name="python6.jpg" %}

**2.** Copy the "calibration" folder located in the RootSD folder to your desktop. 

**3.** Start IDLE python, in IDLE: File> Open and open the get-pip.py file located in the / calibration / Installation folder 

Press F5 once the file is open to run the get-pip.py program 

{% include manuelimg.md name="python1.jpg" %}

**4.** When execution is complete, open a Windows command prompt. 

Copy and run the following command: "python -m pip install --user numpy scipy matplotlib ipython jupyter pandas sympy nose" 

{% include manuelimg.md name="python2.jpg" %}

Restart the computer after the command is executed and completed. 

**5.** Follow the calibration steps **1. 2. & 3.** of the calibration via the above web server to perform the vario calibration. 

**6.** Delete the “RECORD00.CAL” file already present in the “calibration” folder on your desktop

**7.** Copy the “RECORD00.CAL” file from the SD card to the “calibration” folder on your desktop


**8.** Launch IDLE python, in IDLE: File> Open and open the calibrate.py file located in the "calibration" folder on your desktop

{% include manuelimg.md name="python3.jpg" %}

**9.** Press F5 to launch the program

{% include manuelimg.md name="python4.jpg" %}

**10.** You can also write the command python calibrate.py directly on a windows command prompt to the address of your calibration folder:

{% include manuelimg.md name="python5.jpg" %}

**11.** At the end of the execution of the program, copy all the parameters of the calibration in the variocal.cfg file on the SD card.

{% highlight shell_session %}
variocal.cfg file

[VERSION=1.0]

/* Calibration */
[VERTACCEL_GYRO_CAL_BIAS_00=0xad]
[VERTACCEL_GYRO_CAL_BIAS_01=0x80]
[VERTACCEL_GYRO_CAL_BIAS_02=0x0f]
[VERTACCEL_GYRO_CAL_BIAS_03=0x80]
[VERTACCEL_GYRO_CAL_BIAS_04=0x00]
[VERTACCEL_GYRO_CAL_BIAS_05=0x1e]
[VERTACCEL_GYRO_CAL_BIAS_06=0xfd]
[VERTACCEL_GYRO_CAL_BIAS_07=0x3f]
[VERTACCEL_GYRO_CAL_BIAS_08=0x01]
[VERTACCEL_GYRO_CAL_BIAS_09=0x00]
[VERTACCEL_GYRO_CAL_BIAS_10=0xf4]
[VERTACCEL_GYRO_CAL_BIAS_11=0xff]
[VERTACCEL_ACCEL_CAL_BIAS_00=5101]
[VERTACCEL_ACCEL_CAL_BIAS_01=16835]
[VERTACCEL_ACCEL_CAL_BIAS_02=5334]
[VERTACCEL_ACCEL_CAL_SCALE= -433 ]
[VERTACCEL_MAG_CAL_BIAS_00=-10569]
[VERTACCEL_MAG_CAL_BIAS_01=-2289]
[VERTACCEL_MAG_CAL_BIAS_02=18776]
[VERTACCEL_MAG_CAL_PROJ_SCALE= -3553 ]
[VERTACCEL_ACCEL_CAL_BIAS_MULTIPLIER= 8 ]
[VERTACCEL_MAG_CAL_BIAS_MULTIPLIER= 6 ]

{% endhighlight %}


**12.** Put back the SD card in your variometer. It is now calibrated.