## Käyttötapaukset

#### Järjestelmän loppukäyttäjät

Sovelluksen käyttäjäryhmää ovat Metropolian opiskelijat, opettajat ja muu henkilökunta (vahtimestari, siistijät).

#### Käyttötapauskaavio

![](http://users.metropolia.fi/~santtk/Ohjelmistotuotanto-projekti-kaavio01.PNG)

#### 1. käyttötapausskenaario

1. Alkutila <br >
     Käyttäjä etsii luokkahuonetta jossa hänellä on alkamassa oppitunti. Hän kirjautuu sisään Tuubiin ja valitsee          Lukkarit-osiosta Kartta ja resurssit -välilehden.

2. Normaali kulku <br >
     Vaihtoehtoina on joko hakea luokkahuonetta tunnuksella tai selata karttaa ja etsiä tila manuaalisesti. Käyttäjä       valitsee Haku ja suodatus -toiminnon, kirjoittaa luokkatunnuksen ja valitsee Hae tai suodata.
      
3. Lopputila <br >
     Sovellus näyttää luokkahuoneen kartalla ja ruudulle ilmestyy Navigoi kohteeseen -painike.   

4. Miten normaali kulku voi mennä pieleen?
     Käyttäjä kirjoittaa luokaahuoneen tunnuksen sijaan luokaahuoneen nimen (esim. Dolphin), eikä haku tuota tulosta.

#### 2. käyttötapausskenaario

1. Alkutila <br >
      Käyttäjä haluaa tietää onko koulussa vapaana tietokonetta, jossa on asennettuna Adobe Premiere Pro CC -ohjelma.          Hän kirjautuu sisään Tuubiin ja valitsee Lukkarit-osiosta Kartta ja resurssit -välilehden.

2. Normaali kulku <br >
      Käyttäjä valitsee Haku ja suodatus -toiminnon, merkitsee haluamansa ominaisuudet ja valitsee Hae tai suodata.

3. Lopputila <br >
      Sovellus näyttää missä luokissa on vapaita tietokoneita kyseisillä ominaisuuksilla. Käyttäjä voi valita jonkin           luokista ja klikata Navigoi kohteeseen.

4. Miten normaali kulku voi mennä pieleen?
     Käyttäjä ei huomaa, että Adobe Premierestä on useampi versio (CS6, CC), valitsee väärän ja päätyy luokkaan, jossa ei pystykään työskentelemään.

#### 3. käyttötapausskenaario

1. Alkutila <br >
     Siistijä on siivoamassa auditoriota. Hän huomaa, että ylemmän sisäänkäynnin elektroninen tunniste ei toimi. Hän valitsee Lukkarit-osiosta Kartta ja resurssit -välilehden.

2. Normaali kulku <br >
     Siistijä joko valitsee perusnäkymästä Ilmoita ongelmasta -välilehden tai etsii ensin auditorion, avaa tilan kohde popup -ikkunan ja valitsee Ilmoita ongelmasta saadaksen esille esitäytetyn lomakkeen. Hän täyttää lomakkeeseen ongelman kategorian ja kertoo sanallisesti mistä on kyse. Tämän jälkeen hän valitsee Tallenna ilmoitus.
      
3. Lopputila <br >
     Sovellus ilmoittaa, että tallennus on onnistunut ja palauttaa käyttäjän peruskarttanäkymään.

4. Miten normaali kulku voi mennä pieleen?
     Siistijä ei huomaa antaa tarpeeksi tarkkaa selvitystä ongelmasta ja vahtimestari saapuu pyynnön huomattuaan alemmalle ovelle, jonka tunniste on kunnossa.
