## Harjoitus 5: K�ytt�liittym�n suunnittelu

#### 1. Selit� seuraavat k�sitteet:

  1. N�kym� (view)
	- Ohjelmiston eri vaiheiden / ominaisuuksien n�kym�t ulkoasuineen.
  2. Wireframe
  3. Mockup
	- Kuvaa / designia / mallia lopullisen tuotteen ulkon��st�. Ohjelmistotuotannossa k�ytet��n n�ytt�m��n milt� n�kym�t n�ytt�v�t loppuk�ytt�j�lle (UI).
  4. Prototyyppi

#### 2. K�ytt�liittym�n n�kym�t (User interface, views), oma projektiaihe. Voi tehd� pienryhmiss�. 

1. Miten k�ytt�tapaukset ja k�ytt�liittym�t voisi yhdist�� toisiinsa vaatimusm��rittelydokumentaatiossa? Perustele
vastauksesi.

2. Listaa j�rjestelm�n k�ytt�liittym�n olennaisimmat n�kym�t & 3. Kuvaile n�kym�t *sanallisesti*: mit� n�kym�ll� tehd��n ja mit� siin� n�kyy. Pyri m��rittelem��n t�ss� n�kym�t *toiminnallisesta n�k�kulmasta*, �l� niink��n ajattele milt� ne n�ytt�v�t & 5. Listaa jokaista n�kym�� kohti tieto siit�, millaista tietosis�lt�� tai data k�ytt�liittym�ss� n�ytet��n.
	- Peruskarttan�kym�
		- "Kartta ja resurssit" -v�lilehti, sis. suodatus ja hakutoiminnot. P��n�kym�n� on kartta, johon merkattu tilat resursseineen yms. Lis�ksi sivulla on sidebar (mobiilissa sivupaneeli) jossa on checkboxeilla, slidereilla, hakupalkeilla yms suodattimet k�yt�ss� mahdollisuus rajata n�ytett�vi� kohteita kartalla.
		- Datat: Oma sijainti, luokkien ja muiden tilojen k�ytett�vyys (lukkarit), tietokoneiden k�ytett�vyys (vapaana/varattu), vessojen k�ytett�vyys (vapaana/varattu), tietyiss� k�ytt�j�ryhmiss� my�s huoltopyynn�t (helpdesk, siivouspyynn�t yms.)
	- Kohde popup
		- Tietoa valitusta kohteesta. Avautuu kun jotain kohdetta kartalla on klikattu ja ikkuna n�ytt�� t�rkeimm�t tiedot kohteesta: mahdolliset resurssit, tietokoneohjelmat, vapaiden koneiden m��r�t, matka-aika kohteeseen, navigoinnin k�ynnist�minen kohteeseen nappi, ongelman ilmoittamisnappi jne..
		- Datat: tilan k�ytett�vyys (lukkarit), tietokoneiden k�ytett�vyys (vapaana/varattu), tietyiss� k�ytt�j�ryhmiss� my�s huoltopyynn�t (helpdesk, siivouspyynn�t yms.), laskenta omasta sijainnista kohteeseen (pituus, aika)
	- Navigointin�kym�
		- Navigoitaessa kohteeseen. Perusn�kym�n� kartta jossa on merkattuna oma sijainti sek� kohteen sijainti. Lis�ksi karttaan piirrettyn� reitti, jota tulee kulkea; matka-aika ja reitin pituus kohteeseen, arvioitu saapumisaika
		- Datat: oma sijainti, kohteen sijainti, laskenta omasta sijainnista kohteeseen (pituus, aika, lyhyin reitti)
	- Ilmoita ongelmasta popup
		- Kohteen ongelmasta ilmoittaminen. Kaikki k�ytt�j�ryhm�t voivat nappia klikattuaan valita tilan / k�yt�v�n / resurssin kartalta ja ilmoittaa sit� koskevan ongelman k�ynnistyv�ll� lomakkeella Lomakkeessa seuraavat tiedot: Kohde (automaattinen t�ytt� tilasta / vastaavasta), Kuvaus ongelmasta, Ongelman kategoria (tietokoneen helpdesk, kiinteist�n ongelmat, siivous, yms)
		- Datat: aiemmasta n�kym�st� mahdollisesti automaattisesti saatu kohdetieto

4. M��rit� n�kymien v�liset siirtym�t korkealla tasolla, mist� n�kym�st� p��see minnekin? Mill� tavoin visualisoisit tilasiirtym�t?


#### 3. Visualisoi listaamasi n�kym�t ja niihin liittyv�t siirtym�t

- v�hint��n 3 n�kym��
- Voit k�ytt�� Painttia, Visiota tai esimerkiksi [Moqupsia](https://moqups.com/). 

**Palauta linkki projektinne tiedostoon (Github), mist� l�ytyv�t vastaukset teht�viin. Vaikka teitte ty�n ryhm�ty�n�, jokainen palauttaa linkin Tuubiin henkil�kohtaisesti.**