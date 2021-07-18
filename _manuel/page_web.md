---
step: 6
title: Manual
description: Webserver
---

The GnuVario-E embeds a Web server. It is accessed after the wifi connection, via an Internet browser. See the previous [page]({{site.baseurl}}/manual/wifi.html) of the manual.

The home page looks like this:
{%include manuelimg.md name="pageweb_01EN.jpg"%}

or like this, if the screen width does not allow the display of all the menus.

{%include manuelimg.md name="pageweb_02EN.jpg"%}

In the latter case, simply click on the menu icon, at the top right, to access the menu.


### *"My flights" menu*{: style="color: #138ca2; opacity: 1;" }

This is the menu offered by default. It lists the different IGC files of the flights saved on the SD card.
There are three tabs:

**My pending tracks where for each flight you can:**{: style="color: #138ca2; opacity: 1;" }
- Upload it to the paraglidinglogbook.com website
- Place it in your flight log
- download it
- delete the recording
- visualize it in a summary way

{% include manuelimg.md name="mestracesenattenteEN.jpg" %}

**My flight diary**{: style="color: #138ca2; opacity: 1;" }
- List of flights
- Allows you to edit them
- Flight statistics

{% include manuelimg.md name="moncarnetdevolsEN.jpg" %}

**My flight sites**{: style="color: #138ca2; opacity: 1;" }
- Allows you to add flight sites.
- Geographical coordinates must be entered in decimal format. You can find the coordinates on google earth, your IGC track and convert them to decimals using this [website](https://fr.planetcalc.com/1129/):

{% include manuelimg.md name="messitesdevolsEN.jpg" %}



### *"SD card" tab*{: style="color: #138ca2; opacity: 1;" }

Shows the contents of the SD card. Allows you to create / delete folders, download or upload files.
{% include manuelimg.md name = "SDcard_01.jpg"%}

**Folders**{: style="color: #138ca2; opacity: 1;" }

The folders are proposed first. Clicking on the title of a folder opens it, and the included files are displayed. We see it in the previous screenshot, for the 'flights' folder.
You can drop new files into a folder by clicking on the blue 'Download' icon. You can also delete a folder and all the included files by clicking on the red 'Delete' icon.

**Files**{: style="color: #138ca2; opacity: 1;" }

The file can be downloaded to the computer by clicking on the green 'Download' icon. you can also delete the file by clicking on the red icon 'Delete'.

### *"Wifi" tab*{: style="color: #138ca2; opacity: 1;" }

Allows you to specify the wifi networks to which the vario can potentially connect.
It is possible to declare up to 4 wifi networks.
The result is written to the SD card, in the file '/wifi.cfg'

### *"Configuration" tab*{: style="color: #138ca2; opacity: 1;" }

The options offered in this tab allow you to customize the operation of the vario. They are linked to the '/params.jso' file on the SD card.
The parameters are described in the ['Configuration']({{site.baseurl}}/6-configuration.html) part of the GNUVario documentation.

These parameters are divided into 5 tabs:
'_Main_' - '_Vario_' - '_Flight start_' - '_System_' - '_Calibration_'
{% include manuelimg.md name = "configuration_01EN.jpg"%}
- Main  
Allows you to describe the wing (s) on which you are flying, and the name of the pilot.
Mainly used for IGC flight registrations

 - Vario  
Used to configure the operation of the vario: threshold for triggering audible beeps, and various options

 - Flight start  
Allows you to define the criteria that will allow the vario to determine that a flight has just started.

- System  
Allows you to set various parameters relating to the operation of the vario: beeps when starting the vario, the flight, the GPS fix, activation of flight recording, etc.

- Calibration  
Used to generate the variocal.cfg file after having calibrated its vario [(see dedicated page)]({{ site.baseurl }}/manuel/Calibration.html)

### *"Update" tab*{: style="color: #138ca2; opacity: 1;" }
Allows you to update the software (firmware) of the vario.
{% include manuelimg.md name = "update_01.jpg"%}
The update can be done 'locally', from a computer that has a desired firmware version.

It is also possible to automatically update the firmware from the internet if available.

See the documentation dedicated to updating the vario.

### *"Settings/Preferences" tab*{: style="color: #138ca2; opacity: 1;" }


The options offered in this tab allow you to customize the webservers:

- interface

Allows you to choose the theme, colors, fonts of the webserver pages

- Language

Allows you to choose between French, English and Russian.

- Paraglidinglogbook.com

Allows to [activate]({{site.baseurl}}/manuel/paralogbook.html) the flight log option on the Paraglidinglogbook.com site

- Dropbox

Allows to [activate]({{site.baseurl}}/manuel/Dropbox.html) the option allowing to save his tracks and logbook on a Dropbox account.


{% include manuelimg.md name = "preferences.jpg"%}

### *"DB to Dropbox" tab*{: style="color: #138ca2; opacity: 1;" }

Allows you to save the database of flights and sites recorded in your logbook (tab displayed only if you have activated [option]({{site.baseurl}}/manuel/Dropbox.html)).

{% include manuelimg.md name = "dropbox0EN.jpg"%}