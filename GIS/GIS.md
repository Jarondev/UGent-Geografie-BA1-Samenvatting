# 1. GIS?
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
# 2. Spatial Data
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
# 3. Spatial Data Modelling
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
→ dikwijls topologisch, aanvullend met afstanden
- Boomnetwerk (hierarchisch)
- Circuitnetwerk (gesloten lus)
## Benaderingen
- **Laaggebaseerd**
	→ laag per thema afhankelijk van kenmerk/gebruik
# 4. Database Management
## Intro
**Data**
- Grote hoeveelheid: veel bronnen, dikwijls automatisch
- Veel soorten: nummers, tekst, afbeeldingen,...
**Databank**: georganiseerde verzameling van gegevens
- Soorten:
	- Eenvoudig (excel)
	- Eenvoudig relationeel
	- Complexe relationeel
	- Niet-relationeel
**Ruimtelijke entiteit**: 
- Ruimtelijke gegevens (waar?)
- Attribuutgegevens (wat?)
**DBMS (Database Management System)**: software om databank aan te maken & te onderhouden
	-> bv. SQL, Oracle
## Waarom databank?
- Toegang tot data is **gecontroleerd en gecentraliseerd**
- Beperkte **redundantie**
- Data wordt opgeslagen onafhankelijk van toepassing
- Eenvoudig te **onderhouden** en updaten
## Relationele Databank
- Relatie tussen tabellen is de basis
- Elke rij is **uniek** (in GIS vaak **locatie**)
- 1 waarde per cel
- **Sleutels linken tabellen**
## Een database maken
1. Data **onderzoeken**
2. Data **modelleren**
	-> maken conceptueel model entiteiten en relaties
3. Databank **ontwerp**
	-> Creeren model in specifiek DBMS
4. **Implementatie**
5. **Onderhoud**
# 5. Data Input and Editing
## Methods of data input
- **Keyboard entry**
	-> manueel, typfouten
- **Manual digitizing**
	-> manueel, voor veel data, indien ruimtelijke data topologie moet hebben
	-> kan fouten hebben afhankelijk van ervaring, schaal, kwaliteit,..
- **Automatic digitizing**
	- **Scanning**
		- **Raster**
		- Problemen: optische distorties, koffievlekken, kwaliteit,..
	- **Line-following**
		- **Vector**
		- Via image-processing software
		- Sterk bij contrasterende en eenvoudige lijnen
- **Electronic Data Transfer**
	- Data verkregen via GPS, LiDAR, satelliet
	- Dikwijls **dataconversie nodig** door vele formaten
## Data Editing
### Fouten detecteren en corrigeren
- Fouten zijn afhankelijk van brondata, encodering, data conversie
### Detecteren
- **Attribuutdata**
	- Manueel vergelijken met oorspronkelijke data
	- Systematisch
		-> onmogelijke waarden, extreme waarden, consistency check, plots/trends
- **Ruimtelijke data**
	- **Visuele vergelijking**
	- Afhankelijk datamodel (vector vs raster) en acquisitie
	- Fouten bij **vectordata**:
		- GIS heeft edit tools om fouten te identificeren en verwijderen
			-> gevaar fouten 
	- Fouten bij **rasterdata**:
		- noise (foute waarden van een pixel)
		- missing entities