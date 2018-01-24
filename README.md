# LedRGB
Arduino library for RGB led

## API description
Description of the methods offered by this class:  
  
LedRGB::LedRGB(int RedLedPin, int GreenLedPin, int BlueLedPin)
Initialize LED RGB
parameter: the 3 pins where  the RGB cathodes of the LED are connected
use PWM digital outputs
-----------------  
void LedRGB::switchOFF() 
Switch off the RGB LED
Avec une LED RGB anode commune : la LED s'allume sur niveau BAS, et s'éteint sur niveau HAUT
-----------------  
void LedRGB::setColorRGB(int Red, int Green, int Blue)  
allume la LED RGB , avec la couleur R,G,B demandée
reçoit une valeur comprise entre 0 et 255 par composante couleur
-----------------  
void LedRGB::setColorHSL(int Hue, int Saturation, int Lightness)  
Light the LED with the specified color
parameters:
Hue : 0..255			
Saturation: 0..255	As the LED cannot display grey, a low saturation is some kind of white
Lightness:	0..255
-----------------  
void LedRGB::setFastColorHSL(int Hue, int Lightness)  
Light the LED with the specified color.
Hue       : 0..255
Luminosity: 0..255
This function does not use the trigonometry, so the execution time is faster.  
Saturation is fixed to 100%.  
-----------------  
float LedRGB::fastSin(float value)  
Fast Sinus function.  
value: value in radian (0..2xPI).  
-----------------  
float LedRGB::fastCos(float value)   
Fast Cosinus function.  
value: value in radian (0..2xPI).  


