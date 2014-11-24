## Vaatimukset 

#### Funktionaaliset vaatimukset

###### Kartta ja resurssit
1. Näkymässä pitää olla taustalla kartta ja käyttäjän sijaintia kuvaava ikoni.
2. Tilojen kohdalla on luettava tilan tunnus, status (varattu, vapaa), mahdollinen vapautumisajankohta ja vapaana olevien koneiden lukumäärä.
3. Näkymässä on käytävä ilmi missä kerroksessa käyttäjä on ja kerroksien välillä on pystyttävä siirtymään.
4. Yläkulmassa on oltava Menu-painike, josta voidaan siirtyä esimerkiksi Haku ja suodatus sekä Ilmoita ongelmasta -osioihin.

###### Tietoja
1. Tietoja-valikon tulee näyttää kellonajat, jolloin tila on vapaana ja mitä kursseja siellä on mahdollisesti menossa.
2. Valikosta pitää nähdä kuinka paljon tietokoneita tilassa on vapaana.
3. Näkymässä pitää olla taulukko, joka näyttää koneisiin asennetun ohjelmiston.
4. Valikossa on oltava painikkeet Avaa tilan lukujärjestys, Navigoi kohteeseen ja Ilmoita ongelmasta.

###### Haku ja suodatus
1. Välilehdellä on oltava hakupalkki, johon voi syöttää tilan tunnuksen.
2. Suodatuksessa pitää olla vaihtoehtoina valita tilan tyyppi ja tietokoneen ohjelmisto. Vessoja etsittäessä vaihtoehtoina tulee olla miesten WC, naisten WC ja inva WC.
3. Muutosten tulee tallentua evästeisiin seuraavan käyttökerran nopeuttamista varten.
4. Välilehdellä pitää olla painikkeet Takaisin lukkariin ja Ilmoita ongelmasta.

###### Navigointi
1. Navigoinnin pitää näyttää reitti valittuun tilaan ja pitää tilan nimi näkyvillä.
2. Kerroksesta toiseen siirryttäessä portaiden / hissien edessä on oltava ikoni, joka ohjaa käyttäjän vaihtamaan kerrosta.
3. Navigoinnin tulee näyttää jäljellä oleva matka ja arvioitu aika kohteeseen.

###### Ilmoita ongelmasta
1. Lomakeen on täytettävä tila-kohta automaattisesti joko käyttäjän valitseman kohteen tai oman sijainnin perusteella. Käyttäjän on silti pystyttävä muokkaamaan kohtaa.
2. Lomakkeessa on oltava Ongelman kategoria -lista, josta käyttäjä voi valita kuvauksen (esim. ATK-ongelma, epäsiisteys) ilmoitukselleen.
3. Käyttäjän on pystyttävä kuvailemaan ongelmaa myös omin sanoin tyhjään kenttään.

#### Ei-funktionaaliset vaatimukset

1. Riittävän lyhyt vasteaika palvelimelle (sivun lataus alle 1 sekunti, kartan lataus alle 2 sekuntia, resurssien päivitys ja käyttäjän paikantaminen alle 3 sekuntia = korkeintaan 6 sekuntia kokonaislatausta katkeamattomalla 100Mbps WiFillä).
2. Evästeiden tallenus selaimeen.
3. Sovelluksen on oltava responsiivinen ja skaalautua kahdeksi eri versioksi (työpöytä ja mobiili).
4. Riittävä palvelinteho ylläpitämään lyhyttä vasteaikaa.
5. Sovelluksessa tulee käyttää vain HTML5-, JS- ja muita Phonegap-yhteensopivat tekniikoita, jotta internet-sivun lisäksi projektista voidaan helposti portata tarvittaessa mobiilisovellus.
6. Koodin tagit yms. piilonimet ja vastaavat tulee kirjoittaa HTML ja XML -standradien mukaisesti, jotta kolmansien osapuolien käytettävyysohjelmat (korkeakontrastisuuskäännökset, teksti puheeksi) toimisivat oikein.







* Ei-funktionaaliset vaatimukset
  * Esim käytettävyyteen, tietoturvaan, tehokkuuteen, skaalautuvuuteen, hintaan ja prosessimalliin liittyvät vaatimukset
* **Muista esittää vaatimukset jäljitettävässä muodossa, yksiselitteisesti**
* Keskeinen tapa (erityisesti ei-funktionaalisiin vaatimuksiin) yksiselitteisille kuvauksille on vaatimusten **mitattavuus** (software metrics)
