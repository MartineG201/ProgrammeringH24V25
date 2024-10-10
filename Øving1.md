# Øving 1

### Læringsmål:
- Printe tekst og tall til konsoll
- Skrive et enkelt program

## Gå inn på python.com i en ny fane

## `print()` - tutorial del 1:

Les gjerne denne før du gjør de neste oppgavene, særlig hvis du ikke kan programmere fra før.

Programmer som skal brukes av mennesker, må ofte vise informasjon på skjermen. En enkel måte for dette i Python er funksjonen `print()`.

Koden under gir en mest mulig selvforklarende intro til `print`-setningen:

```python
print('Det som skal ut på skjermen, settes inni parentesen til print().')
print("Tekst må omsluttes med fnutter (apostrof)")
print('eller med dobbelfnutter (hermetegn).')
print("Tall trenger ikke fnutter rundt seg:")
print(42)
print('En blank linje kan printes med tom parentes:')
print()
print('Du kan printe flere ting, med komma mellom:', 5, 6)
print('Desimaltall må skrives med punktum i Python:', 3.14)
print('Hvis du bruker komma, tolkes det som to adskilte tall:', 3, 14)
print('Komma inni en tekst kommer ut på skjermen:', ',', ',', 'komma', 'mellom', 'tekster gjør ikke det.')
```

Som forklaringen sier, er det to **alternative tegn** som kan brukes for å omslutte tekststrenger i Python:

1. **Apostrof**. På norsk PC-tastatur er den mellom Æ og Enter. På Mac på tasten til venstre for tallet 1.
2. **Hermetegn** – både på PC og Mac på samme tast som tallet 2.

Om du bruker apostrof eller hermetegn, er et spørsmål om smak og behag – bare du er konsekvent og bruker samme tegn foran og bak tekststrengen. I visse situasjoner vil et av alternativene være å foretrekke, som forklart i del 2 av tutorialen.

Hvis du ved et uhell får feil tegn, som bøyd apostrof eller bøyd hermetegn i stedet for rett (nøytral) apostrof og rett (nøytralt) hermetegn som det er snakk om her, vil koden din ikke funke. Hvis du for eksempel skriver Python-kode i Word, kan Word automatisk omforme hermetegn til bøyde hermetegn (som ser forskjellig ut avhengig av om det står før eller etter teksten som hermes). Dette er en av mange gode grunner til å **ikke skrive Python-kode i Word** – bruk en dedikert kode-editor som Jupyter, Spyder eller PyCharm.

### a) 
Lag et program som gir følgende utskrift til skjermen:

```python
Jeg digger programmering!
```
### b)
Lag et program som gir følgende utskrift til skjermen: (det er en blank linje mellom Norge og Areal)
```python
Norge
 
 
Areal (kv.km): 385180
 
Folketall (mill.): 5.3
```
### 'print()' - tutorial del 2:

Nyttig info om fnutter i streng før oppgave c og d. Koden under viser hvorfor Python har flere alternativer for fnutter rundt tekststrenger heller enn å standardisere på bare ett fast tegn for dette formålet. Ta gjerne å endre på koden for å se hva som skjer! print('Hvorfor tilbys både enkle', "og doble fnutter?")

```python
print('Jo, hvis det er doble "fnutter" i teksten, funker kun enkle rundt,')
print("og med enkle fnutter i teksten er'e bare doble som funker rundt.")
print("Med samme fnutt både rundt og inni, tror Python teksten slutter midt i.")
print("Skal du ha begge typer fnutter i teksten? Da må du ha triple fnutter rundt:")
print('''Er'u gær'n? spurte "Arne" og lo sykt.''')
print("""Trippel apostrof ' og trippel hermetegn " funker begge deler""")
print("""Triple fnutter kan også brukes
for tekststrenger
som skal gå over flere linjer.""")
```

### c) Lag et program som skriver ut på skjermen teksten: "Jeg elsker ITGK" ropte studenten da 1c funket.
(Hermetegnene rundt teksten skal være med i det som kommer ut på skjermen.) 

### d) Lag et program som skriver ut på skjermen teksten vist under. (Hint: For å slippe å skrive så mye, kopier teksten inn i boksen under, så trenger du bare selv å skrive print, parenteser og passende fnutter rundt teksten.
Tekst til oppgave d: 
```python
Noen barn sto og hang ved lekeplassen.
Diskusjonstemaet deres var noe uventet.

- Hvorfor heter'e "Python"?
- Var'e slanger som laget det? - Nei, Guido van Rossum.
- Likte slanger kanskje da? - Nei, digga "Monty Python".
- Hva er det? Et fjell?
- Nei, engelsk komigruppe. Begynte i '69
- Wow! Var'e fremdeles dinosaurer da?
```

