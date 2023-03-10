<h1 align="center">Hi 👋, Ich bin Antonio</h1>
<h3 align="center">"Vereinfachen Sie Ihre Smart Home-Automatisierung mit Home-Assistant und ESPHome"</h3>

<p align="left"> <img src="https://komarev.com/ghpvc/?username=antonio-030&label=Profile%20views&color=0e75b6&style=flat" alt="temperatursensor" /> </p>

- 📫 So erreichen Sie mich ctoni030@proton.me


<h3 align="left">Sprachen and Tools:</h3>
<p align="left">  <a href="https://www.arduino.cc/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/arduino-1.svg" alt="arduino" width="40" height="40"/> </a> <a href="https://www.w3schools.com/cpp/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" alt="cplusplus" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a> <a href="https://dart.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/dartlang/dartlang-icon.svg" alt="dart" width="40" height="40"/> </a> <a href="https://www.djangoproject.com/" target="_blank" rel="noreferrer"> <img src="https://cdn.worldvectorlogo.com/logos/django.svg" alt="django" width="40" height="40"/> </a> <a href="https://www.docker.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original-wordmark.svg" alt="docker" width="40" height="40"/> </a> <a href="https://flutter.dev" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/flutterio/flutterio-icon.svg" alt="flutter" width="40" height="40"/> </a> <a href="https://grafana.com" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/grafana/grafana-icon.svg" alt="grafana" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://www.linux.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/linux/linux-original.svg" alt="linux" width="40" height="40"/> </a> <a href="https://mariadb.org/" target="_blank" rel="noreferrer"> <img src="https://www.vectorlogo.zone/logos/mariadb/mariadb-icon.svg" alt="mariadb" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://www.nginx.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nginx/nginx-original.svg" alt="nginx" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://www.photoshop.com/en" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/photoshop/photoshop-line.svg" alt="photoshop" width="40" height="40"/> </a> <a href="https://www.php.net" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg" alt="php" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://redis.io" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redis/redis-original-wordmark.svg" alt="redis" width="40" height="40"/> </a> </p>

# temperatursensor
Um einen Temperatursensor mit ESPHome zu bauen,
benötigen Sie einen Wemos-d1-mini-esp8266 Mikrocontroller und einen BMP180 Temperatursensor.
Hier sind die Schritte, um einen Temperatursensor zu bauen:

1. Besorgen Sie sich einen ESP8266 Mikrocontroller sowie einen kompatiblen Temperatursensor. Ein gängiger Temperatursensor ist der BMP180.

