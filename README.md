# The-In-Sanitizer
Portable/Robotic cup cleaning device. Developed by Seamus Graham, Christian Mueth, and Kenny Nguyen at Virginia Tech

Link to YouTube video:
https://www.youtube.com/watch?v=80qrmtLNZe8
![20220501_145339 (3)](https://user-images.githubusercontent.com/59476460/173171011-c7e11cf8-a72d-4c1a-85d2-9a88a3a99f30.jpg)

//Code for motor control:

#include <Servo.h>

Servo ESC;

void setup()

{
  pinMode(10,OUTPUT);
  pinMode(11,OUTPUT);
  digitalWrite(10,HIGH);
  digitalWrite(11,LOW);
  ESC.attach(9,1000,2000);
  ESC.write(100);
  delay(2000);
  ESC.write(0);
  delay(2000);
  ESC.write(75);

}

void loop()

{


 digitalWrite(10,LOW);

 digitalWrite(11,HIGH);

 delay(2000);
 
 digitalWrite(10,HIGH);

 digitalWrite(11,LOW);
 
 delay(780);
