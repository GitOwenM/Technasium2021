# PvA

### De opdrachtgever:
Richel Bilderbeek, richel@richelbilderbeek.nl.

### De opdracht:
Richel doet zelf onderzoek naar vaccins, hierbij gebruikt hij 2 verschillende modellen (Epitope Predictions en MHCnuggets). Deze modellen voorspellen de sterkte van verschillende peptidebindingen? (Een IC50-waarde?) in een cel bij verschillende haplotypes. Dit kan gebruikt worden om betere vaccins te maken. Het probleem dat hierbij komt kijken is dat deze 2 modellen soms compleet verschillende uitkomsten hebben bij dezelfde input. Dit is in onderstaande afbeelding te zien, de uitkomsten van het ene model staan op de x-as, die van het andere model op de y-as. Het is aan ons om uit te zoeken waarom deze modellen verschillende uitkomsten geven. Richel gaf een goede analogie: stel je hebt twee thermometers, de ene geeft de temperatuur weer in graden Celsius en de andere in Fahrenheit. De thermometers geven beide verschillende getallen weer, maar de temperatuur is hetzelfde. Wat er hier echter gebeurt is dat de ene ‘thermometer’ bijvoorbeeld MHCnuggets een hoge IC50 waarde geeft terwijl de andere ‘thermometer’ (Epitope Predictions) dan een hele lage waarde geeft. De ene thermometer zegt dus dat het koud is terwijl de andere zegt dat het warm is. Dit is het probleem. Hierbij hoort ook dat we moeten onderzoeken wat deze modellen precies proberen te voorspellen en wat alle termen betekenen.\
\
![image](https://user-images.githubusercontent.com/68740180/110619936-b8c71900-8198-11eb-8c05-a9c5c1809125.png)
\
Voor meer informatie: https://github.com/richelbilderbeek/ep_vs_mhcn \
\
[RJCB: mooi! Een plaatje!]\
[RCB: warm! Dit is echter niet het grote probleem. Het derde plaatje, echter, met een rode lijn met een negatieve richtingscoeffient toont deze wel]

### Onderzoeksvraag
Hoe en waarom geven de 2 modellen Epitope Prediction en MHCNuggets bij dezelfde input een andere, en soms zelfs compleet de tegenovergestelde, output en hoe is dit op te lossen?

### Individuele delen
Hidde: Verdiepen in de werking van Epitope Predictions.\
Jasper: Verdiepen in de code van dit geval en proberen te runnen in R. Begrip krijgen van werking R. Ook de biologische kant, hoe binden deze peptiden precies? Wat is de biologische betekenis van ic50? etc. \
Owen: Verdiepen in de werking van MHCNuggets.

### Deelvragen
Hoe komt Epitope Predictions aan de resultaten, welke methode wordt gebruikt?\
Hoe doet MHCnuggets dit?\
Is een van de methoden onjuist?\
Waarom zijn de resultaten verschillend?\
Wat betekent dit?\
Is dit een probleem?\
Zo ja, is dit probleem op te lossen en zo ja, hoe?

### Communicatie met team en opdrachtgever
We hebben regelmatig via Discord contact met onze opdrachtgever: we plannen ongeveer elke week wel een gesprek. Richel maakt vaak een planning met punten die in het gesprek aan bod komen. De communicatie binnen het team gaat elke keer via Discord of Teams, tenzij we weer naar school mogen. We hebben elke les wel contact met elkaar.

### Planning
Onze planning is te vinden op: https://github.com/GitOwenM/Technasium2021
