# Datatypes
## Kwantitatief

- **Interval/Continu**: meetbare verschillen zonder nulpunt (temperatuur, IQ)
- **Ratio/Discreet**: meetbare verschillen met absoluut nulpunt (neerslag, afstand)
## Kwalitatief

- **Nominaal**: unieke, aparte observaties (bodemtype, nationaliteit,..)
- **Ordinaal**: observaties met rangorde groter/kleiner
# Steekproef

- Meestal **onmogelijk** om over **volledige populatie** iets te weten te komen
	-> steekproef
# Types Statistisch Onderzoek
````col
```col-md
## Waarnemingsonderzoek
- **Twee of meer populaties** verschillen in karakteristiek
- **Willekeurige steekproef** wordt genomen uit beide
### Voordeel
- Individu wordt geobserveerd zoals ze in werkelijkheid zijn
### Nadeel
- Oorzaak en gevolg moeilijk te onderscheiden
- Mogelijkse invloed storende variabelen (**confounding factors**)

> [!Example] Voorbeeld
> Volgen van groep mensen om te kijken wie een bepaalde ziekte ontwikkelt
```
```col-md
## Experimenteel Onderzoek
- Twee of meer steekproeven worden **uit 1 populatie** genomen
- **Verschillende experimenten** op beide steekproeven toegepast
### Voordeel
- Oorzaak en gevolg worden duidelijk uitgeklaard
### Nadeel
- Steekproeven vertegenwoordigen niet volledige populatie
- Kunstmatige setting kan effect hebben op resultaten

> [!Example] Voorbeeld
> Klinische trial met nieuwe medicatie
```
````
# Beschrijvende Statistiek

> [!Warning] Belangrijk
> Begin altijd met samenvattingen van een dataset door kerncijfers en grafieken
> 
> In een **tabel**:  gemiddelde, min/max, mediaan...
> In een **grafiek**: histogram, boxplot..

## Grafische Methodes
### Histogram

X-as: **variabele** - categorieen
Y-as: **frequentie** 
	-> *absoluut* of *relatief* (%)

> [!Example] Voorbeeld
> ![[Pasted image 20240919123626.png]]
> <sup>Schoolgaande kinderen per gezin</sup>
> Waarbij (a) de absolute frequentie gebruikt (aantal gezinnen) en (b) de relatieve frequentie
### Boxplot

````col
```col-md
flexGrow=1
===
**Snorharen & uitschieters**

**Box**:
- Bovenste zijde is 75e percentiel of derde kwartiel Q<sub>3</sub>
- Lijn middenin box geeft *mediaan* weer
- Onderste zijde is 25e percentiel of eerste kwartiel Q<sub>1</sub>

**IQR**: Interkwartielafstand (afstand tussen Q<sub>1</sub> en Q<sub>3</sub>)

```
```col-md
flexGrow=1
===
![[Pasted image 20240919133106.png|164]]
```
````
### Error Bar
````col
```col-md
flexGrow=1
===
**Punt**: gemiddelde
**Lijn**: *spreiding* rond gemiddelde

Minder effectief voor asymetrische verdelingen
```
```col-md
flexGrow=1
===
![[Pasted image 20240919134517.png|325]]
```
````
## Numerieke Methodes
### Centraliteitsmaten

- **Gemiddelde** (gevoelig voor extreme waarden, goed bij symmetrische verdeling)
- **Mediaan**: Te verkiezen boven gemiddelde bij assymetrische verdeling
- **Modus**: meest voorkomende waarde
- **Gegroepeerd gemiddelde**: 
	- *Klassemidden * frequentie*, alle *producten optellen* en *delen* door *totale frequentie*
		-> ∑(f * x<sub>m</sub>) / ∑ f
		-> waarbij f de frequentie is, en x<sub>m</sub> het klassemidden
### Spreidingsmaten

- **Minimum & maximum**
- **Spreidingsbreedte** (*'range'*): maximum - minimum
- **Interkwartielafstand (IQR)**: maat van spreiding voor middelste 50% van de waarden
	-> positie Q<sub>1</sub> berekend door *(n+1)/4* te doen
- **Variantie** (s<sup>2</sup>): maat voor afwijking tegenover gemiddelde
- **Standaardafwijking** s
- **Variatiecoefficient**: vergelijking variabiliteit tussen verschillende verdelingen
- **Scheefheid/skewness**: helling histogram
- **Kurtosis**: platheid/puntigheid histogram
	-> leptokurtosis: >3
	-> platykurtosis: <3
- **Standaardscore**: hoeveel zijn standaardafwijkingen verwijderd van gemiddelde
# Beschrijvende Ruimtelijke Statistiek
## Beperkte Afstanden
*Euclidische* (Pythagoras) of *Manhattan*-afstand
## Afstanden op Mondiale Schaal
*Grootcirkelafstanden*: boog of astand op een bol tussen 2 punten P1(a1, b1) en P2(a2, b2)

## Zwaartepunt of Centroid
**Gemiddelde X en Y**, eventueel met gewichten
## Standaardafstand
Ruimtelijke *variatie* van locaties rond centraal punt (ruimtelijke standaarddeviatie)

## Hoekgegevens
*Circulair* **histogram of roosdiagram** indien relevant voor data

> [!Example] Voorbeeld
> Windrichting o.b.v. 146 observaties
> 
> ![[Pasted image 20240919163623.png|252]] ![[Pasted image 20240919163643.png|226]]

# Specifieke Aandacht voor Ruimtelijke Data

- ***Modifable Areal Unit Problem*** (MAUP): resultaten van statistische analyses worden beïnvloed door de zonering van de geaggregeerde data
- ***Gerrymandering***:  **manipuleren** van **grenzen** van **kiesdistricten** om een politiek voordeel te halen
- ***Grensovergangen***: **fenomenen buiten studiegebied** kunnen deze in het studiegebied beinvloeden