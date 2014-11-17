B. Oman projektin aloitus

Edelliseen analyysiin pohjautuen luonnostele seuraavia asioita ryhm�si projektiin liittyen:

##### lyhyt kuvaus projekti-ideastanne
- Metropolian lukkarikoneen yhteyteen teht�v� sis�tilapaikannus-j�rjestelm�, jonka p��toiminnallisuudet ovat lukuj�rjestykseen, hakuihin yms. pohjautuen opastaa (navigoida) k�ytt�j� haluttuun tilaan tai n�ytt�� haluttuja resursseja kartalla (esim. vapaita tietokoneita, vessoja, kirjasto yms. yleisi� palveluita). Projektin tuotenimi metroPaikannus

##### k�ytt�tapaukset (use cases): listaa oleellsimmat ranskalaisin viivoin 
- Lukuj�rjestyksen osaa (esim. oppituntia) klikkaamalla aukeaa popup-ikkuna, jossa esitell��n kyseisen tunnin tietoja. T�h�n yhteyteen nappi "Navigoi tilaan", jota klikkamalla k�ynnistyy navigointi tilaan karttanavigointina.
- Lukkarikoneen tabien (Haku, lukuj�rjestys, asetukset) joukkoon "Kartta ja resurssit", jota klikkaamalla k�ynnistyy kartta ja n�ytt�� k�ytt�j�n sijainnin sek� l�hettyvill� olevat vapaat resurssit kartalla. My�s haku- ja suodatustoiminnot oikean reunan sidebarissa (mobiililla sivupaneeli)

##### k�ytt�j�ryhm�kohtaisesti tai piirr� k�ytt�tapauskaavio
- Opiskelijat
	- Navigointi (lukkari, tilat, yms.)
	- N�yt� kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, k�yt�v�t, resurssit yms.)
- Opettajat
	- Navigointi (lukkari, tilat, yms.)
	- N�yt� kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, k�yt�v�t, resurssit yms.)
- Muu henkil�kunta
	- Navigointi (huoltopyynn�t helpdeskiin, siivousta tarvitsevat tilat yms.)
	- N�yt� kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, k�yt�v�t, resurssit yms.)
- Vierailijat (my�s muiden toimipisteiden opiskelijat)
	- Navigointi (tilat yms.)
	- N�yt� kartta ja resurssit (vapaat koneet, vessat yms.)
	- Ilmoita ongelmasta (tilat, k�yt�v�t, resurssit yms.)

##### toiminnalliset vaatimukset (functional requirements)
NAVIGOINTI
- Navigointi lukkarista saatuun tilaan
- Navigointi muuten valittuun tilaan (esim. haku, huoltopyynt�, siivousta tarvitseva tila tai vastaava metroPaikannus API:a k�ytt�v� palvelu)
	- Navigoinnin pit�� n�ytt�� kartan p��lle piirretty reitti kohteeseen
	- Portaiden / hissien kohdalla n�ytet��n vastaava ikoni, joka osoittaa k�ytt�j�n siirtyv�n toiseen kerrokseen
	- Navigoinnin pit�� n�ytt�� j�ljell� oleva matka ja arvioitu aika kohteeseen
	- Navigoinnin pit�� n�ytt�� tekstin� navigoitavan kohteen nimi
	- Navigoinnin tulee keskitt�� kartta k�ytt�j�n sijaintiin
	- Navigoinnin 
KARTTA JA RESURSSIT
- Kartan ja resurssien n�ytt�minen
	- Hakupalkki, jolla voidaan hakea:
		- Tiloja
		- Vapaita tietokoneita
		- Vapaita vessoja
	- Suodatustoiminto, jolla voidaan:
		- Valita n�ytett�v�ksi vain tiettyj� ohjelmia sis�lt�vi� tietokoneita / vapaita tiloja
			- Ohjelmina esim. Photoshop, 3D-ohjelmat yms.
		- Valita n�ytett�v�ksi vain tytt�jen / poikien / inva vessoja
	- Kartta ja suodatustoimintojen muutokset pit�� tallentua ev�steisiin, jotta k�ytt�j�n "asetukset" tallentuvat seuraava k�ytt�kertaa helpottavasti
	- Kartassa n�ytett�vien tilojen nimien yhteydess� lukee suluissa vapaiden koneiden lukum��r� / kaikkien koneiden lukum��r� (esim. 12/20 konetta k�yt�ss�)
	- Kartassa n�ytett�viss� tiloissa taustan v�ri tilan k�ytett�vyyden mukaan ja lis�ksi kuvausteksti (vihre� = vapaa XX asti, keltainen = vapautuu XX kuluttua, punainen = varattu XX asti).
- Tietyill� k�ytt�j�ryhmill� kartta ja resurssit -v�lilehden tulee n�ytt�� ilmoitetut ongelmat (huoltopyynn�t yms ilmoitetut ongelmat, my�s suodatukset ja haut sek� navigoinnit n�ihin tulee olla k�ytett�viss�)
	- T�m� toiminto tulee yhdist�� olemassaoleviin palveluihin (helpdesk), josta syyst� t�t� ei k�sitell� t�ss� projektissa sen enemp��, koska kyseess� olisi toinen kahden projektin yhdist�minen)
ILMOITA ONGELMASTA
- Kartta ja resurssit -tarkastelussa tulee olla sivupaneelissa linkki "Ilmoita ongelmasta"
	- Kaikki k�ytt�j�ryhm�t voivat nappia klikattuaan valita tilan / k�yt�v�n / resurssin kartalta ja ilmoittaa sit� koskevan ongelman k�ynnistyv�ll� lomakkeella
		- Lomakkeessa seuraavat tiedot:
			- Kohde (automaattinen t�ytt� tilasta / vastaavasta)
			- Kuvaus ongelmasta
			- Ongelman kategoria (tietokoneen helpdesk, kiinteist�n ongelmat, siivous, yms)
MUUT
- metroPaikannus API (mahdollisuus muille palveluille sy�tt�� navigoitavia kohteita, k�ytt�� karttaa ja resurssitietoja yms.)

##### laadulliset vaatimukset (non-functional requirements)
- Riitt�v�n lyhyt vasteaika palvelimelle (sivun lataus alle 1 sekunti, kartan lataus alle 2 sekuntia, resurssien p�ivitys ja k�ytt�j�n paikantaminen alle 3 sekuntia = korkeintaan 6 sekuntia kokonaislatausta katkeamattomalla 100Mbps WiFill�)
- Ev�steiden tallennus k�ytettyyn selaimeen
- Portability � Vain HTML5, JS ja muut Phonegap yhteensopivat tekniikat, jotta internet-sivun lis�ksi projektista voidaan helposti portata tarvittaessa mobiilisovellus
- Responsiivisuus (kaksi versiota: ty�p�yt�, mobiili)
- Kapasiteetti (riitt�v� palvelinteho yll�pit�m��n riitt�v�n lyhyt vasteaika)
- K�ytett�vyys
	- Koodin tagit yms. piilonimet ja vastaavat tulee kirjoittaa HTML ja XML -standradien mukaisesti, jotta kolmansien osapuolien k�ytett�vyysohjelmat (korkeakontrastisuusk��nn�kset, teksti puheeksi yms) toimisivat oikein.

##### k�ytt�liittym�luonnos (mockup)
Periaatteessa n�ht�viss� lukkarit.metropolia.fi -osoitteessa, sama design yms. kuvaillut toiminnot pystyy t�ss� vaiheessa kuvittelemaan kuvailujen perusteella sivuihin upotettuina.
