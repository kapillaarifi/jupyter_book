# Suhteellinen kosteus

*Alkuperäinen kadonnut versio tästä tekstistä oli vuodelta 2020. Samoja asioita sisältävä, mutta uudelleen kirjoitettu versio on vuodelta 2024.*

## Mitä on suhteellinen kosteus?

Suhteellinen kosteus on yksi keskeisimmistä rakennusfysiikan suureista. Se kuvaa ilmassa olevan vesihöyryn määrää suhteessa siihen vesihöyryn määrään, mikä ilmaan enimmillään mahtuu. Suhteellisen kosteuden määritelmä on:

$$
\varphi = \frac{\nu}{\nu_{sat} \left( T \right)} 
= \frac{p_\nu}{p_{\nu,sat} \left( T \right)}
$$

jossa $\varphi$ on suhteellinen kosteus, -, $\nu$ on vallitseva vesihöyrypitoisuus, g/m$^3$, $\nu_{sat}$ on kyllästysvesihöyrypitoisuus, g/m$^3$, $p_\nu$ on vallitseva vesihöyryn osapaine, Pa, $p_{\nu,sat}$ on vesihöyryn kyllästysosapaine, Pa ja $T$ on lämpötila, $^\circ$C.

Yllä olevan määritelmän mukaan suhteellinen kosteus voidaan laskea siis vesihöyrypitoisuuksista tai vesihöyryn osapaineista. Myös muiden yksiköiden käyttäminen on mahdollista. Suomessa käytetään yleensä vesihöyrypitoisuuksia $\nu$, kun taas Keski-Euroopassa käytetään usein vesihöyryn osapaineita $p_\nu$. Muunnokset vesihöyrypitoisuuden ja vesihöyryn osapaineen välillä voidaan tehdä tarvittaessa ideaalikaasun tilanyhtälön avulla.

Suhteellinen kosteus on hetkellinen ja pistemäinen arvo, joka yleisesti ottaen muuttuu tarkastelupisteestä toiseen ja ajanhetkestä toiseen siirryttäessä. Tämä johtuu siitä, että osoittajassa oleva vallitseva vesihöyrypitoisuus vaihtelee rakennuksissa ulko-olosuhteiden, rakennuksen käytön ja taloteknisten järjestelmien mukaan ja määräytyy tapauskohtaisesti kunkin tarkastelutilanteen mukaan. Esimerkiksi jos ulkoilmassa on vesihöyryä 6 g/m$^3$ ja sisäilmassa on kosteuslisä 3 g/m$^3$ ulkoilmaan nähden, on tällöin sisäilman vallitseva vesihöyrypitoisuus 9 g/m$^3$.

Nimittäjässä oleva kyllästysvesihöyrypitoisuus on kokeellisesti määritetty funktio, joka tavanomaisissa rakennusfysikaalisissa tarkasteluissa riippuu ainoastaan tarkastelupisteen lämpötilasta. Lämpötila taas on suure, joka myös riippuu useista tekijöistä, kuten ulko-olosuhteista, rakennuksen ominaisuuksista ja rakennuksen käytöstä.

Kyllästysvesihöyrypitoisuuden funktio on esitetty seuraavassa kuvassa.

```{figure} \sites\suhteellinen_kosteus\v_sat_ice_kapillaarifi.png
---
width: 80%
name: kuva_kyllastysvesihoyrypitoisuus
---
Kyllästysvesihöyrypitoisuus, eli lämpötilasta riippuva määrä vesihöyryä, jonka ilma pystyy enimmillään sitomaan.
```

Suhteellisen kosteuden voidaan siis sanoa olevan lämpötilan ja vallitsevan vesihöyrypitoisuuden funktio:

$$
\varphi = \varphi \left( \nu, T \right)
$$

Suhteellinen kosteus ilmaistaan usein prosentteina välillä 0...100 % tai desimaalilukuna välillä 0...1. Prosentteja käytettäessä on mukava lisä merkata prosenttimerkin perään kirjaimet "RH" (relative humidity), jolla viestitään, että kyse on nimenomaan suhteellisesta kosteudesta. Tällöin siis suhteellinen kosteus on esimerkiksi 40 % RH.


## Ulkoilman lämpötila, vesihöyrypitoisuus ja suhteellinen kosteus

