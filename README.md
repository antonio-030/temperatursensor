# temperatursensor
Um einen Temperatursensor mit ESPHome zu bauen,
benötigen Sie einen Wemos-d1-mini-esp8266 Mikrocontroller und einen BMP180 Temperatursensor.
Hier sind die Schritte, um einen Temperatursensor zu bauen:

1. Besorgen Sie sich einen ESP8266 Mikrocontroller sowie einen kompatiblen Temperatursensor. Ein gängiger Temperatursensor ist der BMP180.

![wemos-d1-mini-esp8266-4041305302](https://user-images.githubusercontent.com/99229976/212190994-6b7ca951-23d7-43ba-93cf-5314f3266812.jpg)

![OKY3062-1_BMP180_SENSOR_8_1099x1099-59105308](https://user-images.githubusercontent.com/99229976/212192921-f0c39856-0977-47b8-867e-569d9e907eec.jpg)

2. Verbinden Sie den Temperatursensor mit dem Mikrocontroller. Der BMP180 hat vier Pins: VIN, GND, SCL, SDA. Verbinden Sie VIN mit 3,3V, GND mit GND, SCL mit D1, SDA mit D2 digtallen Pin des Mikrocontroller.

![Untitled Sketch_Steckplatine](https://user-images.githubusercontent.com/99229976/212202038-242aec20-f547-4523-b372-ff4c3838d483.jpg)

3. Installieren Sie ESPHome auf Ihrem Computer. ESPHome ist eine Open-Source-Firmware, die es ermöglicht, ESP8266- und ESP32-Mikrocontroller als Smart-Home-Geräte einzurichten.

4. Erstellen Sie eine YAML-Datei für Ihren Temperatursensor. In dieser Datei konfigurieren Sie den Mikrocontroller und den Temperatursensor. Sie müssen beispielsweise den Pin angeben, an dem der Sensor angeschlossen ist, und welches Protokoll verwendet wird.

5. Übertragen Sie die YAML-Datei auf den Mikrocontroller. Sie können dies über die ESPHome-Weboberfläche oder die ESPHome-Kommandozeile tun.      

6. Überprüfen Sie, ob der Temperatursensor erfolgreich eingerichtet wurde. Sie sollten in der Lage sein, die gemessenen Temperaturen in der ESPHome-Weboberfläche oder über eine integrierte Home-Automatisierungsplattform wie Home Assistant zu sehen.

Beachten Sie, dass es je nach verwendetem Sensor und Mikrocontroller leichte Unterschiede in den Schritten geben kann. Stellen Sie sicher, dass Sie die Dokumentation und Datenblätter des verwendeten Sensors und Mikrocontroller sorgfältig lesen, bevor Sie mit dem Aufbau beginnen.
