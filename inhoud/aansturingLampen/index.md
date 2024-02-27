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

We werken met 3 convertors:
* 2x [QSKJ DC-DC Adjustable Step-down Buck Converter XL4016 200W](https://www.tinytronics.nl/en/power/voltage-converters/buck-(step-down)-converters/dc-dc-ajustable-step-down-buck-converter-xl4016-200w)
        vervangen potentiometer door digitale potentometer
        we regelen met voltage, en laten we LEDs de stroom die ze willen trekken bij ingestelde voltage
        todo: uitmeten potentiometer waarden voor volgende ingestelde waarden:
                voor **C**:     18,09V bij 750mA
                                17,39V bij 500mA
                voor **D**:     16,32V bij 750mA
                                15,09V bij 500mA

* 1X [50V/12A TL494 Step-Up DC-DC Converter – CV/CC Control](https://handsontec.com/index.php/product/50v-12a-tl494-step-up-dc-dc-converter-cv-cv-control/)