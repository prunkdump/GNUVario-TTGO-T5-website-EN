---
step: 5
title: Manual
description: Web page
---

The GnuVario-E embeds a Web server; it is accessed after the wifi connection, via a web browser. See previous page of the manual.

The home page looks like this:
{%include manuelimg.md name="pageweb_01EN.jpg"%}

or like this, if the screen width does not allow the display of all the menus.
{%include manuelimg.md name="pageweb_02EN.jpg"%}

In the latter case, simply click on the menu icon, at the top right, to access the menu.

The different menu options are described now.

### "My flights" menu

This is the menu offered by default. It lists the different IGC files of the flights saved on the SD card.
There are three tabs:

**My pending tracks where for each flight you can:**
- Upload it to the paraglidinglogbook.com website
- Place it in your flight log
- download it
- delete the recording
- visualize it in a summary way

{% include manuelimg.md name="mestracesenattenteEN.jpg" %}

**My flight diary**
- List of flights
- Allows you to edit them
- Flight statistics

{% include manuelimg.md name="moncarnetdevolsEN.jpg" %}

**My flight sites**
- Allows you to add flight sites.
- Geographical coordinates must be entered in decimal format. You can find the coordinates on google earth, your IGC track and convert them to decimals using this [website](https://fr.planetcalc.com/1129/):

{% include manuelimg.md name="messitesdevolsEN.jpg" %}



### "SD card" 

Presents the contents of the SD card. Allows you to create / delete folders, download or upload files.
{%include manuelimg.md name="SDcard_01.jpg"%}
#### Folders
The files are proposed first. If you click on the title of a folder, you open it, and the included files are displayed; we see it in the previous screenshot, for the 'flights' folder.
New files can be placed in a folder by clicking on the blue 'Download' icon. You can also delete a folder and all the files included by clicking on the red 'Delete' icon.
#### Files
The file can be downloaded to the computer by clicking on the green 'Download' icon. You can also delete the file by clicking on the red 'Delete' icon.

### "Wifi" 

Allows you to specify the wifi networks to which the vario can potentially connect.
It is possible to declare up to 4 wifi networks.
The result is written on the SD card, in the file '/wifi.cfg'

### "Configuration" 

The options offered in this tab allow you to customize the operation of the vario; they are linked to the file '/params.jso' on the SD card.
The parameters are described in the ['Configuration']({{site.baseurl}}/6-configuration.html) part of the GNUVario documentation.

These parameters are divided into 4 tabs:
'_Général_' - '_Vario_' - '_Début du vol_' - '_Système_'- '_Calibration_'   
{%include manuelimg.md name="configuration_01EN.jpg"%}
- General
Used to describe the sails or sails on which we are flying, and the name of the pilot.
Mainly used for UGC flight recordings
- Vario
Allows you to configure the operation of the vario: threshold for triggering beeps, and different options
- Flight start
Defines the criteria that will allow the vario to determine that a flight has just started.
- System
Allows you to adjust various parameters relating to the operation of the vario: beeps when starting the vario, the flight, the fixed GPS, activation of flight recording...
- Calibration     
Used to generate the variocal.cfg file after having calibrated its vario (see dedicated page)

### "Update" 
Used to update the vario software.
{%include manuelimg.md name="update_01.jpg"%}
The update can be done 'locally', from a computer that has a desired firmware version.

It is also possible to automatically update the firmware from the web.

See the documentation dedicated to updating the vario.