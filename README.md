# ssd1306-i2c-opi

Simple library for 128x64. Works fine with SH1106 1.3" OLED and OLED 12864 Orange Pi board. You just need to activate I2C interface by going armbian-config, then activate System, toogle Hardware. 

Connect the display board as wiring bellow and install the i2c toold with command sudo apt-get install i2c-tools

![oled12864](https://user-images.githubusercontent.com/5319910/142386739-ab7a71be-d3cb-4f05-b6d2-3daf197fcd00.jpg)

Then check the board with "i2cdetect -l" you will see board as i2c-1 or i2c-0. Test with "sudo i2cdetect -y 0" (or 1). If your display has 3d address instead 3c, change OLED_I2C_ADDR parameter it in the oled.h. 

![image](https://user-images.githubusercontent.com/5319910/142387020-eef8d5f0-6ca3-476b-8079-e41631011360.png)


Enter "make" to compile and run demo with "sudo ./oled_demo /dev/i2c-0".

This library was written by Sonal Pinto for Arduino and ported to Linux by Vladimir Komendantskiy. Borombo in Arambian forum just wrote functions for text drawing and add three little fonts. This library only can  draw text at X Y with specified font and draw custom pixel, but it is easy to write line, circle, rectangle drawing functions.

I just upload here to share for everyone can use it and developpment
