/*
        Turorial Arduino
------------------------------------------------*
  Video 4: Juego de Luces                       *
                                                *
  Juego de luces a partir de contadores,        *
  utilizando funciones y 10 diodo leds.         *
                                                *
  Autor: Diseño Electrónico A2P                 *
------------------------------------------------*
*/


#define pulsador 2
#define led1     3
#define led2     4
#define led3     5
#define led4     6
#define led5     7
#define led6     8
#define led7     9
#define led8     10
#define led9     11
#define led10    12

int contador = 0;
int estado;

void setup() {
  // put your setup code here, to run once:

  pinMode(led1,  OUTPUT);
  pinMode(led2,  OUTPUT);  
  pinMode(led3,  OUTPUT);
  pinMode(led4,  OUTPUT);
  pinMode(led5,  OUTPUT);
  pinMode(led6,  OUTPUT);
  pinMode(led7,  OUTPUT);
  pinMode(led8,  OUTPUT); 
  pinMode(led9,  OUTPUT);
  pinMode(led10, OUTPUT);     
  
  Serial.begin(9600);

}

void loop() {
  // put your main code here, to run repeatedly:
  
  if (digitalRead(pulsador)== HIGH){
    estado=1;
  }

  if (estado == HIGH && digitalRead(pulsador)== LOW){
    contador++;
    Serial.print("Numero");
    Serial.println(contador);
    estado=0;
  }

   if (contador==1){
    secuencia_1 ();    
   }
   if (contador==2){
    secuencia_2 ();
   }   
   if (contador==3){
    secuencia_3 ();
   }   
   if (contador==4){
    secuencia_4 ();
   }   
   if (contador==5){
    secuencia_5 ();
   } 
   if (contador==6){
    secuencia_6 ();
   }  
   if (contador==7){
    contador=0;
   }    
         
}   

 void secuencia_1 (){
    digitalWrite(led1, HIGH);delay(50);digitalWrite(led2, HIGH);delay(50);digitalWrite(led3, HIGH);delay(50); 
    digitalWrite(led4, HIGH);delay(50);digitalWrite(led5, HIGH);delay(50);digitalWrite(led6, HIGH);delay(50);
    digitalWrite(led7, HIGH);delay(50);digitalWrite(led8, HIGH);delay(50);digitalWrite(led9, HIGH);delay(50);
    digitalWrite(led10,HIGH);delay(50);digitalWrite(led10,LOW); delay(50);digitalWrite(led9, LOW); delay(50);
    digitalWrite(led8, LOW); delay(50);digitalWrite(led7, LOW); delay(50);digitalWrite(led6, LOW); delay(50);
    digitalWrite(led5, LOW); delay(50);digitalWrite(led4, LOW); delay(50);digitalWrite(led3, LOW); delay(50);
    digitalWrite(led2, LOW); delay(50);digitalWrite(led1, LOW); delay(50); 
 }

 void secuencia_2 (){
    digitalWrite(led1, HIGH);delay(50);digitalWrite(led2, HIGH);delay(50);digitalWrite(led3, HIGH);delay(50); 
    digitalWrite(led4, HIGH);delay(50);digitalWrite(led5, HIGH);delay(50);digitalWrite(led6, HIGH);delay(50);
    digitalWrite(led7, HIGH);delay(50);digitalWrite(led8, HIGH);delay(50);digitalWrite(led9, HIGH);delay(50);
    digitalWrite(led10,HIGH);delay(50);digitalWrite(led1, LOW); delay(50);digitalWrite(led2, LOW); delay(50);
    digitalWrite(led3, LOW); delay(50);digitalWrite(led4, LOW); delay(50);digitalWrite(led5, LOW); delay(50);
    digitalWrite(led6, LOW); delay(50);digitalWrite(led7, LOW); delay(50);digitalWrite(led8, LOW); delay(50);
    digitalWrite(led9, LOW); delay(50);digitalWrite(led10,LOW); delay(50); 
 } 

 void secuencia_3 (){
    digitalWrite(led10, HIGH);delay(50);digitalWrite(led9, HIGH);delay(50);digitalWrite(led8, HIGH);delay(50); 
    digitalWrite(led7, HIGH);delay(50);digitalWrite(led6, HIGH);delay(50);digitalWrite(led5, HIGH);delay(50);
    digitalWrite(led4, HIGH);delay(50);digitalWrite(led3, HIGH);delay(50);digitalWrite(led2, HIGH);delay(50);
    digitalWrite(led1,HIGH);delay(50);digitalWrite(led10, LOW); delay(50);digitalWrite(led9, LOW); delay(50);
    digitalWrite(led8, LOW); delay(50);digitalWrite(led7, LOW); delay(50);digitalWrite(led6, LOW); delay(50);
    digitalWrite(led5, LOW); delay(50);digitalWrite(led4, LOW); delay(50);digitalWrite(led3, LOW); delay(50);
    digitalWrite(led2, LOW); delay(50);digitalWrite(led1,LOW); delay(50); 
 }  
 
 void secuencia_4 (){
    digitalWrite(led5, HIGH);digitalWrite(led6, HIGH); delay(80);digitalWrite(led4, HIGH);digitalWrite(led7, HIGH);delay(80); 
    digitalWrite(led3, HIGH);digitalWrite(led8, HIGH); delay(80);digitalWrite(led2, HIGH);digitalWrite(led9, HIGH);delay(80); 
    digitalWrite(led1, HIGH);digitalWrite(led10, HIGH);delay(80); 
    digitalWrite(led1, LOW); digitalWrite(led10, LOW); delay(80);digitalWrite(led2, LOW);digitalWrite(led9, LOW); delay(80);
    digitalWrite(led3, LOW); digitalWrite(led8, LOW);  delay(80);digitalWrite(led4, LOW);digitalWrite(led7, LOW); delay(80);
    digitalWrite(led5, LOW); digitalWrite(led6, LOW);  delay(80);    
 }
 
 void secuencia_5 (){
    digitalWrite(led1, HIGH); delay(50); digitalWrite(led1, LOW); digitalWrite(led3, HIGH);  delay(50); digitalWrite(led3, LOW); 
    digitalWrite(led5, HIGH); delay(50); digitalWrite(led5, LOW); digitalWrite(led7, HIGH);  delay(50); digitalWrite(led7, LOW);
    digitalWrite(led9, HIGH); delay(50); digitalWrite(led9, LOW); digitalWrite(led10, HIGH); delay(50); digitalWrite(led10, LOW);
    digitalWrite(led8, HIGH); delay(50); digitalWrite(led8, LOW); digitalWrite(led6, HIGH);  delay(50); digitalWrite(led6, LOW);   
    digitalWrite(led4, HIGH); delay(50); digitalWrite(led4, LOW); digitalWrite(led2, HIGH);  delay(50); digitalWrite(led2, LOW); 
 }
 void secuencia_6 (){
    digitalWrite(led1, HIGH);delay(100);digitalWrite(led2, HIGH);delay(100);digitalWrite(led3, HIGH);delay(100); 
    digitalWrite(led4, HIGH);delay(100);digitalWrite(led5, HIGH);delay(100);digitalWrite(led6, HIGH);delay(100);
    digitalWrite(led7, HIGH);delay(100);digitalWrite(led8, HIGH);delay(100);digitalWrite(led9, HIGH);delay(100);
    digitalWrite(led10,HIGH);delay(100);digitalWrite(led10,LOW); delay(100);digitalWrite(led9, LOW); delay(100);
    digitalWrite(led8, LOW); delay(100);digitalWrite(led7, LOW); delay(100);digitalWrite(led6, LOW); delay(100);
    digitalWrite(led5, LOW); delay(100);digitalWrite(led4, LOW); delay(100);digitalWrite(led3, LOW); delay(100);
    digitalWrite(led2, LOW); delay(100);digitalWrite(led1, LOW); delay(100);   
    digitalWrite(led1, HIGH); delay(50); digitalWrite(led1, LOW); digitalWrite(led3, HIGH);  delay(50); digitalWrite(led3, LOW); 
    digitalWrite(led5, HIGH); delay(50); digitalWrite(led5, LOW); digitalWrite(led7, HIGH);  delay(50); digitalWrite(led7, LOW);
    digitalWrite(led9, HIGH); delay(50); digitalWrite(led9, LOW); digitalWrite(led10, HIGH); delay(50); digitalWrite(led10, LOW);
    digitalWrite(led8, HIGH); delay(50); digitalWrite(led8, LOW); digitalWrite(led6, HIGH);  delay(50); digitalWrite(led6, LOW);   
    digitalWrite(led4, HIGH); delay(50); digitalWrite(led4, LOW); digitalWrite(led2, HIGH);  delay(50); digitalWrite(led2, LOW); 
    digitalWrite(led1, HIGH); delay(50); digitalWrite(led1, LOW); digitalWrite(led3, HIGH);  delay(50); digitalWrite(led3, LOW); 
    digitalWrite(led5, HIGH); delay(50); digitalWrite(led5, LOW); digitalWrite(led7, HIGH);  delay(50); digitalWrite(led7, LOW);
    digitalWrite(led9, HIGH); delay(50); digitalWrite(led9, LOW); digitalWrite(led10, HIGH); delay(50); digitalWrite(led10, LOW);
    digitalWrite(led8, HIGH); delay(50); digitalWrite(led8, LOW); digitalWrite(led6, HIGH);  delay(50); digitalWrite(led6, LOW);   
    digitalWrite(led4, HIGH); delay(50); digitalWrite(led4, LOW); digitalWrite(led2, HIGH);  delay(50); digitalWrite(led2, LOW);     
 } 
