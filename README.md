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
* GPIO16 - General Purpose In-/Output 16
* PIN 1 - första pin

Detta gäller

| GPIO Pin | I/O Index Number |
|----------|:----------------:|
| GPIO0  | 3 |
| GPIO1  | 10 | 
| GPIO2  | 4 |
| GPIO3  | 9 |
| GPIO4  | 2 | 
| GPIO5  | 1 |
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

När det i koden står 

```javascript
const int SDA_PIN = 5;  //GPIO5 (D1) [2:a pinnen]
const int SCL_PIN = 4;
```
eller...
```javascript
#define DHTPIN D3       //GPIO0 (D3) [4:e pinnen]
```

## Skapa konto
Vi läser väderprognoser och -observationer från Weather Underground. 
* Skapa konto på https://www.wunderground.com/
* Gå till Weather API
* Key settings
* Välj Developer ($0) - notera 10 calls/minute
* Purchase Key
* Notera Key ID


## Installera Arduino IDE
* Gå till https://www.arduino.cc/
* ```Download the Arduino IDE``` - Aktuell version är 1.8.5


## Ladda ned exempelkod
* Öppna terminal med Git
* Navigera till Proj-mapp i filsystemet
* Följande skapar ny mapp i Proj med namnet ```WeatherStation```

```git clone https://github.com/johansundstrom/WeatherStation.git```

* Navigera in i den nya mappen ```WeatherStation```
* I den mappen ligger ```Home_Weather_Station_Final```
* Dubbelklicka på ```Home_Weather_Station_Final.ino```






