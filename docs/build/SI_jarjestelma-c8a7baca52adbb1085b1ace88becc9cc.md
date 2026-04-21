
# SI-järjestelmän uusi määritelmä

_Julkaistu alunperin 2020-10-05. Päivitetty uudet SI-järjestelmän määrittävät vakiot taulukkomuotoon 2023-12-26._

[Takaisin etusivulle](https://www.kapillaari.fi/)


## Johdanto

Mittaustekniikassa suure on: ”Ilmiön, kappaleen tai aineen ominaisuus, jonka suuruus voidaan ilmaista lukuarvona ja referenssinä” ([MIKES julkaisu J4/2011](https://cris.vtt.fi/en/publications/laadukkaan-mittaamisen-perusteet)). Suureita ovat esimerkiksi pituus, aika ja kiihtyvyys. Suureen suuruus (eli suureen arvo) annetaan suureeseen liittyvän mittayksikön ja siihen liittyvän lukuarvon tulona ([SI-opas 2019](https://sfs.fi/palvelut/oppimateriaalit-ja-oppilaitosyhteistyo/lataa-si-opas/), s. 7), eli mittayksikön monikertana:

$$
suureen arvo = lukuarvo \cdot yksikko
$$


Suureiden suuruuden ilmaisemiseksi tarvittavia mittayksiköitä on eri suureille olemassa useita erilaisia. Esimerkiksi pituutta voidaan mitata [Ångströmeina](https://en.wikipedia.org/wiki/Angstrom), jalkoina, metreinä, syleinä, maileina, peninkulmina ja valovuosina. [Aikaa](https://en.wikipedia.org/wiki/Unit_of_time) taas voidaan mitata esimerkiksi Planckin aikoina (aika, joka valolta kuluu yhden Planckin etäisyyden taittamiseen), jiffeinä (aika, joka valolta kuluu tyhjiössä yhden fermin taittamiseen), sekunteina, tunteina ja vuosisatoina. Tiesitkö muuten, että [markka](https://fi.wikipedia.org/wiki/Vanhat_suomalaiset_mittayksik%C3%B6t) on vanha painomitta? Myös ulkomailta löytyy monenlaisia [vanhentuneita mittayksiköitä](https://en.wikipedia.org/wiki/List_of_obsolete_units_of_measurement).

Aloituskappaleen esimerkkisuureista pituus ja aika ovat perussuureita, kun taas kiihtyvyys on johdannaissuure. Näiden ero on, että perussuureita ei voi ilmaista muiden suureiden avulla, kun taas johdannaissuureet määritellään perussureiden avulla. Yksiköiden osalta perussuureiden yksiköt (eli perusyksiköt) eivät sisällä muiden suureiden yksiköitä, kun taas johdannaissuureiden yksiköt kootaan perussuureiden yksiköistä.

Edellä olevasta huomataan, että erilaisia suureita ja erityisesti niiden yksiköitä on melkoisen suuri määrä, mikä lisää eri mittayksiköihin liittyvien sekaannusten riskiä ja järjestelmän ylläpitämiseen tarvittavan työn määrää. Miten tätä kaikkea tulisi hallita?


## SI-järjestelmän aikaisempi rakenne

Mittasuureista ja niiden yksiköistä voidaan koota järjestelmiä, joissa kaikista tarjolla olevista suureista valitaan tietty alijoukko ja näille kiinnitetään sopivat perusyksiköt. Moderneista mittajärjestelmistä tunnetuin on SI-järjestelmä, eli kansainvälinen yksikköjärjestelmä (Le Système International d’Unités, The International System of Units). Maailman metrologian päivään 20.5.2019 asti SI-järjestelmä määriteltiin seuraavien seitsemän perussuureen sekä niiden perusyksiköiden avulla.



```{list-table} SI-järjestelmän perussuureet ja perusyksiköt ([BIPM 2019 SI Brochure, 9th ed, s. 130](https://www.bipm.org/en/publications/si-brochure/)).
:header-rows: 2
:name: suureetJaYksikot

* - Perussuure
  - holder
  - Perusyksikkö
  - holde
* - Nimi
  - Tunnus
  - Nimi
  - Tunnus
* - aika
  - _t_
  - sekunti
  - s
* - pituus
  - _l, x, r, etc._
  - metri
  - m
* - massa
  - _m_
  - kilogramma
  - kg
* - sähkövirta
  - _I, i_
  - ampeeri
  - A
* - termodynaaminen lämpötila
  - _T_
  - kelvin
  - K
* - ainemäärä
  - _n_
  - mooli
  - mol
* - valovoima
  - _Iv_
  - kandela
  - cd

```


Kullekin seitsemälle perussuureelle on määritelty suureen nimi, suureen tunnus, perusyksikön nimi ja perusyksikön tunnus, jotka ovat SI-järjestelmää käytettäessä ensisijaisia tapoja eri suureiden kuvaamiseen. SI-järjestelmässä on käytössä myös suureiden kerrannaisetuliitteitä välillä 10\-24...1024 , kuten nano, mikro, milli, sentti, kilo ja mega. Lisäksi joukko johdannaisyksiköitä on saanut oman nimensä, kuten pascal (\[Pa\] = kg/(ms2), joule (\[J\] = kgm<sup>2</sup>/s<sup>2</sup>) ja watti (\[W\] = kgm<sup>2</sup>/s<sup>3</sup>).

Perusyksiköiden määritelmät ovat muuttuneet useaan kertaan aikojen saatossa mittaustarkkuuden ja toistettavuuden parantamiseksi. Joskus vanhat, käytöstä poistuneet perusyksiköiden määritelmät voivat kuitenkin havainnollistaa kyseisten yksiköiden taustoja tehokkaasti. Käydään tässä yhteydessä läpi yhdet vanhat SI-järjestelmän perusyksiköiden määritelmät sekä muutama SI-järjestelmää edeltävä määritelmä. Yksiköiden vanhoja määritelmiä on kuvattu esimerkiksi [SI-järjestelmää esittelevässä julkaisussa](https://www.bipm.org/en/publications/si-brochure/) ja [tällä Wikipedia-sivustolla](https://en.wikipedia.org/wiki/International_System_of_Units#History_2). Listan ensimmäisellä tasolla en nykyistä edeltävä SI-järjestelmän mukainen yksikön määritelmä ja kakkostasolla yksi tai useampi sitä vanhempi määritelmä.

*   sekunti: 9 192 631 770 kappaletta cesium 133 -atomin perustilan ylihienorakennesiirtymän jaksonaikoja
    *   1/31 556 925,9747 osa vuoden 1900 trooppisesta vuodesta (vuoden pituus 365,2422 vrk)
    *   1 / (24 \* 60 \* 60) osa keskimääräisestä aurinkovuorokaudesta (mean solar day).
    *   Todellisen aurinkovuorokauden (apparent solar day) kesto on se, jonka jälkeen aurinko paistaa uudelleen kohtisuorasti tietylle pituuspiirille. Maan ja Auringon välisen liikkeen muutoksista johtuen tämä vaihtelee hieman vuoden aikana, joten sekunnin vanhassa määritelmässä on käytetty vuoden keskimääräistä arvoa.
*   metri: valon kulkema matka tyhjiössä 1/299 792 458 sekunnin aikana
    *   metrin prototyypin pituus
    *   1/10 000 000 osa etäisyydestä päiväntasaajalta pohjoisnavalle Pariisin kautta kulkevaa pituuspiiriä pitkin.
    *   Jos Maa oletetaan ympyräksi, jonka säde on 6500 km, niin tällöin ”metriksi” saadaan: (1/10 000 000) \* (2 \* 3,14 \* 6 500 000 m / 4) = 1,0205 m. Huom. Tässä metri on määritelty metrin avulla, mutta ei takerruta siihen.
*   kilogramma: kilogramman prototyypin massa
    *   Yhden kilogramman massa on myös lähellä sulavan jään lämpötilassa olevan vesilitran massaa. Yksi litra on kuutiometrin tuhannesosa.
*   ampeeri: sähkövirta, joka aiheuttaa kahden pitkän yhdensuuntaisen johtimen välille tietynsuuruisen voiman
    *   Vanhempi määritelmä perustui hopean siirtymiseen hopeanitraattiliuksessa, kun liuoksessa olevan anodin ja katodin välillä oli tietynsuuruinen sähkövirta.
*   kelvin: lämpötila-asteen suuruus on 1/273,16 osa veden kolmoispisteen lämpötilasta
    *   Suora viiva saadaan piirrettyä kahden pisteen avulla, jolloin kelvin asteikon ovat määrittäneet absoluuttinen nollapiste (0 K) ja veden kolmoispiste.
    *   Celsius-asteikossa 0 °C on veden jäätymispiste ja 100 °C veden kiehumispiste. Asettamalla veden kolmoispisteen kelvin-lämpötilan sopivasti (kuten nyt on tehty), saadaan celsius- ja kelvin-asteikkoilla esitetyt lämpötilaerot yhtä suuriksi.
*   mooli: ainemäärä kuvattuna aineen perusosasten (elementary entities) lukumäärällä. Yhdessä moolissa ainetta on yhtä monta perusosasta, kuin 12 grammassa hiili-12 -isotooppia on atomeita.
    *   Ainemäärään liittyvät perusosaset tulee nimetä erikseen ja ne voivat olla atomeita, molekyylejä, ioneita, elektroneja tai muita partikkeleita tai partikkeleiden ryhmiä.
*   kandela: taajuudella 540 · 10<sup>12</sup> Hz monokromaattista säteilyä tiettyyn suuntaan lähettävän säteilylähteen valovoima (eli valon intensiteetti tai valon kirkkaus), kun kyseisen säteilylähteen säteilyintensiteetti tähän samaan suuntaan on 1/683 W/sr
    *   Vanhan määritelmän mukaan kandela vastaa osapuilleen yhden tavallisen kynttilänvalon valovoimaa.
    *   Valaisinten yhteydessä myös valon jakautumisella eri suuntiin on merkitystä ja ”sr” tarkoittaa steradiaania, eli avaruuskulmaa. Jos valaisimesta lähtevän valon määrä (=valovirta, lm) lumeneina pidetään vakiona, mutta valo kohdistetaan pienempään ja pienempään avaruuskulmaan (sr), niin tällöin valaisimen valovoima eli valon intensiteetti kandeloina kasvaa ([motiva.fi](https://www.motiva.fi/koti_ja_asuminen/hyva_arki_kotona/lamput_ja_valaistus)).

Suureiden määritteleminen prototyyppien (esimerkkikappaleiden) avulla on ollut käytännöllistä ja soveltunut sen aikaiseen tieteen tasoon. Menetelmien kehittyessä ja tarkkuusvaatimusten kasvaessa näiden käytöstä on kuitenkin muodostanut myös hankaluuksia, koska vanha määritelmä on voinut olla sidottu epätarkempaan menetelmään uusiin menetelmiin verrattuna. Tällöin vanhoja määritelmiä on hiljalleen korvattu uudemmilla atomien ominaisuuksia ja sähkömagnetiikkaa hyödyntävillä määritelmillä, jotka mahdollistavat tarkemmat tulokset, mutta ovat samalla monimutkaisempia ja hankalammin ymmärrettäviä.

SI-järjestelmän kehittyessä on ollut käynnissä tilanne, jossa massan yksikkö viimeisenä suureena on määritelty kilogramman prototyypin avulla, kun taas vaikkapa sekunti ja metri on määritelty jo pitkään luonnosta löytyvien, niin kutsuttujen määrittävien vakioiden avulla.


## SI-järjestelmän uusi rakenne

SI-järjestelmän määritelmä muuttui maailman metrologian päivänä 20. toukokuuta 2019 alkaen ([FINAS](https://www.finas.fi/ajankohtaista/artikkelit/Sivut/SI-j%C3%A4rjestelm%C3%A4-uudistuu-%E2%80%93-mittaustarkkuus-paranee.aspx), [VTT](https://www.vttresearch.com/fi/uutiset-ja-tarinat/si-mittayksikot-suomessa), [BIPM](https://www.bipm.org/en/measurement-units/)). Kyseisestä päivämäärästä eteenpäin SI-järjestelmä määritellään seitsemän määrittävän vakion avulla, jotka ovat:


```{list-table} SI-järjestelmän määrittävät vakiot.
:header-rows: 1
:name: uusi_jarjestelma

* - Nimi
  - Tunnus
  - Lukuarvo
  - Yksikkö
* - 133-cesiumatomin häiriintymättömän perustilan ylihienorakennesiirtymän taajuus
  - _f<sub>Cs</sub>_
  - 9 192 631 770
  - Hz
* - Valonnopeus tyhjiössä
  - _c_
  - 299 792 458
  - m/s
* - Planckin vakio
  - _h_
  - 6,626 070 15 × 10<sup>-34</sup>
  - Js
* - Alkeisvaraus
  - _e_
  - 1,602 176 634 × 10<sup>-19</sup>
  - C
* - Boltzmannin vakio
  - _k_
  - 1,380 649 × 10<sup>-23</sup>
  - J/K
* - Avogadron vakio
  - _N<sub>A</sub>_
  - 6,022 140 76 × 10<sup>23</sup>
  - 1/mol
* - Taajuudella 540 × 10<sup>12</sup> Hz säteilevän yksivärisen valon valotehokkuus
  - _Kcd_
  - 683
  - lm/W

```


Osa SI-järjestelmän perustana olevista määrittävistä vakioista on luonnovakioita, kuten valonnopeus tyhjiössä ja alkeisvaraus. Osa vakioista on sen sijaan sopimuksenvaraisempia suureita, kuten moolin määritelmän taustalla oleva Avogadron vakio. Vakioitujen suureiden kokoelma ei ole ainut mahdollinen, vaan sen muodostamisessa on otettu huomioon tällä hetkellä käytettävissä olevat ja riittävän luotettaviksi arvioidut mittausmenetelmät sekä aikaisemmin käytössä olleet suureet. Vakioksi kiinnitetyistä suureista esimerkiksi cesium-atomin siirtymätaajuus on ollut sekunnin perusteena jo 1960-luvulta lähtien.

SI-järjestelmän perussuureet ja perusyksiköt ovat edelleen samat kuin aikaisemminkin. Toisin sanoen esimerkiksi pituuden perusyksikkö on edelleen metri ja ajan perusyksikkö sekunti. Uuden SI-järjestemän määritelmä koostuu nyt kuitenkin ensimmäistä kertaa kokonaisuudessaan vakioiduista suureista, mikä mahdollistaa jatkuvan uusien menetelmien käyttöön ottamisen ja yksiköiden mittausepävarmuuden jatkuvan pienentämisen nykyisen järjestelmän puitteissa.

Esimerkiksi aikaisemmin kilogramman prototyypin massa katsottiin tarkaksi arvoksi, kun taas Planckin vakio sisälsi tietyn määrän mittausepävarmuutta. Nyt tilanne on toisin päin, eli yllä listattu Planckin vakio katsotaan tarkaksi arvoksi ja kilogramman prototyypin massan mittaustulos sisältää tietyn määrän mittausepävarmuutta. Massan määrittämisen mittausepävarmuutta voidaan kuitenkin pyrkiä nyt pienentämään mitä tahansa soveltuvaa menetelmää hyväksi käyttäen, eikä menetelmän valintaa tarvitse rajoittaa prototyypin asettamien ehtojen mukaan.

Mielenkiintoinen yksityiskohta on, että uudessa järjestelmässä ei ole enää teknistä tarvetta säilyttää jakoa perus- ja johdannaissuureisiin, koska kaikki yksiköt voidaan nyt johtaa suoraan järjestelmän määrittelevistä vakioista. Tämä jaottelu on kuitenkin säilytetty sen käytännön hyödyllisyyden ja laajan tunnuttuvuuden vuoksi. ([SI Brochure, s. 129](https://www.bipm.org/en/measurement-units/)).

Käydään seuraavassa vielä hieman tarkemmin läpi yksiköiden määrittäminen luonnonvakioista liikkeelle lähdettäessä.


## Esimerkkejä perusyksiköiden määrittämisestä

Taajuuden yksikkö hertsi (Hz) kertoo, kuinka monta kertaa tietty tapahtuma toistuu sekunnissa. Tätä on käytetty sekunnin määrittelemiseen asettamalla sekunti siksi ajaksi, joka kuluu 9 192 631 770 toistolle cesiumatomin perustilan ylihienorakennesiirtymän jaksonaikoja.

Sekunnin määrittämisen jälkeen metri saadaan sinä etäisyytenä, jonka valo ehtii kulkemaan 1/299 792 458 sekunnin aikana ($v = s/t$). Toisaalta uusi määritelmä mahdollistaa metrin määrittelemisen myös sähkömagneettisen säteilyn peruslausekkeiden avulla, jossa sähkömagneettisen säteilyn etenemisnopeus tyhjiössä on säteilyn taajuus kerrottuna säteilyn aallonpituudella ($v = \lambda \cdot f$).

Uudessä SI-järjestelmän määrittelytavassa myös kilogramma voidaan nyt määrittää useilla eri tavoilla. Eri menetelmiä ovat ainakin mittaukset Kibblen vaa’an (wattivaa’an) avulla, muodostamalla yhteys silikonipallon massan ja sen atomien lukumäärän välille sekä mittaukset atomien törmäyksistä (atomic recoil).

Sähkövarauksen yksikkö voidaan kirjoittaa sähkövirran yksikön ja ajan yksikön avulla seuraavasti: 1 C = 1 A · 1 s. Käyttämällä alkeisvarausta ja sekuntia saadaan, että ampeerin suuruisessa sähkövirrassa siirtyy 1/1,602 176 634 × 10\-19 alkeisvarausta sekunnissa.

Boltzmannin vakio ja lämpötila esiintyvät ainakin mustan kappaleen säteilyominaisuuksien lausekkeissa, joten näitä on mahdollista käyttää myös kappaleen lämpötilan määrittämiseen.

Eri yksiköiden määrittämiseen liittyviä menetelmävaihtoehtoja on kuvattu tarkemmin muun muassa virallisen SI-esitteen [liitteessä 2](https://www.bipm.org/en/publications/mises-en-pratique/) (_mises en pratique_).


## Yhteenveto

Kansainvälisesti käytetyin ja myös Suomessa käytössä oleva SI-järjestelmä muodostaa laajan, mutta samalla johdonmukaisen kokonaisuuden suureita ja niiden yksiköitä, mikä helpottaa tiedon välittämistä ihmisten ja tietojärjestelmien kesken ja pienentää virheiden todennäköisyyttä terveydelle ja turvallisuudelle kriittisissä tehtävissä. SI-järjestelmä ei kuitenkaan ole muuttumaton järjestelmä, vaan se on kokenut useita erilaisia muutoksia yli satavuotisen olemassaolonsa aikana. Siirtymä uuteen SI-järjestelmän määrittelytapaan on jännittävä ja mielenkiintoinen asia, ja se mahdollistaa omalta osaltaan uusia tulevaisuuden kehityskulkuja tieteen ja tekniikan kehittämiseen.


## Lähteet

1.  [MIKES julkaisu J4/2011](https://cris.vtt.fi/en/publications/laadukkaan-mittaamisen-perusteet)
2.  Suomen standardisoimisliitto SFS. SI-opas 2019. Kansainvälinen suure- ja mittayksikköjärjestelmä. [Linkki 1](https://sfs.fi/palvelut/oppimateriaalit-ja-oppilaitosyhteistyo/lataa-si-opas/), [linkki 2](https://sfs.fi/wp-content/uploads/2020/10/SI-opas.pdf).
3.  [Wikipedia, Ångström](https://en.wikipedia.org/wiki/Angstrom)
4.  [Wikipedia, Unit of time](https://en.wikipedia.org/wiki/Unit_of_time)
5.  [Wikipedia, Vanhat suomalaiset mittayksiköt](https://fi.wikipedia.org/wiki/Vanhat_suomalaiset_mittayksik%C3%B6t)
6.  [Wikipedia, List of obsolete units of measurement](https://en.wikipedia.org/wiki/List_of_obsolete_units_of_measurement)
7.  [BIPM 2019, SI Brochure, 9th ed](https://www.bipm.org/en/publications/si-brochure/) (tämä on keskeinen lähde SI-järjestelmään)
8.  [Wikipedia, International System of Units](https://en.wikipedia.org/wiki/International_System_of_Units#History_2)
9.  [Motiva.fi, Lamput ja valaistus, vierailtu 26.12.2023](https://www.motiva.fi/koti_ja_asuminen/hyva_arki_kotona/lamput_ja_valaistus)
10.  [FINAS, SI-järjestelmä uudistuu – mittaustarkkuus paranee](https://www.finas.fi/ajankohtaista/artikkelit/Sivut/SI-j%C3%A4rjestelm%C3%A4-uudistuu-%E2%80%93-mittaustarkkuus-paranee.aspx)
11.  [VTT, SI-mittayksiköt Suomessa](https://www.vttresearch.com/fi/uutiset-ja-tarinat/si-mittayksikot-suomessa)
12.  [BIPM, The International System of Units](https://www.bipm.org/en/measurement-units/)
13.  [SI, Brochure, 9th ed, App. 2](https://www.bipm.org/en/publications/mises-en-pratique/)

[Takaisin etusivulle](https://www.kapillaari.fi/)
