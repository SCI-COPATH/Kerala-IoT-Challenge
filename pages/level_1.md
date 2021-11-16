# Kerala IoT Challenge Level-1

### [**Arduino Tutorial Full Course**](https://youtube.com/playlist?list=PLqN-fAjatOhIxiOwHaPqVcskxGkPgwnWW)
### [**Arduino Tutorial Crash Course**](https://youtube.com/playlist?list=PLqN-fAjatOhIiUwQGeQlP8OW84j9I8kjb)

### Experiment 1 - Hello World LED Blinking
#### Components
* Arduino Uno
* Breadboard
* LED
* Jumper wire
* Restsor 150 ohm

#### Circuit
![Expriment 1](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp1.png)
#### Video

#### Tutorial 

#### Code
```ino
#define LED 8
void setup(){ 
  pinMode(LED, OUTPUT);
} 
void loop(){
  digitalWrite(LED, HIGH);
  delay(1000);
  digitalWrite(LED, LOW);
  delay(1000);
}
```

