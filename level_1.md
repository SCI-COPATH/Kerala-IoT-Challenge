# Kerala IoT Challenge Level-1

### Experiment 1 - Hello World LED Blinking

![Hello World LED Blinking](https://user-images.githubusercontent.com/44474792/132120834-bddf79e5-99d3-4d99-a355-b5776fd7c1a0.jpg)
#### Code
```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```

### Experiment 2 - Traffic Light

![Traffic Light](https://user-images.githubusercontent.com/44474792/132121020-4329f96c-e525-4472-aad3-e703826993d2.jpg)
#### Code
```ino
void setup() 
{
   pinMode(13, OUTPUT);
   pinMode(10, OUTPUT);
   pinMode(8, OUTPUT);
}

void loop()
{
  digitalWrite(13, HIGH);
  delay(5000);
  digitalWrite(13, LOW);
  
  for(int i=0; i<3; i++)
  {
    delay(500);
    digitalWrite(10, HIGH);
    delay(500);
    digitalWrite(10, LOW);
  }
  
  delay(500);
  digitalWrite(8, HIGH);
  delay(5000);
  digitalWrite(8, LOW);
}
```

### Experiment 3 - LED Chasing Effect

![image](https://user-images.githubusercontent.com/44474792/132120873-538e171f-9ffd-4356-aa7f-45576711db21.jpg)
#### Code
```ino
void setup()
{
   for (int i = 7; i < 13; i ++) 
   {
     pinMode(i, OUTPUT);
   }
}
void loop()
{
   for (int i = 7; i < 13; i ++) 
   {
     digitalWrite(i, LOW);
     delay(200);
   }
   for (int i = 7; i < 13; i ++) 
   {
     digitalWrite(i, HIGH);
     delay(200);
   }  
}
```

### Experiment 4 - Button Controlled LED

![image](https://user-images.githubusercontent.com/44474792/132127544-f42e9f96-9f2c-4898-93ce-e479ee40d3d3.png)
#### Code
```ino
int x;
void setup()
{
  pinMode(11, OUTPUT);
  pinMode(7, INPUT);
}
void loop()
{
  val=digitalRead(7);
  if(x == LOW)
  {
    digitalWrite(11, LOW);
  }
  else
  {
    digitalWrite(11, HIGH);
  }
}
```

### Experiment 5 - Buzzer

![image](https://user-images.githubusercontent.com/44474792/132120819-7dca413d-2dbe-41b3-9929-c44915715aa0.jpg)
#### Code
```ino
void setup() 
{ 
  pinMode(8, OUTPUT);
} 
void loop() 
{
  digitalWrite(8, HIGH);
  delay(1000);
  digitalWrite(8, LOW);
  delay(1000);
}
```

### Experiment 6 - RGB LED

![image](https://user-images.githubusercontent.com/44474792/131454311-4759b60a-1a38-41d7-81ea-0f67c87642ba.png)
#### Code
```ino
int red = 11;
int blue =10;
int green =9;
int x;
void setup() {
  pinMode(red, OUTPUT);
  pinMode(blue, OUTPUT);
  pinMode(green, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(x=255; x>0; x--)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
for(x=0; x<255; x++)
  {
   analogWrite(11, x);
   analogWrite(10, 255-x);
   analogWrite(9, 128-x);
   delay(10); 
  }
 Serial.println(x, DEC);
}
```

### Experiment 8 - Flame Sensor

![image](https://user-images.githubusercontent.com/44474792/132122467-26653513-32ed-4e38-ad54-cf36b7edd49d.jpg)
#### Code
```ino
const int buzzerPin = 12;
const int flamePin = 11;
int Flame = HIGH;

void setup() 
{
  pinMode(buzzerPin, OUTPUT);
  pinMode(flamePin, INPUT);
  Serial.begin(9600);
}

void loop() 
{
  Flame = digitalRead(flamePin);
  if (Flame== LOW)
  {
    Serial.println("Fire!!!");
    digitalWrite(buzzerPin, HIGH);
  }
  else
  {
    Serial.println("No worries");
    digitalWrite(buzzerPin, LOW);
  }
}
```

### Experiment 9 - LM35 Temperature Sensor

![image](https://user-images.githubusercontent.com/44474792/132123183-a7430048-f9c6-4c4f-8406-485e2f29fe5d.png)
![image](https://user-images.githubusercontent.com/44474792/132123315-9d2945a6-47d8-4f57-9b11-d961f9e8ccdf.png)
#### Code
```ino
const int lm35_pin = A1;

void setup() {
  Serial.begin(9600);
}

void loop() {
  int temp_adc_val;
  float temp_val;
  temp_adc_val = analogRead(lm35_pin);
  temp_val = (temp_adc_val * 4.88);
  temp_val = (temp_val/10);
  Serial.print("Temperature = ");
  Serial.print(temp_val);
  Serial.print(" Degree Celsius\n");
  delay(1000);
}
```

### Experiment 10 - IR Remote Control using TSOP

![image](https://user-images.githubusercontent.com/44474792/132744337-ef029ada-923d-4a5d-8d72-0d9344332393.png)
#### Code
```ino
#include <IRremote.h>
int redLed = 5;
int yellowLed = 4;
int greenLed = 3;
int blueLed = 2;
int RECV_PIN = 11;
IRrecv irrecv(RECV_PIN);
decode_results results;


void setup()
{
  pinMode(redLed, OUTPUT);
  pinMode(yellowLed, OUTPUT);
  pinMode(greenLed, OUTPUT);
  pinMode(blueLed, OUTPUT);
  
  Serial.begin(9600);
  Serial.println("Enabling IRin");
  irrecv.enableIRIn(); 
  Serial.println("Enabled IRin");
}

void loop() {
  if (irrecv.decode(&results)) {
    unsigned int value = results.value;
    Serial.println(value);
    switch (value) {
      case 2295: 
      	digitalWrite(redLed, HIGH);
      	delay(500);
      	digitalWrite(redLed, LOW);
      	break;
      
      case 34935:
      	digitalWrite(yellowLed, HIGH);
      	delay(500);
      	digitalWrite(yellowLed, LOW);
      	break;
      
      case 18615:
      	digitalWrite(greenLed, HIGH);
      	delay(500);
      	digitalWrite(greenLed, LOW);
      	break;
      
      case 10455:
      	digitalWrite(blueLed, HIGH);
      	delay(500);
      	digitalWrite(blueLed, LOW);
    }
    
    irrecv.resume();
  }
}
```

### Experiment 11 - Potentiometer analog Value Reading

![image](https://user-images.githubusercontent.com/44474792/132124333-56134c03-b7e2-4573-af4b-6006ee8935ce.jpg)
#### Code
```ino
int potpin = 0;
int ledpin = 13;
int val = 0;
void setup()
{
pinMode(ledpin,OUTPUT);
Serial.begin(9600);
}
void loop()
{
  digitalWrite(ledpin, HIGH);
  delay(50);
  digitalWrite(ledpin, LOW);
  delay(50);
  val = analogRead(potpin);
  Serial.println(val);
}
```

### Experiment 12 - Segment Display

![image](https://user-images.githubusercontent.com/44474792/132795657-db1977a0-412d-426d-a87a-cfdf6b7fa724.png)
#### Code
```ino
int A = 13;
int B = 12;
int C = 11;
int D = 10;
int E = 9;
int F = 8;
int G = 7;
int H = 6;

void setup(void)
{
  pinMode(A, OUTPUT);
  pinMode(B, OUTPUT);
  pinMode(C, OUTPUT);
  pinMode(D, OUTPUT);
  pinMode(E, OUTPUT);
  pinMode(F, OUTPUT);
  pinMode(G, OUTPUT);
  pinMode(H, OUTPUT);
}

void zero(void) {
  digitalWrite(A, LOW);
  digitalWrite(B, HIGH);
  digitalWrite(C, HIGH);
  digitalWrite(D, HIGH);
  digitalWrite(E, HIGH);
  digitalWrite(F, HIGH);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void one(void) {
  digitalWrite(A, LOW);
  digitalWrite(B, LOW);
  digitalWrite(C, LOW);
  digitalWrite(D, HIGH);
  digitalWrite(E, LOW);
  digitalWrite(F, LOW);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void two(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, LOW);
  digitalWrite(C, HIGH);
  digitalWrite(D, HIGH);
  digitalWrite(E, HIGH);
  digitalWrite(F, HIGH);
  digitalWrite(G, LOW);
  digitalWrite(H, LOW);
}

void three(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, LOW);
  digitalWrite(C, HIGH);
  digitalWrite(D, HIGH);
  digitalWrite(E, LOW);
  digitalWrite(F, HIGH);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void four(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, HIGH);
  digitalWrite(C, LOW);
  digitalWrite(D, HIGH);
  digitalWrite(E, LOW);
  digitalWrite(F, LOW);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void five(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, HIGH);
  digitalWrite(C, HIGH);
  digitalWrite(D, LOW);
  digitalWrite(E, LOW);
  digitalWrite(F, HIGH);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void six(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, HIGH);
  digitalWrite(C, HIGH);
  digitalWrite(D, LOW);
  digitalWrite(E, HIGH);
  digitalWrite(F, HIGH);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void seven(void) {
  digitalWrite(A, LOW);
  digitalWrite(B, LOW);
  digitalWrite(C, HIGH);
  digitalWrite(D, HIGH);
  digitalWrite(E, LOW);
  digitalWrite(F, LOW);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void eight(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, HIGH);
  digitalWrite(C, HIGH);
  digitalWrite(D, HIGH);
  digitalWrite(E, HIGH);
  digitalWrite(F, HIGH);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void nine(void) {
  digitalWrite(A, HIGH);
  digitalWrite(B, HIGH);
  digitalWrite(C, HIGH);
  digitalWrite(D, HIGH);
  digitalWrite(E, LOW);
  digitalWrite(F, HIGH);
  digitalWrite(G, HIGH);
  digitalWrite(H, LOW);
}

void loop(void)
{
  zero();
  delay(1000);
  
  one();
  delay(1000);
  
  two();
  delay(1000);
  
  three();
  delay(1000);
  
  four();
  delay(1000);
  
  five();
  delay(1000);
  
  six();
  delay(1000);
  
  seven();
  delay(1000);
  
  eight();
  delay(1000);
  
  nine();
  delay(1000);
}
```

## IoT Challenge Assignments

### **Assignment 1** - Automatic Night Lamp using LDR & LED

![image](https://user-images.githubusercontent.com/44474792/132135947-e491a270-75d1-4671-bff1-b2c5e540ddaf.png)
#### Code
```ino
const int LED = 13;  
const int LDR = A0;  

void setup() {
  Serial.begin(9600);
  pinMode(LED, OUTPUT); 
  pinMode(LDR, INPUT);   
}

void loop()
{
  int ldrStatus = analogRead(LDR);  
  if (ldrStatus <= 400) {
    digitalWrite(LED, HIGH);               
    Serial.println("Room is DARK - LED ON");
  }
  else {
    digitalWrite(LED, LOW);         
    Serial.println("Room is BRIGHT - LED OFF");
    }
}
```

### **Assignment 2** - Digital Dice using 6 LEDs & 1 Push Button

![image](https://user-images.githubusercontent.com/44474792/132137070-709c4008-857c-4ffd-91ae-92aabdb3a2e9.png)
#### Code
```ino
#define DEBUG 0

int first = 2;
int second = 3;
int third = 4;
int fourth = 5;
int fifth = 6;
int sixth = 7;

int button = 12;
int pressed = 0;

void setup() {
  for (int i=first; i<=sixth; i++) {
    pinMode(i, OUTPUT);
  }
  pinMode(button, INPUT);
  randomSeed(analogRead(0));

  #ifdef DEBUG
  Serial.begin(9600);
  #endif

}

void buildUpTension() {
  for (int i=first; i<=sixth; i++) {
    if (i!=first) {
      digitalWrite(i-1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
  for (int i=sixth; i>=first; i--) {
    if (i!=sixth) {
      digitalWrite(i+1, LOW);
    }
    digitalWrite(i, HIGH);
    delay(100);
  }
}

void showNumber(int number) {
  digitalWrite(first, HIGH);
  if (number >= 2) {
    digitalWrite(second, HIGH);
  }
  if (number >= 3) {
    digitalWrite(third, HIGH);    
  }
  if (number >= 4) {
    digitalWrite(fourth, HIGH);    
  }
  if (number >= 5) {
    digitalWrite(fifth, HIGH);    
  }
  if (number == 6) {
    digitalWrite(sixth, HIGH);    
  }
}

int throwDice() {
  int randNumber = random(1,7);
  
  #ifdef DEBUG
    Serial.println(randNumber);
  #endif
  
  return randNumber;
}

void setAllLEDs(int value) {
  for (int i=first; i<=sixth; i++) {
    digitalWrite(i, value);
  }
}

void loop() {
  pressed = digitalRead(button);

  if (pressed == HIGH) {
    setAllLEDs(LOW);
    
    buildUpTension();
    int thrownNumber = throwDice();
    showNumber(thrownNumber);
  } 

}
```

## My Experience
> **Kerala IoT Challenge : Level 1** was an awesome experience. I have been exploring IoT since the beginning of my graduation. As stated earlier, for this challenge too, I'd collected IoT Components from the Mini IoT Lab that we setup at our [**Inovus Labs IEDC**](https://inovus-labs.web.app/). As my 2 colleagues, **Sandra Krishnan** & **Jeevan Joseph** joined the Challenge, we decided to tinker together.

> As some IoT components were in short supply & some were damaged, we decided to opt [**TinkerCad Simulator**](https://www.tinkercad.com/dashboard?type=circuits) for completing such Experiments. It was my first ever experience with TinkerCad. That's the main take-away for me from this challenge. I'd almost 80% of the experiments in TinkerCard; of which some of them are attached in the documentation. And above all, it's my first ever experience of documenting my IoT Experiments.

> I'm eagerly waiting to explore more from **Kerala IoT Challenge : Level 2**. Hope we'll be having some really cool cloud based projects in the upcoming Levels like **Home Automation, Weather Prediction (Big Data)** by collecting & analysing the Temperature & Humidity Sensor values in the Cloud etc:

> **I'm also interested in Mentoring the future tinkerers of Level 1 : Cohort 2**.
