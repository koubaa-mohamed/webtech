# Labo 2 - reflecties

Naam: Mohamed Koubaa

## 2. Selectors lezen

Welke elementen raakt elke selector? Eén zin per selector.

- a. `header nav ul li a`: dit selecteert alle links binnen de lijstitems in een ul binnen een nav binnen een header. 
- b. `article > p`: dit selecteert alle paragrafen die rechtstreeks in een article staan.
- c. `.uren li:nth-child(3)`: dit selecteert elke li binnen .uren dat het derde kind van de ouder is.
- d. `h2 ~ p`: dit selecteert alle paragrafen die na een h2 staan en dezelfde ouder heeft.
- e. `.rassen li:first-child`: dit selecteert elke li binnen .rassen dat het eerste kind van de ouder is, dit geldt ook in de binnenlijsten.

## 3. Voorspel, dan kijk

Vul de eerste twee kolommen in vóór je de pagina opent. Trede: herkomst, specificiteit, volgorde of overerving (of iets anders, benoem het).

| vraag | mijn voorspelling (kleur) | beslissende trede | uitkomst in de browser | juist? |
|---|---|---|---|---|
| 1 | groen | Herkomst: eigen css wint van de browserstijl | groen | ja |
| 2 | blauw | Volgorde: de laatste regel wint | blauw | ja |
| 3 | rood | Specificiteit: class wint van de elementselector | rood | ja |
| 4 | rood | Specificiteit: .v4 a wint van a; .v4 > a raakt de link niet | rood | ja |
| 5 | blauw | Specificiteit: id wint van de 3 classes | blauw | ja |
| 6 | blauw | Rechtstreekse kleur wint van overerving | blauw | ja |
| 7 | rood | Overerving: kleur komt van de class: .v7 | rood | ja |
| 8 | blauw | Specificiteit: inline stijl wint van de class | blauw | ja |
| 9 | rood | Belangrijkheid: !important wint | rood | ja |
| 10 | groen | Syntaxfout: ontbrekende ; | groen | ja |

Bij welke vraag zat je fout, en wat was de reden? (Alles juist? Welke vraag duurde het langst, en waarom?)

Ik had alle 10 vragen juist. Vraag 10 duurde het langst, omdat ik niet zag dat er een puntkomma ontbrak na font-size: 1.5rem. Daardoor is de volgende kleurdeclaratie ongeldig en blijft de tekst groen.

## 4. De nabouw

- Welke selector koos je voor de links in de navigatie, en waarom geen class?

Ik koos de nav a, omdat die dan alle links binnen de navigatie gaat selecteren. Een extra class is dus niet nodig.

- Welke regel kostte je het meeste tijd, en wat was uiteindelijk de oorzaak?

De regel nav a:hover, nav a:focus kostte me het meeste tijd, omdat ik de : voor focus vergeten was, waardoor de focusstijl niet werkte.

## 6. Je site

- Welke drie waarden staan in je tokenblok, en waarom die?

Mijn tokenblok bevat onder andere de achtergrondkleur #fbf7f0, de tekstkleur #2b2b2b en het lettertype Verdana. De achtergrondkleur geeft de site een neutrale basis, de tekstkleur zorgt voor leesbare tekst en het lettertype houdt de vier pagina's gelijk. Daarnaast staan ook de accentkleur, de gedempte kleur, de tekstmaat en de regelhoogte in het tokenblok.

- Wat verandert er in je site als je één token wijzigt?

Alle regels die dat token met var() gebruiken veranderen mee. Als ik bijvoorbeeld --accentkleur ga aanpassen, veranderen de navigatielinks en koppen samen op alle vier de pagina's. Ik hoef die kleur dus maar op 1 plaats aan te passen.

## Thuis: R2.3 (met AI)

Prompt en onbewerkte output staan in `review/`. Minstens vijf bevindingen, elk met een verwijzing naar de sectie of het foutnummer:

1. De kleuren en lettertypen staan in :root en worden met var() gebruikt. Dat volgt de tokenregel (2.9).
2. De lettergroottes staan in rem. 1rem is normaal 16px, maar hangt af van de browserinstelling (2.8).
3. nav a en footer p zijn eenvoudige selectors. Er staan geen id-selectors of !important in de CSS (2.7).
4. body geeft de tekstkleur, het lettertype en de regelhoogte door aan de andere elementen (2.6).
5. :nth-child(odd) maakt het zebrapatroon. :hover en :focus werken voor de muis en het toetsenbord (2.5).
