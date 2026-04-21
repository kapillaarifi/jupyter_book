# Teknologian kypsyysaste apuna vaihtoehtojen vertailussa

_Julkaistu alunperin 2022-12-12._

[Takaisin etusivulle](https://www.kapillaari.fi)

Kun uusia asioita kehitetään, olisi hyvä olla yhteinen kieli ja viitekehys asioiden käsittelylle. Tutkimuksen ja tuotekehityksen käyttöön kehitettiin Yhdysvalloissa 70-luvulla teknologian kypsyysasteen (Technology Readiness Level, TRL) käsite, joka mittaa tietyn teknologian kehitysvaihetta ja valmiutta markkinoille. Tässä kirjoituksessa otetaan ensiaskeleet tähän TRL-asteikkoon tutustumiseksi.

## Käsitteiden määrittelyä

Tiede ja tekniikka menevät koko ajan eteenpäin. Perustutkimuksessa pyritään tunnistamaan eri tilanteisiin liittyviä ilmiöitä ja ymmärtämään niihin liittyviä säännönmukaisuuksia. Yritykset kehittävät uusia tuotteita ja parantavat olemassa olevia, ja kuluttajat etsivät rahalleen parempaa laatua tai samaa tuotetta halvemmalla hinnalla. Tavoite tehdä nykyisiä asioita aiempaa halvemmalla ja helpommin tai toisaalta saada tehtyä uusia asioita, joita ennen ei pystytty tekemään, toimii pitkäkestoisena voimana kehitykselle.

Tekniikka-sanalle [Kielitoimiston sanakirja](https://www.kielitoimistonsanakirja.fi/tekniikka) antaa kolme eri määritelmää: 1) ”luonnon mahdollisuuksien hyödyntäminen, varsinkin aineellisten tuotteiden valmistus ja käyttö luonnontieteiden sovelluksiin perustuvin keinoin; myös näistä keinoista”, 2) ”teknisistä laitteista, rakenteista tai muista sellaisista” ja 3) ”jonkin valmistuksessa tai suorittamisessa käytettävä menetelmä, teko- tai suoritustapa; teko- tai suoritustaito”.

Teknologia-sanalle [Kielitoimiston sanakirja](https://www.kielitoimistonsanakirja.fi/teknologia) antaa seuraavan selityksen: ”varsinkin pitkälle kehittynyt tekniikka ja sen sovellukset, usein nähtynä laajoina kokonaisuuksina”. [Suomen etymologinen sanakirja](https://kaino.kotus.fi/suomenetymologinensanakirja/?p=article&amp;etym_id=ETYM_c5dfe080399b1a798e3de433f18eecfd&amp;word=teknologia) antaa lisätietoina, että teknologia-sana tulee suomen kieleen ensisijaisesti englannin kielen *technology*-sanasta, joka tarkoittaa teknologiaa tai tekniikkaa. Englannin kieleen sana taas tulee kreikan *tekhnología*-sanasta, joka muodostuu sanoista *tékhnē* ”taito, tiede” ja *-logía* ”tutkiminen, puhuminen”. Englannin kielessä *technology*-sanalla voidaan tarkoittaa toisaalta tiedon soveltamista käytännönläheisten tavoitteiden saavuttamiseen yksityiskohtaisella ja toistettavalla tavalla; tai toisaalta tällaisen prosessin lopputuotosta [Wikipedia/Technology](https://en.wikipedia.org/wiki/Technology).

Tekniikan ja teknologian käsitteiden määritelmiä vuosina 1880-1999 on tutkittu pro gradu -työssä [Heinonen 2018](http://urn.fi/URN:NBN:fi:hulib-201803281560). Työn mukaan 1880-luvulla tekniikka-sana tarkoitti taidetta ja taitoja (esimerkiksi taidemaalarin sivellintekniikkaa), mutta hiljalleen siirryttäessä kohti 1950-lukua, käsitteen abstraktiotaso nousi ja kattavuus laajeni tarkoittamaan monia laitemaailman ilmiöitä. Teknologia käsitteenä taas tarkoitti 1800-luvun lopussa ja 1950-luvun tuntumaan asti ensisijaisesti tiettyjä oppialoja, eikä siinä tapahtunut tämän ajanjakson aikana erityisiä muutoksia. Tämän jälkeen teknologia-käsitteen abstraktiotaso ja kattavuus lähtivät kuitenkin kasvamaan ja noin 1970-luvulla tekniikka- ja teknologia-käsitteet olivat suurelta osin samalla tasolla. Tämän jälkeen teknologia-sanan abstraktiotaso on noussut edelleen, kun taas tekniikka-sanalla tarkoitetaan konkreettisempia asioita. (Heinonen 2018, luku 6.1)

Tekniikka- ja teknologia-sanoilla on siis päällekkäisyyksiä, mutta teknologialla tarkoitetaan tässä tekniikka-sanaan verrattuna laajempaa teknisen tiedon ja sen käytännön sovellutusten kokonaisuutta, jolla on myös sosiaalisia, taloudellisia ynnä muita vaikutuksia.

Englannin kielen sana ”readiness” tarkoittaa suomeksi valmiutta ja ”level” tasoa tai kehitysastetta. ”Technology Readiness Level” voisi siis suomeksi olla esimerkiksi ”teknologian valmiustaso” tai ”teknologian kehitysaste”.

TRL pyrkii kuvaamaan tietyn teknologian kypsyyttä (eng. maturity) siihen, että teknologia on saatavilla markkinoilla. Koska TRL-tasoilla kuvataan tätä kypsyyttä markkinoille, on TRL:stä käytetty suomenkielistä termiä: ”teknologian kypsyystaso” [Leppälä 2011](http://www.provisec.fi/Sources/TRL_opas.pdf), [Älymaatalous 2030 tiekartta](https://projects.luke.fi/agrihubi/wp-content/uploads/sites/52/2022/02/Alymaatalous-2030-tiekartta-.pdf). Myös termiä: ”teknologian kypsyysaste” on käytetty usein [Sitra 2017](https://www.sitra.fi/app/uploads/2017/02/Cleantech-teknologiat_lisaavat_tyollisyytta_ja_parantavat_vaihtotasetta.pdf), [fingridlehti.fi 24.9.2020](https://www.fingridlehti.fi/tutkimus-ja-kehitystyo-tahyaa-tulevaisuuteen), [Heino 2018](https://urn.fi/URN:NBN:fi-fe2018052424615). Tämä viimeisin termi ”teknologian kypsyysaste” näyttää antavan eniten tuloksia internetin hakukoneista, joten käytetään sitä myös tässä kirjoituksessa.

Kypsyysaste-luokituksen määrittämiseksi on olemassa ”Technology Readiness Assessment”, TRA, eli teknologian kypsyysasteen arviointi. Kypsyysasteluokkien käyttämistä ajatellen yhteisten arviointiperusteiden olemassaolo ja niiden käyttäminen ovat tärkeitä asioita. Tekstin loppupuolella näitä sivutaan lyhyesti.


## Esimerkkejä teknologioista rakennusalalla

Tämän kirjoittajalla ei ole tiedossa, että jossain olisi valmiina hyvää listausta rakennusalan teknologioista. Noin yleisesti ottaen ensimmäiset esimerkit rakennusalan teknologioista liittyvät kuitenkin rakennusmateriaaleihin ja -tuotteisiin sekä suunnittelun ja työvaiheen menetelmiin, joista seuraavassa on listattu muutamia.  Huom! Listaus on satunnainen otanta ensimmäisenä mieleen tulleista asioista, eikä millään muotoa kattava tai systemaattinen.



- Betoni ja betonielementit
	- Paikallavalurakentaminen muottien avulla (esimerkkinä pitkään käytetystä talonrakentamisen teknologiasta)
	- Betonielementtirakentaminen, kuten sandwich-paneelit, ontelolaatat ja esijännitetyt rakenteet
	- Betoniteknologia, tarkoittaen tässä yhteydessä erilaisia keinoja säätää ja parantaa betonin ominaisuuksia käyttötarpeita vastaaviksi
- Puu ja puutuotteet
	- Massiivihirsirakennukset
	- Rankarunkoiset paikalla tehdyt rakennukset
	- LVL- ja CLT-rakenteet
	- Puuteknologia, sisältäen puun rakenteen ja ominaisuuksien kuvaamisen ja tarkoituksellisen muokkaamisen sekä erilaisten puutuotteiden kehittämisen
- Teräs, tiili, harkko, kermit, kalvot, lämmöneristeet, liimat, jne.
	- Eri materiaaleja ja niistä valmistettuja tuotteita voitaisiin pitää omina teknologioinaan esimerkiksi silloin, kun tietyn teknologian käyttö suurelta osin poissulkee jonkin toisen teknologian käytön
	- Jos taas kohteessa on yhdistelty eri teknologiaratkaisuja, niin silloin voitaisiin puhua hybridikohteista tai yhdistelmäteknologioista
- Suunnittelussa käytettäviä teknologioita
	- Takymetrimittaukset
	- Laserkeilaukset
	- Erilaiset tietokoneilla käytettävät laskenta- ja mitoitusohjelmat
	- CAD-ohjelmat
	- BIM-mallinnusohjelmat
- Työmaavaiheen teknologioita
	- Nosturit, esimerkkinä perinteikkäästä rakentamista muuttaneesta teknologiasta
	- Olosuhdeseurantalaitteet, jotka perustuvat taas omiin teknologioihinsa
	- Kännykkäsovellukset työmaan toteutumatietojen keräämiseen
	- Dronet kohteen lähtötietojen keräämiseen ja työmaan seurantaan
	- AR-järjestelmät asennusta ja tarkastusta helpottamaan
- Käyttövaihe
	- Hissit, mahdollistivat kerrostalot ja korkean rakentamisen
	- Koneellinen ilmanvaihto
	- Lämpöpumput
	- Talotekniikan mittaus-, säätö- ja seurantajärjestelmät.


Eli rakennusalalla on käytössä valtava määrä erilaisia teknologioita, joista osa on ollut käytössä pitkään ja osa on uudempaa. Eri teknologiat myös linkittyvät toisiinsa eri tavoin. Joissain yhteydessä saatetaan puhua pienemmästä kokonaisuudesta, kuin toisessa.

Uusista teknologioista (emerging technologies) on annettu esimerkkejä ainakin [tällä Wikipedia-sivulla](https://en.wikipedia.org/wiki/List_of_emerging_technologies) ja niitä ovat esimerkiksi 6G-tiedonsiirtoverkot, kvanttitietokoneet, energian kerääminen (energy harvesting), aerogeeli-eriste ja rakentamiseen liittyvänä nollaenergiarakennukset. Viimeiseen kohtaan liittyen on hyvä huomata, että Suomessa uudet rakennukset ovat määritelmällisesti *lähes* nollaenergiarakennuksia (nZEB), mutta käytännössä energiankulutukseltaan kaukana nollasta. Mielenkiintoinen ja hauska on myös [listaus teknologioista](https://en.wikipedia.org/wiki/List_of_existing_technologies_predicted_in_science_fiction), jotka ovat ensin esiintyneet scifi-kirjallisuudessa, mutta jotka ovat myöhemmin toteutuneet myös käytännössä. Rakennusten kannalta tällaisia ovat olleet esimerkiksi aurinkopaneelit, älykodit, virtuaalitodellisuus, pilvenpiirtäjät ja sähköiset ulkovalot.


## Technology Readiness Level (TRL) – Teknologian kypsyysaste

Teknologian kypsyysasteen luokitusjärjestelmän historiaa on kuvattu kirjallisuudessa esimerkiksi lähteissä [Mankins 2009](https://doi.org/10.1016/j.actaastro.2009.03.058), [EARTO 2014](https://www.earto.eu/wp-content/uploads/The_TRL_Scale_as_a_R_I_Policy_Tool_-_EARTO_Recommendations_-_Final.pdf) ja [Héder 2017](https://www.innovation.cc/discussion-papers/2017_22_2_3_heder_nasa-to-eu-trl-scale.pdf).

Teknologian kypsyysasteluokitus kehitettiin alun perin NASA:ssa 1970-luvulla, jossa järjestelmää myös kehitettiin eteenpäin 1980- ja 1990-luvuilla. Nykyisenkaltainen luokitus julkaisiin ensimmäisen kerran vuonna 1995 ([Mankins 1995](https://aiaa.kavi.com/apps/group_public/download.php/2212/TRLs_MankinsPaper_1995.pdf) ), joka sittemmin otettiin käyttöön myös Yhdysvaltojen puolustusministeriössä vuonna 2000. Tämän jälkeen TRL-luokituksen käyttö laajeni myös muihin avaruusjärjestöihin ja organisaatioihin. Vuonna 2013 julkaistiin kansainvälinen standardi ISO 16290:2013, jossa on kuvattuna teknologian kypsyysasteen määritelmät ja ohjeita kypsyysasteen määrittämiseen. ISO-standardi on julkaistu myös eurooppalaisena standardina SFS-EN 16603-11:2019. Teknologian kypsyysaste on ollut ja on käytössä myös EU:n Horizon 2020- ja Horizon Europe -ohjelmissa, joista ensimmäisen toimikausi oli 2014-2020 ja jälkimmäisen 2021-2027.

Seuraavassa taulukossa on esitetty teknologian kypsyysasteluokkien kuvaukset muutamasta eri lähteestä, sekä kunkin luokan suomenkielinen kuvaus. Suomenkieliset kuvaukset hyödyntävät aiemmin mainittuja suomenkielisiä lähteitä, mutta sanamuotoja on muutettu selkeyden ja soveltuvuuden parantamiseksi.


```{table} Teknologian kypsyysasteen luokitusasteikko. (Huom 1) Industrially relevent environment in the case of key enabling technologies. (Huom 2) Competitive manufacturing in the case of key enabling technologies; or in space.</figcaption>

| TRL | Mankins 1995 | ISO/FDIS 16290:2013 ja SFS-EN 16603-11:2019 | Horizon Europe, Work programme 2023-2024, 13. General Annexes | Suomenkielinen kuvaus |
|----|----|----|----|----|
|1 | Basic principles observed and reported  | Basic principles observed and reported | Basic principles observed | Perusperiaatteet on havaittu |
|2 | Technology concept and/or application formulated | Technology concept and/or application formulated | Technology concept formulated | Teknologiakonsepti on muodostettu ja/tai sovelluskohde on tunnistettu |
|3 | Analytical and experimental critical function and/or characteristic proof-of-concept | Analytical and experimental critical function and/or characteristic proof-of-concept | Experimental proof of concept | Keskeiset toiminnallisuudet ja/tai ominaisuudet on osoitettu analyyttisellä ja kokeellisella soveltuvuusselvityksellä (proof-of-concept) |
|4 | Component and/or breadboard validation in laboratory environment | Component and/or breadboard functional verification in laboratory environment | Technology validated in a lab | Teknologian keskeisten osien toiminta on todennettu laboratorio-olosuhteissa |
|5 | Component and/or breadboard validation in relevant environment | Component and/or breadboard critical function verification in a relevant environment | Technology validated in a relevant environment (Huom 1) | Teknologian keskeisten osien toiminta on todennettu loppukäytön kaltaisissa olosuhteissa |
|6 | System/subsystem model or prototype demonstration in a relevant environment (ground or space) | Model demonstrating the critical functions of the element in a relevant environment | Technology demonstrated in a relevant environment (Huom 1) | Lopullisen järjestelmän prototyyppiä on käytetty keskeisten toiminnallisuuksien testaamiseen loppukäytön kaltaisissa olosuhteissa |
|7 | System prototype demonstration in a space environment | Model demonstrating the element performance for the operational environment | System prototype demonstration in an operational environment | Lopullisen järjestelmän prototyyppiä on testattu onnistuneesti käyttöolosuhteissa |
|8 | Actual system completed and ”flight qualified” through test and demonstration (ground or space) | Actual system completed and accepted for flight (”flight qualified”) | System complete and qualified | Järjestelmä on valmis ja hyväksytty käytettäväksi todellisissa kohteissa |
|9 | Actual system ”flight proven” through successful mission operations | Actual system ”flight proven” through successful mission operations | Actual system proven in operational environment (Huom 2) | Järjestelmää on käytetty todellisissa käyttökohteissa ja se on osoittautunut niissä toimivaksi |

```


Taulukon englanninkielisistä kuvauksista huomataan, että eri lähteissä esitetyt luokitukset poikkeavat hieman toisistaan, mikä saattaa johtaa hieman eri lopputuloksiin teknologialle määritettävässä luokituksessa. Esimerkiksi vaatimusten asettaminen koko järjestelmälle tai vain sen yksittäiselle osalle on kuvattu eri lähteissä hieman eri tavoin. Suomenkielisissä kuvauksissa on pyritty yhdistämään soveltuvin osin eri lähteiden kuvauksia.

Taulukossa esitettyä luokitusta tulisi pystyä käyttämään moniin eri sovelluksiin, kuten rakennusmateriaaleihin, rakenneratkaisuihin, laskenta- ja suunnitteluohjelmiin, erilaisiin laitteisiin ja moniin muihin asioihin. Luokituksessa käytettyjä käsitteitä tulee tulkita siis väljästi. Esimerkiksi ”laboratorio-olosuhteilla” voidaan tarkoittaa kaikenlaisia kontrolloitavissa olevia, mutta todelliseen käyttötilanteeseen nähden yksinkertaistettuja olosuhteita, kuten olosuhdehuoneita, laboratoriohenkilöstön valvomia prosesseja, vapaaehtoisesti koejärjestelyihin osallistuneita henkilöitä sekä loppukäyttötilanteeseen mahdollisesti liittyvien aikataulu- ja resurssipaineiden puuttumista.

Rakennusfysiikassa puhutaan harvoin prototyypeistä, vaan useammin esimerkiksi testi- tai koekappaleista, koerakenteista, koerakennuksista tai pilottikohteista, sekä joskus myös living labeista. Edellä olevassa taulukossa prototyypillä tarkoitetaan mitä tahansa kehitettävää tuotetta, palvelua tai ohjelmistoa, kunhan se sisältää kaikki loppujärjestelmään kuuluvat osat ja toiminnot.

Teknologian kypsyysasteluokkia yhdistellään eri lähteissä isommiksi kokonaisuuksiksi. Luokat TRL 1 – TRL 2 voidaan käsittää perustutkimukseksi, luokat TRL 3 – TRL 5 teknologian eri osioiden kehitystyöksi, luokat TRL 6 – TRL 7 järjestelmän pilotoimiseksi ja luokat TRL 8 – TRL 9 käyttöönotoksi. Myös muita jaotteluja on käytössä [EARTO 2014](https://www.earto.eu/wp-content/uploads/The_TRL_Scale_as_a_R_I_Policy_Tool_-_EARTO_Recommendations_-_Final.pdf). Jos ollaan tekemisissä aivan uusien tieteen ilmiöiden kanssa [linkki](https://enspire.science/trl-scale-horizon-europe-erc-explained/), niin tällöin ei olla vielä TRL-portailla laisinkaan!

Tietyn TRL-luokan saavuttaminen edellyttää, että kyseisen luokan tehtävät on tehty ja teknologian kehitystyölle asetetut tavoitteet on saavutettu.



## TRL-luokan arviointi

Teknologian kypsyysasteille on olemassa eri lähteissä keskenään hieman erilaisia kuvauksia, jolloin eri lähteiden mukaan määritettyjen TRL-luokkien välillä voi olla eroja. Luokituksissa voi olla myös alakohtaisia eroja, esimerkiksi lääketieteen alalla kypsyysaste voi olla sidottu uusien lääkkeiden kehittämisvaiheisiin[linkki]("https://www.excellenting.com/drug_discovery_trl/), jollaista käytäntöä ei ole muilla aloilla. Muita alakohtaisia TRL-luokituksia on kehitetty jo mainittujen avaruustoiminnan, ilmailun ja puolustusteknologian lisäksi myös [hiilidioksidin talteenottoon](https://www.pnnl.gov/main/publications/external/technical_reports/PNNL-21737.pdf), [teollisiin tuotantomenetelmiin](https://en.wikipedia.org/wiki/Manufacturing_readiness_level) ja luultavasti moneen muuhunkin aihealueeseen. TRL-luokitus on suositeltu aina räätälöitävän sovelluskohteen tarpeita ajatellen ([Héder 2017](https://www.innovation.cc/discussion-papers/2017_22_2_3_heder_nasa-to-eu-trl-scale.pdf)).

Rakentamisen ja rakennusfysiikan osalta voisi olla, että esimerkiksi pitkään käytössä olleet ontelolaatat normaaleilla käyttötavoilla voisivat kuulua kypsyysasteikon luokkaan TRL 9, erilaiset uudet pilottikohteissa testattavat katto- ja seinäelementtijärjestelmät luokiin TRL 6 – TRL 7, laboratoriotiloissa ja koerakennuksissa testattavat uudet rakenteet tai niihin liittyvät tuotteet luokkiin TRL 4 – TRL 5, ja tutkimusvaiheessa selvityksen alla olevat rakenteet luokkiin TRL 1 – TRL 3.

Teknologian kypsyysasteen luokituksessa tulee ottaa huomioon paitsi teknologiaan liittyvät tekniset ratkaisut, myös se, että käytetäänkö järjestelmää sille alun perin tarkoitetuissa olosuhteissa. Jos pitkälle kehitettyä (ns. kypsää) teknologiaa käytetään uusissa olosuhteissa, on tällöin teknologialle määritettävä TRL-luokka matalampi, kuin että samaa teknistä ratkaisua käytettäisiin sille alun perin suunnitelluissa olosuhteissa.

Lisäksi on hyvä huomata, että teknologian ikä ja kypsyys ovat kaksi eri asiaa: Tietty teknologia on saattanut olla olemassa jo pitkän aikaa, mutta jos sitä ei ole jatkuvasti kehitetty, ei teknologian kypsyys ole välttämättä olennaisesti parantunut alkuvaiheen jälkeen.


## Loppusanat

Kun uusi idea syntyy, alkaa pitkä kehityspolku, jossa idean ominaisuuksia jalostetaan ja kehitettävän tuotteen virheitä ja puutteita poistetaan.

Teknologian kypsyysaste ei kuvaa teknologian soveltuvuutta johonkin tiettyyn kohteeseen tai sen laadukkuutta suhteessa muihin kilpaileviin teknologioihin. Jos vertailtavana on kuitenkin kaksi tai useampaa teknologia, jotka kaikki täyttävät samat tekniset vähimmäisvaatimukset, on korkeimman teknologisen kehitysasteen vaihtoehdolla puolellaan laajimmat kokemukset kyseisen tuotteen käytöstä lopullisen käyttötarkoituksen mukaisissa tilanteissa.

Uusia tuotteita ja järjestelmiä kehitettäessä ja otettaessa käyttöön on hyvä tiedostaa, että kehitystyöhön sisältyy aina useita vaiheita, joista kussakin todennäköisesti paljastuu uutta tietoa teknologian toiminnasta ja toimivuudesta. Laadukkaasti tehdyssä työssä pystytään olemaan avoimia teknologian kehitysvaiheesta ja siirtymään seuraaviin vaiheisiin vasta aiempien kehitysaskeleiden jälkeen. Teknologian kehittämiseen liittyvien resurssien määrästä toki riippuu, että kuinka isoilla panostuksilla kukin vaihe tulee toteutetuksi.

Kypsyysasteen luokituksen arviointiperusteita rakentamista ja rakennusfysiikkaa varten kannattaisi kehittää eteenpäin, koska sen avulla saataisiin aikaisempaa tarkemmin keskusteltua eri teknologioiden kehitystilanteesta ja niihin liittyvistä riskeistä. Riskien esille tuominen ja yksilöinti taas auttaa niiden hallinnassa, mikä edelleen tarkoittaisi läpinäkyvämpää päätöksentekoa ja parempaa laatua suhteessa tavoitteisiin.

[Takaisin etusivulle](https://www.kapillaari.fi)
