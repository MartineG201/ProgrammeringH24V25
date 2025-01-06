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

Endre programmet slik at "Kaken kan tas ut av ovnen" kun printes hvis kaken har stått minst 50 minutt. "Større eller lik" skrives i Python >=Tips til servering... skal derimot printes uansett.

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










```{python}

```




```{python}

```


```{python}

```


```{python}

```
