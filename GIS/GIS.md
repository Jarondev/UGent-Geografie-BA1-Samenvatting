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
	1. **Doel** (purpose):
		→ bepaalt ruimtelijke nauwkeurigheid, nodige gegevens & schaal
	2. **Schaal** (observatiezone)
	3. **Ruimtelijke entiteiten** bepalen
		→ **punt**: kleine zaken
		→ **lijn**: geordende opeenvolging punten
		→ **vlak (polygoon)**: gesloten verzameling lijnen
	4. **Voorstelling**: afhankelijk van schaal
	5. **Generalisatie**
		→ simplificatie detail afhankelijk van schaal, benadrukking,... → selectie, vereenvoudig, vetplaatsing, afronding & verbetering
	6. **Projectie**: afhankelijk vandoel & gebied
	7. **Ruimtelijk referentiesysteem**: 2D, 3D?
		- **Geografisch** coordinatensysteem: **lengte- en breedtegraad**
		- **Rechthoekig** coordinatensysteem: 2D met **grid** (kleine gebieden) 
		- **Niet**-coordinatensysteem: **beschrijvende code** ipv coordinaten
			→ beter voor bv postbode
	8. **Topologie**: eigenschappen objecten in de ruimte (geometrische relaties)
		→ 4-intersection matrix
		![[Pasted image 20240718201616.png]]
## KARAKTERISTI
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
- Algoritme om een curve te transformeren naar een gelijkaardige curve met minder punten
![[Pasted image 20240719152605.png|700]]
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
		- Noise (foute waarden van een pixel)
		- Missing entities
## Reprojection, transformation, generalization
- **Herprojectie** naar een gemeenschappelijk projectsysteem
- **Transformatie** naar een gemeenschappelijk coordinaatsysteem
	- Translatie
	- Schaling
	- Roteren
- **Generalisatie**
	- Voor combinatie verschillende schalen
	- Minder opslag en hogere snelheid
	- **Lijngeneralisatie** (line thinning) bij vectordata
		- Verwijdert elk zoveelste punt
		- Behoudt karakteristieken van de vorm
	- **Rasterdata**
		- Aggregatie pixels (geen informatieverlies)
		- Data compactie
		- Filteren

## Edge matching and rubber sheeting
### Edge matching
- **Randen kaartbladen matchen**
- Features matchen
- Topologie herbouwen
- Verwijderen redundante lijnen
### Rubber sheeting
- Typisch bij **herstellen complexe vervorming** of herprojectie met weinig details
- **Controlepunten**
	- Goed herkenbaar
	- Met gekende coordinaat
- **Moeilijkheden**
	- Gebrek geschikte controlepunten
	- Berekeningstijd
## Geocoding address data
- Converteren *niet-geografische* beschrijving (adres, kilometerpaal)
- Gebeurt via geocoders
- **Complex door onduidelijkheden**:
	- Spellingsfouten
	- Afkortingen
	- Andere talen
	- Veranderingen
## Updating and maintaining databases
- Taak van **national mapping agencies**
	-> Informatie Vlaanderen (landmeters) voor Grootschalig Referentiebestand Vlaanderen (GRB)
# 6. Data Analysis
## Measurements
- **Euclidische afstand**: vogelvlucht
- **Manhattan afstand**: snelste route genomen door een grid netwerk
## Queries
![[Pasted image 20240721120446.png|525]]
## Buffering
- Punt, lijn en polygoon
- Gebruik: (vb. welke hotels zijn binnen 200m van een hoofdweg?)
- 1.
	1. **Maak bufferzone** van al het land binnen 200m rondom de hoofdweg
	2. Selecteer hotels via functie **point-in-polygon**
- 2. 
	1. Meet de afstand van **elk hotel** tot hoofdweg met **functie distance**
	2. Selecteer hotels die binnen 200m liggen via **functie select**
## Filters
- Typisch voor **raster**
- Iedere cel krijgt **nieuwe waarde** afhankelijk van oorpsronkelijke waarde & waarde omgevende cellen
- Gebruikte algoritmes: max waarde, meest voorkomende waarde
- Gebruikte fitlers:
	- **Smoothing (low-pass filter)**: gemiddelde (pieken verzwakken)
	- **Edge detection (high-pass filter)**: hoge frequenties doorlaten door te vermenigvuldigen met kernel waarbij som gewichten 0 is
	->  ![[Pasted image 20240721122906.png]]
## Map Overlay
### Vector Overlay
- Point-in-polygon
	-> kijkt welke punten in welke polygoon liggen (bos, veld, stad,..)
		-> soms probleem (wat als het op de grens ligt?)
- Line-in-polygon
	-> splitst lijn in stukken indien nodig afhankelijk van zone waarin het ligt
- Polygon-on-polygon
	- **Union** (OR): combineert alle gebieden en behoudt alle attributen
	- **Erase** (NOT): verwijdert overlappende delen invoerlaag en behoudt niet-overlappende delen
	- **Intersect** (AND): behoudt alleen overlappende delen invoerlagen en combineert attributen van deze gebieden
### Raster Overlay
- **Kaartalgebra** (map algebra)
	- 1 of meerdere lagen als input
	- Omzetting punten, lijnen, polygonen naar rasterdata
	- Herklasseren naar **booleaanse kaart**
		- 1 als voorwaarde wordt voldaan
		- 0 als voorwaarde niet wordt voldaan
- Complexe overlays mogelijk
- **Aandachtspunten**:
	- Resoluties (verrekenen na aggregatie bij slechte resolutie)
	- Verschillende meetschalen
## Spatial Interpolation
-> waarden worden **geschat** door bestaande waarnemingen van omliggende gebieden

**Lokaal/globaal**
**Exact/benaderend**
**Gradueel/bruusk**
**Deterministisch/stochastisch**

|          **Naam**          |                       Attributen                       | Afbeelding                                |
| :------------------------: | :----------------------------------------------------: | ----------------------------------------- |
|   **Thiessen polygoon**    |     Lokaal <br>exact <br>bruusk<br>deterministisch     | ![[Pasted image 20240721132257.png\|172]] |
|          **TIN**           |     Lokaal<br>exact<br>gradueel<br>deterministisch     | ![[Pasted image 20240721132314.png\|179]] |
| **Spatial moving average** | Lokaal <br>benaderend <br>gradueel<br>deterministisch  | ![[Pasted image 20240721132330.png\|175]] |
|     **Trendoppervlak**     | Globaal <br>benaderend <br>gradueel<br>deterministisch | ![[Pasted image 20240721132402.png]]      |
## Surface Analysis
-> oppervlakken van *interpolatie* kunnen worden geanalyseerd (vaak in 2,5D ipv 3D)
### Factoren
- **Helling** (steilte gemeten in graden of %)
- **Aspect** (richting, gemeten in graden tov noorden)
### Weergeven van factoren
- **Analytical hillshading**
	-> berekening locatie schaduw en hoeveelheid bezonning 
- **Curvature**
	-> Beschrijving **verandering helling/aspect**
	Types:
	![[Pasted image 20240721135020.png|325]]
## Visibility Analysis
- Voor **zichtbaarheid** naar **landschappelijke elementen**
- Voor **zichtbaarheid** vanuit **uitkijktorens**
**Viewshed map**: map die laat zien welke gebieden vanaf een specifiek observatiepunt zichtbaar zijn
-> houdt rekening met ooghoogte
-> booleaanse kaart
## Network Analysis
- Shortest path: oplossing -> **Dijkstra-algoritme**
- Dubbele vraag: welke **orde** van stops?, welk **pad** tussen twee stops?