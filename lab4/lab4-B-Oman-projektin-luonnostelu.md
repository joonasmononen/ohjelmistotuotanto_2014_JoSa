B. Oman projektin aloitus

Edelliseen analyysiin pohjautuen luonnostele seuraavia asioita ryhmäsi projektiin liittyen:

##### lyhyt kuvaus projekti-ideastanne
- Metropolian lukkarikoneen yhteyteen tehtävä sisätilapaikannus-järjestelmä, jonka päätoiminnallisuudet ovat lukujärjestykseen, hakuihin yms. pohjautuen opastaa (navigoida) käyttäjä haluttuun tilaan tai näyttää haluttuja resursseja kartalla (esim. vapaita tietokoneita, vessoja, kirjasto yms. yleisiä palveluita). Projektin tuotenimi metroPaikannus

##### käyttötapaukset (use cases): listaa oleellsimmat ranskalaisin viivoin 
- Lukujärjestyksen osaa (esim. oppituntia) klikkaamalla aukeaa popup-ikkuna, jossa esitellään kyseisen tunnin tietoja. Tähän yhteyteen nappi "Navigoi tilaan", jota klikkamalla käynnistyy navigointi tilaan karttanavigointina.
- Lukkarikoneen tabien (Haku, lukujärjestys, asetukset) joukkoon "Kartta ja resurssit", jota klikkaamalla käynnistyy kartta ja näyttää käyttäjän sijainnin sekä lähettyvillä olevat vapaat resurssit kartalla. Myös haku- ja suodatustoiminnot oikean reunan sidebarissa (mobiililla sivupaneeli)

##### käyttäjäryhmäkohtaisesti tai piirrä käyttötapauskaavio
- Opiskelijat
	- Navigointi (lukkari, tilat, yms.)
	- Näytä kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, käytävät, resurssit yms.)
- Opettajat
	- Navigointi (lukkari, tilat, yms.)
	- Näytä kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, käytävät, resurssit yms.)
- Muu henkilökunta
	- Navigointi (huoltopyynnöt helpdeskiin, siivousta tarvitsevat tilat yms.)
	- Näytä kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, käytävät, resurssit yms.)
- Vierailijat (myös muiden toimipisteiden opiskelijat)
	- Navigointi (tilat yms.)
	- Näytä kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, käytävät, resurssit yms.)

##### toiminnalliset vaatimukset (functional requirements)
NAVIGOINTI
- Navigointi lukkarista saatuun tilaan
- Navigointi muuten valittuun tilaan (esim. haku, huoltopyyntö, siivousta tarvitseva tila tai vastaava metroPaikannus API:a käyttävä palvelu)
	- Navigoinnin pitää näyttää kartan päälle piirretty reitti kohteeseen
	- Portaiden / hissien kohdalla näytetään vastaava ikoni, joka osoittaa käyttäjän siirtyvän toiseen kerrokseen
	- Navigoinnin pitää näyttää jäljellä oleva matka ja arvioitu aika kohteeseen
	- Navigoinnin pitää näyttää tekstinä navigoitavan kohteen nimi
	- Navigoinnin tulee keskittää kartta käyttäjän sijaintiin
	- Navigoinnin 
KARTTA JA RESURSSIT
- Kartan ja resurssien näyttäminen
	- Hakupalkki, jolla voidaan hakea:
		- Tiloja
		- Vapaita tietokoneita
		- Vapaita vessoja
	- Suodatustoiminto, jolla voidaan:
		- Valita näytettäväksi vain tiettyjä ohjelmia sisältäviä tietokoneita / vapaita tiloja
			- Ohjelmina esim. Photoshop, 3D-ohjelmat yms.
		- Valita näytettäväksi vain tyttöjen / poikien / inva vessoja
	- Kartta ja suodatustoimintojen muutokset pitää tallentua evästeisiin, jotta käyttäjän "asetukset" tallentuvat seuraava käyttökertaa helpottavasti
	- Kartassa näytettävien tilojen nimien yhteydessä lukee suluissa vapaiden koneiden lukumäärä / kaikkien koneiden lukumäärä (esim. 12/20 konetta käytössä)
	- Kartassa näytettävissä tiloissa taustan väri tilan käytettävyyden mukaan ja lisäksi kuvausteksti (vihreä = vapaa XX asti, keltainen = vapautuu XX kuluttua, punainen = varattu XX asti).
- Tietyillä käyttäjäryhmillä kartta ja resurssit -välilehden tulee näyttää ilmoitetut ongelmat (huoltopyynnöt yms ilmoitetut ongelmat, myös suodatukset ja haut sekä navigoinnit näihin tulee olla käytettävissä)
	- Tämä toiminto tulee yhdistää olemassaoleviin palveluihin (helpdesk), josta syystä tätä ei käsitellä tässä projektissa sen enempää, koska kyseessä olisi toinen kahden projektin yhdistäminen)
ILMOITA ONGELMASTA
- Kartta ja resurssit -tarkastelussa tulee olla sivupaneelissa linkki "Ilmoita ongelmasta"
	- Kaikki käyttäjäryhmät voivat nappia klikattuaan valita tilan / käytävän / resurssin kartalta ja ilmoittaa sitä koskevan ongelman käynnistyvällä lomakkeella
		- Lomakkeessa seuraavat tiedot:
			- Kohde (automaattinen täyttö tilasta / vastaavasta)
			- Kuvaus ongelmasta
			- Ongelman kategoria (tietokoneen helpdesk, kiinteistön ongelmat, siivous, yms)
MUUT
- metroPaikannus API (mahdollisuus muille palveluille syöttää navigoitavia kohteita, käyttää karttaa ja resurssitietoja yms.)

##### laadulliset vaatimukset (non-functional requirements)
- Riittävän lyhyt vasteaika palvelimelle (sivun lataus alle 1 sekunti, kartan lataus alle 2 sekuntia, resurssien päivitys ja käyttäjän paikantaminen alle 3 sekuntia = korkeintaan 6 sekuntia kokonaislatausta katkeamattomalla 100Mbps WiFillä)
- Evästeiden tallennus käytettyyn selaimeen
- Portability – Vain HTML5, JS ja muut Phonegap yhteensopivat tekniikat, jotta internet-sivun lisäksi projektista voidaan helposti portata tarvittaessa mobiilisovellus
- Responsiivisuus (kaksi versiota: työpöytä, mobiili)
- Kapasiteetti (riittävä palvelinteho ylläpitämään riittävän lyhyt vasteaika)
- Käytettävyys
	- Koodin tagit yms. piilonimet ja vastaavat tulee kirjoittaa HTML ja XML -standradien mukaisesti, jotta kolmansien osapuolien käytettävyysohjelmat (korkeakontrastisuuskäännökset, teksti puheeksi yms) toimisivat oikein.

##### käyttöliittymäluonnos (mockup)
Periaatteessa nähtävissä lukkarit.metropolia.fi -osoitteessa, sama design yms. kuvaillut toiminnot pystyy tässä vaiheessa kuvittelemaan kuvailujen perusteella sivuihin upotettuina.
