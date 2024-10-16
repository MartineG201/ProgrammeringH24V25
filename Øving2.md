#Øving 2 - Kalkulasjoner
##Læringsmål:
-Basisferdigheter, sekvensiell programmering
-Utføre enkle kalkulasjoner

I denne oppgaven skal du lære hvordan du skriver matematiske uttrykk for å gjøre utregninger i Python.


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
| [(a + b) ·  c - d] | ((a + b) * c - d)| I matematisk notasjon brukes av og til ulike parentes-symboler () [] {} hvis det er uttrykk med flere nivåer av parenteser nøstet inn i hverandre. I Python må vanlig parentes () brukes for **alle** nivåer. [] og {} har en annen betydning. |

**Presedens** mellom operatorer fungerer som i matematikken.
- Multiplikasjon og divisjon har høyere presedens enn addisjon og subtraksjon.
- 3 + 2 * 5 blir 13, fordi * gjøres før +.
- 5 - 1 / 2 blir 4.5, fordi / gjøres før -.
- Potens har høyere presedens enn multiplikasjon og divisjon.5 * 2 ** 3 blir 40, fordi ** gjøres før *.
- Parenteser kan brukes for å få en annen rekkefølge på regneoperasjonene:(3 + 2) * 5 blir 25, fordi + gjøres før *.
- (5 - 1) / 2 blir 2, fordi - gjøres før /.
- (5 * 2) ** 3 blir 343, fordi * nå gjøres før **.
- Hvis du skal "oversette" et matematisk uttrykk med parenteser til Python, bruk parenteser på samme sted også i Python-koden.

## a) Korrekt programmering av aritmetiske utrykk
 Fyll inn riktig Python-kode i stedet for None på samme måte som vist i de tre øverste linjene,
 Kjør deretter programmet for å se at det virker (kjør gjerne hver gang du har fullført en ny linje, så du får testet en og en).
 
```{python}
print('1+2(−3) =', 1 + 2 * (-3))
print('[(3+5·2) + 1] : 2 =', ((3 + 5 * 2) + 1) / 2)
print('-3^2+5*3-7 =', -3**2 + 5 * 3 - 7)
#1)
print('5:2-4 =', None)
#2)
print('5·12+6-1 =', None)
#3)
print('3(5+2) =', None)
#4)
print('4[(5+3):2 +7] =', None)
#5)
print('(−4)^(-3)+5·(3−7:2) =', None)
```
Hvis du har gjort det riktig skal du få ut dette på skjermen: 
```{python}
1+2(-3) = -5
[(3+5· 2)+1]:2 = 7.0
-3^2 + 5*3 - 7 = -1
5:2-4 = -1.5
5· 12+6-1 = 65
3(5+2) = 21
4[(5+3):2 +7] = 44.0
(-4)^(-3)+5·(3-7:2) = -2.515625
```


## Tutorial - Matteoperasjoner del 2: Heltallsdivisjon og Modulo:

I tillegg til vanlig divisjon `/` har Python også heltallsdivisjon som skrives `//` og modulo som skrives med operatoren `%`.

Heltallsdivisjon og modulo minner om måten du lærte divisjon på barneskolen før du hadde lært desimaltall, altså med hele tall og rest.

Tabellen under illustrerer hvordan disse operatorene virker:

| Uttrykk i Python | Resultat | Forklaring |
|------------------|----------|------------|
| 17 / 5           | 3.4      | Vanlig divisjon |
| 17 // 5          | 3        | Heltallsdivisjon, gir hvor mange hele ganger nevneren 5 går opp i telleren 17 |
| 17 % 5           | 2        | Modulo, gir resten av 17 // 5, dvs. de 2 som blir til overs |
| 7.75 / 2.5       | 3.1      | Vanlig divisjon |
| 7.75 // 2.5      | 3.0      | Heltallsdivisjon, gir hvor mange hele ganger nevneren 2.5 går opp i 7.75. Her blir svaret et flyttall (3.0) heller enn heltallet 3, fordi teller og nevner er flyttall. |
| 7.75 % 2.5       | 0.25     | Modulo, Resten av 7.75//2.5 er 0.25 fordi 2.5 * 3.0 er 7.5 |

Heltallsdivisjon og modulo har en rekke nyttige bruksområder i programmering.

Ett eksempel er regning med enheter som aggregeres på andre måter enn det typiske 10, 100, 1000, slik som 60 sekund per minutt, 60 minutt per time, 24 timer per døgn, 7 døgn per uke.

Koden under viser hvordan `//` og `%` kan brukes til slike beregninger. Prøv å kjør den.

```python
print(215, "sekund blir", 215 // 60, "minutt og", 215 % 60, "sekund.")
print(53, "dager blir", 53 // 7, "uker og", 53 % 7, "dager.")
```
