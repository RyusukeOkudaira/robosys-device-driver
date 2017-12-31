# robosys-device-driver
LED Device Driver for Raspberry Pi3

# Demo
[device driver for LED demo](https://www.youtube.com/watch?v=cTbsFoFUWIg)

# Requirements

- RaspberryPi 3
  - Raspbian
- Linux kernel source
  - douwnload kernel source into /usr/src/linux
  - kernel build scripts : https://github.com/ryuichiueda/raspberry_pi_kernel_build_scripts
- LED

# Installation
- douwnload repository
 ```
 git clone https://github.com/RyusukeOkudaira/robosys-device-driver.git
 ```
- compile and loading kernel module
 ```
 cd robosys-device-driver
 make
 sudo insmod led.ko
 sudo chmod 666 /dev/myled0/
 ```
# Usage
- Turn off all Led
```
echo 0 > /dev/myled0
```
- Light Led 1
```
echo 1 > /dev/myled0
```
- Light Led 2
```
echo 2 > /dev/myled0
```
- Lignt Led 3
```
echo 3 > /dev/myled0
```
- Light All Led
```
echo 4 > /dev/myled0
```
