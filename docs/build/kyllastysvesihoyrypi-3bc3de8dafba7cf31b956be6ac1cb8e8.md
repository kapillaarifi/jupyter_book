

# Kyllästysvesihöyrypitoisuuden taulukot

_Onko silloin tällöin tarve kyllästysvesihöyrypitoisuuden arvoille, mutta sopivaa taulukkoa ei aina ole käsillä ja laskeminen vie aavistuksen verran liian paljon aikaa? Ehkä täältä löytyy apua, sillä tämän kirjoituksen yhteydestä löytyy aiheeseen liittyviä taulukoita._

_Julkaistu alunperin 14.2.2021. Päivitetty 2024._

[Takaisin etusivulle](https://www.kapillaari.fi/)

Pakkasolosuhteissa (<0 $^\circ$ C) kyllästysvesihöyrypitoisuus voidaan ilmoittaa joko nestemäisen veden tai jään suhteen.

Kyllästysvesihöyrypitoisuutta nestemäisen veden suhteen käytetään erityisesti meteorologisissa mittauksissa, kun tarkastellaan laajoja vapaan ilmatilavuuden olosuhteita. Tässä on taustalla se, että vesihöyry vapaasti ilmassa käyttäytyy maltillisiin pakkaslukemiin asti suhteessa nestemäiseen veteen, vaikkakin ilmakehän yläosien kovissa pakkasolosuhteissa kyllästysvesihöyrypitoisuus alkaa siirtyä kohti jään suhteen olevaa arvoa. Kansainvälisen meteorologisen järjestön WMO:n meteorologisia mittauksia käsittelevä CIMO-opas suosittelee suhteellisen kosteuden ilmoitettavaksi aina nestemäisen veden suhteen myös pakkasolosuhteissa. Useat RH-anturit ilmoittavat suhteellisen kosteuden pakkasolosuhteissa nestemäisen veden suhteen.

Rakennusfysikaalisissa tarkasteluissa sen sijaan tulisi käyttää suhteellista kosteutta jään suhteen, koska näissä tilanteissa on aina lyhyt etäisyys kiinteään materiaalipintaan. Jos esimerkiksi tehdään suhteellisen kosteuden mittauksia rakenteiden sisältä, voi RH-anturin näyttämä lukema olla aina alle 100 % RH pakkasolosuhteissa, vaikka rakenteessa suhteellinen kosteus olisi 100 % RH jään suhteen. Tällaiset seikat voivat vaikuttaa tulkintoihin vaikkapa vesihöyryn kondenssin (härmistymisen) esiintymisestä. Mittauksiin liittyy kuitenkin muitakin asioita ja laadukas mittaaminen sekä tulosten tulkinta vaatii hyvää ammattitaitoa. Useissa rakennusfysiikan laskentaohjelmissa kyllästysvesihöyrypitoisuus määritetään pakkasolosuhteissa jään suhteen.

Jos jonkin laitteen tai ohjelman käyttämistä arvoista on epäselvyyttä, pystyy käytettävät kaavat yleensä selvittämään laitteen tai ohjelman käyttöoppaista, testilaskelmilla tai kysymällä valmistajalta.

Seuraavassa taulukossa on esitetty kyllästysvesihöyrypitoisuus pakkasolosuhteissa nestemäisen veden suhteen:


```{figure} \sites\kyllastysvesihoyrypitoisuuden_taulukot\kyllastysvesihoyrypitoisuus_nestemaisen_veden_suhteen_alle_nollan.png
---
width: 90%
name: vsat_liquidwater_subzero
---
Kyllästysvesihöyrypitoisuus <0 $^\circ$C lämpötiloissa nestemäisen veden suhteen (g/m<sup>3</sup>). Kyllästysvesihöyrypitoisuus luetaan vasemman reunan kokonaisluvun ja yläreunan desimaalien leikkauskohdasta.
```


Seuraavassa taulukossa on esitetty vastaavat arvot jään suhteen:

```{figure} \sites\kyllastysvesihoyrypitoisuuden_taulukot\kyllastysvesihoyrypitoisuus_jaan_suhteen_alle_nollan.png
---
width: 90%
name: vsat_ice_subzero
---
Kyllästysvesihöyrypitoisuus <0 &degC lämpötiloissa nestemäisen veden suhteen (g/m<sup>3</sup>). Kyllästysvesihöyrypitoisuus luetaan vasemman reunan kokonaisluvun ja yläreunan desimaalien leikkauskohdasta.
```


Kun ollaan plussan puolella, vesi sulaa ja kyllästysvesihöyrypitoisuutta riittää tarkastella vain suhteessa nestemäiseen veteen. Lämpötilojen >0 &degC mukaiset kyllästysvesihöyrypitoisuudet on esitetty seuraavassa taulukossa:

```{figure} \sites\kyllastysvesihoyrypitoisuuden_taulukot\kyllastysvesihoyrypitoisuus_nollan_ylapuolella.png
---
width: 90%
name: vsat_abovezero
---
Kyllästysvesihöyrypitoisuus >0 $^\circ$C lämpötiloissa (g/m<sup>3</sup>). Kyllästysvesihöyrypitoisuus luetaan vasemman reunan kokonaisluvun ja yläreunan desimaalien leikkauskohdasta.
```




Taulukot ovat ladattavissa myös pdf-tiedostoina näistä linkeistä:

*   [Kyllästysvesihöyrypitoisuuden taulukot, pakkasolosuhteissa nestemäisen veden suhteen](/sites/kyllastysvesihoyrypitoisuuden_taulukot/kyllastysvesihoyrypitoisuus_nestemaisen_veden_suhteen_kapillaari_fi.pdf)
*   [Kyllästysvesihöyrypitoisuuden taulukot, pakkasolosuhteissa jään suhteen](/sites/kyllastysvesihoyrypitoisuuden_taulukot/kyllastysvesihoyrypitoisuus_jaan_suhteen_kapillaari_fi.pdf)


Katsotaan vielä lopuksi kyllästysvesihöyrypitoisuuden laskenta kaavoilla. Seuraavassa on esitetty CIMO-oppaassa esitetyt vesihöyryn kyllästysosapaineen laskentakaavat:

$$ 
p_{\nu,sat} = 
\begin{cases}
611,2 \cdot exp\left( \displaystyle \frac{17,62 \cdot \theta}{243,12+\theta}  \right) & \text{jos} \, \theta \ge 0 ^\circ C \\
611,2 \cdot exp \left( \displaystyle \frac{22,46 \cdot \theta}{272,62+\theta}  \right) & \text{jos} \, \theta \lt 0 ^\circ C
\end{cases}
$$ 

Tässä $\theta$ on lämpötila celsius-asteina.

Standardissa SFS-EN ISO 13788:2012 esitetyt vesihöyryn kyllästysosapaineen laskentakaavat ovat samaa Magnus-tyyppiä, mutta kertoimien desimaaleissa on pieniä eroja. Käytännön vaikutusta tällä ei ole, mutta yllä on käytetty CIMO-oppaan kaavoja, koska kyseinen opas on saatavilla vapaasti internetistä, kun taas standardi on maksullinen.

Muunnos vesihöyryn osapaineen ja vesihöyrypitoisuuden välillä voidaan tehdä ideaalikaasun tilanyhtälön avulla:

$$
\nu = \frac{p_{\nu}}{R_w T_K}
$$

Tässä vesihöyrypitoisuus $\nu$ on yksikössä kg/m<sup>3</sup>, veden ominaiskaasuvakion arvo on $R_w$ = 461,5 J/(kgK) ja lämpötila $T_K$ on kelvin-asteina.

Usein muuttujan tunnusta $T$ käytetään kuvaamaan lämpötilaa celsius-asteina. Tällöin täytyy itse pysyä tarkkana siitä, että milloin muuttujalla tarkoitetaan lämpötilaa celsius-asteina ja milloin kelvin-asteina.

Esimerkki 1: Ilman lämpötila on $\theta$ = 20 $^\circ$C, jolloin vesihöyryn kyllästysosapaine on $p_{\nu,sat}$ = 2333 Pa ja vesihöyrypitoisuus on $\nu_{sat}$ = 0,0172 kg/m$^3$ = 17,2 g/m$^3$.

Esimerkki 2: Ilman lämpötila on $\theta$ = -20 $^\circ$C ja se on lähes kyllästynyt jään suhteen ($\varphi$ = 97 % RH). Vesihöyryn kyllästysosapaine jään suhteen on $p_{\nu,sat}$ = 103,3 Pa ja kyllästysvesihöyrypitoisuus $\nu_{sat}$ = 0,88 g/m$^3$. Vallitseva vesihöyrypitoisuus on $\nu$ = 0,97 &times; 0,88 g/m$^3$ = 0,86 g/m$^3$. Samalla tavanomaisen (CIMO-ohjetta noudattavan) RH-anturin käyttämä vesihöyryn kyllästysosapaine ja kyllästysvesihöyrypitoisuus nestemäisen veden suhteen ovat $p_{\nu,sat}$ = 126,0 Pa ja $\nu_{sat}$ = 1,08 g/m$^3$. Tällöin RH-anturin näyttämä suhteellinen kosteus nestemäisen veden suhteen on $\varphi$ = 100 % &times; (0,86 g/m$^3$ / 1,08 g/m$^3$) = 79,5 % RH.

Tämän verran tällä kertaa, toivottavasti näistä on hyötyä!


## Lähteet

* World Meteorological Organization WMO (2018) Guide to Instruments and Methods of Observation. Volume I - Measurement of Meteorological Variables. WMO-No. 8 ([CIMO-Guide](https://community.wmo.int/en/activity-areas/imop/cimo-guide)), Ch. 4 Measurement of humidity, Annex 4.B
* Hagentoft, Carl-Eric (2001) Introduction to Building Physics. Studentlitteratur, Lund, Sweden. [Linkki](https://buildingphysicshagentoft.com/text-books/introduction-to-building-physics/)
* SFS-EN ISO 13788:2012 Hygrothermal performance of building components and building elements. Internal surface temperature to avoid critical surface humidity and interstitial condensation. Calculation methods.

[Takaisin etusivulle](https://www.kapillaari.fi/)