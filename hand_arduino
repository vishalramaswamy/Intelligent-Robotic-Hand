#include <Servo.h>

int index=A0;
int middle=A1;
int ring=A2;
int little=A3;
int thumb=A4;
int wrist=A15;
int indexvalue=0;
int middlevalue=0;
int ringvalue=0;
int littlevalue=0;
int thumbvalue=0;
int wristvalue=0;
int indexpos=0;
int middlepos=0;
int ringpos=0;
int littlepos=0;
int thumbpos=0;
int wristpos=0;
Servo indexservo;
Servo middleservo;
Servo ringservo;
Servo littleservo;
Servo thumbservo;
Servo wristservo;
void setup()
{
  indexservo.attach(9);
  middleservo.attach(10);
  ringservo.attach(11);
  littleservo.attach(12);
  thumbservo.attach(13);
  wristservo.attach(8);

  Serial.begin(9600);  // start serial for output. Make sure you set your Serial Monitor to the same!
    }
void loop()
{
  int i;
 for(i=0;i<10;i++)
{
 indexvalue+=analogRead(index);
 middlevalue+=analogRead(middle);
 ringvalue+=analogRead(ring);
 littlevalue+=analogRead(little);
 thumbvalue+=analogRead(thumb);
 //wristvalue=analogRead(wrist);
} 
indexvalue/=10;
middlevalue/=10;
ringvalue/=10;
littlevalue/=10;
thumbvalue/=10;
//wristvalue/=10;
Serial.print("Index:");
Serial.println(indexvalue);
/*Serial.print("Middle:");
Serial.println(middlevalue);
Serial.print("Ring:");
Serial.println(ringvalue);
Serial.print("Little:");
Serial.println(littlevalue);
*/Serial.print("thumb:");
Serial.println(thumbvalue);
Serial.print("wrist:");
Serial.println(wristvalue);
indexpos=map(indexvalue,545,620,0,180);
indexservo.write(indexpos);
middlepos=map(middlevalue,660,810,0,180);
middleservo.write(middlepos);
ringpos=map(ringvalue,600,775,0,180);
ringservo.write(ringpos);
littlepos=map(littlevalue,580,780,0,180);
littleservo.write(littlepos);
thumbpos=map(thumbvalue,630,760,0,180);
thumbservo.write(thumbpos);
//delay(70);
wristvalue=analogRead(wrist);
wristpos=map(wristvalue,290,440,0,180);
wristservo.write(wristpos);
}


