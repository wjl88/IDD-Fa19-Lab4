# Paper Puppets

*A lab report by William J Leon*

## In this Report

You'll need to describe your design, include a video of your paper display in operation, and upload any code you wrote to make it move.

## Part A. Actuating DC motors

**Link to a video of your virbation motor**

>> Video taken

## Part B. Actuating Servo motors

### Part 1. Connect the Servo to your breadboard

**a. Which color wires correspond to power, ground and signal?**

Wires on servo
Brown - Ground
Red - 5V
Orange - Signal Line

### Part 2. Connect the Servo to your Arduino

**a. Which Arduino pin should the signal line of the servo be attached to?**

Digital Pin 9

**b. What aspects of the Servo code control angle or speed?**

The function servo.write() takes degrees (0-180) as an argument to control servo arm angle
The delay inbetween writing to the servo serves as a speed control for the device

## Part C. Integrating input and output

**Include a photo/movie of your raw circuit in action.**

>>Video Taken

## Part D. Paper puppet

**a. Make a video of your proto puppet.**

>> Video Taken


```
#include <Servo.h>

Servo myservo;  // create servo object to control a servo
// twelve servo objects can be created on most boards

int pos = 0;    // variable to store the servo position

void setup() {
  myservo.attach(9);  // attaches the servo on pin 9 to the servo object
}

void loop() {
  for (pos = 50; pos <= 120; pos += 1) { // goes from 0 degrees to 180 degrees
    // in steps of 1 degree
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
  for (pos = 120; pos >= 50; pos -= 1) { // goes from 180 degrees to 0 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(15);                       // waits 15ms for the servo to reach the position
  }
}
```

## Part E. Make it your own

**a. Make a video of your final design.**
 
