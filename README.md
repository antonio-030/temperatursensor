# temperatursensor
Um einen Temperatursensor mit ESPHome zu bauen,
benötigen Sie einen Wemos-d1-mini-esp8266 Mikrocontroller und einen BMP180 Temperatursensor.
Hier sind die Schritte, um einen Temperatursensor zu bauen:

1. Besorgen Sie sich einen ESP8266 Mikrocontroller sowie einen kompatiblen Temperatursensor. Ein gängiger Temperatursensor ist der BMP180.

![wemos-d1-mini-esp8266-4041305302](https://user-images.githubusercontent.com/99229976/212190994-6b7ca951-23d7-43ba-93cf-5314f3266812.jpg)

![GY-68_BMP180_130x](https://user-images.githubusercontent.com/99229976/212204934-e10046c8-d9d1-48da-9759-44fa759ab3a5.jpg)

2. Verbinden Sie den Temperatursensor mit dem Mikrocontroller. Der BMP180 hat vier Pins: VIN, GND, SCL, SDA. Verbinden Sie VIN mit 3,3V, GND mit GND, SCL mit D1, SDA mit D2 digtallen Pin des Mikrocontroller.

![mit baterry-Steckplatine](https://user-images.githubusercontent.com/99229976/212208127-2150147d-a407-48f9-8c90-6280cf008982.jpg)

3. Installieren Sie ESPHome auf https://www.home-assistant.io/. ESPHome ist eine Open-Source-Firmware, die es ermöglicht, ESP8266- und ESP32-Mikrocontroller als Smart-Home-Geräte einzurichten.

![Screenshot 2023-01-13 004124](https://user-images.githubusercontent.com/99229976/212204420-26be2957-c39e-4a89-ba95-e7c3fa886c61.jpg)

Home-Assistant ist eine Open-Source-Software, die als smart home-Hub verwendet wird. Es ermöglicht die Steuerung und Automatisierung von Geräten und Diensten in einem intelligenten Zuhause. Es unterstützt eine Vielzahl von Protokollen und Plattformen, einschließlich Zigbee, Z-Wave, Philips Hue, Nest und vielen mehr. Es kann auf einem Raspberry Pi oder einem anderen Computer ausgeführt werden und ermöglicht die Erstellung von Szenen, die die Steuerung von Geräten und Diensten nach Zeitplänen oder Ereignissen automatisieren.

![homeasstendjpg](https://user-images.githubusercontent.com/99229976/212205370-af1be8b6-884e-40aa-9f20-8709b1283d2d.jpg)

![energy](https://user-images.githubusercontent.com/99229976/212205525-bb45ed86-fe0d-48b6-a44f-693175bbce19.jpg)

![3d](https://user-images.githubusercontent.com/99229976/212207432-fa5be4e5-329c-4aa2-9ddf-2403cace3e53.jpg)

4. Erstellen Sie eine YAML-Datei für Ihren Temperatursensor. In dieser Datei konfigurieren Sie den Mikrocontroller und den Temperatursensor. Sie müssen beispielsweise den Pin angeben, an dem der Sensor angeschlossen ist, und welches Protokoll verwendet wird.

5. Übertragen Sie die YAML-Datei auf den Mikrocontroller. Sie können dies über die ESPHome-Weboberfläche oder die ESPHome-Kommandozeile tun.      

6. Überprüfen Sie, ob der Temperatursensor erfolgreich eingerichtet wurde. Sie sollten in der Lage sein, die gemessenen Temperaturen in der ESPHome-Weboberfläche oder über eine integrierte Home-Automatisierungsplattform wie Home Assistant zu sehen.

![temperatur](https://user-images.githubusercontent.com/99229976/212207816-f2074677-9ffb-4ebf-8108-10bfa9c7bea8.jpg)

Beachten Sie, dass es je nach verwendetem Sensor und Mikrocontroller leichte Unterschiede in den Schritten geben kann. Stellen Sie sicher, dass Sie die Dokumentation und Datenblätter des verwendeten Sensors und Mikrocontroller sorgfältig lesen, bevor Sie mit dem Aufbau beginnen.
