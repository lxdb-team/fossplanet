---
title: NodeMCU kann keine I2C-Geräte auslesen
date: 2021-05-10T06:34:44.682Z
draft: true
image: /images/post/20210510_083126.jpg
description: Probleme mit I2C-Geräten am NodeMCU? Dieser Artikel sollte helfen.
categories:
  - Arduino
tags: []
type: featured
post: true
---
Bei mir tat sich dieses Problem auf, als ich versucht hatte, einen BME 280 Sensor über den NodeMCU auszulesen. Mögliche Fehlerquellen, wie Verkabelung, Fehlfunktion, oder fehlende Elemente beim Aufbau werden in diesem Artikel nicht berücksichtigt. Wenn Sie ihren Aufbau also schon mindestens zehnmal überprüft haben, dann sollten sie das Folgende lesen.

### Lösungsversuch 1

Manchmal kann es sein, dass man einfach nur eine falsche Adresse angegeben hat. Alles, was hier also von Nöten ist, ist die Adresse im Sketch anzupassen. Der folgende Sketch von der Seite [Funduino](https://www.funduino.de) bietet Ihnen die Möglichkeit, die Adresse des I2C Gerätes auszulesen.

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