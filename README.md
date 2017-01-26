# Drotek MPU-9250 AHRS

## Hardware 
 
* [Drotek MPU-9250](https://drotek.com/shop/fr/drotek-parts/421-mpu9250-gyro-accelerometre-magnetometre.html)
* Arduino Nano, UNO or NodeMCU Doit.am ESP-12E 8266 (v1.0) have been tested
 
## Sketches
 
### arduino/MPU9250BasicAHRS

This project is a review of the work done on this [github repo](https://github.com/shubhampaul/Real_Time_Planet_Tracking_System.git).

It will send out via Serial the following information:
```
uint32_t delta;								// Time delta between measurements
float ax;									// Acceleration X
float ay;									// Acceleration Y
float az;									// Acceleration Y
float gx;									// Gyroscope X
float gy;									// Gyroscope Y
float gz;									// Gyroscope Z
float mx;									// Magnetometer X
float my;									// Magnetometer Y
float mz;									// Magnetometer Z
float q[4] = {1.0f, 0.0f, 0.0f, 0.0f};  	// Quaternion
float pitch;								// Pitch
float yaw;									// Yaw
float roll;                                 // Roll
```

Few customizations can be made.
Follow instructions in source code for wiring.

```

MPU9250 Breakout ---- Arduino ---- ESP8266 (E.g. NodeMCU ESP 12-E V1.0)
5V  ----------------- 5V --------- 3.3V
GND ----------------- GND -------- GND
SCL ----------------- A5 --------- D2
SDA ----------------- A4 ----------D1

// Set this to x to enable debug mode
#define DEBUG_MODE(x)  
// Define this to enable AHRS
#define AHRS
// Geomagnetic declination to be checked on https://www.ngdc.noaa.gov/geomag-web/
#define MAGNETIC_DECLINATION 1.5f
// Serial baud rate
#define SERIAL_BAUD_RATE 115200
// Define this to enable support for ESP8266 features
#define USING_ESP8266
// Define this to enable UDP
#define USING_UDP
// Define this to set the UDP PORT
#define UDP_PORT 9999
// Minimum width of float string conversion
#define WIDTH 3
// Decimal places rounding for float conversion to text
#define DECIMAL_PLACES 3

```

### arduino/I2CScanner

Useful Arduino sketch to verify if I2C devices are found and their addresses.

## Useful links

* https://github.com/arduino-libraries/MadgwickAHRS
* https://developer.mbed.org/users/onehorse/code/MPU9250AHRS_nRF52832/file/8d11bfc7cac0/MPU9250.h
* https://github.com/Frogofmagic/MPU9250.git
* https://github.com/kriswiner/MPU-9250.git
* https://github.com/shubhampaul/Real_Time_Planet_Tracking_System.git 
* https://github.com/Snowda/MPU9250
* https://www.hackster.io/paulplusx/using-the-mpu9250-to-get-real-time-motion-data-08f011
 

 
