# Nokia-LCD5110-HAL


This library is used to control Nokia's 5110 LCD on STM32 devices.
It was built on STM's HAL and intends to offer an easy and fast way to use 5110 using HAL's GPIOs.
It's based on two other 5110 libraries:
  1) Tilen Majerle's  
     @website	http://stm32f4-discovery.com  
 	   @link	http://stm32f4-discovery.com/pcd8544-nokia-33105110-lcd-stm32f429-discovery-library/  
  	 This library was built for STM devices but it doesn't run on HAL.  
  	 Tilen also has a great site about STM32.
 
  2) RinkyDinkElectronics'
  	 @website http://www.RinkyDinkElectronics.com/
  	 This library was built to control 5110 for Arduino.  
     
And it's also based on this [tutorial](https://www.youtube.com/watch?v=RAlZ1DHw03g) which is a great starting point to learn the basics about the display.
   
I've read both libraries and used many things of them. Some functions are exactly the same but there are modified functions too. Feel free to use this library and modify it. :D
 
## How to use this library?  
This library was built to use with STM32 HAL for STM32 devices. It's recommended to use it with STM32CubeMX.
 
Steps to use this library:  
  1) Configure the desired pins you want to use with the LCD as GPIOs on STM32CubeMX.
  
  2) Import this library into your generated project.
  
  2) Configure your pins using the library set functions:  
  LCD_setRST(PORT, PIN)  
  LCD_setCE(PORT, PIN)  
  LCD_setDC(PORT, PIN)  
  LCD_setDIN(PORT, PIN)  
  LCD_setCLK(PORT, PIN)  
  
  3) Call LCD_init() to initialize the LCD  
  Now the display is initialized and ready to use.  
 
  Example:  
  4) Call: LCD_print("Hello World", 0, 0).

--------------------
Author: Caio Rodrigo  
Github: https://github.com/Zeldax64?tab=repositories

 
