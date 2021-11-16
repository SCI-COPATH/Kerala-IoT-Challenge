# Kerala IoT Challenge

> **Foxlab Makerspace** in association with **GTech - Group of Technology Companies in Kerala** is launching our prestigious program  “*Kerala IoT Challenge 2021*”,  with a vision to mould 100 IoT experts in Kerala, hosting on the MuLearn platform. Kerala IoT Challenge is a program designed in 4 levels followed by a hackathon to identify and train quality industry leaders in the IoT domain, while any novice learner can start with layer 1 and others can enter laterally to the desired layer after an evaluation.

### About Me
> Hey y'all,  I'm Anantha Krishnan R J, a first year Electrical & Electronics Engineering Undergraduate from [**College of Engineering, Trivandrum**](https://www.cet.ac.in/). I'm a beginner to the field of IoT. 

## Level 1:

> Level 1 aims to set the foundation to the field of electonics. It comprises of 12 Experiments which are beginner friendly.

## Experiments 
---

### Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.

>Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over the conventional microcontrollers. It comes with a pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also it is less expensive & beginner friendly.

#### Components Required
   * Arduino Uno Board x1
   * USB Cable x1
   * LED (Any Color) x1
   * 220 OHM Resistor X1
   * Breadboard
   * Jumper Wires (Male to Male ) x2

#### Code

```

int ledPin = 10; // define digital pin 10.

void setup()
{
    pinMode(ledPin, OUTPUT);// define pin with  LED connected as output.
}
void loop()
{
    digitalWrite(ledPin, HIGH); // set the LED on.
    delay(1000); // wait for a second.
    digitalWrite(ledPin, LOW); // set the LED off.
    delay(1000); // wait for a second
} 

```

#### Circuit Diagram

![sc_exp1](assets/images/exp1.jpg)

#### Simulation 

![vid_exp1](assets/simulation/exp1.gif)

#### Snapshot

<iframe width="560" height="315" src="https://www.youtube.com/embed/lnA6eKeujNo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

