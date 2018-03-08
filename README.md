# ESP8266_DHT_AIO
ESP8266 core project reading temp and humidity from DHT11 and posting to AdafruitIO<br><br>
Todo, prioritized<br>
Implement filtering - Done<br>
Get plug value at boot<br>
Hue integration<br>
Temperature 'calibration' from cloud<br>
OTA update<br>
Investigate reboots happening ~15 minutes<br>
Connect to multiple networks<br>
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

<b>put request, not tested</b><br>
HTTPClient http;<br>
  http.begin("https://pushalot.com/api/sendmessage");<br>
  http.addHeader("Content-Type", "application/json");<br>
  String postMessage = String("{'AuthorizationToken' : 'yourapistring here', 'Title' : 'Test', 'Body' : 'Test'}");<br>
  int httpCode = http.PUT(postMessage);<br>
  Serial.print("http result:");<br>
  Serial.println(httpCode);<br>
  http.writeToStream(&Serial);<br>
  http.end();<br>
<br><br>
Maybe exit quotes instead of single quotes?<br>
client.println("{\"on\":false}");
