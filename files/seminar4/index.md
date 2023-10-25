{% include navbar.html %}{% include top-box.html %}

# Instruksjoner for seminar 4
På dette seminaret skal dere løse matteoppgaver med Sympy. Som dere vil se er det en god del oppgaver. I stedet for å løse hver oppgave individuelt, 
skal dere derfor lage funksjoner som tar uttrykkene som argumenter, og så løse hver oppgave. 

Oppgavene skal leveres som en jupyter-fil på github. Bruk repositoriet "SOK-1003-H23" som du laget til [Mappe 1](https://uit-sok-1003-h23.github.io/mappe/mappe1.html), og 
lag en undermappe "sympy" hvor du legger denne besvarelsen.

Oppgaven er levert når det ligger en besvarelse på github innnen fristen.


## [17_Likningssett_faktoriseringsmetoden_oppgaver.pdf](17_Likningssett_faktoriseringsmetoden_oppgaver.pdf)
Lag en funksjon `test_solve(eqs)` der eqs er et Sympy ligningssett, og der du bruker `solve(f)` til å finne løsning på likhetene. Lag en test i funksjonen, ved å sette løsningen inn i likheten. 
Funksjonen skal returnere både svaret og resultatet av løsningen. 

## [19_Grunnleggende_derivasjonsregler_oppgaver.pdf](19_Grunnleggende_derivasjonsregler_oppgaver.pdf)
Løs alle oppgavene med Sympy i én celle. Bruk `diff()`-funksjonen for å derivere, og gjør koden så kort som mulig (i antall tegn, ikke antall linjer).

## [20_Produkt_og_brokregelen_oppgaver.pdf](20_Produkt_og_brokregelen_oppgaver.pdf)

### 1)
Forenkl uttrykkene i Oppgavene 1 a)-d) med færrest mulig tegn. Kommenter hvilke av oppgavene som lar seg forenkle.

### 2)
Lag to funksjoner `f_deriv_prod(f, g)` og `f_deriv_frac(f, g)` som bruker henholdsvis produktregelen og brøkregelen til å derivere et uttrykk. Argumenter skal være de to delene i produktet. 
Om produktet for eksempel er $\sqrt{3x-1}\cdot(1+x)$ skal argumentene være $\sqrt{3x-1}$ og $(1+x)$. Funksjonen skal returnere den deriverte av produktet.

Deriver alle utrykene i e)-m) med disse funksjonene, men velg først ut alle produktene og deriver de, før du i neste omgang deriverer brøkene.

### 3)
Test at produktregelen fungerer ved å printe differansen mellom funksjonene over og derivering av hele uttrykket med `sp.diff()`. Du kan  sette dette inn i koden over om du vil.


## [21_Kjerneregelen_oppgaver.pdf](21_Kjerneregelen_oppgaver.pdf)
### 1)
Lag en funksjon `f_deriv_chain(f, g)` som bruker kjerneregelen til å derivere et uttrykk av typen $f(g(x))$.

Har du for eksempel et uttrykk $\sqrt{3x-1}$, så er $f(y)=\sqrt{y}$ og $g(x)=\sqrt{3x-1}$. Funksjonen skal da returnere $f'(g(x))\cdot g'(x)=\frac{1}{2}\frac{1}{\sqrt{3x-1}}\cdot 3$

Husk å bytt ut $y$ med $g(x)$ (i dette tilfelle $3x-1$) før svaret returneres. 

### 2)
a) Bruk `f_deriv_chain(f, g)` på uttrykkene i Oppgave 1 a), b), d), e) og Oppgave 2 a) og e). 

b) Bruk `f_deriv_prod(f, g)` i kombinasjon med `f_deriv_chain(f(y), g(x))` og løs Oppgave 1 h) og Oppgave 2 b)

Test samtidig resultatene med `sp.diff())`, der du stter inn kjernen i funksjonen før du deriverer. 


## [22_Derivasjon_av_logaritme_og_eksponentialfunksjoner_oppgaver.pdf](22_Derivasjon_av_logaritme_og_eksponentialfunksjoner_oppgaver.pdf)

Løs følgende oppgaver: Oppgave 1 a), b), f) og Oppgave 2 a) og b). Lag koden med så få tegn som mulig-
