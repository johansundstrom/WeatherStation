# WeatherStation
Väderstation

## Delarna
* NodeMCU (ESP-12E) - https://nodemcu.readthedocs.io/en/master/
* DHT22 (AM2302) - http://akizukidenshi.com/download/ds/aosong/AM2302.pdf
* OLED (SSD1306 display) - https://cdn-shop.adafruit.com/datasheets/SSD1306.pdf

## NodeMCU pinout
<img src="https://pradeepsinghblog.files.wordpress.com/2016/04/nodemcu_pins.png">

Observera att en pinne, exempelvis översta till höger, kan ha flera benämningar.
* D0 - säger kortet
* GPIO16 - är dess General Purpose In/Output 16
* PIN 1 - första pin
Detta gäller

| GPIO Pin | I/O Index Number |
|----------|------------------|
| GPIO0    | 3                |
| GPIO1    | 10               | 
| GPIO2    | 4                |
| GPIO3    | 9                |
| GPIO4    | 2                | 
| GPIO5    | 1                |
| GPIO6 | N/A |
| GPIO7 | N/A | 
| GPIO8 | N/A |
| GPIO9 | 11 |
| GPIO10 | 12 |
| GPIO11 | N/A |
| GPIO12 | 6 |
| GPIO13 | 7 |
| GPIO14 | 5 |
| GPIO15 | 8 |
| GPIO16 | 0 |