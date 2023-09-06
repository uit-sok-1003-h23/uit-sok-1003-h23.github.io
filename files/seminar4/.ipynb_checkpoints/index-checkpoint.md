{% include navbar.html %}{% include top-box.html %}

# Instruksjoner for seminar 4
På dette seminaret skal dere løse matteoppgaver med Sympy. Som dere vil se er det en god del oppgaver. I stedet for å løse hver oppgave individuelt, 
skal dere derfor lage funksjoner som tar uttrykkene som argumenter, og så løse hver oppgave. 

Oppgavene skal leveres som en jupyter-fil.


## [17_Likningssett_faktoriseringsmetoden_oppgaver.pdf](17_Likningssett_faktoriseringsmetoden_oppgaver.pdf)
Lag en funksjon `test_solve(eq)` der eq er en Sympy-ligning, og der du bruker `solve(f)` til å finne løsning på likhetene. Lag en test i funksjonen, ved å sette løsningen inn i likheten. 
Funksjonen skal returnere både svaret og resultatet av løsningen. Kjør funksjonen på alle oppgavene i én celle, og gjør koden så kort som mulig (færrest mulig linjer) . 

## [19_Grunnleggende_derivasjonsregler_oppgaver.pdf](19_Grunnleggende_derivasjonsregler_oppgaver.pdf)
Løs alle oppgavene med Sympy i én celle. Bruk `diff()`-funksjonen for å derivere, og gjør koden så kort som mulig.

## [20_Produkt_og_brokregelen_oppgaver.pdf](20_Produkt_og_brokregelen_oppgaver.pdf)

### 1)
Lag en funksjon `simp(f)` som forenkler uttrykkene i Oppgavene 1 a)-d), og løs disse oppgavene med denne funksjonen. Kommenter hvilke av oppgavene som lar seg forenkle.

### 2)
Lag en funksjon `f_deriv_prod(f, g)` som bruker produktregelen til å derivere et produkt. Argumenter skal være de to delene i produktet. 
Om produktet for eksempel er $\sqrt{3x-1}\cdot(1+x)$ skal argumentene være $\sqrt{3x-1}$ og $(1+x)$. Funksjonen skal returnere den deriverte av produktet.

### 3)
Test at produktregelen fungerer ved å sjekke at differansen mellom funksjonen du nettopp laget og derivasjon av hele utrykket med `diff()`-funksjonen er null.
Er uttrykket en brøk, for eksempel  $\frac{\sqrt{3x-1}}{(1+x)}$, blir argumentene $\sqrt{3x-1}$ og $\frac{1}{(1+x)}$. 


## [21_Kjerneregelen_oppgaver.pdf](21_Kjerneregelen_oppgaver.pdf)
### 1)
Lag en funksjon `f_deriv_chain(f, g)` som bruker kjerneregelen til å derivere et uttrykk av typen $f(g(x))$.

Har du for eksempel et uttrykk $\sqrt{3x-1}$, så er $f(y)=\sqrt{y}$ og $g(x)=\sqrt{3x-1}$. Funksjonen skal da returnere $f'(g(x))\cdot g'(x)=\frac{1}{2}\frac{1}{\sqrt{3x-1}}\cdot 3$

Husk å bytt ut $y$ med $g(x)$ (i dette tilfelle $3x-1$) før svaret returneres. 

### 2)
Bruk `f_deriv_chain(f, g)` på uttrykkene i Oppgave 1 og Oppgave 2. Du kan også bruke `f_deriv_prod(f, g)` i kombinasjon med `f_deriv_chain(f(y), g(x))`, om du synes det passer. 
Finn differansen mellom uttrykkene derivert med disse funksjonene, og uttrykkene derivert med ´diff()´-funksjonen. Denne differansen (som bør være null) er tilstrekkelig svar for hvert uttrykk. 


## [22_Derivasjon_av_logaritme_og_eksponentialfunksjoner_oppgaver.pdf](22_Derivasjon_av_logaritme_og_eksponentialfunksjoner_oppgaver.pdf)

Løs alle oppgavene i samme celle med så kort kode som mulig.
