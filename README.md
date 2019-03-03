# 15-Febrero
int rojo=2;
int verde=4;
int amarillo=6;
int r;
int rv;
int v;
int vv;
int r2;
int r2v;
void setup() {
  {
  Serial.begin(9600);
  Serial.println("¿Cuantos milisegundos quieres que prenda el led rojo?");
  delay(5000);
  while(Serial.available()==0){
  }
  r=Serial.parseInt();
  pinMode(rojo,OUTPUT);
  }
  {
  Serial.println("¿Cuantas veces quieres que prenda el led rojo?");
  delay(5000);
  while(Serial.available()==0){
  }
  rv=Serial.parseInt();
  pinMode(rojo,OUTPUT);
  }
  {
  Serial.println("¿Cuantos milisegundos quieres que prenda el led verde?");
  delay(5000);
  while(Serial.available()==0){
  }
  v=Serial.parseInt();
  pinMode(verde,OUTPUT);
  }
  {
  Serial.println("¿Cuantas veces quieres que prenda el led verde?");
  delay(5000);
  while(Serial.available()==0){
  }
  vv=Serial.parseInt();
  pinMode(verde,OUTPUT);
  }
  {
  Serial.println("¿Cuantos milisegundos quieres que prenda el led rojo 2?");
  delay(5000);
  while(Serial.available()==0){
  }
  r2=Serial.parseInt();
  pinMode(amarillo,OUTPUT);

}
  {
  Serial.println("¿Cuantas veces quieres que prenda el led rojo 2?");
  delay(5000);
  while(Serial.available()==0){
  }
  r2v=Serial.parseInt();
  pinMode(amarillo,OUTPUT);
  }
}

  

void loop() {
  for(int i=0; i<rv; i++){
digitalWrite(rojo,HIGH);
delay(r);
digitalWrite(rojo,LOW);
delay(r);
  }
  for(int i=0; i<vv; i++){
digitalWrite(verde,HIGH);
delay(v);
digitalWrite(verde,LOW);
delay(v);
  }
  for(int i=0; i<r2v; i++){
digitalWrite(amarillo,HIGH);
delay(r2);
digitalWrite(amarillo,LOW);
delay(r2);
  }
}
