# API description
Description of the methods offered by this class:  

```c++
LedRGB::LedRGB(int RedLedPin, int GreenLedPin, int BlueLedPin)
```
> Initialize the LED. Use PWM digital outputs.  
> _parameters_: the 3 pins where the RGB cathodes of the LED are connected.

```c++
void LedRGB::switchOFF()
```
> Switch off the LED.  
> With an RGB LED Common-Anode: the LED lights on LOW level, ans switch off on HIGH level.

```c++
void LedRGB::setColorRGB(int Red, int Green, int Blue)
```
> Switch on the RGB LED with the given R,G,B color.  
> _Red_: value between 0 and 255.  
> _Green_: value between 0 and 255.  
> _Blue_: value between 0 and 255.  

```c++
void LedRGB::setColorHSL(int Hue, int Saturation, int Lightness)
```
> Light the LED with the given color.  
> _Hue_ : 0..255  
> _Saturation_: 0..255	As the LED cannot display grey, a low saturation is some kind of white  
> _Lightness_: 0..255

```c++
void LedRGB::setFastColorHSL(int Hue, int Lightness)
```
> Light the LED with the given color.  
> _Hue_       : 0..255  
> _Luminosity_: 0..255  
> This function does not use the trigonometry, so the execution time is faster.  Saturation is fixed to 100%.  

```c++
float LedRGB::fastSin(float value)
```
> Fast Sinus function.  
> _value_: value in radian (0..2xPI).  

```c++
float LedRGB::fastCos(float value)
```
> Fast Cosinus function.  
> _value:_ value in radian (0..2xPI).  

-----
Available on GitHub @Sphinkie/LedRGB
