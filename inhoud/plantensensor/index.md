---
title: Plantenmonitoring
---

Hier kunnen jullie alles terug vinden ivm. het plantenmonitoring. Zoals schema's, PCB ontwerp, datasheets etc. 

Voor de planten werden 2 verschillende soorten PCB's gerealiseerd. De 1e soort is een PCB die een relais aanstuurt. Dit is dezelfde als die bij team water gebruikt wordt. Zij hebben deze ontworpen dus alle info betreffende deze PCB is te vinden bij watermonitoring. De 2e soort PCB werd door ons ontworpen. De PCB's die we ontworpen hebben kunnen voorzien worden van twee SCD40 sensoren en twee grond-vochtigheidsensoren. We hebben echter besloten om slechts 1 SCD40 sensor per bordje aan te sluiten door het dure prijskaartje van de sensor. Aan de hand van de SCD40 kan de CO2, temperatuur en vochtigheid van de lucht gemeten worden. Deze zijn cruciaal voor de groei van de planten en moeten dus gemonitord worden. Zo kunnen de waarden bijgestuurd worden als ze niet goed zijn voor de plantengroei. De grond-vochtigheidsensor kan gebruikt worden om de meten hoe vochtig de grond is en zo de planten extra of minder water de geven.

# Ventilatoren
Er zijn 6 ventilatoren aanwezig, voor elke plantenbak 1. Het hoofddoel van de ventilatoren is zorgen voor de stevigheid van de planten. Er moet wat wind aanwezig zijn om een sterke stengel te krijgen. Daarnaast beïnvloeden de ventilatoren ook de temperatuur en luchtvochtigheid. Als het warmer wordt dan 28°C op 1 van de 3 SCD40 sensoren zullen de ventilatoren aanschakelen. Daarnaast zullen ze ook aanschakelen als de luchtvochtigheid bij 1 van de sensoren groter wordt dan 90%. De ventilatoren die we gebruiken werden uit oude computers gedemonteerd en hebben dus geen geld gekost. Ze werken op 12V, deze 12V wordt geschakeld aan de hand van een relais.

# SCD40

Met de SCD40 kan er in de vertical farm CO2 metingen gebeuren. Dit in een range van 400-2000 ppm. Hierbij is er een accuracy van +_ 50 ppm + 5% reading bij het interval 400 ppm-2000ppm.
Deze kan ook de luchtvochtigheid meten. 
Als laatste meet deze ook de temperatuur dat ook een cruciale rol is in het groeien van planten. Deze heeft een range van -10°C- 60°C. 
De communicatie van deze sensor gebeurd via I2C. 

# Grondsensor

# PCB-design

<iframe src="schematic.pdf" width="100%" height="600px"></iframe>
![](PCB_plantensensor.png)

# Yaml Files 
[Download soil-moisture.yaml](soil-moisture.yaml)
[Download ventilator.yaml](ventilator.yaml)
