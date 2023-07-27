Hello.
In this code, without a radio controller, we want to calibrate the speed controller with stm32f103c8t6. For this, the 30 A speed controller data sheet (yellow color) which is attached in this file is used.

I have used keil and cubemx.

To use this code, just setup Timer 3 and then replace the main.c file with your own main.c file(copy and paste codes).in this program, micros is also used, so you just need to put micros.h file in the core/inc folder.

timer frequency=60 HZ
ARR=37500
PSC=31

Maximum pulse width =2ms= 4495 of 37500
minimum pulse width =1ms= 2255 of 37500

*In this program, I have used the stm32cubemonitor as a key to control the remote controller and go from one step to the next. If you don't have access to stm32cubemonitor, you can use real push buttons. (to control permit1 ,permit2)

*In this code, channel 1 timer 3 is used. So connect the signal wire of the speed controller to this channel.
