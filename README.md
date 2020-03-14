
The color of an object is due to the interaction of the surface of a body with a ray of light and an observer. Color categories are related to objects, materials, light sources, etc., based on their physical properties such as light absorption, reflection, or emission spectra. There are different color spaces that help in quantifying color attributes numerically, for example, RGB color space. In this project the color space being used is RGB color space. The color values are measured using a combination of an LDR and a LED network. In this chapter the theory of color sensing, the differentiation and the different components that are used are discussed and finally, few other projects that are of relevance to this project are summarized and presented. 
 
 The color of an object is due to the interaction of the surface of a body with a ray of light and an observer. Color categories are related to objects, materials, light sources, etc., based on their physical properties such as light absorption, reflection, or emission spectra. There are different color spaces that help in quantifying color attributes numerically, for example, RGB color space. In this project the color space being used is RGB color space. The color values are measured using a combination of an LDR and a LED network. In this chapter the theory of color sensing, the differentiation and the different components that are used are discussed and finally, few other projects that are of relevance to this project are summarized and presented. 
 
 The Arduino is controlling the LEDs. Each group of the LEDs has to have a variable resistor; to control the 5 volts that the Arduino feeds and make sure all the LEDs has exactly the same brightness to avoid having major errors in the intensity which the LDR detects. A resistor should be used with the LDR to take the voltage difference in between. As the light intensity increases, the LDRâ€™resistance will keep decreasing so that the voltage .The Light from the LED is reflected by an object to the LDR. The black rectangle in Figure-3 represents a barrier to insure the light is the reflected one, not from the LED directly. 
 
 The voltage dropson the LDR when each of Red, Green and Blue LEDs are on separately is measured. Each group color of LEDs will turn on for 0.5 second and then turn off. When the LED color matches the color of the surface then it will have less voltage on that LED timing. For example, if the object is red, the red LED will have less voltage than the blue and green when it is on.  If the object color is orange, the voltage will decrease in the same rate but slightly different from the Red. 
















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
