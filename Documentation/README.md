# DOCS SINA

La documentation pour SINA se trouve ici. Lisez la notice d'indentification des versions et la list des modules coeurs ci-dessous, puis aventurez-vous dans l'aperçu des versions. À l'heure de l'écriture de ce document, "V2 Half-Stack Quad MC [WIP]" a le diagramme d'aperçu le plus complet.

## Identification de version

| Version | MàJ principale |
|-|-|
|V1| Version publique originale de SINA|
|V2|  MàJ des méthodes de calcul du coeur (en développement)|
|V3| MàJ "Lighthouse"|

## Modules coeurs pour V2/3

| Nom | Utilité | Version
-|-|-
Lighthouse | ***[Hors des vaisseaux]*** Smart Transmitting node, Makes it's position public such that it's transmitter can be used as a fixed reference point for the ISAN system |V3
Scanner | YOLOL program to find 4 Reference points for use by the rest of the positioning system| V2, V3
Decoder | Decodes the messages of lighthouses selected by the scanner | V3
Datastore | Stores coord information on Dev-Transmitters, made availible to the Inversion engine on selection by the Scanner | V2, V3
Inversion Engine |  Performs the necessary 4x4 matrix Inversion & some additional calculations to create the operating constants for Axis/Position processors (Potentially off-ship, will be for Micro) | V2, V3
Axis processor | Uses axis constants & receiver signal to calculate the position of the ship on **one** axis, ships will have 3 of these. (The multi-chip version of a Position Processor) | V2, V3
Position Processor | Will calculated the X,Y,Z position of the craft based on axis constants & receiver input. (Compacts the three Axis processors onto one chip at the cost of speed.)| V2, V3


#### Sub-version identifiers 

| Identifier | Meaning | Applicable to:
|-|-|-|
| Mono **(M)** | Uses a single receiver core | * |
| Quad **(Q)** | Uses **four** receiver core | * |
| SC | Single Chip | *, assume this if MC not stated|
| MC | Multiple Chip | V2, V3|
| Isolated **(I)** | Hardcoded to use only original 4 dev transmitters | *,assume if stack-ness not stated|
| Half Stack **(HS)** | Able to use any 4 transmitters where coords are hardcoded , Expected to ship with Dev transmitter scanner* | V2, V3 |
| Full Stack **(FS)** | Able to use any 4 of a vast network of Lighthouse nodes for maximum position coverage | V2, V3
| Micro | Offloads some stack components to a special lighthouse-like node AKA "a Guidestar" for minimal components on-ship.| V3+


*Dev Transmitter scanner will allow any for automatic selection of 4 dev transmitters, which will then be used to configure the positioning system
