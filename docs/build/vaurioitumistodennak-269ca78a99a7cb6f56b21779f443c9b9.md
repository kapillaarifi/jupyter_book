# Vaurioitumistodennäköisyyden arviointi Monte Carlo -menetelmän avulla

_Tämä kirjoitus julkaistiin alun perin vuonna 2023, mutta nettisivujen poistumisen myötä itse teksti katosi internetin syövereihin. Kirjoitus on nyt laadittu uusiksi tuolta ajalta säilyneiden kooditiedostojen ja kuvaajien avulla._

[Takaisin etusivulle](https://www.kapillaari.fi)

Rakennusten suunnittelussa yleinen lähestysmistapa on, että rakenteilla ja rakennusmateriaaleilla ajatellaan olevan jokin kestävyys tai sietokyky, kun taas ympäristöstä rakenteisiin aiheutuu erilaisia rasituksia. Jos rasitukset jäävät kestävyyttä pienemmiksi, arvioidaan rakenne toimivaksi. Jos taas rasitukset ylittävät kestävyyden, rakenne vaurioituu. Rasitukset ja kestävyys eivät kuitenkaan ole yksittäisiä lukuarvoja, vaan ilmiöissä on aina hajontaa ja epävarmuutta. Yksi tapa tutkia rakenteen kykyä kestää vaurioitumatta on käyttää niin kutsuttua Monte Carlo -menetelmää.

## Peruskäsitteiden määrittely

### Käsitteitä

Eurokoodit ovat kokoelma eurooppalaisia standardeja, jotka muodostavat kantavien rakenteiden suunnittelun järjestelmän. Eurokoodien ensimmäinen sukupolvi julkaistiin vuosina 2002-2007 ja toinen sukupolvi tulee vahvistaa käytettäväksi myös Suomessa syyskuun 2027 loppuun mennessä. Eurokoodien osa SFS-EN 1990:2023 käsittelee rakenteiden ja geoteknisen suunnittelun perusteita ja on mielenkiintoinen dokumentti myös rakennusfysiikan kannalta. Dokumentti esimerkiksi sisältää valmista sanastoa ja menettelytapojen kuvauksia rakenneratkaisujen hyväksyttävyyden arvioimiseen suunnitteluvaiheessa. Vaikka menetelmien siirtymää kantavien rakenteiden mitoituksesta rakennusfysikaaliseen mitoitukseen ei voikaan suoraan tehdä, saattaisi sanastojen ja käytänteiden yhtenäistäminen selkiyttää myös rakennusfysikaalisen suunnittelun käytänteitä.

Pyritään ensin määrittelemään muutamia käsitteitä. Määritelmissä on hyödynnetty [sanastot.suomi.fi](https://sanastot.suomi.fi/) -palvelua ja standardia SFS-EN 1990:2023.

* *rakennus*
	- paikallaan pysyväksi tarkoitettu, omalla sisäänkäynnillä varustettu, katettu ja ulkoseinien rajaama rakennuskohde
* *rakennusosa*
	- rakennusosia ovat yläpohja, välipohja, alapohja, ulkoseinä, väliseinä, ikkunat ja ovet. Rakennusosa koostuu yhdestä tai useammasta rakenneosasta.
* *rakenneosa*
	- fyysisesti erottuva rakenteen osa, esim. pilari, palkki, laatta tai perustus
	- tietty rakenneratkaisu kokonaisuudessaan rakennuksessa. Esimerkiksi jos rakennuksessa on käytetty kahta erilaista ulkoseinää, muodostavat kaikki ulkoseinät yhdessä "ulkoseinät"-rakennusosan, mutta joka samalla muodostuu "ulkoseinä A" ja "ulkoseinä B" -rakenneosista. Rakenneosat liittyvät toisiinsa rakenneosien liitoksissa.
* *rakennetyyppi*
	- samanlaisena läpi rakenneosan toistuva rakenneratkaisu. Rakennetyyppi voidaan yksilöidä rakennetyypin piirustuksen avulla, jossa on näytetty rakennetyypin muodostavat rakennusmateriaalit ja niiden geometriset mitat.
* *rakennusmateriaali*
	- käsitteen ajatellaan sisältävän tässä laajasti erilaiset rakennusaineet ja -tuotteet, joita voi ostaa rautakaupasta ja joilla usein on CE-merkintä.
* *rakenne*
	- rakenneosa tai rakenneosien liitos
* *suunniteltu käyttöikä*
	- oletettu ajanjakso, jolloin rakennetta tai sen osaa on määrä käyttää aiottuun tarkoitukseensa ennakoiduin kunnossapitotoimenpitein, mutta niin, että olennaiset korjaukset eivät ole välttämättömiä
	- "Tekninen"-sanan mukaan ottamisella (suunniteltu tekninen käyttöikä) halutaan painottaa arvioinnin riippumattomuutta esteettisistä, taloudellisista tai käyttömääriin liittyvistä tekijöistä.
* *kestävyys* $ R $
	- rakenteen tai sen jonkin osan kyky kestää kuormia vaurioitumatta
* *kuorma*
	- ympäristöstä suoraan tai välillisesti kohdistuva mekaaninen vaikutus rakenteeseen tai rakenneosaan (SFS-EN 1990:2023)
	- rakennusfysiikassa kuormia voi nähdä olevan esimerkiksi rakenteisiin kohdistuvat lämpötilamuutokset, ilmavirtaukset ja kosteuden siirtyminen rakenteeseen.
* *kuorman ominaisarvo*
	- kuorman arvo, joka on mahdollisimman pitkälle tilastollisin perustein valittu vastaamaan määrättyä todennäköisyyttä, että se ei ylity epäedullisesti määritellyn vertailujakson aikana
* *kuorman vaikutus* $ E $
	- kuormien kohdistumisesta syntyvä vaikutus rakenneosaan tai koko rakenteeseen
	- rakennusfysiikassa voidaan ajatella ulko- ja sisäolosuhteiden sekä ilma- ja sadevuotojen olevan kuormia, joiden vaikutus rakenteeseen ovat tietyt lämpötila- ja kosteusolosuhteet rakenteessa
* *materiaalin tai rakennustuotteen ominaisuuksien ominaisarvo*
	- materiaalin tai rakennustuotteen ominaisuuden arvo, jota ei annetulla todennäköisyydellä saavuteta oletetuissa äärettömän laajoissa testisarjoissa
* *mitoitusarvo*
	- laskettu ominaisarvosta kasvattamalla kuormaa tai pienentämällä kestävyyttä
* *toistumisjakso*
	- keskimääräinen määrä vuosia, joiden aikana kyseinen kuorma tilastollisesti ylittyy kerran
* *vertailujakso*
	- ajanjakso, jota käytetään arvioitaessa tilastollisesti muuttuvien kuormien ääriarvojen toteutumista ja mahdollisesti onnettomuuskuormien yhteydessä
	- meteorologiassa ilmastolliset vertailusuureet määritetään 30 vuoden pituisesta säädata-aineistosta


Eurokoodissa ominaisarvot voivat olla keskiarvoa kuvaavia nimellisarvoja, jos poikkeamat ja niiden vaikutukset tästä ovat pieniä. Jos poikkeamien vaikutukset tulee ottaa huomioon, on Eurokoodin perusarvot tällöin 5 % ja 95 % fraktiilit sen mukaan, että suureen jakaumalta valitaan varmalla puolella oleva arvo. Rakenteiden lämpö- ja kosteusteknisessä käyttäytymisessä on kuitenkin paljon tilanteita, joissa jakauman hännistä tehtävien ominaisarvojen valinnalle ei ole käytettävissä riittävästä tilastollista dataa tai tietoa lähtötietojen hajonnan vaikutuksista tuloksiin. Näitä tilanteita varten yksi vaihtoehto olisi tarkastaa tilanteet sekä matalalla että korkealla arvolla, mikä voi yksinkertaisissa tilanteissa tuottaa riittävästi informaatiota rakenteen käyttäytymisestä. Monimutkaisessa tilanteessa tarkastelutapausten määrä alkaa kuitenkin kasvaa voimakkaasti ja tulosten tulkinta vaikeutuu, jolloin myös muut menetelmät tulevat myös mahdollisiksi.


### Kestävyysfunktio

Yleisesti ottaen vaatimus on, että kuormien vaikutus rakenteeseen tulee olla sen kestävyyttä pienempi:

$$ E \leq R $$

Määrittämällä teoreettinen kestävyysfunktio $ g $ voidaan kirjoittaa:

$$ g = R - E $$

Jos $g$ on positiivinen, on kestävyys suurempi kuin kuormien vaikutus ja rakenne kestää kyseisen tilanteen vaurioitumatta. Jos $g$ on negatiivinen, kuormien vaikutus on kestävyyttä suurempi ja rakenteeseen muodostuu vaurio. Vauriolla tarkoitetaan tässä tilannetta, jossa mikä tahansa vaurioitumista kuvaava matemaattinen suure ylittää sille asetetun raja-arvon. Se, että rakenne kestää siihen kohdistuvat rasitukset vaurioitumatta tarkoittaa siis tilannetta:

$$ g > 0 $$

Mitoitusehdon määrittelyä ja käsittelyä kosteusriskitarkasteluissa on käsitelty esimerksi julkaisussa [Nevander & Elmarsson (1991)](https://portal.research.lu.se/en/publications/fuktdimensionering-av-tr%C3%A4konstruktioner-riskanalys/).


### Monte Carlo -menetelmä

Monte Carlo -menetelmillä tarkoitetaan tietokoneella tehtävän satunnaisotannan käyttöä jonkin numeerisen ongelman ratkaisemiseen. Numeerisia ongelmia ovat esimerkiksi optimointi, integrointi ja arvojen generointi todennäköisyystiheysfunktiosta erilaisia mallinnustarkasteluja varten. Kaikista näistä ryhmistä löytyy useita erilaisia Monte Carlo -menetelmän sovellutuksia. Keskeinen idea kuitenkin on valita laskentatapauksia satunnaisesti ennalta määrätyistä lähtötietojakaumista ja ajaa laskentaa läpi niin monta kertaa, että tulokset kuvaavat koko tarkasteltavan tilanteen.

Monte Carlo -menetelmän käyttöä rakennusfysiikassa on tutkittu laajemmin esimerkiksi IEA Annex 55 -hankkeessa [linkki](https://www.iea-ebc.org/projects/project?AnnexID=55), jossa kehitettiin menetelmiä, data-aineistoja ja työkaluja rakenteiden lämpö- ja kosteusteknisen toiminnan arvioimiseen. Keskeinen lähestysmistapa on määrittää rakenteen lämpö- ja kosteusteknistä toimintaa kuvaava malli, kaikkien lähtötietoparametrien todennäköisyystiheysfunktiot, ja tämän jälkeen ajaa mallia läpi todennäköisyystiheysfunktioista arvotuilla lähtötiedoilla, kunnes tulosarvojen jakauma on selvillä halutulla tarkkuudella.

Iso etu Monte Carlo -lähestymistavassa on se, että laskennassa käytettävä malli voi olla hyvin monimutkainen ja vaikeasti ennustettava. Analyyttisia ratkaisuja on olemassa vain hyvin rajattuihin tapauksiin ja kaikkien mahdollisten tapausten ristiintaulukointi aiheuttaa nopeasti kombinatorisen räjähdyksen, jolloin kaikkien tapausten läpikäynti ei ole mahdollista. Monte Carlo -lähestymistapa tarjoaa keinon saada tietoa tulosten käyttäytymisestä lähtötietojen muuttuessa satunnaisesti, ilman kaikkien tapausten läpikäyntiä.

Haasteita Monte Carlo -menetelmässä ovat laskentavaatimusten kasvu yhden tapauksen ajamiseen verrattuna ja epävarmuus lopullisen tulosjakauman löytämisestä. Jos aiemmin on laskettu yksi laskentatapaus arvatuilla lähtötidoilla, ja tämän jälkeen laskettaisiin vaikkapa tuhat tapausta arvatuilla lähtötiedoilla, niin tuhannesta tapauksesta saa huomattavasti enemmän tulosdataa, mutta myös laskentatyön määrä on isompi. Lisäksi tapausten kokonaismäärän valitseminen sisältää epävarmuutta, koska lähtötiedot valitaan satunnaisesti ja tarkasteltava tilanne voi olla epälineaarinen ja epäjatkuva. Yksi puhtaan Monte Carlon jatkokehitysmenetelmistä on Markovin ketjun Monte Carlo (Markov Chain Monte Carlo, MCMC), jolla vähennetään vähän uutta tietoa tuottavien laskentatapausten ajamista.


## Laskentaesimerkki

Asioiden havainnollistamiseksi tehdään yksinkertaistettu laskentaesimerkki.

Ajatellaan, että meillä on rakenne, jonka kestävyysfunktio on:

$$
R = \mathcal{N} ( \mu_R, \sigma_R^2 )
$$

Oletetaan, että $ \mu_R = 85$ ja $ \sigma_R = 5 $. Käsitellään lukuarvoja tässä yksiköttöminä, mutta tarvittaessa lukuarvojen voi ajatella kuvastavan rakenteen kestämää suhteellisen kosteuden tasoa.

Vastaavasti rasitustason osalta tehdään olettamus, että rakenteeseen kohdistuva rasitustaso vastaa normaalijakaumaa parametreilla $ \mu_E = 60 $ ja $ \sigma_E = 10 $. Lisäksi oletetaan, että on olemassa 5 % todennäköisyys kosteusvuodolle, joka nostaa suhteellisen kosteuden tasoa rakenteessa 50 %-yksiköllä, mutta kuitenkin niin, että rasitustaso voi olla enintään 100 %. Tällöin saadaan:

$$
\begin{align}
E =& \mathcal{N} ( \mu_E = 60, \sigma_E^2 = 10 ) \\
   &+ X \cdot 50
\end{align}
$$

Muuttuja $X$ in diskreetti satunnaismuuttuja, joka saa arvon $X$ = 1 (kosteusvuoto esiintyy) todennäköisyydellä 5 %, ja arvon $X$ = 0 (kosteusvuotoa ei esiinny) todennäköisyydellä 95 %. Muuttuja on siis Bernoulli-jakautunut. Jos kosteusvuoto esiintyy, sen oletetaan vaikuttavan rakenteeseen läpi teknisen käyttöikätavoitteen.

Seuraavassa kuvassa on esitetty rasitustason ja kestävyyden normaalijaumat, kun rakenteessa ei ole vuotoja.

:::{figure} \sites\vaurioitumistodennakoisyys_MonteCarlo\kapillaarifi_kaksi_normaalijakaumaa.png
:width: 80%
:name: kuva_kaksi_normaalijakaumaa

Rasitustason ja kestävyyden normaalijakaumat. Tarkkoja arvoja ei tunneta, mutta suureiden todennäköisyystiheysfunktiot oletetaan tunnetuiksi.
:::

Rasitustason ja kestävyyden lukuarvot on valittu niin, että jos jätetään vuototilanne pois, niin rasitustason 95 % fraktiiliksi tulee $ E_k $ = 76,4 ja kestävyyden 5 % fraktiiliksi $ R_k $ = 76,8. Eli rasitus on niukasti kestävyyttä pienempi ($ E_k < R_k $) ja tilanne täyttää mitoitusehdon jakaumien häntien mukaisia ominaisarvoja käytettäessä.

Vuodon esiintyminen olisi mahdollista ajatella puutteena rakenteessa itsessään, jolloin kyseessä olisi kestävyyden lasku ja tämä olisi vastaisi ajatusta kestokyvyn heikkenemisestä, jolloin sama ilmastollinen rasitus voi aiheuttaa suuremman seuraamuksen rakenteeseen. Vuodon käsittely on tässä laitettu kuormituksen kasvuksi, minkä voi ajatella edustavan poikkeuksellisten ilmastollisten rasitusten mukaista vuotta. Lisäksi vuodon käsittely rasitustason kasvuna vastaa edellä kuvattua tilannetta, että rakenne täyttää juuri mitoitusehdon vuodottomassa tilanteessa, kun taas vuodon esiintyminen aiheuttaa alkuperäisen mitoituskäytännön mukaisen lisäkuormituksen rakenteeseen.

Kestävyyden ja rasitustason funktiot on yksinkertaistamisen vuoksi määritetty suoraan, eikä niissä ole suurempia laskelmia taustalla. Mikään ei kuitenkaan estä sitä, etteikö $R$ ja $E$ -lukuarvojen taustalla voisi olla vaikka kuinka monimutkaisia laskelmia (rakennusfysiikkasimulointeja, tilastollisia tarkasteluja, virtauslaskentaa, materiaalimallinnusta, jne).

## Tuloksia

### Perustilanteet

Tarkastellaan tilannetta, jossa ajatellaan olevan yksi toteutettava rakenne ja sitä tarkastellaan yhden äärettömän pitkän ajanjakson tilanteessa. Rakenteen kestävyyden ja rasitustason tarkkoja lukuarvoja ei tunneta, mutta niiden jakaumat tunnetaan ja ne oletetaan vakioiksi. Pyritään ratkaisemaan rakenteen vaurioitumistodennäköisyys, eli sen tilanteen esiintymisen todennäköisyys, jossa $ g < 0 $.

Aloitetaan tarkastelemalla teoreettista kestävyysfunktiota $ g $ analyyttisesti, kun rakenteeseen ei kohdistu vuotoja. Kahden normaalijakautuneen satunnaismuuttujan erotuksen keskiarvo on keskiarvojen erotus, eli $ \mu_{diff} = \mu_R - \mu_E $. Kahden normaalijakautuneen ja toisistaan riippumattoman satunnaismuuttujan erotuksen keskihajonta taas on satunnaismuuttujien varianssien summan neliöjuuri, eli $ \sigma_{diff} = \sqrt{ \sigma_R^2 + \sigma_E^2 } $. Kestävyysfunktion kuvaaja on esitetty seuraavassa:

:::{figure} \sites\vaurioitumistodennakoisyys_MonteCarlo\kapillaarifi_erotuksen_normaalijakauma_analyyttisesti.png
:width: 80%
:name: kuva_erotuksen_normaalijakauma_analyyttisesti

Teoreettinen kestävyysfunktio analyyttisesti laskettuna, eli kahden normaalijakautuneen satunnaismuuttujan erotuksena.
:::

Erotuksen odotusarvo on 25 yksikköä, keskihajonta 11,2 yksikköä, nollan alitus tapahtuu 2,24 keskihajonnan päässä odotusarvosta ja vaurioitumistodennäköisyys ($ g < 0 $) on 1,27 %. Sama vaurioitumistodennäköisyys saadaan sekä kuvan mukaisesti normaalijakaumasta, että standardinormaalijakauman kertymäfunktiosta käyttämällä z-arvoa -2,24.

Arvioidaan kestävyysfunktiota $g$ seuraavaksi Monte Carlo -menetelmän avulla. Riittävän tarkkojen tulosten tuottamiseksi arvotaan miljoona kappaletta arvoja kestävyysfunktiosta ja rasitusfunktiosta kustakin erikseen. Tehdään yhtä monta vähennyslaskua, jossa vuorotellen kestävyysarvoista vähennetään rasitustaso. Seuraavassa kuvassa on histogrammi tuloksista.

:::{figure} \sites\vaurioitumistodennakoisyys_MonteCarlo\kapillaarifi_erotuksen_normaalijakauma_numeerisesti.png
:width: 80%
:name: kuva_erotuksen_normaalijakauma_numeerisesti

Teoreettinen kestävyysfunktio numeerisesti laskettuna, eli valitsemalla miljoona otosta sekä kestävyyden että rasitustason arvoja ja tämän jälkeen vähentämällä ne toisistaan.
:::

Negatiivisten lukujen osuus histogrammista laskettuna on 1,26 %, eli isolla otosmäärällä tuli lähes sama tulos, kuin analyyttisesta ratkaisusta. Tälle tapaukselle analyttisen ratkaisun käyttö olisi kuitenkin suositeltavampi, kun sellainen kerran on olemassa.



### Yksi tai useampi rakennus

Monimutkaistetaan seuraavaksi tilannetta. Miten vaurioitumisen esiintyminen käyttäytyy, jos tiettyä rakennetta esiintyisi lähekkäin 100 kpl ja tarkastellaan 50 vuoden ajanjaksoa? Ajatellaan, että kukin vuosi on toisistaan riippumaton ja vaurioituminen yhtenä vuonna rajautuu vain kyseiseen vuoteen. Nämä ovat ns. isoja olettamuksia, mutta käytetään niitä seuraavassa esimerkissä silti.

Arvotaan 100 kpl kestävyysarvoja (eli 100 rakennusta) ja 50 kpl rasitustason arvoja (eli 50 vuotta). Tämän jälkeen vuosi kerrallaan verrataan kutakin kestävyysarvoa kyseisen vuoden rasitustason arvoon ja lasketaan teoreettisen kestävyysfunktion arvo.


:::{figure} \sites\vaurioitumistodennakoisyys_MonteCarlo\kapillaarifi_n100_t50_s1_eiVuotoja.png
:width: 80%
:name: kuva_n100_t50_s1_eiVuotoja

Yksi mahdollinen toteuma tilanteesta, jossa 100 kpl samaa rakennetta altistuu 50 peräkkäiselle rasitustilanteelle. Kaikki tilanteet oletetaan toisistaan riippumattomiksi. Rakenteisiin ei kohdistu vuotoja, eli harvinaisia vikatilanteita ei esiinny.
:::

Rasitustasoon $E$ liittyvä keskihajonta oli suurempi, kuin kestävyyteen $R$. Tämä näkyy kuvaajassa niin, että yksittäisen rakenteen sisällä tulokset ovat enemmän nipussa, kuin peräkkäisten vuosien välillä. Tarkastelujaksolla esiintyy siis yksittäisiä vuosia, jolloin $E$ on saanut poikkeuksellisen ison tai pienen arvon ja nämä näkyvät kuvaajissa erityisen matalalla tai korkealla olevina ryhminä.

Yllä olevassa tilanteessa kestävyyden ylityksiä esiintyi 100 % * (54 kpl / 5000 kpl) = 1,08 %. Näistä suuri osa on kuvan perusteella keskittynyt kahteen rakenteeseen, joihin on osunut keskimääräistä heikompi kestävyys.

Kuvan mukainen tilanne on kuitenkin vain yksi mahdollinen monista, koska kullekin rakenteelle olisi voinut päätyä jokin muukin kestävyys, ja vastaavasti 50 vuoden jaksolla kunakin vuonna olisi voinut olla myös jokin muu rasitustaso. Näin ollen kattavamman kuvan saamiseksi sama 100 rakenteen ja 50 vuoden kokonaisuus tulee simuloida monta kertaa, jotta saadaan kattavampi kuva rakenteen käyttäytymisestä isommassa joukossa. 

Seuraavassa kuvassa on tulokset tarkastelusta, jossa edeltävän kuvan mukainen tilanne on ajettu läpi monta kertaa. Tuloksista on esitetty kunkin ajon mukainen osuus rasitustason ylityksistä.


:::{figure} \sites\vaurioitumistodennakoisyys_MonteCarlo\kapillaarifi_MC_scatterHistogram_eiVuotoja.png
:width: 80%
:name: kuva_MC_scatterHistogram_eiVuotoja

Monte Carlo -ajojen (n = 2000) tulokset kestävyystason ylittymisestä, kun kukin ajo koostuu 100 kpl rakenteita 50 vuoden jaksolla. Rakenteisiin ei kohdistu vuotoja.
:::

Kuvaajan perusteella keskimääräinen kestävyyden ylittymisosuus oli 1,3 %, mikä vastaa aiempaa analyyttisen ratkaisun tulosta. Tämän lisäksi kuva nostaa esille sen, että satunnaismuuttujien luonteesta johtuen tuloksissa esiintyy myös keskiarvoa korkeampia kestävyyden ylittymisprosentteja. Kaikista Monte Carlo -ajoista laskettaessa 95 % oli sellaisia, että kestävyys ylittyi enintään 3,3 %:ssa tilanteista.

Seuraavana ja viimeisenä kohtana katsotaan vielä tilannetta, jossa rakenteeseen saattoi kohdistua vuototilanne. Aiemmin kuvatun mukaisesti poikkeustilanteen aiheuttama lisäys rasitustasoon on siis asetettu sellaiseksi, että vikatilanteen tapahtuessa rakenteen kestävyys ylittyy hyvin todennäköisesti. 


:::{figure} \sites\vaurioitumistodennakoisyys_MonteCarlo\kapillaarifi_MC_scatterHistogram_vuodotMahdollisia.png
:width: 80%
:name: kuva_MC_scatterHistogram_vuodotMahdollisia

Monte Carlo -ajojen (n = 2000) tulokset kestävyystason ylittymisestä, kun kukin ajo koostuu 100 kpl rakenteita 50 vuoden jaksolla. Rakenteisiin kohdistuu vuotoja 5 % todennäköisyydellä.
:::

Kun rakenteisiin voi kohdistua vuototilanteita, kasvoi kestävyyden ylittymistapahtumien osuus selvästi. Ylittymisosuus vuotoja sisältävässä tilanteessa oli keskimäärin 6,2 %, joka on melko lailla 5 %-yksikköä, eli vuototilanteen todennäköisyyden verran suurempi, kuin kestävyyden ylittymisosuus vuotoja sisältämättömässä tilanteessa (1,3 %). Muilla lukuarvoilla ja tilanteilla ylittymisosuuden kasvu ei välttämättä vastaisi yhtä suoraan vuototapausten todennäköisyyttä.

Vuotoja sisältävissä tilanteissa on myös kuvan perusteella nähtävissä ylittymisosuuksien jakauman siirtyminen kohti suurempia arvoja. Sadan rakennuksen ja 50 peräkkäisen tarkastelujakson ryhmissä esiintyi vain pieni määrä tapauksia, joissa kestävyyden ylittymisosuus pysyi nollassa. Hieman alle kahden ja puolen prosentin kohdalla esiintyy kuvassa raja, mutta asiaa voisi selvittää pidemmälle, että onko kyse laskennan katkaisurajoista ($ E \leq 100 $ vai jostain muusta.

Vuotoja sisältävien tapausten kuvaajasta on mielenkiintoista nähdä myös jakauman yläreunan taso. Kun vuotoja ei esiintynyt, kestävyyden ylittymistilanteita esiintyi 95 %:ssa ajoista enintään 3,3 %:ssa tapauksista. Sen sijaan kun vuotoja esiintyi, vastaava osuus kasvoi 12,1 %:iin. Jos tavoitellaan tilannetta, että suurin osa rakenteista täyttää asetetut vaatimukset koko käyttöiän ajan, tämä olisi jo huomattava tavoitteesta jääminen. Lukuarvojen yksityiskohdat riippuvat siitä, miten tarkastelutapaukset on määritelty.


## Yhteenveto

Tässä kirjoituksessa käytiin läpi vaurioitumistodennäköisyyden laskentaa Monte Carlo -simulointien avulla. Arviointi tehtiin määrittämällä kestävyyden ja kuormitustason arvot suoraan normaalijakaumina ja vetämällä näistä jakaumista arvoja tuloskuvaajia varten.

Monte Carlo -laskelmien etuna on, että siinä voidaan tarvittaessa käyttää myös yksityiskohtaisia laskentamalleja ja tarkastella laajasti erilaisia tilanteita, ja samalla ottaa huomioon eri lähtötietojen todennäköisyydet. Tällöin saadaan näkyviin koko tulosarvojen jakauma, mikä on tärkeää eri tapahtumien todennäköisyyksien määrittämistä varten. Selkeänä heikkoutena Monte Carlo -menetelmissä on työkalujen ja käytänteiden tarve, joita ei välttämättä ole valmiina, sekä suuri laskentaresurssien tarpeen kasvu.



[Takaisin etusivulle](https://www.kapillaari.fi/)





## Lähteet

IEA EBC. Annex 55. Reliability of Energy Efficient Building Retrofitting - Probability Assessment of Performance & Cost (RAP-RETRO). https://www.iea-ebc.org/projects/project?AnnexID=55

Nevander, L. E. & Elmarsson, B. (1991) Fuktdimensionering av träkonstruktioner: riskanalys. (BFR Rapport; Vol 1991:R38). Byggförskningsrådet (BFR). http://www.byggnadsmaterial.lth.se/fileadmin/byggnadsmaterial/BFR-publ/BFR_1991-R38.pdf

SFS-EN 1990:2023 Eurokoodi. Rakenteiden suunnittelun ja geoteknisen suunnittelun perusteet. 

Wikipedia Combinatorial expolosion. https://en.wikipedia.org/wiki/Combinatorial_explosion

Wikipedia Monta Carlo method. https://en.wikipedia.org/wiki/Monte_Carlo_method

