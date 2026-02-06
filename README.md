# Transparent Van Gogh clock

## HARDWARE STUFF
* **brain:** esp32 (coz of the built-in wifi)
* **screen:** 1.51" transparent oled (ssd1309 driver)
* **button:** just one tactile switch on the side for on/off

## THE SLAP OF MY ART ON IT

i am an a professional artist (so yeah, i obv know a very lil about hardware) and i am sick of boring clean "black and white" non sense minimalism fr. so i am gonna paint Van gogh's "starry night" all over the clock (because i love that painting man), i could have bought a clock and done that on it but nah man wheres the kick that. 

## HOW IMMA MAKE IT WORK

### 1. syncin the time
since i used an esp32, i dont have to manually set the time like a boomer. when u flip the switch, it connects to my wifi and talks to an **ntp server**. it gets the exact time in unix format and then i use some logic to convert it to my local timezone. 

### 2. vertical oled logic
the display is usualy horizontal but i wanted it vertical to look cooler on a desk. i will used the `u8g2` library to rotate the buffer by 90 degrees. because the screen is transparent, there is no "black" color, the pixels are either glowing or they are see through. imma choose chose a clean, bold font so the time looks like it's floating in the air, atleast thats what i'll try to do.

### 3. the one button
i didnt want a bunch of menus or setings. there is literaly just one physical button. it works as a hard power toggle. if you want the time, you turn it on. if you want it off, you click it thats cuz i want that artwork to be the hero (or lets say i know i will mess it up if i tried anything sophisticated).
