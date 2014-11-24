## Harjoitus 5: Käyttöliittymän suunnittelu

#### 1. Selitä seuraavat käsitteet:

  1. Näkymä (view)
	- Ohjelmiston eri vaiheiden / ominaisuuksien näkymät ulkoasuineen.
  2. Wireframe
	- Näkymän "luuranko" koostuu wireframeista eli rautalankamalleista. Niiden avulla voidaan määritellä sisältöjen paikat ruudulla.
  3. Mockup
	- Kuvaa / designia / mallia lopullisen tuotteen ulkonäöstä. Ohjelmistotuotannossa käytetään näyttämään miltä näkymät näyttävät loppukäyttäjälle (UI).
  4. Prototyyppi
	- Ensimmäinen versio teollisesta tuotteesta.

#### 2. Käyttöliittymän näkymät (User interface, views), oma projektiaihe. Voi tehdä pienryhmissä. 

1. Miten käyttötapaukset ja käyttöliittymät voisi yhdistää toisiinsa vaatimusmäärittelydokumentaatiossa? Perustele
vastauksesi.
	- Dokumentissa esitetään käyttöliittymät yksinkertaisin havainnekuvin. Käyttötapaukset näytetään muutaman kohdan kuvasarjalla, joihin on liitetty myös sanallinen kuvaus käyttötapauksesta.

2. Listaa järjestelmän käyttöliittymän olennaisimmat näkymät & 3. Kuvaile näkymät *sanallisesti*: mitä näkymällä tehdään ja mitä siinä näkyy. Pyri määrittelemään tässä näkymät *toiminnallisesta näkökulmasta*, älä niinkään ajattele miltä ne näyttävät & 5. Listaa jokaista näkymää kohti tieto siitä, millaista tietosisältöä tai data käyttöliittymässä näytetään.
	- Peruskarttanäkymä
		- "Kartta ja resurssit" -välilehti, sis. suodatus ja hakutoiminnot. Päänäkymänä on kartta, johon merkattu tilat resursseineen yms. Lisäksi sivulla on sidebar (mobiilissa sivupaneeli) jossa on checkboxeilla, slidereilla, hakupalkeilla yms suodattimet käytössä mahdollisuus rajata näytettäviä kohteita kartalla.
		- Datat: Oma sijainti, luokkien ja muiden tilojen käytettävyys (lukkarit), tietokoneiden käytettävyys (vapaana/varattu), vessojen käytettävyys (vapaana/varattu), tietyissä käyttäjäryhmissä myös huoltopyynnöt (helpdesk, siivouspyynnöt yms.)
	- Kohde popup
		- Tietoa valitusta kohteesta. Avautuu kun jotain kohdetta kartalla on klikattu ja ikkuna näyttää tärkeimmät tiedot kohteesta: mahdolliset resurssit, tietokoneohjelmat, vapaiden koneiden määrät, matka-aika kohteeseen, navigoinnin käynnistäminen kohteeseen nappi, ongelman ilmoittamisnappi jne..
		- Datat: tilan käytettävyys (lukkarit), tietokoneiden käytettävyys (vapaana/varattu), tietyissä käyttäjäryhmissä myös huoltopyynnöt (helpdesk, siivouspyynnöt yms.), laskenta omasta sijainnista kohteeseen (pituus, aika)
	- Navigointinäkymä
		- Navigoitaessa kohteeseen. Perusnäkymänä kartta jossa on merkattuna oma sijainti sekä kohteen sijainti. Lisäksi karttaan piirrettynä reitti, jota tulee kulkea; matka-aika ja reitin pituus kohteeseen, arvioitu saapumisaika
		- Datat: oma sijainti, kohteen sijainti, laskenta omasta sijainnista kohteeseen (pituus, aika, lyhyin reitti)
	- Ilmoita ongelmasta popup
		- Kohteen ongelmasta ilmoittaminen. Kaikki käyttäjäryhmät voivat nappia klikattuaan valita tilan / käytävän / resurssin kartalta ja ilmoittaa sitä koskevan ongelman käynnistyvällä lomakkeella Lomakkeessa seuraavat tiedot: Kohde (automaattinen täyttö tilasta / vastaavasta), Kuvaus ongelmasta, Ongelman kategoria (tietokoneen helpdesk, kiinteistön ongelmat, siivous, yms)
		- Datat: aiemmasta näkymästä mahdollisesti automaattisesti saatu kohdetieto

4. Määritä näkymien väliset siirtymät korkealla tasolla, mistä näkymästä pääsee minnekin? Millä tavoin visualisoisit tilasiirtymät?
	- Peruskarttanäkymästä voi siirtyä navigointinäkymään, valita kartalta esimerkiksi luokan ja siirtyä kohde popup -näkymään. Lisäksi peruskarttanäkymän valikosta pääsee ilmoita ongelmasta -näkymään.
	- Kohde popup -ikkunan kautta voi siirtyä ilmoita ongelmasta -näkymään, jossa valmiiksi täytettynä kyseisen tilan tiedot.
	- Navigointinäkymästä pääsee peruskarttanäkymään klikkaamalla nuoli-ikonia ja kohde popup -ikkunan saa auki valitsemala jonkin tilan.
	- Ilmoita ongelmasta popup -näkymästä voi siirtyä taaksepäin kohde popup -ikkunaan tai vaihtoehtoisesti peruskarttanäkymään riippuen käyttäjän kulkemasta polusta.

#### 3. Visualisoi listaamasi näkymät ja niihin liittyvät siirtymät

[Linkki Moqup-palveluun, johon tehty näkymät (ei hotspotteja)](https://moqups.com/mononen.joonas@gmail.com/XyncHA5V)


