# Rakennusmateriaalien hygroskooppisuus

_Julkaistu alunperin 2020-08-31_

[Takaisin etusivulle](https://www.kapillaari.fi/)


## Yleistä

Hygroskooppisuudella tarkoitetaan materiaalien kykyä sitoa kosteutta ympäröivästä ilmasta itseensä ja vapauttaa sitä myöhemmin sinne takaisin. Useimmat tavallisesti käytössä olevat rakennusmateriaalit ovat vähintään jossain määrin hygroskooppisia, eli ne sitovat ympäröivästä ilmasta kosteutta itseensä ja vapauttavat sitä sinne takaisin olosuhteiden mukaan. Hygroskooppisten materiaalien lisäksi on olemassa myös ei-hygroskooppisia materiaaleja, jotka eivät sido ympäröivästä ilmasta kosteutta tai jopa hylkivät sitä (hygrofobiset materiaalit).

Seuraavassa kosteusvirralla tarkoitetaan suuressa vesimolekyylijoukossa tapahtuvaa molekyylien nettomääräistä siirtymistä tiettyyn suuntaan.

Kosteuden hygroskooppisessa sitoutumisessa materiaalin huokosrakenteen ja huokosveden pinnat sitovat vesimolekyylejä huokosilmasta. Jotta kosteuden hygroskooppinen sitoutuminen voi jatkua, tulee huokosilmaan virrata ympäristöstä lisää vesihöyryä. Jos kosteutta ei tule ympäristöstä lisää, pienenee huokosilman vesihöyrypitoisuus jossain vaiheessa siinä määrin, että vesimolekyylien nettomääräinen sitoutuminen materiaaliin pysähtyy ja kosteusolosuhteet saavuttavat tasapainotilanteen.

Materiaalin kuivuessa hygroskooppisesti vesimolekyylejä siirtyy nettomääräisesti enemmän huokosten pinnoilta ja huokosvedestä huokosilmaan, kuin takaisin päin, jolloin huokosilman vesihöyrypitoisuus kasvaa. Jotta materiaalin kuivuminen voi jatkua, tulee kosteuden päästä virtaamaan huokosilmasta ympäristöön. Jos näin ei tapahdu ja vesihöyrypitoisuus huokosilmassa nousee riittävästi, hidastuu vesimolekyylien nettomääräinen siirtyminen huokosten pinnoilta ja huokosvedestä huokosilmaan, kuivuminen pysähtyy ja kosteusolosuhteet saavuttavat uuden tasapainotilanteen.

Edellä olevasta kuvauksesta huomataan, että hygroskooppisuuteen liittyy kaksi pääasiallista prosessia:

1.  Vesimolekyylien nettomääräinen liike huokosilman sekä huokosten pintojen ja huokosveden välillä
2.  Vesihöyryn siirtyminen huokosilman ja ympäristön välillä.

Kohtaan 2 liittyvät tavat vesihöyryn siirtymiselle huokosilman ja ympäristön välillä ovat diffuusio ja konvektio ja näitä käsitellään erikseen myöhemmissä kirjoituksissa. Huokosiin sitoutuneen veden kapillaarista siirtymistä materiaalin sisällä ei katsota tässä yhteydessä hygroskooppisuudeksi ja myös sitä käsitellään erikseen myöhemmin.

Seuraavassa käsitellään muutamia muita rakennusmateriaalien hygroskooppisuuteen liittyviä asioita.


## Sorptiokäyrät

Materiaalien sisältämän kosteuden määrä riippuu tyypillisesti epälineaarisesti ympäröivän ilman olosuhteista. Tällöin yksittäiset vakioarvot eivät anna tarkkaa kuvaa materiaalien kosteuspitoisuudesta, vaan tarvitaan erilaisia käyrästöjä, matemaattisia lausekkeita ja taulukoita kuvaamaan materiaalien kosteuspitoisuutta. Kaksi keskeistä tapaa epälineaarisen kosteuspitoisuuden kuvaamiseen ovat hygroskooppiset ja kapillaariset tasapainokosteuspitoisuuden kuvaajat. Seuraavassa on esitetty periaate-esimerkki hygroskooppisesta tasapainokosteuspitoisuuden käyrästä.

:::{figure} \sites\hygroskooppisuus\kapillaarifi_annex24concrete.png
:width: 80%
:name: kuva_annex24

Betonin hygroskooppiset tasapainokosteuspitoisuuden käyrät, eli niin kutsutut sorptiokäyrät. Lähde: [Annex 24, task 3 final report](https://www.iea-ebc.org/projects/project?AnnexID=24).
:::

Adsorptio tarkoittaa kosteuden sitoutumista materiaaliin ja desorptio kosteuden vapautumista. Adsorptio- ja desorptiokäyrät kuvaavat tilannetta, jossa materiaalin kosteusolosuhteet muuttuvat hyvin hitaasti ja tasaisesti yhteen suuntaan kerrallaan. Adsorptiolla tarkoitetaan ensisijaisesti kosteuden sitoutumista johonkin pintaan (esimerkiksi huokosen) ja absorptiolla tarkoitetaan sitoutumista kokonaiseen materiaalikappaleeseen (vaikkapa betoniseinään).

Käyrien alkupäät ($\varphi$ = 0…20 % RH) on piirretty katkoviivoilla. Lähteen mukaisia regressiolausekkeita käytettäessä adsorptio- ja desorptiokäyrät vaihtavat tuolla alueella puolia, eli desorptiokäyrä jää adsorptiokäyrän yläpuolelle. Tällöin siis kastumistilanteessa olisi hyvin matalan suhteellisen kosteuden olosuhteissa enemmän kosteutta (kg/m3), kuin kuivumistilanteessa, mikä ei vaikuta oikealle. Molempien käyrien päättyminen arvoon 0 kg/m3 on kuitenkin lähtökohtaisesti oikein, koska kuvan 1 mukaiset hygroskooppiset tasapainokosteuskäyrät kuvaavat vain vapaasti ilmasta materiaaliin sitoutuneen veden määrää.

Käyrien loppupäät($\varphi \geq$ 98 % RH) on myös piirretty katkoviivoin. Nyt käytetyillä regressiolausekkeille ne kohtaavat arvossa 147,5 kg/m<sup>3</sup>, mutta edellä käytetyssä lähteessä näin ei ole kaikissa tapauksissa, koska hygroskooppisen alueen yläraja ei ole vielä materiaalin huokostilavuuteen mahtuvan kosteuden enimmäismäärä. Esimerkiksi kontakti nestemäiseen veteen tai materiaalin upottaminen kokonaan veteen tuottaa vähintään hygroskooppisen alueen ylärajan suuruisen kosteuspitoisuuden ja joissain tapauksissa huomattavasti suuremman arvon. Näitä erittäin korkean kosteuspitoisuuden asioita voidaan kuvata kapillaarisen tasapainokosteuskäyrän avulla, jota käydään läpi omassa artikkelissaan. Seuraavaksi käydään kuitenkin läpi tarkemmin sitä, miten rakennusmateriaaleissa voi olla sitoutuneena runsaasti kosteutta, vaikka ympäröivä ilma sallisi kosteuden haihtumisen vapaasti vedenpinnasta.


## Tasapainotilanteen muodostuminen

Aikaisemmassa kirjoituksessa käytiin läpi kyllästysvesihöyrypitoisuuteen liittyviä asioita ja myös se, että vapaan vesipinnan viereisessä ilmassa kyllästysvesihöyrypitoisuus on samalla näiden kahden faasin tasapainotilanne. Tällöin esimerkiksi juomalasissa oleva vesi jatkaa haihtumistaan ympäröivään huoneilmaan, kunnes kaikki vesi on haihtunut tai huoneilman suhteellinen kosteus asettuu arvoon 100 % RH. Koska rakennusten lämmitys ja ilmanvaihto tyypillisesti pitävät ilman suhteellisen kosteuden reilusti alle tämän arvon, jatkaa vesi haihtumistaan, kunnes juomalasi on tyhjä.

Rakennusmateriaaleihin hygroskooppisesti sitoutunut kosteus ei kuitenkaan ole vapaata vettä, vaan vesimolekyyleihin vaikuttavat myös molekyylien välisten voimien lisäksi molekyylien ja huokosseinämien väliset adheesiovoimat.

Hygroskooppisuuden perusteorian mukaan alussa täysin kuivan materiaalin huokospinnoille voi kertyä yksittäisiä vesimolekyylejä. Jos huokosilmassa on kosteutta riittävästi tarjolla, huokosten pinnoille voi muodostua yhden tai myöhemmin useamman molekyylin paksuisia vesimolekyylikerroksia. Yhden ja useamman molekyylikerroksen käyttäytymistä voidaan kuvata [BET-teorian](https://en.wikipedia.org/wiki/BET_theory) avulla.

Jos materiaaliin hygroskooppisesti kertyvän kosteuden määrä kasvaa tästä edelleen, muodostuu huokosiin niin kutsuttuja meniskuksia, eli [pintajännityksen](https://michaelberryphysics.files.wordpress.com/2013/07/berry018.pdf) alaisia nestealueita. Näiden kaareutuneiden pintojen kohdalla veden kyllästysvesihöyrypitoisuus laskee vapaaseen vedenpintaan nähden. Mitä pienempi on meniskuksen säde, sitä voimakkaammin kyllästysvesihöyrypitoisuus pienenee. Toisin sanoen meniskuksen koon pienentyessä huokosen kyllästysvesihöyrypitoisuus laskee ja on lopulta vallitsevan vesihöyrypitoisuuden suuruinen. Tällöin suhteellinen kosteus huokosessa on 100 % RH, vaikka ilman suhteellinen kosteus ympäristössä olisi tätä pienempi. Tämä siis mahdollistaa kosteuden sitoutumisen ympäröivästä ilmasta huokoiseen rakennusmateriaaliin.

[Kapillaarikondenssilla](https://en.wikipedia.org/wiki/Capillary_condensation) tarkoitetaan tilannetta, jossa ympäröivän ilman vallitseva vesihöyrypitoisuus ylittää materiaalin huokosissa olevan kaareutuneen vesipinnan asettaman kyllästysvesihöyrypitoisuuden. Jos tällainen tilanne esiintyy, ympäröivästä ilmasta kondensoituu kosteutta rakennusmateriaaliin. Kapillaarikondenssin edetessä pienimmät huokoset täyttyvät vedellä, jolloin meniskuksen huokossäde kasvaa, kuten myös kyllästysvesihöyrypitoisuus. Tasapainotilanteessa kaareutuneen huokosvedenpinnan mukainen kyllästysvesihöyrypitoisuus vastaa taas ympäröivän ilman (huokosilman) vallitsevaa vesihöyrypitoisuutta.

Näin ollen kutakin ympäröivän ilman suhteellisen kosteuden arvoa kohti on olemassa vastaava meniskuksen säde, jonka suuruiset ja jota pienemmät huokoset pysyvät huokosvedellä kyllästyneinä. Rakennusmateriaalien täyttyminen hygroskooppisesti ympäröivän ilman vesihöyrystä käynnistyy siis pienimmistä huokosista ja jatkuu, kunnes ympäröivän ilman suhteellista kosteutta vastaavan kokoiset huokoset ovat täyttyneet ensin yksittäisten molekyylikerroksien ja sitten kapillaarikondenssin kautta.


## Hystereesi

Kuvassa 1 esiintyvää eroa adsorptio- ja desorptiokäyrien välillä kutsutaan hystereesiksi. Esimerkiksi jos uunikuivattu materiaali viedään 60 % RH ympäröiviin olosuhteisiin, päädytään pitkän aikavälin tasaantuneissa olosuhteissa noin 35 kg/m3 kosteuspitoisuuteen. Jos taas sama materiaali kastellaan ensin huokostilavuudeltaan aivan täyteen vettä ja tämän jälkeen viedään samoihin 60 % RH olosuhteisiin, on pitkän ajan tasapainokosteuspitoisuus noin 55 kg/m<sup>3</sup>.

Hystereesi vaikeuttaa huomattavasti kosteusteknisten laskelmien tekemistä, koska sen vuoksi yhteys materiaalin kosteuspitoisuuden (veden määrän) ja huokosilman suhteellisen kosteuden (vesihöyryn määrän) välillä ei ole yksiselitteinen. Esimerkiksi tiettyä suhteellisen kosteuden arvoa voi vastata usea eri materiaalin kosteuspitoisuus ja vastaavasti tiettyä kosteuspitoisuutta voi vastata usea eri suhteellisen kosteuden arvo. Yleisesti käytössä olevissa rakennusfysikaalisissa simulointiohjelmissa tasapainokosteuskäyrän hystereesiä ei oteta huomioon. Tällöin laskennassa käytetään vaihtelevasti joko adsorptiokäyrää, desorptiokäyrää, näiden keskiarvoa tai jotain muuta yhdistelmää.

Perinteikäs selitys hystereesille on ollut niin kutsuttu mustepulloanalogia: Materiaalin huokosrakenteessa on umpinaisia huokosia, jotka kuivan materiaalin kastuessa jäävät kuiviksi ja toisaalta märän materiaalien kuivuessa märiksi. Tätä voi testata esimerkiksi työntämällä tyhjää ämpäriä ylösalaisin veteen, jolloin ämpärissä oleva ilma estää veden työntymisen ämpäriin. Vastaavasti jos vedellä täyttynyttä ämpäriä lähtee nostamaan vedenpinnan alapuolelta ylöspäin, pysyy vesi ämpärissä, vaikka ämpäpärin kylki nousisi jonkin matkaa vedenpinnan yläpuolelle.

Vesimolekyylien tarttumisen ja irtoamisen epäsymmetrialle on löydetty myös molekyylitason mekanismeja, jotka antavat eri näkökulmia erilaisten materiaalien käyttäytymiseen. Näihin mekanismeihin liittyy myös kosteuden sitoutuminen [ajasta riippuvana ilmiönä](https://orbit.dtu.dk/en/publications/validation-of-hygrothermal-material-modelling-under-consideration) ja [materiaalien kosteusmuodonmuutokset](https://doi.org/10.1038/s41467-018-05897-9).


## Lämpötilan vaikutus tasapainokosteuskäyrään

Kuvassa 1 esitetyt regressiokäyrät ovat isotermejä, eli käyrät on määritetty vastaamaan tiettyä vakiolämpötilaa. Tasapainokosteuskäyrän arvot riippuvat kuitenkin kuvassa näkyvän suhteellisen kosteuden lisäksi myös lämpötilasta.

Tasapainokosteuskäyrien arvot määritetään tyypillisesti laboratorioiden tavallisissa huonelämpötiloissa 20…25 °C, joten tavallisissa käyttölämpötiloissa tasapainokosteuskäyrän arvot voivat poiketa laboratoriossa määritetyistä arvoista. Lämpötilan vaikutus tasapainokosteuskäyrän arvoihin katsotaan yleensä selvästi suhteellisen kosteuden vaikutusta pienemmäksi, mutta omalta osaltaan se kuitenkin aiheuttaa epävarmuuksia laskentatarkasteluihin ja mittaustulosten tulkintaan.

Kemiassa on olemassa periaate [(Poyet 2009, s. 17)](https://hal-cea.archives-ouvertes.fr/cea-01272821/document), jonka mukaan systeemi pyrkii kompensoimaan vastakkaiseen suuntaan siihen kohdistuneet muutosvoimat. Tällöin esimerkiksi materiaalikappaleen lämpötilan nostaminen tuo siihen lisää energiaa, mutta tämä kompensoituu kosteudesta suuremman osuuden muuttumisella vesihöyryksi. Jos materiaalissa olevan kosteuden määrä pysyy lämpötilaa nosteassa vakiona ja vesihöyryn määrä kasvaa, pienenee materiaalissa olevan nestemäisen veden määrä. Vastaavasti lämpötilan laskeminen pyrkii pienentämään kappaleessa olevan energian määrä, joka taas pyrkii kompensoitumaan vesihöyryn määrän pienenemisellä.

Tällainen suljettu tilanne ei tavallisesti toteudu tavallisissa rakennusmateriaaleissa, mutta esitetty idea kuvaa lämpötilan vaikutuksen suunnan tasapainokosteuskäyrään: Lämpötilan nosto tyypillisesti pienentää materiaalin kosteuspitoisuutta tasapainotilanteessa, kun ympäröivän ilman suhteellinen kosteus pysyy samana. Toisin sanoen, saman kosteuspitoisuuden säilyttäminen materiaalissa edellyttää ympäröivän ilman suhteellisen kosteuden nostoa, jos materiaalin lämpötila nousee.

Kääntäen ilmaistuna, materiaalin kosteuspitoisuus asettuu kylmässä lämpötilassa korkeampaan arvoon kuin lämpimässä, jos suhteellinen kosteus on molemmissa tapauksissa sama. Vastaavasti, saman kosteuspitoisuuden säilyttämiseksi riittää matalampi ympäröivän ilman suhteellinen kosteus, kun kappaleen lämpötila laskee.


## Yhteenveto

Tässä kirjoituksessa käytiin läpi perusteita rakennusmateriaalien hygroskooppisuudesta, joka tarkoittaa materiaalien kykyä sitoa kosteutta ympäröivästä ilmasta ja vapauttaa sitä sinne takaisin. Materiaalien hygroskooppisia ominaisuuksia kuvataan isotermisillä adsorptio- ja desorptiokäyrillä, joiden välisen hystereesin materiaalin huokosverkoston ominaisuudet määrittävät. Lämpötilalla on pieni vaikutus tasapainokosteuskäyriin tyypillisesti siten, että lämpötilan nosto pienentää tasapainotilanteen kosteuspitoisuutta.

Materiaalien hygroskooppisuutta voidaan tarkastella materiaalikappaleen, huokosverkoston tai yksittäisten molekyylien tasolla. Kaikkien näiden eri lähestymistapojen hyödyntäminen mahdollistaa tarkemman käsityksen muodostamisen hygroskooppisuuteen liittyvistä eri ilmiöistä.

[Takaisin etusivulle](https://www.kapillaari.fi/)