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
![Expriment 1](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp1.png)
### Video
![Expriment ](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp1.gif)
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
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp2.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp2.gif)
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
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp3.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp3.gif)
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
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp4.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp4.gif)
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
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp5.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp5.gif)


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
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp6.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp6.gif)
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
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp7.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp7.gif)

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

## Experiment  8- FLAME SENSOR 
### Components
* Arduino Uno
* Breadboard
* RED LED
* BUZZER
* Jumper wire
* Restsor 220 ohm 10 k
* Flame Sensor

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp8.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp8.gif)

### Tutorial 
#### Analog Write

[![push buttion](https://img.youtube.com/vi/ABhevxYkiFQ/0.jpg)](https://youtu.be/ABhevxYkiFQ)

#### UntraSonic

[![push buttion](https://img.youtube.com/vi/tKnVDJwvXkk/0.jpg)](https://youtu.be/tKnVDJwvXkk)

#### UntraSonic Distance

[![push buttion](https://img.youtube.com/vi/DWgt-iInhzs/0.jpg)](https://youtu.be/DWgt-iInhzs)

#### Simple if

[![push buttion](https://img.youtube.com/vi/MIoKLvJZ-AY/0.jpg)](https://youtu.be/MIoKLvJZ-AY)

#### else if laddar

[![push buttion](https://img.youtube.com/vi/kUHdW2-leaQ/0.jpg)](https://youtu.be/kUHdW2-leaQ)

#### Switch

[![push buttion](https://img.youtube.com/vi/596gRADm_OY/0.jpg)](https://youtu.be/596gRADm_OY)

### Code
```ino
#define FLAME A0 // Flaem sensor CONNECT A0
#define RED 11 // Red LED CONNECT 11
#define BUZZER 10 // Buzzer LED Connect 10

int data;
void setup(){ 
  pinMode(RED,OUTPUT);
  pinMode(FLAME,INPUT);
  pinMode(BUZZER,OUTPUT);
  Serial.begin(9600);
} 
void loop(){
  data=analogRead(FLAME);
  Serial.print("DATA :");
  Serial.println(data);
  if(data>600){
    digitalWrite(RED,HIGH);
    digitalWrite(BUZZER,HIGH);
    delay(1000);
  }else{
    digitalWrite(RED,LOW);
    digitalWrite(BUZZER,LOW);
  }
}
```

## Experiment  9- LM35 Temperature Sensor
### Components
* Arduino Uno
* Breadboard
* Jumper wire

### Sensor
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/temp1.jpg)

![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/temp2.jpg)

![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/temp3.png)
### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp9.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp9.gif)


### Code
```ino
#define LM35_SENSOR A0 // Flaem sensor CONNECT A0
float readData;
float tempC,tempF;
void setup(){ 
  pinMode(LM35_SENSOR,INPUT);
  Serial.begin(9600);
} 
void loop(){
  readData=analogRead(LM35_SENSOR);
  tempC=(readData/1024.0)*500;
  Serial.print("Temprature : ");
  Serial.print(tempC);
  Serial.print(" *C =");
  tempF=(tempC*9.0)/5.0 + 32.0;
  Serial.print(tempF);
  Serial.println(" *F");
}
```



## Experiment  10- IR Remote Control Using TSOP
### Components
* Arduino Uno
* Breadboard
* Jumper wire
* IR Recever (TSOP)
* 5 LED
* 220 ohm Resistor
* IR REMOTE (Any remote)

### Sensor
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/ir1.jpg)

## IR Decode 

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp101.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp101.gif)


### Code
```ino
#define IR_PIN A0 // IR sensor connect
#include<IRremote.h> // IR library
IRrecv irrecv(IR_PIN); // connect ir pin to library
decode_results  result; 
void setup(){ 
  Serial.begin(9600);
  irrecv.enableIRIn(); 
  
} 
void loop(){
  if(irrecv.decode(&result)){
    Serial.println(result.value,HEX);
    irrecv.resume();
  }
}
```

# IR LED Controll 

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp102.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp102.gif)


### Code
```ino
#define IR_PIN A0 // Flaem sensor CONNECT A0
#include<IRremote.h>
unsigned long receveData[]={0x1FE50AF,0x1FED827,0x1FEF807,0x1FE30CF,0x1FEB04F,0x1FE708F};
bool statusData[]{0,0,0,0,0,0};
int led[]={7,6,5,4,3,2};
IRrecv irrecv(IR_PIN);
decode_results  result;
void setup(){ 
  Serial.begin(9600);
  irrecv.enableIRIn();
  for(int i=0;i<6;i++)
    pinMode(led[i],OUTPUT);
} 
void loop(){
  if(irrecv.decode(&result)){
    Serial.println(result.value,HEX);
    for(int i=0;i<6;i++){
      if(result.value==receveData[i]){
        statusData[i]=!statusData[i];
        digitalWrite(led[i],statusData[i]);
      }
    }
    irrecv.resume();
  }
}
```



## Experiment  12- Seven Segment Display
### Components
* Arduino Uno
* Breadboard
* Seven Segment Display
* Jumper wire
* Restsor 220 ohm

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/exp12.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/exp12.gif)

### Tutorial 
#### Function Part 1

[![push buttion](https://img.youtube.com/vi/BDBEbeV0VbM/0.jpg)](https://youtu.be/BDBEbeV0VbM)

#### Function Part 2

[![push buttion](https://img.youtube.com/vi/XKQ-9TCcaIQ/0.jpg)](https://youtu.be/XKQ-9TCcaIQ)




### Code
```ino

int sevenSeg[]={13,12,11,10,9,8,7,6};
void number(int i){
  switch(i){
    case 0: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],HIGH);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
    case 1: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],HIGH);
            digitalWrite(sevenSeg[2],HIGH);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],HIGH);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],HIGH);
            digitalWrite(sevenSeg[7],HIGH);
            break;
    case 2: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],HIGH);
            
           // digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],HIGH);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
    case 3: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],HIGH);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
    case 4: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],HIGH);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],HIGH);
            digitalWrite(sevenSeg[7],LOW);
            break;

    case 5: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],HIGH);
            break;
   case 6: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],HIGH);
            break;
    case 7: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],HIGH);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],HIGH);
            
            digitalWrite(sevenSeg[5],HIGH);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
   case 8: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
   case 9: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
      
  }
  
}
void setup(){ 
  Serial.begin(9600);
 
  for(int i=0;i<8;i++){
    pinMode(sevenSeg[i],OUTPUT);
    digitalWrite(sevenSeg[i],HIGH);
  }
  
    
} 
void loop(){
  for(int i=9;i>=0;i--){
    number(i);
    delay(750);
  }
}
```

# Assigenment 

## Assigenment  1- Night lighting system 
### Components
* Arduino Uno
* Breadboard
* RED,GREEN LED
* Jumper wire
* Restsor 220 ohm 10 k
* LDR Sensor

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/ass1.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/ass1.gif)

### Code
```ino
#define LDR A0// LDR CONNECT A0
#define LED 11 // LED CONNECT 11
int readData=0;
void setup(){ 
  pinMode(LED,OUTPUT);
  pinMode(LDR,INPUT);
  Serial.begin(9600);
} 
void loop(){
  readData=analogRead(LDR);
  Serial.println(readData);
  if(readData>200)
    digitalWrite(LED,HIGH);
  else
    digitalWrite(LED,LOW);
}
```

## Assigenment 2 - 6 Number Random Dice

### Components
* Arduino Uno
* Breadboard
* pushbuttion
* Jumper wire
* Restsor 220 ohm
* push buttion

### Circuit
![Expriment 3](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/image/level1/ass2.png)
### Video
![Expriment 2](https://sci-copath.github.io/Kerala-IoT-Challenge/assat/videos/level1/ass2.gif)


### Code
```ino
#define readPin A0
bool readStatus=0;
int sevenSeg[]={13,12,11,10,9,8,7,6};
void number(int i){
  switch(i){
    case 0: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],HIGH);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
    case 1: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],HIGH);
            digitalWrite(sevenSeg[2],HIGH);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],HIGH);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],HIGH);
            digitalWrite(sevenSeg[7],HIGH);
            break;
    case 2: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],HIGH);
            
           // digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],HIGH);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
    case 3: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],HIGH);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
    case 4: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],HIGH);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],HIGH);
            digitalWrite(sevenSeg[7],LOW);
            break;

    case 5: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],HIGH);
            break;
   case 6: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH); 
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],HIGH);
            break;
    case 7: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],HIGH);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],HIGH);
            
            digitalWrite(sevenSeg[5],HIGH);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
   case 8: digitalWrite(sevenSeg[0],LOW);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
   case 9: digitalWrite(sevenSeg[0],HIGH);
            digitalWrite(sevenSeg[1],LOW);
            digitalWrite(sevenSeg[2],LOW);
            
            //digitalWrite(sevenSeg[3],HIGH);
            digitalWrite(sevenSeg[4],LOW);
            
            digitalWrite(sevenSeg[5],LOW);
            digitalWrite(sevenSeg[6],LOW);
            digitalWrite(sevenSeg[7],LOW);
            break;
      
  }
  
}
void setup(){ 
  Serial.begin(9600);
 
  for(int i=0;i<8;i++){
    pinMode(sevenSeg[i],OUTPUT);
    digitalWrite(sevenSeg[i],HIGH);
  }
  pinMode(readPin,INPUT_PULLUP);
  
  
    
} 
void loop(){
  if(readStatus==0&&digitalRead(readPin)==LOW){
    number(random(1,7));
    readStatus=1;
  }else if(digitalRead(readPin)==HIGH&&readStatus==1){
    readStatus=0;
  }
  delay(50);
}
```