---
title: Planten sensoren
---

Hier kunnen jullie alles terug vinden ivm. de plantensensoren. Zoals schema's, PCB ontwerp, datasheets etc. 

De PCB die we ontworpen hebben kan voorzien worden van twee SCD4X sensoren en twee grond-vochtigheidsensoren. 
SCD4X kan de CO2, temperatuur en vochtigheid van de lucht meten. Deze zijn cruciaal voor de groei van de planten om te monitoren. 
De grond-vochtigheidsensor kan gebruikt worden om de meten hoe vochtig de grond is en zo de planten extra of minder water de geven.

# SCD4X

Om de planten goed te voorzien van 

# PCB-design

<iframe src="schematic.pdf" width="100%" height="600px"></iframe>
![](PCB_plantensensor.png)
[Download](soil-moisture.yaml)

<script>
fetch('soil-moisture.yaml')
  .then(response => response.text())
  .then(data => {
    // Assuming YAML data is loaded as plain text
    // You may need a YAML parser library if the data is not in plain text format
    document.getElementById('yamlContent').innerText = data;
  })
  .catch(error => {
    console.error('Error:', error);
  });
</script>

