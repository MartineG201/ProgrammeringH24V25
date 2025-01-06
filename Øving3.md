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


### d) Variabler kan være tall som vi kan regne med

```{pyhton}
print("Har en sirkel med radius", None, "som er grunnflate i en sylinder med høyde", None)
print("Omkrets av sirkelen:", None) 
print("Areal av sirkelen:", None)
print("Areal av sylinderen:", None)
```



```{pyhton}

```
















