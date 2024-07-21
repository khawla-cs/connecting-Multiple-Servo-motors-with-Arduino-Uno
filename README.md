# How to connect multiple Servo motors with arduino?

## Requirements:
- Arduino Board
- Servo Motors x6
- breadboard
- external battery connected to the breadboard 4X(type:AA) 
- Wires

## Step 1: Build the circuit
<img width="959" alt="image" src="https://github.com/user-attachments/assets/a02cae14-b754-483c-8c8a-8406aaf1eed0">

## step 2 : write the code
i have explained every part of code here:
```
//add the Servo library
#include <Servo.h>

//Define our Servos
Servo servo1;
Servo servo2;
Servo servo3;
Servo servo4;
Servo servo5;
Servo servo6;

//Servo position in degrees
int servoposition1 = 0;

void setup(){
  //Define Servo signal inputs
  servo1.attach(3);
  servo2.attach(5);
  servo3.attach(6);
  servo4.attach(9);
  servo5.attach(10);
  servo6.attach(11);
    
}
void loop(){
  //Scan from 0 to 180 degrees
  for(servoposition1 = 0 ;servoposition1<180 ; servoposition1++)
  {
    servo1.write(servoposition1);
    servo2.write(servoposition1);
    servo3.write(servoposition1);
    servo4.write(servoposition1);
    servo5.write(servoposition1);
    servo6.write(servoposition1);
    delay(100);
  }
  //scan back from 180 to 0 degrees
  for(servoposition1 = 180 ;servoposition1>0 ; servoposition1--)
  {
    servo1.write(servoposition1);
    servo2.write(servoposition1);
    servo3.write(servoposition1);
    servo4.write(servoposition1);
    servo5.write(servoposition1);
    servo6.write(servoposition1);
    delay(100);
  }    
}
```