Ulkoilman suhteellinen kosteus riippuu ulkoilman lämpötilasta ja vallitsevasta vesihöyrypitoisuudesta. Eri suureiden yhteyttä toisiinsa tarkastellaan tässä rakennusfysikaalisen mitoitusvuoden [Jokioinen 2011](https://research.tuni.fi/rakennusfysiikka/kosteusanalysointimenetelma/rakennusfysikaaliset-mitoitusvuodet-2022/) toteutuneiden olosuhteiden avulla. Rakennusfysikaalisten mitoitusvuosien roolia käydään mahdollisesti läpi tulevissa kirjoituksissa.

Seuraavassa kuvassa on esitetty ulkoilman tunnittaiset lämpötilat ja niistä laskettu yhden viikon liukuva keskiarvo.

```{figure} \sites\suhteellinen_kosteus\Te_Jok2011_kapillaarifi.png
---
width: 80%
name: kuva_lampotila_Jokioinen_2011
---
Ulkoilman lämpötilan toteutuneet tuntiarvot rakennusfysikaalisena mitoitusvuotena Jokioinen 2011. Kuvaan on lisätty myös 168 tunnin liukuva keskiarvo.
```

Kuvan mittakaava ja valinta liukuvan keskiarvon aikaikkunan leveydestä saattaa helposti hämätä. Esimerkiksi kesällä on melko erilaiset olosuhteet riippuen siitä, onko ulkoilman lämpötila noin +15 $^\circ$C vai +20 $^\circ$C, mutta kuvasta näitä eroja ei välttämättä suoraan huomaa, vaan niitä täytyy osata erikseen etsiä.

Seuraavassa kuvassa on esitetty vastaavat arvot ulkoilman vesihöyrypitoisuuden osalta.

```{figure} \sites\suhteellinen_kosteus\ve_Jok2011_kapillaarifi.png
---
width: 80%
name: kuva_vesihoyrypitoisuus_Jokioinen_2011
---
Ulkoilman vesihöyrypitoisuuden toteutuneet tuntiarvot rakennusfysikaalisena mitoitusvuotena Jokioinen 2011. Kuvaan on lisätty myös 168 tunnin liukuva keskiarvo.
```

Kuvan perusteella ulkoilman vallitseva vesihöyrypitoisuus on matalimmillaan talvella ja korkeimmillaan kesällä. Talven matalat arvot ovat seurausta siitä, että ulkoilmaan mahtuu kyllästysvesihöyrypitoisuuden mukaisesti kylmässä lämpötilassa vähemmän vesihöyryä, verrattuna kesäkauden korkeampiin lämpötiloihin.

Seuraavassa kuvassa on esitetty vastaavat arvot ulkoilman suhteellisen kosteuden osalta.

```{figure} \sites\suhteellinen_kosteus\RHe_water_Jok2011_kapillaarifi.png
---
width: 80%
name: kuva_suhteellinen_kosteus_Jokioinen_2011_RHe_water
---
Ulkoilman suhteellisen kosteuden toteutuneet tuntiarvot rakennusfysikaalisena mitoitusvuotena Jokioinen 2011. Kuvaan on lisätty myös 168 tunnin liukuva keskiarvo.
```

Esimerkkivuonna ulkoilman suhteellinen kosteus oli korkeimmillaan talvella ja matalimmillaan keväällä ja kesällä, mikä on tyypillinen tilanne. Samalla huomataan, että suhteellisen kosteuden vaihtelu oli suurempaa keväällä ja kesällä, kuin talvella.

Seuraavassa ja viimeisessä kuvassa on esitetty ulkoilman suhteellinen kosteus näitä vastaavien tunnittaisten lämpötilojen funktiona.

```{figure} \sites\suhteellinen_kosteus\RHe_water_vs_Te_Jok2011_kapillaarifi.png
---
width: 80%
name: kuva_RHe_water_vs_Te_Jokioinen_2011
---
Ulkoilman suhteellisen kosteuden tuntiarvot näitä vastaavien lämpötilojen funktiona.
```

Kuvan perusteella eniten korkeita (~100 % RH) suhteellisen kosteuden olosuhteita esiintyi lämpötila-alueella -5 $^\circ$C...+15 $^\circ$C. Kun ulkoilman lämpötila oli tätä korkeampi, oli erityisen korkeiden suhteellisen kosteuden arvojen esiintyminen harvinaista. Matalalla lämpötila-alueella (< -5 $^\circ$C) suhteellisen kosteuden huippuarvojen pienentymisessä on kyse mittalaitteiden ominaisuuksista, johon palataan myöhemmissä kirjoituksissa.


## Yhteenveto

Suhteellinen kosteus on yksi rakennusfysiikan perussuureista. Tässä kirjoituksessa käsiteltiin suhteellisen kosteuden määritelmää ja sitä, miten suhteellinen kosteus riippuu ilman vallitsevasta vesihöyrypitoisuudesta sekä lämpötilasta riippuvasta kyllästysvesihöyrypitoisuudesta. Lisäksi tarkasteltiin yhden esimerkkivuoden kuvaajien avulla ulkoilman lämpötilan, vesihöyrypitoisuuden ja suhteellisen kosteuden olosuhteita peruskäsitteiden havainnollistamiseksi.





