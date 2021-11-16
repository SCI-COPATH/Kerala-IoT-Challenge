# Kerala IoT Challenge Level-1

## [**Arduino Tutorial Full Course**](https://youtube.com/playlist?list=PLqN-fAjatOhIxiOwHaPqVcskxGkPgwnWW)
## [**Arduino Tutorial Crash Course**](https://youtube.com/playlist?list=PLqN-fAjatOhIiUwQGeQlP8OW84j9I8kjb)

## Experiment 1 - Hello World LED Blinking
### Components
* Arduino Uno
* Breadboard
* LED
* Jumper wire
* Restsor 150 ohm

### Circuit
![Expriment 1](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp1.png)
### Video

### Tutorial 
#### Episode 1

[![Episode 1](https://img.youtube.com/vi/DlvjYghBKKU/0.jpg)](https://youtu.be/DlvjYghBKKU "Episode 1")

#### Episode 2

[![Episode 2](https://img.youtube.com/vi/JMvJE9pLN_Y/0.jpg)](https://youtu.be/JMvJE9pLN_Y "Episode 2")

#### Episode 3

[![Episode 3](https://img.youtube.com/vi/o5wSSsODvZw/0.jpg)](https://youtu.be/o5wSSsODvZw "Episode 3")

#### Episode 4

[![Episode 4](https://img.youtube.com/vi/rbxlbgfqMLk/0.jpg)](https://youtu.be/rbxlbgfqMLk "Episode 4")

### Code
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

