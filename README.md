# Drotek MPU-9250 AHRS

## Hardware 
 
* [Drotek MPU-9250](https://drotek.com/shop/fr/drotek-parts/421-mpu9250-gyro-accelerometre-magnetometre.html)
 
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

// MPU9250 Breakout -------- Arduino
// 5V  --------------------- 5V
// GND --------------------- GND
// SCL --------------------- A5
// SDA --------------------- A4

// Set this to x to enable debug mode
#define DEBUG_MODE(x)  
// Define this to enable ASCII output via Serial
#define ASCII_MODE
// Define this to enable BIN output via Serial
//#define BIN_MODE
// Define this to enable AHRS
#define AHRS
// Geomagnetic declination to be checked on https://www.ngdc.noaa.gov/geomag-web/
#define MAGNETIC_DECLINATION 1.5f
// Serial baud rate
#define SERIAL_BAUD_RATE 115200
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
 

 
