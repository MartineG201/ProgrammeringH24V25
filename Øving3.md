 # Øving 3 Input og variable
 
### Læringsmål:
- Lage programmer der brukeren gir inn tekst med input()
- Enkel bruk av variable
- Korrekt navngivning av variable


## Tutorial del 1: funksjonen input()

**Hvorfor trenger vi input?** I mange programmer er det viktig å kunne la brukeren gi input. I en nettbutikk må kunden kunne velge produkt, oppgi adresse det skal sendes til, betalingsmåte, osv.

Input kan gis på mange måter, f.eks. via berøringsskjermer, mus, eller med stemme. Her skal du lære den måten som er lettest å programmere, nemlig input av tekst fra tastatur.
Dette gjøres i Python ved hjelp av funksjonen input(). I likhet med print() er dette en funksjon i Pythons standardbibliotek.

Kjør koden under, så ser du noen viktige forskjeller på print() og input().

```{python}
print("print() skriver tekst ut på skjerm og skifter linje")
input("input() venter at du skriver noe og slår Enter: ")
print("print() kan ha", "mange tekster", "skilt med komma")
input("input() tillater kun en tekst! OK? ")
```

Den ene teksten input() kan inneholde, er den såkalte ledeteksten som skal forklare brukeren hva slags input som forventes.
Ledeteksten bør være presis så brukeren vet hva slags opplysning det er spurt om.F.eks. er "Oppgi vekt i kg: " en bedre ledetekst enn bare "Oppgi vekt: ", som igjen er mye bedre enn "Skriv et tall: " eller "Gi input: ".
Blankt tegn bakerst i ledeteksten er ofte en fordel, ellers kommer brukerens input kloss i ledeteksten.I det lille eksemplet over brukte vi ikke resultatet fra input(), men vanligvis ber vi brukeren om data fordi dataen trengs til noe.
For noe litt mer nyttig, anta at vi ønsker å spørre brukeren om navn - og deretter benytte dette navnet i en påfølgende print-setning, så vi får en liten dialog mellom bruker og maskin:

```{python}
Hei, hva heter du? Nina  
Nina - det var et fint navn.
```
Her spør maskinen "Hei, hva heter du?", brukeren svarer "Nina" og maskinen skriver "Nina - det var et fint navn."Denne lille dialogen kan oppnås med følgende kodelinje:

```{python}
print(input("Hei, hva heter du? "), "- det var et fint navn.")
```

Denne koden funker fordi parenteser alltid utføres innenfra og ut. Print-setningen kan ikke kjøres før man vet hva som skal printes,
Derfor må input-setningen kjøres først, den gir som resultat det navnet brukeren skriver inn (f.eks. Nina).Dette navnet skrives deretter ut sammen med den påfølgende teksten "- det var et fint navn.")

### a) Simpel bruk av input direkte i print()-setning

Ta utgangspunkt i tutorial-koden nedenfor (og kjør den gjerne en gang for å se hvordan den virker; hvis du ikke forstår hvordan, les først tutorial):

```{python}
print(input("Hei, hva heter du? "), "- det var et fint navn.")
```
 Endre tekststrengene i denne kodelinjen så dialogen med brukeren i stedet blir som vist nedenfor. Maskinen skal alltid gjenta det navnet brukeren skrev, Nina er bare et eksempel.

 ```{python}
Navn? Nina  
Nina - kult navn!
```
Legg så til en ny, lignende kodelinje som spør om brukerens favorittfag. Ved ferdig program skal dialogen se ut som nedenfor.Utskriften til programmet skal selvsagt tilpasse seg det brukeren skriver inn som navn og favorittfag.

```{python}
Navn? Per
Per - kult navn!  
favorittfag? Matematikk  
Matematikk - interessant!
```
## Tutorial del 2: variable - grunnleggende intro

Hvorfor trenger vi variable? Poenget med variable er å **huske data underveis** i utførelsen av et program.
Variable er derfor et sentralt konsept i programmering, ikke bare i Python men uansett hva slags språk man programmerer i.
Uten variable støter vi fort på en rekke problemer fordi programmet vårt ikke kan huske noe, f.eks. at

- vi må be brukeren gi inn opplysninger på nytt som brukeren har gitt tidligere
- vi må regne ut på nytt data vi allerede har regnet ut tidligere

Dette sløser tid og strøm og vil i mange tilfeller gjøre programmet fullstendig ubrukelig.

I det lille eksempelprogrammet i tutorial del 1 klarte vi oss uten noen variabel,
fordi navnet vi innhentet fra bruker kun ble benyttet én gang, og dette skjedde umiddelbart etter at det var tastet inn.

```{python}
  print(input("Hei, hva heter du? "), "- det var et fint navn.") 
```

```{python}
Hei, hva heter du? Nina  
Nina - det var et fint navn.  
```

Men ofte skal samme data brukes flere ganger, og etter at vi har gjort andre ting i mellomtiden. 
Da må data huskes i variable. Anta at vi ønsker en bare litt mer avansert dialog med brukeren:

