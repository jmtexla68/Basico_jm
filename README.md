# Basico_jm
Ejemplo de programa básico de Arduino
/*
Ejemplo de programa basico
Todo programa para Arduino presenta una estructura básica:
1ª parte int x=0; Declarar las variables.
2ª parte void setup() {…} Configuración de Arduino.
3ª parte void loop() {…} Comandos que regirán el
comportamiento de Arduino.

*/
//1º parte, declara variables
int pin3 = 3;  //damos nombre al pin 3
int pin13 = 13;   //damos nombre al pin 13
int estadoPulsador = 0;  //variable para cargar el valor de un pin

void setup() {
  //2º parte, define si los pines van a ser entradas o salidas
pinMode (pin3, INPUT);
pinMode (pin13, OUTPUT);
}
void loop() {
  //3º parte/ instrucciones de programa
  estadoPulsador = digitalRead(pin3);
  if (estadoPulsador == HIGH) {
  digitalWrite(pin13, HIGH);
}
else {
  digitalWrite(pin13, LOW);
}
}
