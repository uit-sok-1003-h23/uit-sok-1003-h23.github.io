{% include navbar_open.html %}
# Installere Python, git og Jupyter på Windows

[Se video her!](https://mediasite.uit.no/Mediasite/Play/636342e259e441ffa5776b2ec3ebf29c1d)

## 1. Installere python 3.8.10

1. Gå til [installasjonssiden for Python 3.8.10](https://www.python.org/downloads/release/python-3810/){:target="blank"}
3. Velg filen «Windows x86-64 executable installer»  
4. Installer for alle brukere (krever elevering/admin login) og **hak av for å legge til "PATH"**. 
    
(Jeg har endret litt på "oppskriften" etter at videoen ble spilt inn. Det er nå lenker direkte til installasjonsidene istedet for til Google)

## 2. Installere git

1. Gå til [installasjonsiden for git](https://git-scm.com/downloads){:target="blank"}
4. Last ned for windows og installer for alle brukere (krever elevering/admin login)
  
## 3. Installere Jupyter lab

1. åpne kommandovinduet: Skriv "cmd" i søkefeltet på maskinen, HØYREKLIKK og start "Command Promt"/"Ledetekst" SOM ADMIN. 
2. Skriv inn `pip install jupyterlab`

## 4. Hente kursmateriell fra github

For å hente filene til Jupyter  åpner du kommanovinduet på nytt, men denne gangen UTEN Å HØYREKLIKKET, siden du nå skal arbeidet på ditt hjemmeområde. Videre gjør du slik:

2. Lag en ny mappe på ditt hjemmeområde ved å skrive inn i terminalvinduet

```mkdir sok-1003```

3. Gå så inn i den mappen du har laget ved å skrive 

```cd sok-1003```
        
4. Last ned kursmateriellet ved å kopiere inn følgende kommando i kommandovinduet: 

```git clone https://github.com/uit-sok-1003-h22/notebooks/```
        
5. Filene på github kommer til å endres, og da må du oppdatere dem. Det kan derfor være lurt å ha en 
kopi av notebooks-folderen hvor du kan gjøre egne endringer som ikke overskrives når du henter oppdaterte notater.For å lage en slik kopi skriver du:
        
```xcopy notebooks notebooks_edit```
        
6. For å åpne filene i "notebooks_edit"-mappen i jupyter lab skriver du
```
cd notebooks_edit
jupyter lab
```
