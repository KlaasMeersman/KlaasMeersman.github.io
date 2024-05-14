---
title: Aansturing LED's
---

# Left array: Marta Pozzi en Hayato Nakanishi

This LED-array is powered by a [x1 500mA constant current source](https://www.mouser.be/ProductDetail/RECOM-Power/RACT12-500?qs=gt1LBUVyoHnLAK5OjzGrww%3D%3D) and [x1 1400mAconstant current source](https://www.mouser.be/ProductDetail/MEAN-WELL/PCD-25-1400B?qs=%2F%2Bo%2FYLy8OFqnTDCUJjd14g%3D%3D).



---

# Middle array: LED-array M𝔲ήeeв
This LED-array consists of two identical PCB's that are powered in parallel. (look in LED en PCB for schematics of the PCB's).

This LED-array is powered by [x2 1400mA current source](https://www.mouser.be/ProductDetail/MEAN-WELL/LPC-60-1400?qs=O2yOKspD61Aj4Vv%2BmwlI7Q%3D%3D) and [x1 1050mA current source](https://www.mouser.be/ProductDetail/MEAN-WELL/LPC-60-1050?qs=O2yOKspD61CwHxEZesuS%2Fw%3D%3D):

- The 72 red LEDs are powered by one 1400mA current source. It powers the red LEDs on the two PCB's in parallel. Every red LED has 350mA going through it. Every red LED has a forward voltage of 2.09V and 350mA going through it. The power going through the red LEDs is thus (2.09V * 0.35 A * 72 =) 53W.
- The 24 white LEDs are powered by one 1400mA current source. It powers the white LEDs on the two PCB's in parallel. Every white LED has a forward voltage of 2.8V and 700mA going through it. The power going through the white LEDs is thus (2.8V * 0.7 A * 24 =) 47W.
- The 24 blue LEDs are powered by one 1050mA current source. It powers the blue LEDs on the two PCB's in parallel. Every blue LED has a forward voltage of 3V and 175mA going through it. The power going through the white LEDs is thus (3V * 0.175 A * 24 =) 12.6W.



---

# Right array: LED-array Yuta en Jualiang
This LED-array consists of two identical PCB's that are powered in parallel. (look in LED en PCB for schematics of the PCB's).

This LED-array is powered by [x1 1050mA current source](https://www.mouser.be/ProductDetail/MEAN-WELL/LPC-60-1050?qs=O2yOKspD61CwHxEZesuS%2Fw%3D%3D) and [x2 350mA current source](https://www.mouser.be/ProductDetail/MEAN-WELL/APC-12-350?qs=DNaZHaGatO0h%2FjPDgBoC1g%3D%3D).

- The 72 white and 12 blue LEDs are powered by the 1050mA source as their forward voltage is similar enough (Vf~white~ = 2.85V Vf~blue~ = 3V).
    - Every white LED has 3V (due to it being parallel with the blue LEDs) going over it and 75mA going through it. The power going through the white LEDs is thus (3V * 0.075 * 72 =) 16,2W.
    - Every blue LED has a forward voltage of 3V and 75mA. The power going through the blue LEDs is thus (3V * 0.075 * 12 =) 2.7W.

- The 12 red LEDs are powered by one 350mA current source. It powers the red LEDs on the two PCB's in parallel. Every red LED has a forward voltage of 2.15V and 175mA going through it. The power going through the red LEDs is thus (2.15V * 0.175 * 12 =) 4.5W.

- The 12 far red LEDs are powered by one 350mA current source. It powers the red LEDs on the two PCB's in parallel. Every red LED has a forward voltage of 2.15V and 175mA going through it. The power going through the red LEDs is thus (2.15V * 0.175 * 12 =) 4.5W.


__
White: 72  => forward current = 150 (30-480mA), forward voltage typ=  2.85V        |
    => 1050mA x (6/7) = 900mA serie (6/7 bron): 6 serie, x12 voor parallel                   |
        = 72leds/(6/7) bron * (6/7)bronnen = 72leds                                                                 > => 1050/7 = 150mA door elke rail 
                                                                                                                                                           |
Blue: 12 => forward current = 150 (10-240mA), forward voltage typ= 3V                    |
    => 1050mA/7 = 150mA (1/7 bron): 6 serie, x2 voor parallel                                          |
        = 6leds/(1/7)bron * (1/7)bron = 12 leds                                                                           |
                                                                                                                                                        --
Red: 12 => forward current = 130 (10-250mA), forward voltage typ= 2.15V
    => 350mA bron: 6 serie, x2 voor parallel = 12leds/bron * 1bron = 12leds

Far red: 12 => forward current = 175 (10-300mA), forward voltage typ= 2.15V
    => 350mA bron: 6 serie, x2 voor parallel = 12leds/bron * 1 bron = 12leds 


---

# Controlling the LED-sources
The LED sources are controlled by a controller board (POWERLOGGER, LEDs SWITCH board).