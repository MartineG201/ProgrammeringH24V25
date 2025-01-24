# Øving 5



### a)
 Spør brukeren om hvor mange cookies han eller hun ønsker å bake og skriv ut hvor mange ingredienser som trengs for å lage så mange cookies.

 Eksempel på kjøring:

 
```{python}
Hvor mange cookies ønsker du å bake? 24
Antall cookies: 24 
sukker(g): 200.0
smør(g): 160.0
sjokolade(g): 250.0
egg: 1.0
hvetemel(g): 230.0
```

### b) Lag notater i koden din
Når vi lærer oss å kode eller har en veldig stor kode vi prøver å forstå, kan det være lurt å lage notater i python.

Kjør kodene under hver for seg.
```{python}
print("Denne teksten vil komme opp på skjermen")
#Denne teksten kommer ikke til å bli printet. 
#Det blir heller ikke gitt ut en feilkode.
```


```{python}
print("Denne teksten vil komme opp på skjermen")
#Denne teksten kommer ikke til å bli printet.
Men her, hvis du kjører koden, vil du få en feilmelding
```


```{python}
print("Denne teksten vil komme opp på skjermen") #Det er også mulig å skrive en kommentar ved siden av kodelinjene dine
```

Prøv å legg til noen kommentarer i de neste oppgavene du gjør. Det kan jo være lurt å ta screenshot av oppgaver og lagre de til senere, for å øve til neste prøve.


## Sammenligning av strenger


Når man sammenligner to strenger i Python vil strengene sammenlignes karakter for karakter. F.eks. vil et program som sammenligner strengene "Ola" og "Ole" og sjekker om de er like, først sammenligne 'O' mot 'O', så 'l' mot 'l', og til slutt 'a' mot 'e'. Det er først ved sammenligningen av 'a' mot 'e' at det vil bli returnert False


```{python}
a = "Ola"
b = "Ole"
  
print("Sammenligner", a, "og", b)
if a == b:
    print("Navnene er like")
else:
    print("Navnene er IKKE like")
```


Om man derimot sammenligner navnene Markus og Marcus, vil testen av betingelsen returnere False når 'k' blir sammenlignet med 'c'. Det betyr at 'u'  mot 'u' og 's' mot 's' ikke blir sjekket.


```{python}
a = "Markus"
b = "Marcus"
  
print("Sammenligner", a, "og", b)
if a == b:
    print("Navnene er like")
else:
    print("Navnene er IKKE like")
```

### c) 
Prøv kodene ovenfor, men sett inn de ulike navnene under. Gjett før du kjører koden, hva som vil komme opp.


```{python}
# a = "Ann", b = "Anne"
```

```{python}
# a = "Anders", b = "Anders"
```

```{python}
# a = "Anders", b = "anders"
```

Forstår du hvorfor du får de resultatene du gjør?


 

Se koden under. Hva er galt?

```{python}
tall1=input("Gi meg et tall så skal jeg dobble det")
dobbel=tall1*2
```


Gjør deg opp en mening og gjerne test koden før du ser svaret under.




svar: Når brukeren taster inn et tall blir det konvertert til en string og ikke et tall (float/int) slik at koden ikke skriver det dobbelte av tallet men tallet to ganger etter hverandre.

Du kan løse probel
```{python}

```

### d) 
Bruk int() for å rette på koden.

Løsningsforslag:Se eksempelet nedenfor.

```{python}
tall1=input("Gi meg et tall så skal jeg dobble det")
tall1=int(tall1)
dobbel=tall1*2
```

# Intro om løkker

Noe av det datamaskiner er best på, er gjentatte handlinger i høyt tempo. Dette er også et vanlig behov.

Eksempler: 
- Et firma skal utbetale lønn til alle sine ansatte hver måned.
- Et digitalt eksamenssystem skal vise spørsmål til, og motta svar fra, alle studenter som tar eksamen.
- Et system som styrer industrielt produksjonsutstyr skal motta informasjon fra en rekke sensorer hvert eneste sekund, om trykk, temperatur, osv., og gjøre handlinger basert på verdiene.
- Utstyr på et sykehus skal overvåke pasienters hjerterytme osv. sekund for sekund, og kunne slå alarm hvis noe er unormalt.
- Utstyr for opptak av musikk skal kunne sample lyden tusenvis eller millionvis av ganger per sekund.
- Et program for å vise video på en mobilskjerm må likeledes kunne oppdatere fargen i hver piksel på skjermen mange ganger i sekundet.

Du har kanskje erfaring med bruk av regneark? Der er det vanlig hvis man skal bruke samme formel på alle radene i en tabell at man kopierer formelen nedover.

Å kopiere samme kodesetning flere ganger er mulig i Python også, men bare praktisk hvis antall repetisjoner er lavt og kjent på forhånd.
Eksemplet nedenfor viser et slikt tilfelle, hvor en kodelinje er gjentatt 3 ganger.

```{python}
print("Hipp")
print("Hipp")
print("Hipp")
print("Hurra!")
```
 Samme utskrift kan oppnås med løkke:

```{python}
 for i in range(3):
    print("Hipp!")
print("Hurra!")
```


```{python}

```


'''{python}

'''



'''{python}

'''



'''{python}

'''



'''{python}

'''




'''{python}

'''




'''{python}

'''



'''{python}

'''
