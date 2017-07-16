# Nokia-LCD5110-HAL


This library is used to control Nokia's 5110 LCD on STM32 devices.
It was built on STM's HAL and intends to offer an easy and fast way to use 5110 using HAL's GPIOs.
It's also based on two other 5110 libraries:
  1) Tilen Majerle's  
     @website	http://stm32f4-discovery.com  
 	   @link	http://stm32f4-discovery.com/pcd8544-nokia-33105110-lcd-stm32f429-discovery-library/  
  	 This library was built for STM devices but it doesn't run on HAL.  
  	 Tilen also has a great site about STM32.
 
  2) RinkyDinkElectronics'
  	 @website http://www.RinkyDinkElectronics.com/
  	 This library was built to control 5110 for Arduino.
   
I've studied both libraries and used many things of them. Some functions are exactly the same but there are modified functions too.
  
This library is an unfinished job (but it works!). Some things that might be added in the future:
  1) The rest of the functions of both libraries mentioned above  
  2) Add the possibility to use SPI peripheral
 
 Feel free to use this library and modify it. :D
 
## How to use this library?  
This library was built on HAL for STM32 devices, so HAL is necessary. It's recommended to use it
with STM32CubeMX.
 
Steps to use this library:  
  1) Import this library into your code (!)  
  2) Configure your pins using set function: LCD_setRST(PORT, PIN)  
                   						   					   LCD_setCE(PORT, PIN)  
  						   					                   LCD_setDC(PORT, PIN)  
  						   					                   LCD_setDIN(PORT, PIN)  
  						   					                   LCD_setCLK(PORT, PIN)  
  3) Call LCD_init() to initialize the LCD  
  Now the display is initialized and ready to use.  
 
  Example:  
  4) Call, for example, LCD_print("Hello World", 0, 0) and then call LCD_refreshScr() to update the screen.
 
  Remember: all functions modify a buffer variable in a struct (LCD_att). You must update the screen
  			    using LCD_refreshScr() or LCD_refreshArea() in order to send data to the screen.  

## Motivation
In 2016 I wanted to use a Nokia's 5110 LCD in a project in college but I hadn't found any library which uses HAL. Then I decided to port my own library to HAL. I based my project on two already existent libraries: Tilen Majerle's library for STM32 and RinkyDinkElectronics' library for Arduino. I finished my project and this library stayed here in my computer since then.  
Now I decide to share it because I think this might be useful to someone :D  

--------------------
Author: Caio Rodrigo  
Github: https://github.com/Zeldax64?tab=repositories
--------------------
 
