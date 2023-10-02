---
title: Mappe 1
---
{% include navbar.html %}{% include top-box.html %}
# Mappe 1
Husk å følge instruksjonene nøye. All kode skal kommenteres, og figurer skal ha tydelig merkede akser. Oppgaven leveres ved å ligge i et repositorie 
kalt “SOK-1003-H23” som er delt med faglærer og studentassistent [som beskrevet her](https://uit-sok-1003-h23.github.io/mappeoppgave.html)


## Om ChatGPT/Kunsig intelligens (KI)
Det er lov å bruke ChatGPT og annen kunstid intelligens, men dialogen med KI må legges ved. Husk at god og veldokumentert bruk av KI belønnes karatkermessig. Det er lov å starte en ny chat
for å få en mer oversiktlig logg, dersom det er mye unødvendig og irrelelevant i den orginale chatten. 

Ved å legge ved chatten, dokumenterer dere også eventuelle feil som KI gjør, og slipper å hefte ved det. KI kan gjøre feil helt uten grunn, men kanskje oftere fordi spørsmålet ikke er formulert bra nok. 

Bruk av KI uten å dokumentere det er langt mer risikabelt. For det første er det 
juks, med de konsekvenser det kan medføre om det blir oppdaget. For det andre vil dere hefte ved alle feil som KI gjør. 

## Karakter
Denne mappen vil inngå i den endelige karaktervurderingen, men dere får kun godkjent/ikke godkjent på denne innleveringen. Dere vil få mulighet til å forbedre svarene 
på både Mappe1 og Mappe2 i tiden før endelig innlevering. 


## Oppgave 1:

1. Les inn ['bilparken_ssb.csv']('https://github.com/uit-sok-1003-h23/uit-sok-1003-h23.github.io/blob/main/mappe/bilparken_ssb.csv') inn i en variable df med pandas
2. Sorter tabellen med `df = df.sort_values('Personbiler vraket mot pant (prosent av bestanden)', ascending=True)`
<br><br>Du kan lage grafer av et datasett i pandas med plot-objektet. Du kan for eksempel lage et søylediagram med `df.plot.bar(etikketer, verdier)` og et scatter-plott med `df.plot.scatter(x, y)`. 
Argumentene i funksjonen er navnene på variablene i datasettet. 

3. Lag et søylediagram med prosentvis andel av kjøretøy vraket for hvert bilmerke. 

4. Lag et scatter-plott med antall biler som er over 20 år og prosentvis andel biler som er vraket. Ser det ut til å være en sammenheng?
<br><br>Du kan lage en ny variabel som den naturlige logaritmen med for eksempel `df['log20år'] = np.log(df['Over 20 år'])`.

5. Lag nye variabler med den naturlige logaritmen for antall biler som er over 20 år og prosentvis andel biler som er vraket, og lag et scatter-plott av disse. Ser det nå ut tilå være en sammenheng?


## Oppgave 2:
1. Lag tilbuds- og etterspørselsfunksjoner for Tesla. Prøv å benytte ikke-lineære funksjoner hvis mulig.

   Formen funksjonene kan du bestemme selv, men de må være slik at 
    1. En likevekt kan bestemmes.
    2. Likevektsprisen er omtrent det en Tesla koster i dag.

2. Lag en funksjon som 
    1. tar en etterspørsel- og tilbudsfunksjon, som argument (altså to argumenter)
    2. som regner ut likevekten med Sympy
    3. som tegner tilbud og etterspørselskfunksjonene, med konsument og produsentoverskudd
    
4. Anta at det pålegges en avgift på 50 0000 på hver Tesla (for hver mengde langs x-aksen, er kostnade/tilbudskurven 50 0000 høyere). Hvor mye synker etterspørselen med etterspørselsfunksjonen din?
    
3. Test funksjonen på minst to ulike etterspørselsfunksjoner og to ulike tilbudsfunksjoner (fire kombinasjoner totalt).

4. Lag en helt flat tilbudsfunksjon, og regn ut likevekten. Det kan argumenteres for at tilbudsfunksjonen for Tesla er flat i Norge, hva tror du argumentasjonen er for det?