```{pyhton}
Hei, hva heter du? Nina  
Nina - det var et fint navn.  
Lykke til med programmering, Nina!
```
Her vil vi bruke det innleste navnet i to påfølgende print-setninger. Hvis vi prøver samme triks som tidligere med å sette input-setning direkte i print-setning, får vi koden:


```{pyhton}
print(input("Hei, hva heter du? "), "- det var et fint navn.")
print("Lykke til med programmering,", input("Hei, hva heter du?")) 
```


Kjøring viser hva som er dumt med denne koden, nemlig at spørsmålet "Hei, hva heter du?" kommer to ganger.

```{pyhton}
Hei, hva heter du? Nina  
Nina - det var et fint navn.  
Hei, hva heter du? Nina  
Lykke til med programmering, Nina
```


Ikke noe katastrofalt problem her, men tenk deg et program hvor samme opplysning skal brukes 100 ganger eller mer i en kritisk arbeidsoppgave som haster.
Kan vi løse det på en bedre måte? JA - med en variabel for å huske navnet. Koden blir da

```{pyhton}
navn = input("Hei, hva heter du?" )
print(navn, "- det var et fint navn.")
print("Lykke til med programmering,", navn)
```

 Dette programmet kan forklares som følger:

- linje 1, til høyre for = : bruker input() for å spørre hva brukeren
- heterlinje 1, til venstre for =: oppretter en variabel som heter navn.
- linje 1, tegnet =. Dette er tilordningsoperatoren. Betyr at verdien av uttrykket på høyre side, resultatet av input(), blir husket i variabelen kalt navn. Hvis brukeren skriver Nina, vil variabelen navn da inneholde strengen 'Nina'
- linje 2, variabelen navn brukes fremst i print-setningen. Merk at variabelnavnet ikke skal ha fnutter rundt seg. Med fnuttter ville vi i stedet ha skrevet "navn - det var et fint navn". Ordet navn som står bakerst i setningen "det var et fint navn." er ikke variabelen, her er ordet navn bare del av en tekststreng.
- linje 3, variabelen navn brukes bakerst i print-setningen. Igjen uten fnutter; det er ikke ordet navn vi ønsker å skrive, men den tekststrengen som variabelen navn inneholder (f.eks. Nina)


Ved hjelp av variabelen som her ble kalt navn, unngår vi å stille samme spørsmål to ganger. Vi spør bare én gang, i starten av programmet, og husker da opplysningen brukeren gir oss ved å putte den inn i en variabel.

Videre i programmet kan vi benytte denne variabelen hver gang vi trenger navnet - enten det som her var bare to ganger, eller om det hadde vært flere.

### b) huske input i varabel

 Kjør koden under for å se hvordan den virker. Som du vil se, plager den brukeren med å gjenta begge spørsmålene to ganger.
 
Forbedre koden ved å introdusere en variabel for navn og en annen variabel for favorittfag, slik at brukeren får hvert av spørsmålene bare en gang (dvs. spørres kun en gang om navn og kun en gang om favorittfag).Hvis du er i tvil om hvordan du skal angripe problemet, se lignende eksempel i tutorial like over.

```{pyhton}
print("Hei,", input("Navn? "))
print(input("Favorittfag? "), "- interessant!")
print("Ha en fin dag,", input("Navn? "))
print("- og lykke til med", input("Favorittfag? "))
```

Hvis du får til å bruke de to variablene som tenkt, skal kjøringen av det forbedrede programmet se slik ut (men også funke om brukeren skriver inn noe annet enn Ada på spørsmålet Navn? og noe annet enn Matematikk på Favorittfag?)


```{pyhton}
Navn? Ada  
Hei, Ada  
Favorittfag? Matematikk  
Matematikk - interessant!  
Ha en fin dag, Ada  
- og lykke til med Matematikk
```
### c) Huske og skrive ut personalia
Lag et program som spør brukeren om navn, adresse og alder. Husk å lagre denne informasjonen fordi til slutt skal du printe ut en setning som sier " Hei (navn), som er (alder) år, håper du bor fint i (adressen)" og her hvor det står navn, alder og adressen skal det stå navnet, alderen og adressen til brukeren. 


## Tutorial del 3: Konvertering mellom datatyper
Vi kan ha ulike typer data, som tekststrenger (f.eks. "Python"), heltall (f.eks. 42) og  flyttall (f.eks. 9.80).
Ofte kommer vi i situasjoner hvor vi har data av en viss type, men vi trenger samme data bare med en annen type. Da må vi konvertere dataene. Noen vanlige konverteringsfunksjoner:

int() - konverterer til heltall.
- int('423') gir 423 (dvs. tekststrengen blir konvertert til et tall).Virker kun hvis tekststrengen faktisk inneholder et heltall.
- int(5.69) gir 5 (dvs. for flyttall blir desimaldelen fjernet)

float() - konverterer til flyttall
- float('5.69') gir 5.69
- (tekststreng konvertert til tall)float('5') gir 5.0, dvs. float() virker på tekststrenger enten de inneholder flyttall eller heltall (men ikke på strenger som er noe annet enn tall)
- float(5) gir 5.0
- 
str() - konverterer til tekststreng

