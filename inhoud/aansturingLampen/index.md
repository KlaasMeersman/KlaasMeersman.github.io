---
title: Aansturing lampen
---

* **A**(R+B): 39V
* **C**(uit): 15V
* **D**(FR): 12V 
Er moeten metingen gebeuren om nodige lichthoeveelheid (mmol/(m²*s)) te bepalen. We gaan uit van maximaal 

        ((39+15+12)V * 1A  =) 66W

 We willen kunnen meten tussen 3.3W(50mA) en 66W(1A).
	
Volgende punten moeten verder uitgewerkt worden en zijn de eerste stappen die we zullen nemen:

* papers lezen voor nodige lichthoeveelheid (mmol/(m²*s))
* boost-buck convertor voor aansturing: minimaal 39,15,12V. 1A max, eerder 500mA waarschijnlijk
* reverse engineeren van [stroommeter](https://www.digikey.be/en/products/detail/sparkfun-electronics/SEN-14544/9452026). Deze stroommeter kan van 10mA tot 5A meten, dit valt binnen de door ons opgelegde specificaties.
* high voltage input, low voltage output opmap for voltage sensing
* implementatie op één pcb; 3 boostbuck convertors, 3 metingen voor voltage en stroom (controleerbaar met ESP32)

