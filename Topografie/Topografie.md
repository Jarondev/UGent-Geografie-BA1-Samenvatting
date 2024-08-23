- [Inleiding](#Inleiding)
	- [Geschiktheid toestel voor metingen](#Geschiktheid%20toestel%20voor%20metingen)
	- [Types fouten](#Types%20fouten)
- [Eenheden](#Eenheden)
- [Instrumentarium](#Instrumentarium)
	- [Vizierlijn](#Vizierlijn)
	- [Kijkers](#Kijkers)
	- [Onderdelen instrumenten](#Onderdelen%20instrumenten)
- [Hoogtemetingen](#Hoogtemetingen)
	- [Hulpmiddelen](#Hulpmiddelen)
	- [Types](#Types)
		- [Absoluut](#Absoluut)
		- [Relatief](#Relatief)
		- [Trigonomische hoogtemetingen](#Trigonomische%20hoogtemetingen)
- [Hoekmetingen](#Hoekmetingen)
	- [Zenithale hoekmeting](#Zenithale%20hoekmeting)
	- [Horizontale hoekmeting](#Horizontale%20hoekmeting)
	- [Metingen](#Metingen)
		- [Veelhoeksmeting/polygonatie](#Veelhoeksmeting/polygonatie)
		- [Vrije stationnering/resectie/zijwaardse insnijding](#Vrije%20stationnering/resectie/zijwaardse%20insnijding)
		- [Voorwaartse insnijding](#Voorwaartse%20insnijding)
		- [Achterwaardse insnijding](#Achterwaardse%20insnijding)
		- [Hoogtebepaling van een onbereikbaar punt](#Hoogtebepaling%20van%20een%20onbereikbaar%20punt)
- [Afstandsmetingen](#Afstandsmetingen)
	- [Rechtstreekse methodes met meetband](#Rechtstreekse%20methodes%20met%20meetband)
		- [Nauwkeurigheidsmodel](#Nauwkeurigheidsmodel)
	- [Stadimetrische afstandsmeting (optisch)](#Stadimetrische%20afstandsmeting%20(optisch))
	- [Electromagnetische afstandsmeting](#Electromagnetische%20afstandsmeting)
		- [Puls-generatie & tijdmeting](#Puls-generatie%20&%20tijdmeting)
		- [Fazeverschilmeting](#Fazeverschilmeting)
- [Waterpassing](#Waterpassing)
	- [Afstellen](#Afstellen)
		- [Aanbevelingen](#Aanbevelingen)
	- [Fouten](#Fouten)
		- [Waarnemer](#Waarnemer)
		- [Instrumenten](#Instrumenten)
		- [Atmosfeer](#Atmosfeer)
	- [Formules](#Formules)
		- [Enkelvoudige waterpassing](#Enkelvoudige%20waterpassing)
	- [Nauwkeurigheid](#Nauwkeurigheid)
		- [Hoogtemetingen](#Hoogtemetingen)
		- [Afstandsmetingen](#Afstandsmetingen)
- [Totaalstation](#Totaalstation)
	- [Componenten](#Componenten)
		- [Elektronische compensator](#Elektronische%20compensator)
	- [Opstellen](#Opstellen)
	- [Nauwkeurigheid](#Nauwkeurigheid)
		- [Hoekmetingen](#Hoekmetingen)
		- [Afstandsmeting](#Afstandsmeting)
- [GNSS](#GNSS)
	- [Werking](#Werking)
	- [Nadelen](#Nadelen)
	- [Methodes](#Methodes)

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
### Trigonomische hoogtemetingen
- H= h<sub>A</sub> - h<sub>B</sub> + L.cos(θ) + (L * sin(θ))<sup>2</sup> / 2R
	- H = hoogteverschil tussen punt A en B
	- h<sub>A</sub> = hoogte punt A
	- h<sub>B</sub> = hoogte punt B
	- L = horizontale afstand tussen punt A en B
	- θ = zenithale hoek
	- R = straal van de aarde
# Hoekmetingen
## Zenithale hoekmeting
- Hoek tussen verticale en de richting van het punt
## Horizontale hoekmeting
- Richting viziervlak tov horizontale nulrichting
	-> richting van Y-as = nulrichting
- **Niet doorgeslagen**: horizontale hoek af te lezen op horizontale cirkelrand
- **Doorgeslagen**:  horizontale hoek +/- 200 gon af te lezen op verticale cirkelrand
	-> horizontale hoek is positief in richting van X-as
## Metingen
### Veelhoeksmeting/polygonatie
Coordinaten van onbekende punten meten volgens een veelhoekslijn + bepalen tussenpunten
### Vrije stationnering/resectie/zijwaardse insnijding
Uitzetten van een opgemeten punt door de richtingen te meten naar omliggende aansluitpunten
### Voorwaartse insnijding
Coordinaten nieuw punt berekenen vanuit gekende punten
### Achterwaardse insnijding
Coordinaten onbekend punt berekenen door omliggende aansluitpunten te meten
### Hoogtebepaling van een onbereikbaar punt
Voorwaartse insnijding om planimetrische coordinaten N te bepalen + trigonomische hoogtebepaling
# Afstandsmetingen
## Rechtstreekse methodes met meetband
- **Stap-methode**: trapsgewijs
- **Reductie-methode**: schuine afstand corrigeren met formules
- **Vrij doorhangende meetband**: helling compenseren met hanging meetband
### Nauwkeurigheidsmodel
F<sub>r</sub> = F<sub>a</sub> / s = a/s + b/ sqrt(s) + c
- F<sub>r</sub> = relatieve fout op afstandmeting
- F<sub>a</sub> = absolute fout op afstandsmeting
- a = afstandsonafhankelijke afleesfout
- b = factor toevallige fouten
- c = factor systematische fouten
- s = afstand
## Stadimetrische afstandsmeting (optisch)
Door middel van stadia-draden in de kijker en aflezen boven- en onderdraad
**Nauwkeurigheid**: 0,5-2 mm/100m
L = a + c * H
- L = afstand
- a = optelconstante (K + F)
- c = vermenigvuldigingsconstante (0,5 * cot(ω / 2))
	- ω = hoek tussen boven- en onderdraad
## Electromagnetische afstandsmeting
Met prisma of **puntkenmerk**
**Nauwkeurigheid:** 1-3 mm + 1-3 mm/km
Afstandsfout = a + b * L
- a = 1-3mm
- b = 1-3 ppm
-> bij microgolf: beide 10
### Puls-generatie & tijdmeting
Zendt elektromagnetishce puls uit die wordt rereflecteerd door oppervlak
- Grote afstand (10-15km)
- Grote nauwkeurigheid
- L = t * c / 2
	- L = afstand
	- t = looptijd tussen tijdstip uitsturen en ontvangen
	- c = lichtsnelheid in atmosfeer 
		-> = lichtsnelheid vacuum / brekingsindex atmosfeer
### Fazeverschilmeting
- Meet fazeverschil tussen uitgezonden en teruggekaatste golf
- Types:
	- Electro-optisch (licht)
	- Microgolf (radiogolven)
# Waterpassing
![[Pasted image 20240822202928.png|525]]
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
## Formules
### Enkelvoudige waterpassing
- h = R - J - C<sup>aardkromming</sup> + C<sup>refractie</sup>
	- h = hoogteverschil
	- R = hoogte baak
	- J = hoogte waterpastoestel
	- C = correctie voor aardkromming
#### Aardkromming
- C<sup>aardkromming</sup> = d^2 / 2R
	- C = correctiefactor
	- d = horizontale afstand instrument en meetpunt
	- R = straal van de aarde (6371000m)
#### Refractie:
Wet van Snellius-Descartes
- C<sup>refractie</sup> = n * sin(i)
	- C = correctiefactor
	- n = brekingsindex 
	- i = hoek met de normale op het scheidingsvlak tussen beide milieus
## Nauwkeurigheid
### Hoogtemetingen
| Type           | Afwijking | Optimale afstand |
| -------------- | --------- | ---------------- |
| **Geodetisch** | < 1 mm/km | < 25m            |
| **Ingenieurs** | 1-3 mm/km | < 50m            |
| **Bouw**       | > 3 mm/km | < 100m           |
# Totaalstation
= **electronische theodoliet** + laserafstandsmeting = bijkomende sensoren..
![[Pasted image 20240822203013.png]]
## Componenten
### Elektronische compensator
- Detecteert en corrigeert horizontale hellingen (1D en 2D)
## Opstellen
- **Eerste as verticaal** brengen
	-> draaien aan regelschroeven
	-> verlenging statiefpoten
	-> buisniveau
- **Centreren boven opstelpunt**: schietlood, optisch lood, laserlood
## Nauwkeurigheid
### Hoekmetingen
| Type           | Afwijking      | Dwarsafwijking op 100m |
| -------------- | -------------- | ---------------------- |
| **Geodetisch** | < 0,5 mgon     | 1,5mm                  |
| **Ingenieurs** | 0,5 - 1,5 mgon | 4,7mm                  |
| **Bouw**       | > 1,5 mgon     | 47mm                   |
### Afstandsmeting
- Met **laser**: baak wordt vervangen door prismareflector
# GNSS
![[Pasted image 20240822202836.png|325]]
## Werking
**Code**: meet de tijd die het duurt voor een signal code om van de satelliet naar de ontvanger te reizen
**Fase:** Meet het faseverschil van de draaggolf van het signaal tussen satelliet en ontvanger

4 satellieten:
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
