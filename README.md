# Iot-mproject
int signal=A0;
int value=0;
void setup()
{
  Serial.begin(9600);         
  pinMode(signal,INPUT);
}
void loop()
{
  delay(500);
  value=analogRead(signal);
  Serial.println(value);
  delay(500);

//different colors

  if (value>100)
  {
    Serial.println("White");
  }
   else if (value<15)
  {
    Serial.println("Black");
  }
  else if (value<= 65 && value >50)
  {
    Serial.println("RED");
  } 
   else if (value>=68 && value<80) 
   {
    Serial.println("Green");
  }
  else if (value<30 && value>20)
  {
    Serial.println("Blue");
  }
}
