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
## 