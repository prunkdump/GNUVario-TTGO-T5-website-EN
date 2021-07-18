---
step: 2
description:  Update the SD card and the web server
---

# **1. First update**{: style="color:   #138ca2; opacity: 1;" }

If you have just built your variometer, just download the latest version of the "RootSD" folder corresponding to your firmware version from the [**download site**](http://gnuvario-e.yj.fr /).

After unzipping it, copy the files contained in this folder directly to the root of your blank microSD card previously formatted in Fat16 or 32.

Then download the zip ["www"](http://gnuvario-e.yj.fr/) (Tab **"Download web files"**) corresponding to your version and after having unzipped it, copy the file **www.gz** at the root of the microSD card.

Don't forget to download the topographic files for your region [**here**](https://vps.skybean.eu/agl/) and copy them to the AGL folder.

Insert the card into your vario and start it. The web server will update and then restart. Your vario is ready to be [configured]({{site.baseurl}}/manuel/page_web.html).

  

# **2.Following updates**{: style="color:   #138ca2; opacity: 1;" }

The following updates are similar but some files should not be replaced in order not to lose your data and settings.
 
Download the latest version of the "RootSD" folder corresponding to the version of your firmware on the [**download site**](http://gnuvario-e.yj.fr/)
After unzipping it, copy the files in this folder directly to the root of your microSD card **EXCEPT**{: style="color: #ff3349; opacity: 1;" }:

**The files:**{: style="color: #138ca2; opacity: 1;" }

- `prefs.jso` (Webserver preferences)

- `params.jso` (Webserver settings)

- `variocal.cfg` (your calibration)

- `variosound.cfg` (your custom sound curve)

- `wifi.cfg` (your wifi codes)

**The folders:**{: style="color: #138ca2; opacity: 1;" }

- `AGL` (your topographic files already downloaded)

- `db` (the database including classified flights and recorded sites)

- `flights` (if you have flights not yet classified).

Then download the zip ["www"](http://gnuvario-e.yj.fr/) (Tab **"Download web files"**) corresponding to your version and after having unzipped it, copy the file **www.gz** at the root of the microSD card.

When your vario starts up, the web server will update and then the vario will restart.

Before any update, we recommend that you make a backup copy of your microSD card.

