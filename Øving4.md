# if-setninger
**Læringsmål:
Betingelser (if-setninger)**




## Generelt om if-setninger

Studer koden under.

```{python}
regn = float(input("Hvor mange mm regn er det meldt? "))
print("Da anbefaler jeg paraply!")
print("Ha en fin tur til universitetet!")
```


Paraply bør anbefales bare ved behov, f.eks. hvis det var meldt mer enn 0.2 mm regn. Det oppnår vi med en if-setning:


```{python}
regn = float(input("Hvor mange mm regn er det meldt? "))
if regn > 0.2:
    print("Da anbefaler jeg paraply!")
print("Ha en fin tur til skolen!")
```
Den ovenstående kodeblokken viser en if-setning. Den har følgende struktur:

- starter med ordet if, dette er et beskyttet ord i Python og kan derfor ikke brukes som variabelnavn e.l.
- bak if kommer en logisk betingelse - i dette tilfellet regn > 0.2 - som vil være enten sann (True) eller usann (False), her avhengig av innholdet i variabelen regn
- bak betingelsen må if-setningen ha : (kolon) - hvis du glemmer kolon vil du få syntaksfeil.
- kodelinjen like under if har et innrykk (tabulator), dette betyr at denne linjen - print("Da anbefaler jeg paraply") - er del av if-setningen. Den vil bli utført kun hvis betingelsen i if-setningen er sann, som vil inntreffe hvis brukeren skriver inn et større tall enn 0.2

Siste setning, print("Ha en fin tur til universitetet!") , har derimot ikke innrykk, denne vil derfor bli utført uansett og er ikke knyttet til if-setningen.


 Det er mulig å ha flere programsetninger som del av if-setningen, for eksempel:

```{python}
 regn = float(input("Hvor mange mm regn er det meldt? "))
if regn > 0.2:
    print("Da anbefaler jeg paraply!")
    print("Gjerne en paraply med Østmarka-logo.")
print("Ha en fin tur til skolen!")
```

Her vil begge "print"-setningene om paraply kun bli utført hvis betingelsen er sann, mens "fin tur"-setningen fortsatt blir utført uansett utfall av if-setningen. 

**Altså: I Python viser innrykk hvor mange av de påfølgende setningene som styres av if-betingelsen.** Det er derfor viktig å være nøye med innrykkene og få alle programsetninger på korrekt indentasjonsnivå.

### a) Test koden ut selv og prøv med ulike tall over og under 0,2







### b) Banankake
Du lager en banankake som skal stå minst 50 min i ovnen. Ta utgangspunkt i følgende program, som har den svakheten at det sier at kaken skal ut uansett hvor lenge den har stekt.

Endre programmet slik at "Kaken kan tas ut av ovnen" kun printes hvis kaken har stått minst 50 minutt. **"Større eller lik" skrives i Python >=
**

Tips til servering... skal derimot printes uansett.

```{python}
tid = int(input("Hvor mange minutt har kaken stått i ovnen? "))
print("Kaken kan tas ut av ovnen.")
print("Tips til servering: vaniljeis.")
```
 Eksempel på utskrift fra tre ulike kjøringer, hvis du har fått det til riktig:

```{python}
Hvor mange minutt har kaken stått i ovnen? 35  
Tips til servering: vaniljeis.  
>>>  
  
Hvor mange minutt har kaken stått i ovnen? 50  
Kaken kan tas ut av ovnen.  
Tips til servering: vaniljeis.  
>>>
  
Hvor mange minutt har kaken stått i ovnen? 65  
Kaken kan tas ut av ovnen.  
Tips til servering: vaniljeis.
>>>
```

### c) Epler til barn
Ta utgangspunkt i følgende program, som ber brukeren taste inn antall epler og antall barn og deretter regner ut hvor mange epler det blir på hver.


```{python}
epler = int(input("Hvor mange epler har du? "))
barn = int(input("Hvor mange barn passer du? "))
print("Da blir det", epler // barn, "epler til hvert barn")
print("og", epler % barn, "epler til overs til deg selv.")
print("Takk for i dag!")
```

Under vises to kjøreeksempler:


```{python}
Hvor mange epler har du? 14  
Hvor mange barn passer du? 3  
Da blir det 4 epler til hvert barn  
og 2 epler til overs til deg selv.  
Takk for i dag!
>>>>
```


```{python}
Hvor mange epler har du? 4
Hvor mange barn passer du? 0
Traceback (most recent call last):  ...
ZeroDivisionError: integer division or modulo by zero
```

Det første, hvor brukeren skriver inn tallene 14 og 3, funker fint. Hvis brukeren derimot svarer 0 barn, vil programmet gi feilmelding (ZeroDivisionError) fordi det er umulig å dele på null. Negativt antall barn vil "funke", men ikke gi mening.

