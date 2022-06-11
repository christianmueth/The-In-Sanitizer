# The-In-Sanitizer
//Portable/Robotic cup cleaning device. Developed with Seamus Graham and Kenny Nguyen at Virginia Tech

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
