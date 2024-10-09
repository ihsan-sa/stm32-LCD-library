# LCD Library for the STM32 NUCLEO-F401RE Board

Header file ("lcd.h") in Src folder.

How to use:
- Download "lcd.h" file.  
- Import header file and add to Src folder in STM32CubeIDE.  
- Configure stm32 pins as GPIO_Output and assign labels accordingly:  

Label        (Port):  

LCD_D0         (PB4)  
LCD_D1         (PB5)  
LCD_D2         (PC0)   
LCD_D3         (PC1)  
LCD_D4         (PB0)  
LCD_D5         (PA4)  
LCD_D6         (PA1)  
LCD_D7         (PA0)  
LCD_RS         (PA9)  
LCD_RW         (PA8)  
LCD_E          (PB10)  
  
  
Commands available are:  
  
lcd_clear()  --> Clears LCD  
lcd_print_chars([string to print], [time between printing each char - 10ms])  --> Prints a string literal  
lcd_init() --> Sets up LCD for basic standard operation: 2 line mode, display, cursor, cursor blink on  
send_lcd_instruction( [8-bit instruction], [RW bit], [RS Bit])   --> Sends specific instruction to LCD. Consult LCD [datasheet]((https://eater.net/datasheets/HD44780.pdf)).  
  
You will need to consult the lcd screen datasheet for more instructions and functionality. For the moment, this library serves to make it easier to send these commands and basic functionality.  
