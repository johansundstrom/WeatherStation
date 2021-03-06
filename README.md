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
Allt handlar om att benämna pinnarna logiskt, fysiskt eller kronologiskt

Detta gäller...

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


## Installera Arduino IDE
* Gå till <a href="https://www.arduino.cc/">
* ```Download the Arduino IDE``` - Aktuell version är 1.8.5


## Skapa konto
Vi läser väderprognoser och -observationer från Weather Underground. 
* Skapa konto på https://www.wunderground.com/
* Gå till Weather API
* Key settings
* Välj Developer ($0) - notera 10 calls/minute
* Purchase Key
* Notera Key ID


## Ladda ned exempelkod
* Öppna terminal med Git
* Navigera till Proj-mapp i filsystemet
* Följande skapar ny mapp i Proj med namnet ```WeatherStation```

```git clone https://github.com/johansundstrom/WeatherStation.git```

* Navigera in i den nya mappen ```WeatherStation```
* I den mappen ligger ```Home_Weather_Station_Final```


## Redigera exempelkoden
Titta in i följande filer i denna ordning:
1. ```stationDefines.h```
2. ```stationCredentials.h```
3. ```WeatherStationImages.h```
4. ```WeatherStationFonts.h```
5. ```Home_Weather_Station_Final.ino```

### Redigera 
* ```stationCredentials.h``` - uppdatera följande...
1. WIFI_SSID
2. WIFI_PWD
3. API_KEY
4. LANGUAGE
5. COUNTRY
6. CITY

### Läs ut
* ```stationDefines.h``` - Vilken pinne antas DHT22 vara ansluten till?
* ```Home_Weather_Station_Final.ino``` - Vilka pinnar antas OLED vara kopplad till?

### Koppla
* Anslut enligt schema
* Gå igenom anslutningarna igen (blir det fel finns risken att det kan det gå sönder)
* Anslut USB-kabeln
* Se till att datorn hittar porten (COMMx)
* I Boardmanager, kontrollera att denna rad är med ```http://arduino.esp8266.com/versions/2.3.0/package_esp8266com_index.json```
* I Arduino, kontrollera 1) rätt board 2) 115200baud 3) 80MHz 4) Rätt COMMx
* Kompilera, länka och ladda ned programmet på NodeMCU



