How to make Robo Car

Items required:
Arduino Uno
HC-05 Bluetooth Module
L298N Motor driver Module
Bo Motor with Tyre
Castor 360 wheel
12 Volt Battery with connector 
Jumper cables(f-f, m-m, m-f)
Fibre board

Cost of build:
Arduino Uno x 1 = 850/-
HC-05 Bluetooth Module x 1 = 250/-
L298N Motor driver Module x 1 = 150/-
Bo Motor with Tyre x 2 = 220/-
Castor 360 wheel x 1 = 30/-
12 Volt Battery with connector x 1 = 50/-
Jumper cables x 15 = 30/-
Fibre board x 1 = 20/-
Total cost: 1600/-

![design](https://github.com/no-naame/Car-Using-Audrino/assets/145124868/acc584af-3a3b-4c34-85ec-7b2a505fd134)

Source Code:
// Starting of Program
int m1a = 9;
int m1b = 10;
int m2a = 11;
int m2b = 12;
char val;

void setup() 
{  
pinMode(m1a, OUTPUT);  // Digital pin 10 set as output Pin
pinMode(m1b, OUTPUT);  // Digital pin 11 set as output Pin
pinMode(m2a, OUTPUT);  // Digital pin 12 set as output Pin
pinMode(m2b, OUTPUT);  // Digital pin 13 set as output Pin
Serial.begin(9600);
}

void loop()
{
  while (Serial.available() > 0)
  {
  val = Serial.read();
  Serial.println(val);
  }

  if( val == 'F') // Forward
    {
      digitalWrite(m1a, HIGH);
      digitalWrite(m1b, LOW);
      digitalWrite(m2a, HIGH);
      digitalWrite(m2b, LOW);  
    }
  else if(val == 'B') // Backward
    {
      digitalWrite(m1a, LOW);
      digitalWrite(m1b, HIGH);
      digitalWrite(m2a, LOW);
      digitalWrite(m2b, HIGH); 
    }
else if(val == 'L') //Left
    {
    digitalWrite(m1a, LOW);
    digitalWrite(m1b, LOW);
    digitalWrite(m2a, HIGH);
    digitalWrite(m2b, LOW);
    }
    else if(val == 'R') //Right
    {
    digitalWrite(m1a, HIGH);
    digitalWrite(m1b, LOW);
    digitalWrite(m2a, LOW);
    digitalWrite(m2b, LOW); 
    }
    
  else if(val == 'S') //Stop
    {
    digitalWrite(m1a, LOW);
    digitalWrite(m1b, LOW);
    digitalWrite(m2a, LOW);
    digitalWrite(m2b, LOW); 
    }
  else if(val == 'I') //Forward Right
    {
    digitalWrite(m1a, HIGH);
    digitalWrite(m1b, LOW);
    digitalWrite(m2a, LOW);
    digitalWrite(m2b, LOW);
    }
  else if(val == 'J') //Backward Right
    {
    digitalWrite(m1a, LOW);
    digitalWrite(m1b, HIGH);
    digitalWrite(m2a, LOW);
    digitalWrite(m2b, LOW);
    }
   else if(val == 'G') //Forward Left
    {
    digitalWrite(m1a, LOW);

Problems I faced:
It was my first time working on some Hardware project so I faced some difficulties during the time like not giving the proper voltage and making lots of errors , etc

Application used:
Bluetooth RC Controller (Control your car)
Arduino IDE (Put you code in the microcontroller)

Final Look:

<img width="364" alt="Screenshot 2024-03-26 at 2 40 32 AM" src="https://github.com/no-naame/Car-Using-Audrino/assets/145124868/f7377406-2f7c-43a7-8b21-7617d22bd999">



