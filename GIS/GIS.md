# Hoofdstuk 1: GIS?
## Definitie
- Veel definities: afhankelijk van wie
- GIS is een **computersysteem** dat instaat voor **beheer en analyse** van **geografische gegevens**
## Componenten
- Computersysteem
- Gegevens (**dataware**)
- Gegevensbeheer en analyse (**orgware**)
- Mensen en GIS (**humanware**)
## Spatial data
= **geografische gegevens**
- Bestaat uit 
	- positie
	- verbindingen
	- attributen
- **Gegevensinvoer**! 
	→ GIGO (Garbage In, Garbage Out)
- Moeten goed gestructureerd zijn
	→ via **DBMS**
- Gegevenstransformatie:
	- Raster/vector
	- Digitalisatiefouten opkuisen
## Mensen en GIS
- 1 tot veel gebruikers
- **Geograaf klei tussen informaticus en domeinspecialist**
# Hoofdstuk 2: Spatial Data
## Intro
- Data: ruwe getallen zonder context
- Informatie: data met betekenis en context
## Kaarten en inzichten
- **Soorten**:
	- Thematisch
	- Topografisch
	- Schets
- **Process** om kaart te maken:
	- **Doel** (purpose):
		→ bepaalt ruimtelijke nauwkeurigheid, nodige gegevens & schaal
	- **Schaal** (observatiezone)
	- **Ruimtelijke entiteiten** bepalen
		→ **punt**: kleine zaken
		→ **lijn**: geordende opeenvolging punten
		→ **vlak (polygoon)**: gesloten verzameling lijnen
	- **Voorstelling**: afhankelijk van schaal
	- **Generalisatie**
		→ simplificatie detail afhankelijk van schaal, benadrukking,... → selectie, vereenvoudig, vetplaatsing, afronding & verbetering
	- **Projectie**: afhankelijk vandoel & gebied
	- **Ruimtelijk referentiesysteem**: 2D, 3D?
		- **Geografisch** coordinatensysteem: **lengte- en breedtegraad**
		- **Rechthoekig** coordinatensysteem: 2D met **grid** (kleine gebieden) 
		- **Niet**-coordinatensysteem: **beschrijvende code** ipv coordinaten
			→ beter voor bv postbode
	- **Topologie**: eigenschappen objecten in de ruimte (geometrische relaties)
		→ 4-intersection matrix
		![[Pasted image 20240718201616.png]]
## Karakteristiek
### Attributen
- **Nominaal**: gegevens zonder rangorde of volgorde (bv. geslacht)
- **Ordinaal**: gegevens met inherente volgorde (bv. rangen in een wedstrijd)
- **Interval**: gelijke afstanden tussen waarden zonder nulpunt (bv. kalenderdata, temperatuur)
- **Ratio**: interval met nulpunt (bv. lengte, gewicht)
### Temporeel
- Lineair, vertakt, cyclisch
## Bronnen
- Volkstellingen en enquetes
- Luchtfoto's
	→ verticaal vs obliek
- Sattelietbeelden
- GPS
# Hoofdstuk 3: Spatial Data Modelling
## Entity Definition
- Probleem selecteren entiteiten
	- Wereld is dynamisch en niet statisch
	- Entiteiten zijn afhankelijk van toepassing
	- Schaalafhankelijk
	- Objecten kunnen discreet of continu zijn
	- Soms vage grenzen
## Spatial Data Models
- **Raster**
	- ruimtelijke eenheid = **pixel**
	- **celgrootte** bepaalt resolutie
	- beperkt voor cartografie
- **Vector**
	- **reele getallen**
	- **meeteenheid** bepaalt resolutie
	- objectgericht
### Douglas-Peucker algoritme
- algoritme om een curve te transformeren naar een gelijkaardige curve met minder punten
![[Pasted image 20240719152605.png]]
## Spatial Data Structures
### Raster Data Structures
- **Run Length Encoding (RLE)**
	- **Lijn per lijn** opgeslagen
	- Geen coordinaten nodig
- **Block Encoding**
	- RLE in 2 dimensies
	- Coordinaten zijn nodig
	- Opgeslagen op **block size** (1, 4, 9,...)
- **Chain Coding**
	- Ketting beschrijft grens (boundary)
	- Geen info over binnenkant entiteit
- **Quadtree**
	- Recursieve subdivisies van vierkanten
		→ oppervlak wordt steeds opgesplits in 4 delen tot nodige resolutie bereikt is
- **Spaghetti structure**
	- Opeenvolging van punten
	- Heeft enkel X,Y opgeslagen
	- Redundante informatie
- **Topological data structure**
	- Punt: een locatie
	- Lijn: van beginpunt naar eindpunt
	- Polygoon: geordende verzameling punten
## Modeling Surfaces
### DTM
- Modellen die hoogte zonder objecten weegeven
- Meestal verkregen door LiDAR of fotogrammetrie
### Raster
- Grid van hoogtewaarden
- Accuraatheid afhankelijk van complexiteit en resolutie
### Vector
- **Vector grid**
	→ nabootsing rasterbenadering
- **Triangulated irregular network**
	- Constructie **driehoeken**
		→ hoekpunten: pieken, depressies
		→ zijden: kammen, valleien
		→ oppervlakten: gradient
	- Veelgebruikt in complex terrein, weinig in vlak
## Modelling Networks
**Netwerk**: locaties verbonden door segmenten waar langs transport/communicatie mogelijk is
- Boomnetwerk (hierarchisch)
- Circuitnetwerk (gesloten lus)
- 