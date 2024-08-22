# Inleiding
- Hoek: verschil 2 richtingen
- **Azimuthale hoek**: hoek waarbij Noorden nulrichting is
- **Zenithale hoek:** hoek waarbij zenith de nulrichting (verticaal boven) is 
## Geschiktheid toestel voor metingen
|                   | Afstanden | Hoogteverschil | Richtingen |
| ----------------- | --------- | -------------- | ---------- |
| **Waterpassing**  | -         | ++             | -          |
| **Totaalstation** | ++        | +              | ++         |
| **GNSS**          | ++        | +/-            | ++         |
## Types fouten
- **Toevallige**
	-> *precisie*: maat verspreiding resultaten
- **Systematische**
	-> *juistheid*: overeenstemming exacte waarden
- **Grove**
	-> *betrouwbaarheid*: waarschijnlijkheid van geen vergissingen
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
	- **Collimatorkijker**: om richting te benaderen
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
|            | Optiek                                          | Beeld                             | Vergroting |
| ---------- | ----------------------------------------------- | --------------------------------- | ---------- |
| **Kepler** | *Convexe* objectief & oculairlens               | Omgekeerd                         | Hoger      |
| **Wild**   | *Convexe* objectieflens & *concave* oculairlens | Rechtopstaand door *omkeerprisma* | Lager      |

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
## Formule met aardkromming
# Waterpassing
## Afstellen
#### Grove horizontaliteitsstelling
- Met **doosniveau**
#### Fijne horizontaliteitsstelling
- Met buisniveau (handmatige toestellen)
- Met compensator (**automatische** toestellen)
### Aanbevelingen
- Foutfactoren minimaliseren
- Waterpastoestellen gebruiken met voldoende nauwkeurigheid
	- Hogere precisie buisniveau of compensator
	- Hogere optische vergrotingsfactor
	- Invarbaak gebruiken met baaksteun
- Viseerafstand beperken tot vergrotingsfactor
## Fouten
### Waarnemer
- Verkeerde aflezing
- Parallax bij aflezen
### Instrumenten
- Hellingsfout
- Instrumentencontrole nodig om systematische afwijkingen vast te stellen
- Niet-verticale baak, onjuiste lengte baak, verzakking baak, verwarming baak
- Verzakking, verwarming waterpastoestel
#### Berekenen hellingsfout
- E = h * ((d1 - d2)/d)
	- E = hellingsfout
	- h = hoogteverschil tussen twee punten
	- d1 = afstand naar eerste meetpunt
	- d2 = afstand naar tweede meetpunt
	- d = totale afstand tussen twee meetpunten
### Atmosfeer
- Refractie, ondulatie of luchttrilling
#### Wet van **Snellius-Descartes**:
- n * sin(i) = c
	- n = brekingsindex 
	- i = hoek met de normale op het scheidingsvlak tussen beide milieus
## Formules
### Enkelvoudige waterpassing
- h = R - J - C
	- h = hoogteverschil
	- R = hoogte baak
	- J = hoogte waterpastoestel
	- C = correctie voor aardkromming
#### Aardkromming
- C = d^2 / 2R
	- C = correctie voor aardkromming
	- d = horizontale afstand instrument en meetpunt
	- R = straal van de aarde (6371000m)
### Trigonomische hoogtemetingen

## Nauwkeurigheid
### Hoogtemetingen
- **Geodetisch**: > 1  mm/km; < 25m afstand
- **Ingenieurs**: 1-3 mm/km; < 50m afstand
- **Bouw**: > 3 mm/km; < 100m afstand
### Afstandsmetingen
