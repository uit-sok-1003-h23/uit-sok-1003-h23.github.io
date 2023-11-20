---
title: Mappe 2
---
{% include navbar.html %}{% include top-box.html %}

Husk å følge instruksjonene nøye. All kode skal kommenteres, og figurer skal ha tydelig merkede akser. Oppgaven leveres ved å være merket "Mappe 2" og ligge i et repositorie 
kalt “SOK-1003-H23” som er delt med faglærer og studentassistent [som beskrevet her](https://uit-sok-1003-h23.github.io/semesteroppgave.html)


# Om ChatGPT/Kunsig intelligens (KI)
Det er lov å bruke ChatGPT og annen kunstid intelligens, men dialogen med KI må legges ved. Husk at god og veldokumentert bruk av KI belønnes karatkermessig. Det er lov å starte en ny chat
for å få en mer oversiktlig logg, dersom det er mye unødvendig og irrelelevant i den orginale chatten. 

Ved å legge ved chatten, dokumenterer dere også eventuelle feil som KI gjør, og slipper å hefte ved det. KI kan gjøre feil helt uten grunn, men kanskje oftere fordi spørsmålet ikke er formulert bra nok. 

Bruk av KI uten å dokumentere det er langt mer risikabelt. For det første er det 
juks, med de konsekvenser det kan medføre om det blir oppdaget. For det andre vil dere hefte ved alle feil som KI gjør. 

# Karakter
Denne mappen vil inngå i den endelige karaktervurderingen, men dere får kun godkjent/ikke godkjent på denne innleveringen. Dere vil få mulighet til å forbedre svarene 
på både Mappe1 og Mappe2 før endelig innlevering. 


# Forklaring:
Husk å forklare hva du gjør hele tiden i markedown in jupyterboken. 

# Oppgave 1:

Last ned modulen [download.py](https://uit-sok-1003-h23.github.io/mappe/download.py), og legg den i arbeidsmappen din (samme mappe som der jupyter arbeidsboken du jobber i er). 

I denne modulen finnes funksjonen `ssb`. Den laster tabeller fra [Statistikkbanken til Statistisk Sentrabyrås (SSB)](https://www.ssb.no/statbank) inn i en pandas DataFrame. 

* Finn én tabell i [SSBs statistikkbank](https://www.ssb.no/statbank) med et par variabler som du tror det kan være en sammenheng mellom. Husk å velge endel år. 
* Tabellen må inneholde data for flere år
* Velg data og trykk "Vis tabell"
* Scroll helt nederst, der du finner en knapp som heter "API-spørring for denne tabellen". Trykk på denne. 
* Du vil nå se to tekstfelt, én for URL og én for "JSON-spørring"
* Bruk disse tekststrengene i følgende kode

```
import download

json = """
<lim inn JSON-spørringen her>
"""
url = <lim inn url'en her>

df = download.ssb(url, json)

df
```
* Kjør denne, slik at du ser dataene, og identifiser hva tidsvariablene er (vanligvis "År" eller "Tid"). Definer tid som tabellens indeks slik (bytt ut \<tisvariabel\> med navnet på tidsvariabelen):
```
df = df.set_index(<tidsvariabel>)
```

* Dataene vil normalt være i "langt format", slik at variablene du er interessert i ligger etterhverandre i én av kolonnene. Du kan få hver verdi i en kolonne som en egen kolonne med denne kommandoen:
```
df = df.pivot(columns=<navnet på kolonnen med verdiene du ønsker som kolonnenavn>, values=<navnet på kolonnen der dataverdiene ligger>)
```

Du skal nå ha en DataFrame med minst de to kollonene som du tror det kan være sammenheng mellom.

Husk å forklare hvilke data du har valgt og hvorfor. 

# Oppgave 2:

1. Definer de to kollonnene du har valgt som henholdsvis x og y
2. Lag et scatter-plott med x og y, med variabelnavn langs aksene. 
3. Beregn "kovariansmatrisen" for de to variablene slik som angitt under og beregn a og b med denne koden:
```
import numpy as np
cov = np.cov(x, y)
b = cov[0,1]/cov[0,0]
a = np.mean(y) - b*np.mean(x)
```
Kovariansmatrisen forteller noe om i hvilken grad det er sammenheng mellom variabler. Elementene  `cov[0,0]` og `cov[1,1]` forteller hvor mye den første og den andre variablene varierer.  `cov[1,0]` og `cov[0,1]` er identiske, og forteller hvor mye sammenheng det er mellom variablene. 

4. Lag en funksjon `f(x, a, b)`, som returnerer `a + b * x`
5. Lag et nytt plott, som er likt det gamle, men der du legger til et plott av denne funksjonen. Gi plottet av funksjonen etiketten (label) 'predicted',  og sørg for at etiketten vises i plottet.
6. Forklar hva du tror figuren viser.
7. Definer følgende funksjon

```
def sumsq_errs(x, y, f, a, b):
    return np.var((y-f(x, a, b)))
```
Denne funksjonen returnerer et mål på hvor stor forskjelle det er mellom elementene i variabel y og elementene fra funksjonen f(x, a, b)

# Oppgave 3

1. Lag en funksjon `calc_errs(x, y, f, a, b, its)` som regner ut dette avviket for ulike verdier av b. De nye verdiene for b skal være i intervallet b-0.5 til b + 0.5. Antall verdier i intervallet som det skal regnes på, er gitt ved `its`. 
2. Lag en funksjon plot_and_print(x, y, f, a, b, its)
    1. lage et scatterplott med de avvikene fra sumsq_errs langs y aksen og verdiene for b langs x-aksen
    2. Identifiserer for hvilken verdi av b avvikene er minst
    3. print en f-streng med verdien av denne b'en, verdien av den opprinnelige b'en (fra oppgave 2.2) og differansen mellom disse. 
3. Kjør plot_and_print for its =10, its=100 og its= 1000. 
4. Kommenter resultatet og forklar hva du tror du har gjort. 
5. Definer b som et sympysymbol og bruk sympy til å minimere `sp.diff(cov[1,1]- 2*cov[0,1]*b + b**2*cov[0,0])`
6. Legg `sp.diff(cov[1,1]- 2*cov[0,1]*b + b**2*cov[0,0])` inn i plottet i plot_and_print








