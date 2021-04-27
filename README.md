# ESP32_MQ135_Gas_Measurement

This project is my personal development is derived from general base programming system using arduino framework

Project:
Concerning Corona virus we found out that fresh air exchange inside our rooms is to be improved.  

Breaf description of system and dependancies:

- Visual Studio Code with PlatformIO is used as developing environment on WIN10

- official libraries are linked to project path <project>\.pio\libdeps\esp32dev.
  Most they are included in PIO library fetch, that insert then in platformio.ini as "lib_deps = ..."
  A few are added manual. 

- Additional libraries are part of the game. They are stored outside project in projets path as a project 
  parallel to all other projects. They are organized as own public repositories in path \md_lib.
  This is to be implemented in platformio.ini as lib_extra_dirs = .\..\md_lib  
  - library md_utils is collection of my home made tools for several purposes  
  - the other libraries of md_lib are easy to use interfaces/drivers for standard libraries

- The system is designed to use is with various hardware, that mainly is to be configured. 
  This is done using the configuration files "prj_config.h" in src directory 

Used HW - out of Arduino model kit:

- ESP32_D1_R32 (Arduino Uno shape) 
- OLED display 1.3", 128x64 ( I2C ), Chip 1106 (1306 also tested)
- Gas sensor MQ135 breakout ( I2C )
- Passive Buzzer breakout ( 1x IOout )  
- Traffic light ( 3x IOout )
- potentimeter 20kOhm, to be replace by resistor (to be calibrated)
