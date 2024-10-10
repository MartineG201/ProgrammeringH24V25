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

Som forklaringen sier, er det to **alternative tegn** som kan brukes for å omslutte tekststrenger i Python:

1. **Apostrof**. På norsk PC-tastatur er den mellom Æ og Enter. På Mac på tasten til venstre for tallet 1.
2. **Hermetegn** – både på PC og Mac på samme tast som tallet 2.

Om du bruker apostrof eller hermetegn, er et spørsmål om smak og behag – bare du er konsekvent og bruker samme tegn foran og bak tekststrengen. I visse situasjoner vil et av alternativene være å foretrekke, som forklart i del 2 av tutorialen.

Hvis du ved et uhell får feil tegn, som bøyd apostrof eller bøyd hermetegn i stedet for rett (nøytral) apostrof og rett (nøytralt) hermetegn som det er snakk om her, vil koden din ikke funke. Hvis du for eksempel skriver Python-kode i Word, kan Word automatisk omforme hermetegn til bøyde hermetegn (som ser forskjellig ut avhengig av om det står før eller etter teksten som hermes). Dette er en av mange gode grunner til å **ikke skrive Python-kode i Word** – bruk en dedikert kode-editor som Jupyter, Spyder eller PyCharm.

### a) 
Lag et program som gir følgende utskrift til skjermen:

```python
Jeg digger programmering!

### b)


