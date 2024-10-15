#Øving 2 - Kalkulasjoner



# Tutorial - Matteoperasjoner del 1: Vanlige operatorer, parenteser, presedens

Det er mange likheter mellom Python og vanlig matematisk skrivemåte av aritmetiske uttrykk, men også noen forskjeller.

Tabellen under oppsummerer det mest grunnleggende:

| Matematikk        | Python           | Merknad                                                                                                                                                  |
|-------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| a + b             | a + b            | Det er vanlig å sette et mellomrom på hver side av + men ikke påkrevd. Kunne også ha skrevet a+b. Samme gjelder for andre regneoperatorer. Smak og behag, men litt luft gjør ofte uttrykk lettere å lese. |
| a - b             | a - b            | Bruk det vanlige bindestrek-tegnet for minus                                                                                                              |
| a · b             | a * b            | Bruk stjerntegn (asterisk) for multiplikasjon                                                                                                             |
| ab                | **NEI**          | I Python må gangetegn **alltid** skrives eksplisitt, kan ikke utelates                                                                                    |
| a : b             | a / b            | Vanlig skråstrek brukes for divisjon, **ikke** kolon eller horisontal brøkstrek                                                                           |
| a<sup>b</sup>     | a ** b           | Dobbel stjerne for potens. De to stjernene må stå kloss inntil hverandre.                                                                                 |
| [(a + b) * c - d] | ((a + b) * c - d)| I matematisk notasjon brukes av og til ulike parentes-symboler () [] {} hvis det er uttrykk med flere nivåer av parenteser nøstet inn i hverandre. I Python må vanlig parentes () brukes for **alle** nivåer. [] og {} har en annen betydning. |
