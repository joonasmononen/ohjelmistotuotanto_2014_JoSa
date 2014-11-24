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
Tämä näkymä on eniten esillä ohjelmiston käytössä. Siinä suurimmassa roolissa on pohjapiirros, eli kartta koulusta. Kartalla näkyy erilaisia resursseja, kuten luokkatiloja, tietokoneita, kokoushuoneita, vessoja yms. Palvelu hakee datat kyseisten resurssien saatavuudesta muista palveluista ja esittää ne käyttäjälle graafisesti tai tekstinä – tilan saatavuus värinä (vihreä = vapaa, keltainen = pian vapautuva, punainen = varattu) ja lisäksi lisätieto-teksti (esim. "Vapaa 13:00 saakka"), tietyn tilan tietokoneiden määrä ja niistä eriteltynä vielä vapaat tietokoneet (vapaat tietokoneet / tietokoneita yhteensä = eli esimerkiksi "20/24 konetta vapaana"). Tilan saatavuus-tieto on myös vessoista (vaatii vessojen lukkoihin anturin asentamista). Käyttäjä näkee myös oman sijaintinsa kartalla ja pystyy jo pelkästään tämän toiminnon avulla näkemään läheisimmät tarvitsemansa resurssit helposti. Jotain tilaa klikkaamalla aukeaa tarkemmat tiedot kyseisestä tilasta (Tietoja popup) ja Menu-näppäintä painamalla taas saa kartan haku- ja suodatusominaisuudet käyttöönsä (Haku ja suodatus).

![4](http://users.metropolia.fi/~joonasmo/ohtu/4v2.png)

![5](http://users.metropolia.fi/~joonasmo/ohtu/5.png)

![6](http://users.metropolia.fi/~joonasmo/ohtu/6.png)

![7](http://users.metropolia.fi/~joonasmo/ohtu/7.png)

![8](http://users.metropolia.fi/~joonasmo/ohtu/8.png)


ALKUPERÄINEN OHJEISTUS:
* listaa käyttöliittymän näkymät
* niiden keskinäiset suhteet
* kuvaile mitä näkymässä tapahtuu / tehdään
