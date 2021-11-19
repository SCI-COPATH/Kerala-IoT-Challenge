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
![Expriment ](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp1.gif)
### Tutorial 
#### Introduction

[![Episode 1](https://img.youtube.com/vi/DlvjYghBKKU/0.jpg)](https://youtu.be/DlvjYghBKKU "Episode 1")

#### Arduino pinout

[![Episode 2](https://img.youtube.com/vi/JMvJE9pLN_Y/0.jpg)](https://youtu.be/JMvJE9pLN_Y "Episode 2")

#### Arduino Frist Program

[![Episode 3](https://img.youtube.com/vi/o5wSSsODvZw/0.jpg)](https://youtu.be/o5wSSsODvZw "Episode 3")

#### Breadboard

[![Episode 6](https://img.youtube.com/vi/GZQtvCtWEbI/0.jpg)](https://youtu.be/GZQtvCtWEbI "Episode 4")

#### Led blink

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


## Experiment 2 - Traffic Light
### Components
* Arduino Uno
* Breadboard
* LED RED BLUE GREEN
* Jumper wire
* Restsor 220 ohm

### Circuit
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp2.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp2.gif)
### Tutorial 
#### Variable

[![Episode 5](https://img.youtube.com/vi/VrcApmzJzVY/0.jpg)](https://youtu.be/VrcApmzJzVY "Episode 5")

####  For Loop

[![Episode 7](https://img.youtube.com/vi/fqL6mSHM1jg/0.jpg)](https://youtu.be/fqL6mSHM1jg "Episode 5")

####  While Loop

[![While loop](https://img.youtube.com/vi/j-JVj-6yPUo/0.jpg)](https://youtu.be/j-JVj-6yPUo)

### Code
```ino
#define RED 7
#define YELLOW 6
#define GREEN 5
void setup(){ 
  pinMode(RED, OUTPUT);
  pinMode(YELLOW, OUTPUT);
  pinMode(GREEN, OUTPUT);
} 
void loop(){
  //Red led on , green led off and wait 5 secound then Red led OFF
  digitalWrite(RED, HIGH);  
  digitalWrite(GREEN, LOW);
  delay(5000);
  digitalWrite(RED, LOW);
  // yellow led blink 3 time in 0.5 sec
  for(int i=0;i<3;i++){ 
    digitalWrite(YELLOW,HIGH);
    delay(500);
    digitalWrite(YELLOW,LOW);
    delay(500);
  }
  //Green led on , Red led off and wait 5 secound then Green LED OFF
  digitalWrite(GREEN, HIGH);  
  digitalWrite(RED, LOW);
  delay(5000);
  digitalWrite(GREEN, LOW);
  // yellow led blink 3 time in 0.5 sec
  for(int i=0;i<3;i++){ 
    digitalWrite(YELLOW,HIGH);
    delay(500);
    digitalWrite(YELLOW,LOW);
    delay(500);
  }

}
```

## Experiment 3 - LED Chasing Effect
### Components
* Arduino Uno
* Breadboard
* LED 6
* Jumper wire
* Restsor 220 ohm

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp3.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp3.gif)
### Tutorial 
#### Serial monitor

[![Serial Monitor](https://img.youtube.com/vi/-sCEvx2VxC4/0.jpg)](https://youtu.be/-sCEvx2VxC4)

#### String

[![String](https://img.youtube.com/vi/vtg_r1M-Tfw/0.jpg)](https://youtu.be/vtg_r1M-Tfw "Episode 5")

#### Serial Monitor input

[![String](https://img.youtube.com/vi/Un76nTKgADI/0.jpg)](https://youtu.be/Un76nTKgADI "Episode 5")

#### Array

[![Array](https://img.youtube.com/vi/FRhzuWl39qg/0.jpg)](https://youtu.be/FRhzuWl39qg "Episode 5")

#### i++,i--

[![Array](https://img.youtube.com/vi/1juml255rbI/0.jpg)](https://youtu.be/1juml255rbI "Episode 5")
### Code
```ino
//Make array and store led pins
int LED[]={10,9,8,7,6,5};
//commen delay time
int DELAY_TIME = 50;
int i=0; // make a itrating variable and assain value 0
void setup(){ 
  //set all led are output
  for(int i=0;i<6;i++){
    pinMode(LED[i],OUTPUT);
  }
} 
// right looping
void loop(){
  while(i<6){
    digitalWrite(LED[i],HIGH);
    delay(DELAY_TIME);
    digitalWrite(LED[i],LOW);
    delay(DELAY_TIME);
    i++; // i=i+1
  }
  i-=2; // i=i-2
  //left looping
  while(i>=0){
    digitalWrite(LED[i],HIGH);
    delay(DELAY_TIME);
    digitalWrite(LED[i],LOW);
    delay(DELAY_TIME);
    i--; //i=i-1
  }
  i+=2; // i=i+2
  

}
```

## Experiment 4 -Button Controlled LED
### Components
* Arduino Uno
* Breadboard
* LED 
* Jumper wire
* Restsor 220 ohm , 10 ohm
* michro switch

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp4.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp4.gif)
### Tutorial 
#### Arduino push buttion

[![push buttion](https://img.youtube.com/vi/llIk9fHthfQ/0.jpg)](https://youtu.be/XCZ2Vx_rPF0?t=1252)
#### Reading 

[![String](https://img.youtube.com/vi/7BQzt1F1qik/0.jpg)](https://youtu.be/7BQzt1F1qik "Episode 5")
#### INPUT PULLUP 

[![push buttion](https://img.youtube.com/vi/y3rjdNJ-8Bs/0.jpg)](https://youtu.be/y3rjdNJ-8Bs)


### Code
```ino
// set Read pin 10
#define READ_PIN 10
// led colnnect 13 
#define LED 13
bool readData=0;
void setup(){ 
  pinMode(READ_PIN ,INPUT);
  pinMode(LED ,OUTPUT);
} 
void loop(){
  readData=digitalRead(READ_PIN); // read data
  Serial.println(readData);
  digitalWrite(LED,readData); // read data high LED WILL ON otherwice led will off
}
```

## Experiment 5 -BUZZER
### Components
* Arduino 
* Breadboard
* BUZZER
* Jumper wire

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp5.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp5.gif)


### Code
```ino
// Buzzer Connect 13
#define BUZZER 13
void setup(){ 
  pinMode(BUZZER ,OUTPUT);
} 
void loop(){
  digitalWrite(BUZZER,HIGH); // BUZZER ON
  delay(1000);
  digitalWrite(BUZZER,LOW); // BUZZER OFF
  delay(1000);
}
```


## Experiment 6 -RGB LED
### Components
* Arduino Uno
* Breadboard
* RGB LED
* Jumper wire
* Restsor 220 ohm 

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp6.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp6.gif)
### Tutorial 
#### Analog Write

[![push buttion](https://img.youtube.com/vi/G_p7adSctlQ/0.jpg)](https://youtu.be/G_p7adSctlQ)

#### RGB PART 1

[![push buttion](https://img.youtube.com/vi/U7VH3QLO9kk/0.jpg)](https://youtu.be/U7VH3QLO9kk)

#### RGB PART 2

[![String](https://img.youtube.com/vi/1BCXbkFEB-E/0.jpg)](https://youtu.be/1BCXbkFEB-E "Episode 5")


### Code
```ino
int RGB_LED[]={11,9,10};
void setup(){ 
  for(int i=0;i<3;i++)
    pinMode(RGB_LED[i],OUTPUT);
} 
void loop(){
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],j);
    analogWrite(RGB_LED[1],0);
    analogWrite(RGB_LED[2],0);
    delay(5);
  }
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],0);
    analogWrite(RGB_LED[1],j);
    analogWrite(RGB_LED[2],0);
    delay(5);
  }
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],0);
    analogWrite(RGB_LED[1],0);
    analogWrite(RGB_LED[2],j);
    delay(5);
  }
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],j);
    analogWrite(RGB_LED[1],j);
    analogWrite(RGB_LED[2],0);
    delay(5);
  }
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],j);
    analogWrite(RGB_LED[1],0);
    analogWrite(RGB_LED[2],j);
    delay(5);
  }
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],0);
    analogWrite(RGB_LED[1],j);
    analogWrite(RGB_LED[2],j);
    delay(5);
  }
  for(int j=0;j<255;j++){
    analogWrite(RGB_LED[0],j);
    analogWrite(RGB_LED[1],j);
    analogWrite(RGB_LED[2],j);
    delay(5);
  }
  
}
```


## Experiment  7- LDR SENSOR 
### Components
* Arduino Uno
* Breadboard
* RED,GREEN LED
* Jumper wire
* Restsor 220 ohm 10 k
* LDR Sensor

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/exp7.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/exp7.gif)

### Tutorial 
#### AND GATE

[![push buttion](https://img.youtube.com/vi/TdUOHEYF2CY/0.jpg)](https://youtu.be/TdUOHEYF2CY)

#### OR GATE

[![push buttion](https://img.youtube.com/vi/sjyriFBLsDA/0.jpg)](https://youtu.be/sjyriFBLsDA)

#### NOT GATE

[![push buttion](https://img.youtube.com/vi/cBqBqIPWQuM/0.jpg)](https://youtu.be/cBqBqIPWQuM)


### Code
```ino
#define LDR 12 // LDR CONNECT 12
#define RLED 11 // Red LED CONNECT 11
#define GLED 10 // Green LED Connect 10
bool readData=0;
void setup(){ 
  pinMode(RLED,OUTPUT);
  pinMode(GLED,OUTPUT);
  pinMode(LDR,INPUT);
} 
void loop(){
  readData=digitalRead(LDR);
  digitalWrite(RLED,readData);
  digitalWrite(GLED,!readData);
}
```
