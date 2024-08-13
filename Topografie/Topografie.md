# Inleiding
- **Opmeten** fysische wereld -> voorstelling ervan
- **Uitzetten** voorstelling -> fysische wereld
## Wat?
- Afstanden
- Hoogteverschil
- Hoeken
- Richtingen
## Types fouten
- **Toevallige**
	-> *precisie*: maat verspreiding resultaten
- **Systematische**
	-> *jusitheid*: overeenstemming exacte waarden
- **Grove**
	-> *betrouwbaarheid*: waarschijnlijkheid van geen vergissingen
## Afstandsnauwkeurigheden
|                | Waterpassing | Totaalstation |
| -------------- | ------------ | ------------- |
| **Geodetisch** | 0.3-1mm/km   | 1mm+1ppm      |
| **Ingenieurs** | 1-3mm/km     | 2mm+2ppm      |
| **Bouw**       | 3-10mm/km    | 3mm+3ppm      |
# Eenheden
- 400 gon = 360°
- 2π rad = 360°
- 6400 mil = 360°
	-> 1 rad = 1000 mil
	-> cirkel van 1m diameter op 1km afstand heeft een hoek van 1 mil
		-> 1m diameter/1km afstand = 1mil
# Instrumentarium
## Vizierlijn
- Richten op:
	- **punt, prisma, baak, puntkenmerk**
	=> heeft topografische nagel, fenopalen, klevende tekens, speciale kenmerken
- Richten met:
	- **Niet-optisch vizier** -> kruisdraden door gat
		-> nadeel: blinde hoek, parallax
	- **Collimatorkijker**
		- Om richting te benaderen
		- Glas met signaal
		- Klein (3cm lang, 5mm diameter)
	- **Optische kijker**
		- balans van **gewicht, vergroting en helderheid**
		- **Lichtsterkte**: (lensdiameter/vergrotingsfactor)^2
			-> <1: weinig lichtsterkte
			-> 1-2: gemiddeld
			-> >2: veel lichtsterkte
**Auto focus**:
- Scheidingslens scheidt optische stralen
- CCD meet verschil
## Kijkers
### Kepler
- Optiek: **convexe** objectieflens & oculairlens
- Beeld: omgekeerd
- Vergroting: hoger
### Wild
- Optiek: convexe objectieflens & **concave oculairlens**
- Beeld: rechtopstaand (**omkeerprisma**)
- Vergroting: lager
## Onderdelen instrumenten
- **Vizierlijn**
- **Horizontale referentierichting**
	- Astronomisch
		-> zeer tijdrovend
	- Kompas
		-> minder nauwkeurig
	- Gyroscoop
		-> lange opsteltijd nodig
	- GNSS
		-> werkt **niet ondergronds**
- **Verticale referentierichting**
	- Schietlood
	- Buisniveau (waterpas)
	- Optisch lood
	- Laserlood
	- Compensator
		- Opto-mechanisch
		- Electronisch
- **Stabiele opstelling**
	- Statief
		- Stevig
		- Licht & plooibaar
			-> verplaatsbaar
		- Afstelbaar in hoogte en horizontale zin
- **Energievoorziening: batterijen**
# Hoogtemetingen
## Hulpmiddelen
- Baaksteun
- Doosniveau
- Baakstatief
## Types
### Absoluut
| Naam         | Nauwkeurigheid |
| ------------ | -------------- |
| Barometrisch | 5-10m          |
| GPS          | 3-5m           |
### Relatief
| Naam          | Nauwkeurigheid |
| ------------- | -------------- |
| Barometrisch  | > 1m           |
| GPS           | 20-50 mm/km    |
| Trigonomisch  | 10-50 mm/km    |
| Waterpassing  | 0,3-10 mm/km   |
| Hydrostatisch | < 0,3 mm/km    |
# Hoekmetingen
## Nauwkeurigheden
| Naam       | Nauwkeurigheid | Dwarsafwijking op 100m |
| ---------- | -------------- | ---------------------- |
| Geodetisch | < 0,5 mgon     | 1,5 mm                 |
| Ingenieurs | 0,5 - 1,5 mgon | 4,7 mm                 |
| Bouw       | > 1,5 mgon     | 47 mm                  |
# Afstandsmetingen
## Rechtstreekse methodes
- Stap-methode
- Reductie-methode
	-> schuine afstand corrigeren met formules
- Vrij doorhangende meetband
	-> helling compenseren met hanging meetband
## Stadimetrische afstandsmeting (optisch)
Door middel van stadia-draden in de kijker en aflezen boven- en onderdraad
**Nauwkeurigheid**: 5-15 m/km
## Electromagnetische afstandsmeting
Met prisma of puntkenmerk
### Puls-generatie & tijdmeting
- Grote afstand (10-15km)
- Grote nauwkeurigheid
### Fazeverschilmeting
- Meet fazeverschil tussen uitgezonden en teruggekaatste golf
- Types:
	- Electro-optisch (licht)
	- Microgolf (radiogolven)
# GNSS
## Werking
- 4 satellieten:
	- 3 voor elke dimensie
	- 1 voor synchronisatie
## Nadelen
- Open hemel nodig (niet ondergronds)
- Transformatie coordinaten nodig
- Hoogte minder nauwkeurig
- Black box system
	-> je kan berekeningen niet nakijken
## Methodes
| Naam                     | Techniek | Nauwkeurigheid | Prijs (in eur) |
| ------------------------ | -------- | -------------- | -------------- |
| Absolute plaatsbepaling  | Code     | 5m             | 25-250         |
| DGPS                     | Code     | 5dm            | 2500           |
| RTK                      | Fase     | 5cm            | 25000          |
| Relatieve plaatsbepaling | Fase     | 5mm            | 25000          |
# Totaalstation
## Doeleinden
- Voor grotere hellingen
- Voor grotere afstanden
- Lagere nauwkeurigheid
- Meer paramters
## Opstellingseisen
- Eerste as verticaal brengen
- Centreren boven opstelpunt
- Kalibratie (nulpunt instellen)
- Bij vrije stationnereing:
	- Zichtbare referentiepunten
	- Goede spreiding referentiepunten
## Metingen
### Veelhoeksmeting/polygonatie
Coordinaten van onbekende punten meten volgens een veelhoekslijn + bepalen tussenpunten
### Vrije stationnering/resectie/zijwaardse insnijding
Uitzetten van een gekend punt
### Voorwaartse insnijding
Coordinaten nieuw punt berekenen vanuit gekende punten
### Achterwaardse insnijding
Coordinaten onbekend punt berekenen door omliggende referentiepunten te meten
# Waterpassing
## Instrumentenfouten
- Hellingsfout
- Verloop vizierlijn
	-> optische as is niet uitgelijnd met mechanische as
- Verzakking toestel
- Baakfouten:
	- Niet-verticaal
	- Onjuiste lengte
	- Verzakking
	- Thermische uitzetting
## Atmosfeerfouten
- Refractie (lichtbreking)
- Ondulatie/luchttrillingen
## Afstellen
- Grove horizontaliteit (doosniveau)
- Fijne horizontaliteit (buisniveau/compensator)
## Types
| Naam       | Afstand baak | Fout (mm/km) |
| ---------- | ------------ | ------------ |
| Geodetisch | <25m         | <1           |
| Ingenieurs | <50m         | 1-3          |
| Bouw       | <100m        | 3-10         |