![wemos-d1-mini-esp8266-4041305302](https://user-images.githubusercontent.com/99229976/212190994-6b7ca951-23d7-43ba-93cf-5314f3266812.jpg)

![GY-68_BMP180_130x](https://user-images.githubusercontent.com/99229976/212204934-e10046c8-d9d1-48da-9759-44fa759ab3a5.jpg)

2. Verbinden Sie den Temperatursensor mit dem Mikrocontroller. Der BMP180 hat vier Pins: VIN, GND, SCL, SDA. Verbinden Sie `VIN mit 3,3V`, `GND mit GND`,` SCL mit D1`, `SDA mit D2` digtallen Pin des Mikrocontroller.

![mit baterry-Steckplatine](https://user-images.githubusercontent.com/99229976/212208127-2150147d-a407-48f9-8c90-6280cf008982.jpg)

3. Installieren Sie [ESPHome](https://esphome.io/guides/getting_started_hassio.html) in Home-Assistant und fügen sie denn Code am Ende Ihrer YAML-Konfigurationsdateien hinzu.  

ESPHome ist eine Open-Source-Software, die es ermöglicht, ESP8266 und ESP32-basierte Geräte in Home-Assistant einzubinden. ESPHome bietet eine einfache Methode, um die Firmware auf diesen Geräten zu erstellen und zu konfigurieren und ermöglicht die Verwendung von YAML-Konfigurationsdateien, um die Einrichtung von Sensoren, Aktoren und automatischen Regeln zu vereinfachen. Mit ESPHome können Sie auch die MQTT-Protokoll, das OTA-Firmware-Update und die Integration von Home-Assistant integrieren.

```yaml
captive_portal:

deep_sleep:
  run_duration: 20s
  sleep_duration: 900s
 
i2c: 
  sda: GPIO4
  scl: GPIO5
  scan: true
  
sensor:
  - platform: bmp085
    temperature:
      name: "Wohnzimmer Temperature"
    pressure:
      name: "Wohnzimmer Luftdruck"
    update_interval: 5s
    
  - platform: adc
    pin: VCC
    id: "VCC"
    internal: true
    
  - platform: template
    name: "Wohnzimmer.Temperatur.battery_level"
    unit_of_measurement: '%'
    update_interval: 60s
    lambda: |-
      return ((id(VCC).state /3.30) * 100.00);    
```

``Der deep_sleep Abschnitt legt fest, dass das System 20 Sekunden laufen und dann 900 Sekunden schlafen soll.
  In dieser Zeit ist der ESP8266 nicht erreichbar.
  Um die Dauer des Tests zu erhöhen, kann die Variable "run_duration" in dem Code entsprechend angepasst werden. Sie können den Wert erhöhen, um die Dauer des Tests zu verlängern. 
``

Der i2c Abschnitt legt fest, dass der SDA-Pin an GPIO4, der SCL-Pin an GPIO5 angeschlossen ist und das Scannen auf "true" eingestellt ist.
Der Sensorbereich listet drei Sensoren auf: ein BMP085-Sensor (für Temperatur und Druck), ein ADC-Sensor (zur Messung des VCC-Pins) und ein Template-Sensor (zur Messung des Batteriestands).
Der BMP085-Sensor wird alle 5 Sekunden aktualisiert, Der Template-Sensor alle 60 Sekunden und der template Sensor nutzt eine Lambda-Funktion um den Batteriestand zu berechnen.

Mehr zur deep_sleep Funktion [hier](https://esphome.io/components/deep_sleep.html?highlight=deep).

![Screenshot 2023-01-13 004124](https://user-images.githubusercontent.com/99229976/212258143-8122eda8-6d64-4575-aa72-6a05cb7eb025.jpg)

![Screenshot 2023-01-13 080232](https://user-images.githubusercontent.com/99229976/212258434-5940bebe-32f4-414f-b3ff-32b37791ab52.jpg)

[Home-Assistant](https://www.home-assistant.io/) ist eine Open-Source-Software, die als smart home-Hub verwendet wird. Es ermöglicht die Steuerung und Automatisierung von Geräten und Diensten in einem intelligenten Zuhause. Es unterstützt eine Vielzahl von Protokollen und Plattformen, einschließlich Zigbee, Z-Wave, Philips Hue, Nest und vielen mehr. Es kann auf einem Raspberry Pi oder einem anderen Computer ausgeführt werden und ermöglicht die Erstellung von Szenen, die die Steuerung von Geräten und Diensten nach Zeitplänen oder Ereignissen automatisieren.

![homeasstendjpg](https://user-images.githubusercontent.com/99229976/212205370-af1be8b6-884e-40aa-9f20-8709b1283d2d.jpg)


6. Überprüfen Sie, ob der Temperatursensor erfolgreich eingerichtet wurde. Sie sollten in der Lage sein, die gemessenen Temperaturen in der ESPHome-logs oder über eine integrierte Home-Automatisierungsplattform wie Home Assistant zu sehen.

![temperatur](https://user-images.githubusercontent.com/99229976/212207816-f2074677-9ffb-4ebf-8108-10bfa9c7bea8.jpg)

Beachten Sie, dass es je nach verwendetem Sensor und Mikrocontroller leichte Unterschiede in den Schritten geben kann. Stellen Sie sicher, dass Sie die Dokumentation und Datenblätter des verwendeten Sensors und Mikrocontroller sorgfältig lesen, bevor Sie mit dem Aufbau beginnen.
