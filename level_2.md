# Kerala IoT Challenge Level-2

> As **ESP32 Boards** were not available (As of now), I opt for **NodeMCU-ESP8266** for conducting the experiments. Even though both boards differ a lot in features & capabilities, **NodeMCU-ESP8266** could serve my purpose for the present scenario.

### Experiment 1 - Hello World LED Program Using Blynk App  

![Hello World LED Blinking](https://user-images.githubusercontent.com/44474792/138228740-3d4a3a49-e353-4b59-9eec-edc6223c8788.jpg)
#### Code
```ino
#define BLYNK_TEMPLATE_ID "---------"
#define BLYNK_DEVICE_NAME "---------"

#define BLYNK_FIRMWARE_VERSION        "0.1.0"
#define BLYNK_PRINT Serial
#define APP_DEBUG

#include "BlynkEdgent.h"

BLYNK_WRITE(V0) {
  int pinValue = param.asInt();
  digitalWrite(15, pinValue);
}

void setup()
{
  pinMode(15, OUTPUT);
  Serial.begin(115200);
  delay(100);

  BlynkEdgent.begin();
}

void loop() {
  BlynkEdgent.run();
}
```

### Experiment 2 - IoT Remote Light Meter using Arduino IoT Cloud
### Experiment 3 - Soil Moisture Meter
### Experiment 4 - Ultrasonic Sensor
### Experiment 5 - Object Detection using IR Sensor
