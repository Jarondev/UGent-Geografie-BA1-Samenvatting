# Semiology 
	= Study of signs and symbols and their use or interpretation

|          Type           | Compatible Data Type |                                                   Extra Info                                                   |
| :---------------------: | :------------------: | :------------------------------------------------------------------------------------------------------------: |
|     **Shape/Form**      |     Qualitative      | Can be pictoral/associative/abstract<br>Associative: shape suggests feature symbolized (triangle for mountain) |
|        **Size**         |     Quantitative     |                                                                                                                |
|     **Orientation**     |       Nominal        |                                            Direction of the symbols                                            |
| **Perspective height**  |  Interval and ratio  |                                    Less used (for eg. population of states)                                    |
|       **Spacing**       |     Quantitative     |                                          Changes in distance between                                           |
|     **Arrangement**     |       Nominal        |                                                                                                                |
|    *Color*: **Hue**     |         All          |                               Appropriate for nominal data (eg. blue for water)                                |
| *Color*: **Lightness**  |     Quantitative     |                                      Light = smaller value, dark = larger                                      |
| *Color*: **Saturation** |     Quantitative     |                                       How pure the color is (grayscale)                                        |
## Quantitative Data
Suitable if its easy to see **big-small, high-low, dark-light patterns**
## Qualitative Data
Suitable if no clear hierarchy (eg. river or building)
## Perceptual Effects
Perception might be influenced by other aspects of the map
# Colors
## Purpose
- **Clarification** main message (eg. land vs water)
- **Highlight** information (deep vs shallow water)
- Show **variations** in data

Often culture-dependent but several *universal*:
- Warm colors: red/orange/yellow
- Cool colors: blue/purple/green
-> temperature uses *warm for hot areas* and *cool for colder*

***Check for cultural meaning if you are mapping for global audience***
## Models
- **Additive**: color by adding or transmitting light (eg. in digital screens)
- **Subtractive**: color by light absorption or reflection (eg. in printing)
## Dimensions
### Hue
Sensation we perceive when light of a **specific wavelength** reaches eye
### Brightness
How **dark or light** color is with a constant hue
### Saturation
Purity, intensity, **colorfulness** of a hue
## Color Models
### Hardware-oriented
#### RGB
- **Additive**
- Defined by portions of R,G and B (up to 256)
	[+] Relates nicely to *method on display*
	[-] Hue, saturation and lightness not inherent
	[-] Equal steps do not correlate to equal visual steps 
#### CMY(K)
- **Subtractive**
- Like mixing ink
- Same pros/cons as RGB
- *K-variant*: black as additional color
### User-oriented
#### HSV/HSB
	= Hue, Saturation, Brightness/Value
- Projected on circle, higher saturation near edge
#### Munsell System
### CIM (neither hardware or software)

## Color Schemes
### Quantitative Schemes
#### Sequential Schemes
- **Lightness for ordered data**
	- Darker for higher data values
- Include hue differences to provide contrast between colors
- 3-9 classes to keep them distinct
#### Diverging Schemes
- Emphasize both **high and low** values
	- mean values in lighter color
	- extremes more dark hues
### Qualitative Schemes
For unordered features (**nominal data**); varying hues

>[!Error] Waarschuwing
>A well defined qualitative scheme should NOT suggest that data is ordered

If *logical relationships* exist -> *echo* them with related colors
**Use color conventions** if applicable (blue - water; green - forest)
