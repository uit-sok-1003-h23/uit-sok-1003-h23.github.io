{% include navbar_open.html %}
# Installere Python, git og Jupyter på Mac


## 1. Installere python

Gå til [https://www.python.org/downloads/](https://www.python.org/downloads/)
 
## 2. Installere git

[Se her hvordan du installerer git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## 3. Installere Jupyter lab

1. åpne kommandovinduet: Åpne finder og skriv "terminal" i søkefeltet og åne terminal. 
2. Skriv inn "sodu -H pip3 install jupyterlab" ("sodu -H" er for å installere det som admin, slik at du kan åpne jupyter med kommandoen "jupyter")
3. Skriv inn passord

## 4. Hente kursmateriell fra github

For å hente filene til Jupyter gjør du slik:

2. Lag en ny mappe på ditt hjemmeområde ved å skrive inn i terminalvinduet

```mkdir sok-1003```

3. Gå så inn i den mappen du har laget ved å skrive 

```cd sok-1003```
        
4. Last ned kursmateriellet ved å kopiere inn følgende kommando i kommandovinduet: 

```git clone https://github.com/uit-sok-1003-h22/notebooks/```
        
5. Filene på github kommer til å endres, og da må du oppdatere dem. Det kan derfor være lurt å ha en 
kopi av notebooks-folderen hvor du kan gjøre egne endringer som ikke overskrives når du henter oppdaterte notater.For å lage en slik kopi skriver du:
        
```cp -r notebooks notebooks_edit```
        
6. For å åpne filene i "notebooks_edit"-mappen i jupyter lab skriver du
```
cd notebooks_edit
jupyter lab
```
