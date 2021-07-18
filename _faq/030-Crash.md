---
description: My vario is crashing randomly

---

We have identified several situations leading to random crashes of the vario.

**1. List of debugs:**{: style="color:   #138ca2; opacity: 1;" }

Uncomment only the lines `#define PROG_DEBUG` and `#define DATA_DEBUG` in the `Arduino\libraries\VarioLog\DebugConfig.h` file.


{% highlight shell_session %}
#define ENABLE_DEBUG

#if defined(ENABLE_DEBUG)

//              DEBUGING MODE
#define PROG_DEBUG			  //debug principal program
//#define HARDWARE_DEBUG
//#define IMU_DEBUG			  //debug IMU
//#define CAL_DEBUG
//#define I2CDEV_SERIAL_DEBUG   //debug I2Cdev
//#define DEBUG_SERIAL_NMEA_1
//#define SCREEN_DEBUG
//#define SCREEN_DEBUG2
//#define GPS_DEBUG
//#define BUTTON_DEBUG
//#define TONEDAC_DEBUG
//#define MS5611_DEBUG
//#define KALMAN_DEBUG
//#define ACCEL_DEBUG
//#define EEPROM_DEBUG
//#define NMEAPARSER_DEBUG
//#define SDCARD_DEBUG
//#define IGC_DEBUG
#define DATA_DEBUG
//#define BT_DEBUG
//#define WIFI_DEBUG
//#define SOUND_DEBUG
//#define AGL_DEBUG
//#define SQL_DEBUG
//#define BEARING_DEBUG
//#define TWOWIRESCH_DEBUG
//#define POWER_DEBUG
//#define MEMORY_DEBUG
{% endhighlight %}


**2. Reduce the speed of the I2C bus:**{: style="color:   #138ca2; opacity: 1;" }

The most common problem is a loss of altitude information. The CJMCU-117 module which integrates the MS5611 barometer communicates with the ESP32 chip with the [I2C](https://en.wikipedia.org/wiki/I%C2%B2C) protocol . You can try to reduce the BUS communication speed from 400Khz to 100Khz.
To do this, change the value `400000UL` to` 100000UL` from line 355 of the file `Arduino\libraries\HardwareConfig\HardwareConfigESP32.h`

{% highlight shell_session %}
/* Set the freq */
#define VARIO_TW_FREQ 400000UL

to

/* Set the freq */
#define VARIO_TW_FREQ 100000UL

{% endhighlight %}

**3. Quality of solders**{: style="color:   #138ca2; opacity: 1;" } 

It often happens that the solders are the cause of the bugs, even if they appear to be correct. Try to redo the solders on the circuit board.