**Endre koden slik at de to print-setningene som forteller hvor mange epler det blir til barna og deg selv KUN utføres hvis barn > 0. "Takk for i dag!" skal derimot printes uansett.**

Se eksempelet under
```{python}
Hvor mange epler har du? 4  
Hvor mange barn passer du? 0  
Takk for i dag!
```

## Generelt om if-else-setninger
I eksemplene knyttet til (a) og (b) skulle vi gjøre noe ekstra hvis en betingelse var sann, ellers la være. I andre tilfeller kan vi ønske å gjøre en handling hvis betingelsen er sann, og en alternativ handling hvis den er usann.

Det kan vi oppnå med en **if-else-setning**. Eksemplet nedenfor bygger videre på tilsvarende eksempel for if-setninger.

```{python}
regn = float(input("Hvor mange mm regn er det meldt? "))
if regn > 0.2:
    print("Da anbefaler jeg paraply!")
    print("Gjerne en paraply med NTNU-logo.")
else:
    print("Hva med ei T-skjorte med NTNU-logo?")
print("Ha en fin tur til universitetet!")
```

Altså:
- De to setningene som står på innrykk under if blir utført bare hvis betingelsen er sann.
- Setningen som står på innrykk under else blir utført bare hvis betingelsen er usann (kunne også hatt flere setninger på innrykk etter else).
- Den siste printen, som ikke har innrykk (Ha en fin tur...), blir utført uansett.

### d)
Test koden over med forskjellige mengder nedbør

### e) Kan du stemme?
 I denne deloppgaven skal det lages et program som sjekker om en person kan stemme, altså om personen er 18 år eller eldre. Man må da spørre brukeren om alder og lagre svaret i en variabel, for deretter å sjekke om brukerens alder er 18 eller mer.

Eksempel på kjøring av koden: 
```{python}
Skriv inn din alder: 19
Du kan stemme:)
```
```{python}
Skriv inn din alder: 18
Du kan stemme:)
```
```{python}
Skriv inn din alder: 2
Du kan ikke stemme ennå
```

##  Generelt om if-elif-else-setninger

 I eksemplene vi har sett hittil, har det vært kun to mulige utfall på betingelsene - kaken har stått >= 50 minutt, eller ikke; antall barn er > 0, eller ikke; alder er over 18, eller ikke. I mange praktiske situasjoner kan det være tre eller flere mulige utfall.

 F.eks. hvis det var meldt mer enn 3 mm nedbør er kanskje ikke paraply tilstrekkelig, vi ville heller anbefale støvler og regntøy.  Vårt tidligere eksempel kunne da utvides som følger:


```{python}
regn = float(input("Hvor mange mm regn er det meldt? "))
if regn > 3.0:
    print("Da anbefaler jeg støvler og regntøy!")
elif regn > 0.2:
    print("Da anbefaler jeg paraply!")
    print("Gjerne en paraply med Østmarka-logo.")
else:
    print("Hva med ei T-skjorte med Østmarka-logo?")
print("Ha en fin tur til skolen!")
```
### f) kjør koden over med tre ulike mengder nedbør


### g) 
Se på koden under

```{python}
score = int(input("Antall poeng: "))
  
if score >= 89:
    karakter = "A"
elif score >= 77:
    karakter = "B"
elif score >= 65:
    karakter = "C"
elif score >= 53:
    karakter = "D"
elif score >= 41:
    karakter = "E"
else:
    karakter = "F"
 
print("Du fikk", karakter)
```
Du skal lage en liknende kode som gir karakteren "Høy måloppnåelse", "lav måloppnåelse" eller "middels måloppnåelse" på en prøve elevene kan få maks 27 poeng på.
Har eleven fått over eller 22 poeng skal eleven få høy, Mellom 21 og 14, skal de få middels og lavere skal de få lav måloppnåelse. 

### h) 
I koden under har vi gjort en stor feil. Rett opp i feilen slik at koden blir riktig. 
(hint: test koden ved å si at du fikk 89 poeng)
```{python}
score = int(input("Antall poeng: "))
  
if score >= 89:
    karakter = "A"
if score >= 77:
    karakter = "B"
if score >= 65:
    karakter = "C"
if score >= 53:
    karakter = "D"
if score >= 41:
    karakter = "E"
else:
    karakter = "F"
 
print("Du fikk",karakter)
```
i) 
 Lag en utvidet versjon av programmet fra (e) som sier om personen kan stemme eller ikke, med følgende regler:
- alder >= 18: Kan stemme både ved lokalvalg og Stortingsvalg
- alder >= 16: Kan stemme ved lokalvalg, men ikke ved Stortingsvalg
- ellers (alder < 16): Kan ikke stemme.

j) 
 Du skal lage et program som sjekker hvilken billettpris en person skal betale ut ifra alderen til personen.
 
 Oversikt over alder og tilhørende billettpriser:

 

```{python}

```




```{python}

```
