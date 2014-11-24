## Käyttöliittymä
Palvelumme käyttöliittymän testiversiota voi kokeilla osoitteessa: [https://moqups.com/mononen.joonas@gmail.com/XyncHA5V](https://moqups.com/mononen.joonas@gmail.com/XyncHA5V)

Olemme myös ottaneet kuvat kyseisistä käyttöliittymän mockupeista ja tehneet alle tarkat käyttöliittymän näkymien kuvaukset. Lisäksi lopussa oleva kaavio esittää näkymien keskinäisiä suhteita, jotka ovat havaittavissa hyvin myös aikaisemmissa kuvauksissa, kuvissa ja interaktiivisessa testiversiossa.

#### Lukkarit.metropolia.fi – Ennen varsinaista käyttöliittymää
Koska palvelumme on tarkoitettu "sisäänrakennetuksi" lukkarit.metropolia.fi yhteyteen, olemme myös tiedostaneet millaisia muutoksia / lisäyksiä se vaatii lukkarit.metropolia.fi -palvelulle. Tästä syystä teimme myös lukkarit.metropolia.fi -puolen mobiilikäyttöliittymän, joka ei varsinaisesti kuulu oman palvelumme ohjelmistuotuotantoon, mutta on oleellista palvelun ymmärtämiseksi. Olemme olettaneet että lukkarit-palvelun idea pysyy vastaavana ja oma palvelumme käynnistyy klikkaamalla uutta "Kartta ja resurssit" välilehteä, tai avaamalla jotain lukujärjestyksen kohteen kartan tai navigoinnin käynnistävistä napeista.

![1](http://users.metropolia.fi/~joonasmo/ohtu/1.png) ![2](http://users.metropolia.fi/~joonasmo/ohtu/2.png)

Yllä olevassa ensimmäisessä kuvassa on lukkarit.metropolia.fi -etusivu. Kartta ja resurssit -välilehteä klikkaamalla pystyisi käynnistämään karttapalvelumme (Kartta ja resurssit). Toisessa kuvassa on avattu sen sijaan Lukujärjestys -välilehti, jossa klikkaamalla tiettyä kohdetta käynnistyy alla näkyvän kuvan mukainen popup -käyttöliittymä. Tästä lisätietoja esittävästä näkymästä pystyisi suoraan avaamaan kohteen kartalle (Kartta ja resurssit) tai aloittamaan navigoinnin kohteeseen (Navigointi). Myös ongelmien ilmoittamisten lomakkeeseen löytyy suoralinkki tästä näkymästä (Ilmoita ongelmasta).

![3](http://users.metropolia.fi/~joonasmo/ohtu/3.png)

-----

#### Kartta ja resurssit (Päänäkymä)
Tämä näkymä on eniten esillä ohjelmiston käytössä. Siinä suurimmassa roolissa on pohjapiirros, eli kartta koulusta. Kartalla näkyy erilaisia resursseja, kuten luokkatiloja, tietokoneita, kokoushuoneita, vessoja yms. Palvelu hakee datat kyseisten resurssien saatavuudesta muista palveluista ja esittää ne käyttäjälle graafisesti tai tekstinä – tilan saatavuus värinä (vihreä = vapaa, keltainen = pian vapautuva, punainen = varattu) ja lisäksi lisätieto-teksti (esim. "Vapaa 13:00 saakka"), tietyn tilan tietokoneiden määrä ja niistä eriteltynä vielä vapaat tietokoneet (vapaat tietokoneet / tietokoneita yhteensä = eli esimerkiksi "20/24 konetta vapaana"). Tilan saatavuus-tieto on myös vessoista (vaatii vessojen lukkoihin anturin asentamista). Käyttäjä näkee myös oman sijaintinsa kartalla (sininen pallo) ja pystyy jo pelkästään tämän toiminnon avulla näkemään läheisimmät tarvitsemansa resurssit helposti. Oikeassa alareunassa pystyy vaihtamaan tarkasteltavaa kerrosta ja perinteisillä kosketusnäytön panorointi, nipistys ja venytys -eleillä pystyy liikuttamaan ja zoomaamaan karttaa haluamallaan tavalla. Mitä tahansa luokkatilaa klikkaamalla aukeaa tarkemmat tiedot kyseisestä tilasta (Tietoja popup) ja Menu-näppäintä painamalla taas saa kartan haku- ja suodatusominaisuudet käyttöönsä (Haku ja suodatus).

![4](http://users.metropolia.fi/~joonasmo/ohtu/4v2.png)

-----

#### Tietoja (popup)

Tämä näkymä avataan klikkaamalla jotain tiettyä tilaa (esimerkissä B301). Vasemman yläkulman x -näppäintä painamalla saa suljettua popupin ja palaa siihen näkymään mistä siirtyi Tietoja -näkymään. Tämän näkymän oleellisimpia tarkoituksia on esittää kyseisen tilan seuraavat kolme oppituntia / mahdollisesti vapaata palkkia, tämän jälkeen kerrotaan tietokoneiden käyttöasteesta tekstillä ja graafisesti ja tämän jälkeen taulukosta voidaan tarkastella luokkatilan tietokoneille asennettuja ohjelmia. Lisäksi alareunasta pystyy poistumaan karttapalvelusta takaisin seuraamaan kyseisen tilan lukujärjestystä klikkaamalla "Avaa tilan lukujärjestys" -painiketta. "Navigoi kohteeseen" -nappi taas käynnistää navigointipalvelun kyseiseen tilaan (Navigointi) ja ilmoita ongelmasta siirtää käyttäjän ongelman ilmoittamisesta kertovaan lomakkeeseen (Ilmoita ongelmasta), jossa on esitäytettynä kyseisen tilan nimi.

![5](http://users.metropolia.fi/~joonasmo/ohtu/5.png)

-----

#### Haku ja suodatus

Klikkaamalla Kartta ja resurssit -näkymässä Menu -näppäintä, saa avattua tämän Haku ja suodatus -näkymän. Tämän näkymän tarkoituksena on auttaa käyttäjää löytämään haluamansa palvelut nopeasti joko hakemalla spesifiä tilaa tai rajaamalla kartalla näytettäviä kohteita käyttäjän asettamien kriteerien mukaisesti. Jälleen x -näppäintä painamalla poistutaan kyseisestä näkymästä edelliseen Kartta ja resurssit -näkymään. Hakupalkkiin pystyy kirjoittamaan tilan nimen tai tunnuksen, jolloin vain kyseiset kriteerit täyttävät kohteet näytetään kartalla värillisenä ja muut harmaina. Suodata karttanäkymää alueella on erilaisia valintoja, joiden avulla käyttäjä pystyy tekemään omia kriteereitä, joiden mukaan suodattaa omaa karttanäkymäänsä selkeämmäksi. Tämän toiminnon avulla käyttäjä pystyy tekemään esimerkiksi kartan jossa näytetään vain vapaina olevia ATK-luokkia ja vapaita tietokoneita, joissa on asennettuna Adobe CC (valitut checkboxit: Tilat, Tietokoneet; dropdown: Adobe CC; loput checkboxit valitsemattomia). Käyttäjä voi myös nopeuttaa oman karttanäkymänsä latautumista tulemalla poistamaan valinnat joko Tilat, Tietokoneet tai WC-tilat -checkboxeista, jolloin kyseisen kategorian data-tietoja ei ollenkaan haeta ja näin kartan lataaminen nopeutuu. Hae tai suodata -näppäimellä tehdään valittujen kriteerien tai hakupalkin mukainen kysely palvelimelle, joka palauttaa vastauksensa käyttäjälle aukeavaan karttanäkymään (Kartta ja resurssit). Takaisin lukkariin -näppäimellä siirrytään kokonaan pois karttapalvelusta takaisin lukkarit.metropolia.fi -etusivulle. Ilmoita ongelmasta -näppäin käynnistää lomakkeen ongelmien ilmoittamiseen.

![6](http://users.metropolia.fi/~joonasmo/ohtu/6v2.png)

-----

#### Navigointi

Navigointi-tilan saa käynnistettyä joko suoraan lukkarista tai Tietoja -näkymästä löytyvällä Navigoi kohteeseen -näppäimellä. Tässä näkymässä näkyy lähes sama karttapohja kuin Kartta ja resurssit -näkymässä, mutta pelkistettynä. Luokkien ja muiden tilojen nimet näkyvät edelleen ruudussa mutta ylimääräiset tekstit on karsittu pois, väritykset ovat edelleen käytössä suodattimien mukaisesti. Käyttäjä näkee oman sijaintinsa sinisen pallon kohdalla, aivan kuten normaalissa Kartta ja resurssit -näkymässä. Erona on että nyt navigoitava kohde ja käyttäjän sijainti on yhdistetty palvelimella lasketulla lyhimmällä mahdollisella reitillä, joka esitetään kartassa sinisenä viivana. Myös navigoitavan kohteen reunaväri on paksumpi ja sininen. Näin käyttäjä pystyy vaikka täysin ilman mitään paikallistuntemusta liikkumaan hakemaansa tilaan älypuhelimensa opastamana. Alareunassa on uusi mustalla pohjalla oleva palkki, johon on kirjattu jäljellä oleva matka kohteeseen, arvioitu kesto kohteeseen ja navigoitavan kohteen nimi – näiden tietojen avulla käyttäjä pystyy hyvin arvioimaan omaa saapumisaikaansa ja matkan pituutta. Kartalla kohteiden klikkaaminen ei avaa uusia näkymiä, vaikka toki kartan liikuttelu eleillä onnistuu normaalisti, mutta ainoastaan x -näppäintä klikkaamalla pystyy poistumaan edelliseen näkymään Navigoinnista.

![7](http://users.metropolia.fi/~joonasmo/ohtu/7.png)

![8](http://users.metropolia.fi/~joonasmo/ohtu/8.png)


ALKUPERÄINEN OHJEISTUS:
* listaa käyttöliittymän näkymät
* niiden keskinäiset suhteet
* kuvaile mitä näkymässä tapahtuu / tehdään
