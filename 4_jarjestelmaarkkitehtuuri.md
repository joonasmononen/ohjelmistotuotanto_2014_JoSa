##  Järjestelmäarkkitehtuuri

Koska sovellus tullaan suurilta osin integroimaan lukkarit.metropolia.fi -palveluun, tulee sen myös käyttää hyvin vahvasti samoja arkkitehtuureja kuin lukkari-palvelun. Meidän tiedossamme ei ole lukkarit-palvelun tarkkaa arkkitehtuurista taustaa, mutta olemme listanneet asioita olettamuksen perusteella.

#### Yleistä

Sovellus ajetaan pitkälti Javascript-koodin avulla Metropolian Linux-palvelimella. Kartat on tuotu SVG-vektorigrafiikkana ja ulkoasu on tehty uusimpia HTML5 ja jQuery -kirjastoja hyödyntäen. Palvelussa pyritään viimeiseen asti olemaan käyttämättä PHP-koodia, jotta palvelun voisi tulevaisuudessa mahdollisesti myös portata hybridinatiiviksi mobiilisovellukseksi Phonegapin tai AppGyverin kaltaisen palvelun avulla edullisesti. Itse sovellus ei tuota erityisen suurta ja raskasta kuormaa palvelimelle, sillä karttojen koko on vektorigrafiikan käytöstä johtuen erittäin pieni ja lataaminenkin voidaan ääritapauksessa ulkoistaa jollekkin hajautetulle CDN-palvelulle tarvittaessa. Ainoan mahdollisen kankeuden tai pullonkaulan järjestelmän arkkitehtuurissa luo muista palveluista ladattavat datat, eli resurssit.

#### Resurssien lataaminen

Resurssien lataaminen kannattaa tehdä keskitetysti esimerkiksi kerran minuutissa palvelimen toimesta suoraan muille resurssi-dataa antaville palvelimille. Karttapalvelun data ei siis ole täysin realiaikaista, vaan on korkeintaan minuutin jäljessä. Karttapalvelun käyttäjät tekevät hakutuloksensa suoraan omalle palvelimellemme, jolloin muut palvelut eivät ruuhkaudu vaikka karttapalvelussa olisikin tungosta.

Lukkarit.metropolia.fi -palvelusta ladataan kaikki tiloja koskevat kyselyt (lukujärjestykset, aikataulut yms.). Kyseisen palvelun hakukyselyt ovat yleisesti hieman tahmeita, mutta palvelussamme käytetään dynaamista latausta, eli lisää resursseja ja muita tietoja aletaan näyttämään kartalla sitä mukaan kun client saa ne käyttöönsä palvelimelta.

HelpDeskin kautta saa varmasti käyttöönsä jonkin rajapinnan, mistä voidaan hakea tällä hetkellä käytössä olevien tietokoneiden listan, ja verrata sitä sitten kaikkien tietokoneiden listaan jolloin saadaan tieto varatuista ja vapaista tietokoneista.

WC-tilojen saatavuutta varten tarvitaan täysin uusi komponentti karttapalvelua varten. WC-tilojen lukkoihin tulee asentaa jokin anturi (esim. langallinen magneettipari tai langaton WiFi- tai RFID-ratkaisu), joka lähettää tietonsa eteenpäin, josta ne välittyvät lopulta palveimelle, joka ylläpitää listaa varatuista ja vapaista WC-tiloista.

Lisäksi HelpDeskin kautta ja muista palveluiden rajapinnoista saadaan henkilökunnalle näytettävät resurssit, kuten Ongelmat niin tiloissa, siivouksessa, tietokoneissa ja muissa palveluissa. Nämä kaikki kannattaisi kerätä yhteiseen palveluun, josta myös karttapalvelu hakisi tietonsa ja tallettaisi ilmoitukset.
