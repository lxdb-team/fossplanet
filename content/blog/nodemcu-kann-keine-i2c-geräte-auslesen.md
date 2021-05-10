---
title: NodeMCU kann keine I2C-Geräte auslesen
date: 2021-05-10T13:55:34.843Z
draft: true
image: /images/post/20210510_083126.jpg
images:
  - /images/post/20210510_083126.jpg
description: Probleme mit I2C-Geräten am NodeMCU? Dieser Artikel sollte helfen.
categories:
  - Arduino
tags: []
type: featured
post: true
---
Bei mir tat sich dieses Problem auf, als ich versucht hatte, einen BME 280 Sensor über den NodeMCU auszulesen. Mögliche Fehlerquellen, wie Verkabelung, Fehlfunktion, oder fehlende Elemente beim Aufbau werden in diesem Artikel nicht berücksichtigt. Wenn Sie ihren Aufbau also schon mindestens zehnmal überprüft haben, dann sollten sie das Folgende lesen.

### Lösungsversuch 1

Manchmal kann es sein, dass man einfach nur eine falsche Adresse angegeben hat. Alles, was hier also vonnöten ist, ist die Adresse im Sketch anzupassen. Der folgende Sketch von der Seite [Funduino](https://www.funduino.de) bietet Ihnen die Möglichkeit, die Adresse des I2C Gerätes auszulesen.

```cpp
// I2C Scanner
// Written by Nick Gammon
// Date: 20th April 2011
#include <Wire.h>
void setup() {
Serial.begin (115200);
// Leonardo: wait for serial port to connect
while (!Serial)
{
}
Serial.println ();
Serial.println ("I2C scanner. Scanning ...");
byte count = 0;
Wire.begin();
for (byte i = 8; i < 120; i++)
{
Wire.beginTransmission (i);
if (Wire.endTransmission () == 0)
{
Serial.print ("Found address: ");
Serial.print (i, DEC);
Serial.print (" (0x");
Serial.print (i, HEX);
Serial.println (")");
count++;
delay (1); // maybe unneeded?
} // end of good response
} // end of for loop
Serial.println ("Done.");
Serial.print ("Found ");
Serial.print (count, DEC);
Serial.println (" device(s).");
} // end of setup
void loop() {}
```

Wenn sie die Adresse ausgelesen haben, dann sollte der serielle Monitor etwa so aussehen:

![](/images/post/serieller-monitor.png)

Die Adresse des BME 280 ist also 0x76. Diese Adresse kann auch unterschiedlich sein, da man sie am Sensor selbst einstellen kann. Wie und wo das geht finden sie auf ["Last Minute Engineers"](https://lastminuteengineers.com/bme280-arduino-tutorial/).

#### In der Bibliothek

Für den BME 280 benutze ich die Adafruit BME 280 Library, bei der in diesem Fall das Problem liegt. Wenn man nämlich wie ich einen BME 280 hat, bei dem die Adresse 0x76 ist, dann wird eine Zeile der Bibliothek zum Problem. In dem Arduino-Ordner unter `libraries/Adafruit_BME280_Library` sollte die Datei `Adafruit_BME280.h` liegen. Wie auf dem Bild unten zu sehen, ist dort eine Zeile (33), in der normalerweise `#define BME280_ADDRESS (0x77)` steht. Darunter wird die alternative Adresse angegeben (Zeile 37).

![](/images/post/adressen.png)

Wenn Sie nun die Adresse (Zeile 33) durch die Adresse Ihres Sensors ersetzen, dann sollte das Problem behoben sein. Da ich einen BME 280 mit der Adresse 0x76 besitze, habe ich die Werte einfach nur vertauscht. Ab dort gab es für mich keine Probleme mehr.

Wenn es bei Ihnen funktioniert hat, Sie weitere Fragen, oder Probleme haben, dann lassen Sie es uns in den Kommentaren, oder über andere Kommunikationskanäle wissen.