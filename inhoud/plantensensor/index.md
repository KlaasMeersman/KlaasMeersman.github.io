---
title: Plantenmonitoring
---

Hier kunnen jullie alles terug vinden ivm. de plantensensoren. Zoals schema's, PCB ontwerp, datasheets etc. 

De PCB die we ontworpen hebben kan voorzien worden van twee SCD40 sensoren en twee grond-vochtigheidsensoren. 
SCD40 kan de CO2, temperatuur en vochtigheid van de lucht meten. Deze zijn cruciaal voor de groei van de planten om te monitoren. 
De grond-vochtigheidsensor kan gebruikt worden om de meten hoe vochtig de grond is en zo de planten extra of minder water de geven.

# SCD40

Met de SCD40 kan er in de vertical farm CO2 metingen gebeuren. Dit in een range van 400-2000 ppm. Hierbij is er een accuracy van +_ 50 ppm + 5% reading bij het interval 400 ppm-2000ppm.
Deze kan ook de luchtvochtigheid meten. 
Als laatste meet deze ook de temperatuur dat ook een cruciale rol is in het groeien van planten. Deze heeft een range van -10°C- 60°C. 
De communicatie van deze sensor gebeurd via I2C. 

# PCB-design

<iframe src="schematic.pdf" width="100%" height="600px"></iframe>
![](PCB_plantensensor.png)

# Yaml Files 
[Download soil-moisture.yaml](soil-moisture.yaml)
[Download ventilator.yaml](ventilator.yaml)
