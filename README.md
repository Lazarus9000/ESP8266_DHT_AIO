# ESP8266_DHT_AIO
ESP8266 core project reading temp and humidity from DHT11 and posting to AdafruitIO<br><br>
Todo, prioritized<br>

 * ~~Implement filtering~~
 * ~~Hue integration~~
   * ~~Get plug value at boot~~
 * Temperature 'calibration' from cloud
 * OTA update
 * Select filter from cloud (raw, mean or median, reduce amount of feeds needed)
 * Investigate reboots happening ~15 minutes
 * Connect to multiple networks

<br>
<br>
<b>For removing 'particle' from oaks</b><br>Not sure if this step is entirely necessary?<br><br>

C:\Python27\Scripts>esptool.exe --port COM3 --baud 115200 erase_flash<br>
esptool.py v2.3.1<br>
Connecting........_____....._____....._____....._____....._____....._____....._____....._____....._____...<br>
Detecting chip type... ESP8266<br>
Chip is ESP8266EX<br>
Features: WiFi<br>
Uploading stub...<br>
Running stub...<br>
Stub running...<br>
Erasing flash (this may take a while)...<br>
Chip erase completed successfully in 8.5s<br>
Hard resetting via RTS pin...<br>