- str(42) gir '42'
- str(5.69) gir '5.69'

### d)
Koden under feiler fordi vi har glemt å konvertere. Kjør den og se hva som skjer.

```{pyhton}
alder = input("Hvor gammel er du?")
alder_mor = input("Hvor gammel er din mor?")
sum_alder = alder + alder_mor
print("Gratulerer, til sammen er dere", sum_alder, "år!")
```

Oppgaven din er å endre koden slik at den gir den faktiske summen av aldren til mor og deg. 


### e) Variabler kan være tall som vi kan regne med
Lag et program som tar inn informasjon om høyde og radiusen til en sylinder og regner ut omkrets av sirkelen, areal av sirkelen og areal av sylinderen. 

```{pyhton}
print("Har en sirkel med radius", None, "som er grunnflate i en sylinder med høyde", None)
print("Omkrets av sirkelen:", None) 
print("Areal av sirkelen:", None)
print("Areal av sylinderen:", None)
```
## Tutorial del 4: Navngiving av variable

En variabel er et navn som representerer en verdi som lagres i datamaskinens minne. Den vanligste måten å opprette en variabel på er ved en tilordningssetning:

variable = expression

dette tilfellet er variable navnet til variabelen, mens expression er verdien. Noen regler for slike tilordningssetninger:
- variabelen som opprettes skal alltid stå på venstre side av uttrykket, og venstre side skal kun inneholde denne variabelen, ikke noe annet
- høyde side kan alt fra en enkelt verdi (f.eks. et tall) eller en enkelt variabel, til mer sammensatte uttrykk som må beregnes. Hvis høyre side inneholder variable, må dette være variable som allerede er opprettet tidligere i koden.
- variabelnavnet må tilfredsstille følgende regler:ord som er reserverte ord i Python, f.eks. if, def, eller som er navn på standardfunksjoner som print, min, max, ... bør unngås som varibelnavn
- variabelnavn må begynne med en bokstav eller tegnet _ (understrek)kan ellers inneholde bokstaver, tall og understrek, dvs. kan f.eks. ikke inneholde blanke tegn.
- Python skiller mellom små og store bokstaver, så Areal og areal vil være to ulike variable.

Det anbefales å lage variabelnavn som er intuitivt forståelige, f.eks. er areal et bedre navn enn x på en variabel som inneholder et areal. Sammensatte variabelnavn skrives typisk som pukkelord (eng.: camelCase) eller med understrek for å vise hvor ett ord slutter og det neste begynner, f.eks. startTime, pricePerLiter eller start_time, price_per_liter, siden direkte sammensetning uten noe som helst skille vil gi lange variabelnavn som blir vanskelige å lese.

Kodeblokka under viser eksempler på variable som funker og ikke funker:



```{pyhton}
# Eksempel på tilordningssetninger som funker
pokemon_name = "Tyranitar"
MaxCP = 3670
antall = 3
antall = antall + 1      # høyre side regnes ut som 3+1, så 4 blir ny verdi i variabelen antall
resists_fighting = False
level42 = "to be done"   # tall er OK i variabelnavn unntatt helt fremst
  
# Eksempel på tilordninger som IKKE funker
1 = antall              # variabelen må stå på venstre side
antall + 1 = antall     # og v.s. kan KUN inneholde et variabelnavn, ikke et større uttrykk
10kamp = "gøy"          # variabel kan ikke begynne med tall, kun bokstav eller _
antall = 3              # denne er OK, men se neste linje
antall = Antall + 1     # Python skiller mellom store og små bokstaver, Antall vil være en annen
                        # variabel og gir NameError her fordi den ikke er opprettet i en tidligere setning
happy hour = 20         # navn kan ikke inneholde mellomrom, burde vært happy_hour eller happyHour
alkohol% = 4.5          # % kan ikke brukes i variabelnavn (betyr modulo). Samme gjelder andre spesialtegn,
                        # hold deg til vanlige bokstaver og tall
```


### f)
Prøv å kjør koden under. Som du vil se, funker den ikke pga. diverse feil med variabelnavn og tilordningssetninger. Fiks feilene så programmet kjører som det skal.

```{pyhton}
4navn = "Per"
ideal alder = 42
37 = kundensAlder
differanse = ideal alder - kundensAlder
print(4navn, "er", Differanse, "år unna idealalderen")
```


### g) Peppes pizza
Du har nettopp spist middag på Peppes Pizza med noen venner, og mottar denne kvitteringen:

_Pizza: 750kr_

_Studentrabatt: 20%_

_Tips: 8%_

(Oppgaven er delt opp i trinn for å gjøre det lettere å gjennomføre)


I) Lag et program som lagrer verdiene fra regningen i variabler. Variablene skal altså være Pizza, Studentrabatt og Tips.


II) Lag en variabel totalt som er lik den totale summen av middagen


III) Gjør slik at brukeren kan skrive inn hvor mange som deltok på middagen, og print ut hvor mye hver person må betale.

 Hint: For at man skal bruke input i beregninger må den gjøres om til en int.






