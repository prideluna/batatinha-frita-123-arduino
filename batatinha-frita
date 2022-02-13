#include <Servo.h>

Servo myservo;  // create servo object to control a servo

int pos = 0;    // variable to store the servo position
const int trigPin = 10; 
const int echoPin = 9;  
const int pisca = 3;
const int buzzer = 8;

long duration; 
int distance;  
int decreaseSpeed = 500;
float velocity =1.2;
int distance1;
int distance2;

void setup() {
    pinMode(pisca, OUTPUT); 
    pinMode(trigPin,OUTPUT); 
    pinMode(echoPin,INPUT);   
    pinMode(buzzer,OUTPUT);  
    Serial.begin(9600);
    velocity = 1/velocity;
    
    myservo.attach(6);  // attaches the servo on pin 6 to the servo
}

void loop() {
    digitalWrite(trigPin, LOW);  
    delayMicroseconds(5);  
    digitalWrite(trigPin, HIGH);  
    delayMicroseconds(10);  
    digitalWrite(trigPin, LOW); 

    duration = pulseIn(echoPin, HIGH);  
    distance = duration*0.034/2 ;         
    
    
    int distance1;
    int distance2;
    Serial.print("Distancia: ");
    Serial.println(distance);
    delay(50);
        
 distance = duration*0.034/2 ; 
  for (pos = 0; pos < 180; pos += 1) { // goes from 0 degrees to 180 degrees
    myservo.write(pos);              // tell servo to go to position in variable 'pos'
    delay(1);                     // waits 1ms for the servo to reach the position   
}
  distance1 = distance;
 
  for (pos = 180; pos >178;  pos -= 1){ //AGuardian is looking    
    myservo.write(pos); 
    
    delay(1500); 
    
    
    digitalWrite(pisca, HIGH);
    delay(1500);
    digitalWrite(pisca, LOW);
  } 
   distance2 = distance;
                
    for (pos = 178; pos >= 0;  pos -= 1) {
    myservo.write(pos);         
    delay(10);     
               
  }
    for (pos = 3; pos >= 0;  pos -= 1) {
    myservo.write(pos);         
    delay(decreaseSpeed);  
   
  }
    decreaseSpeed = decreaseSpeed - 150;  
    
    //delay(velocity*2000);
     tone(buzzer,261); // Aciona o buzzer na frequencia em Hz
    delay(velocity*300);// Espera um tempo para Desativar
    noTone(buzzer); //Desativa o buzzer
      
    tone(buzzer,390);     
    delay(velocity*300);
    noTone(buzzer); 

    tone(buzzer,390);     
    delay(velocity*600);
    noTone(buzzer);
   
    tone(buzzer,390);       
    delay(velocity*600);
    noTone(buzzer);
   
    tone(buzzer,345);              
    delay(velocity*600);    
    noTone(buzzer); 
 
    tone(buzzer,390);      
    delay(velocity*300);
    noTone(buzzer);  

    tone(buzzer,390);      
    delay(velocity*300);
    noTone(buzzer);
   
    tone(buzzer,297); 
    delay(velocity*300);
    noTone(buzzer); 
   
    tone(buzzer,297); 
    delay(velocity*300);
    noTone(buzzer); 
      
    tone(buzzer,345);                
    delay(velocity*400);    
    noTone(buzzer); 
 
                  
     }
    
