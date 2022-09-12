# Tiivistetty projektisuunnitelma

|  |  |
|:-:|:-:|
| Dokumentti | Tiivistetty projektisuunnitelma |
| Laatija: | Niko, Taru |
| Versio: | 0.1 |
| Päivämäärä: | 00.00.2022 |

![](https://openclipart.org/image/400px/167242)


## 1. Toimeksianto 

Grafiteam Oy:lle tuotamme uudet nettisivut Dynamiitti Orava tiimin toimesta. Nettisivujen toteutukseen annettiin tiimille avoimet kädet ja tällä tavalla sivut myös lähdemme toteuttamaan.

## 1.1 Tausta ja lähtökohdat


![](../assets/work-to-do.png)

<!--Kuvataan toimeksiantoa lyhyesti johdannon muodossa. Tarpeen mukaan ohjataan lukijaa tutustumaan tarvittaessa tarkemmin vaatimusmäärittelydokumenttiin.
>Projektin tavoitteena on pyrkiä yhdistämään .... on tarve kehittää” < kohdetta>… 
>Projekti toteutetaan Jyväskylän ammattikorkeakoulun informaatioteknologian instituutin järjestämän <TTOS2070> ‑opintojakson puitteissa. 
>Kohde on usein laajempi käsite kuin varsinainen projektille määriteltävä tehtävä. Kohde kuvaa selkeällä tavalla, usein graafiseen esitykseen tukeutuen,
>millaisesta järjestelmäkokonaisuudesta tai toiminnasta on kyse, johon ollaan tekemässä nyt projektissa jotain osakokonaisuutta/täydennystä. 
>Tässä siis kuvataan nykyjärjestelmää ja asiakkaan nykyistä toimintatapaa.-->

<!--https://ttc2070.pages.labranet.jamk.fi/fi/5-Harjoitusteht%C3%A4v%C3%A4t/toimeksianto0/-->

CodeCerub Oy lähtee luomaan ja kehittämään asiakastyönä [**WIMMA Lab**](https://www.wimmalab.org/):ille heidän toimintaa laajentavaa Foorumi-palvelua yhdessä Jyväskylän ammattikorkeakoulun informaatioteknologian instituutin järjestämän <TTOS2070> ‑opintojakson kanssa. Palvelun tarkoituksena on avata toimintaa erilaisille sidosryhmille ja tämän takia ollaan kehittämässä uusia sähköisiä palveluja. Foorumi tulee osaksi WIMMA Labin nykyisiä kotisivuja, joka toteutetaan asiakkaan vaatimalla tavalla. [Conduit ohjelmisto](https://github.com/gothinkster/realworld), joka toimii avoimella lähdekoodilla ([**open source**](https://en.wikipedia.org/wiki/Open_source)) saadaan asiakkaan vaatimuksien mukainen toteutus.
Avoimeen lähdekoodiin päädyttiin tiukan aikataulun vuoksi. Avoin lähdekoodi tarjoaa täydelliset puitteet nopeaan käyttöönottoon ja säästetään myös aikaa mm kehitykseltä.

Olemme ottaneet käyttöön demo-palvelin menetelmällä toimivan toimintaympäristön, jossa pääsee tutustumaan foorumin perus rakenteeseen ja toiminnallisuuteen.

Lähtökohtamme on siis se, että meillä on valmis sivu, josta saamme paljon visuaalisuuteen, kuten väreihin, fontteihin ja yleiseen ilmeeseen valmiit pohjat ja kaikkea ei tarvitse tehdä aloittaen täysin ruohonjuuri tasolta. Suurimpina haasteina on saada integraatio onnistumaan ja saada toiminnallisuus täsmäämään odotetulla tavalla.





## 1.2 Tavoitteet ja tehtävät

![](../assets/work-to-do.png)

<!-- ”Tässä dokumentissa kuvataan X-projektin taustaa, tavoitteita, tehtäviä, vaihejakoa, resursseja ja organisaatiota. Vaihejaon yhteydessä on kuvattu jokainen vaihe erikseen lyhyesti.”
> Tähän voi liittää lähteeksi vaatimusmäärittelyn sisältöä
> Määritellään työn keskeisin sisältö tässä projektissa; projektin tehtävä liittyy projektin kohteessa kuvattuun kokonaisuuteen. 
> Mitä toimintaa aiotaan kehittää ja miten?>
> Visio tulevasta tilasta
> Mikä on tuotettava lopputulos (konkreettinen)?
> Mitkä ovat osa- tai välitulokset?
> Mitä henkilöitä, toimijoita tai ryhmiä liittyy projektiin projektin 
> Tähän voi liittää Sidosryhmäkuvauksen tai käyttää lähteenä vaatimusmäärittelyä ?
> Esitellään palvelukuvaus ja sen mahdollinen muutoskohteet projektin myötä-->

Meillä suurimpana tavoitteena on saada foorumista paremmin asiakkaan tarpeisiin sopiva versio. Erityisen tärkeää projektin kannalta on saada foorumi integroitua mahdollisimman hyvin asiakkaan jo olemassa olevan nettisivun kanssa. On huolehdittava, että tämä tapahtuu saumattomasti ja on visuaalisesti ja käytännöllisellä tasolla sulautuva asiakkaan sivuihin nähden. On otettava huomioon sivun toteutus, sivun visuaalinen ilme, graafisuus, mittasuhteet, laitteiden yhteensopivuus. Tietosuoja asiat ovat myös suuressa asemassa projektin toteuttamisen kannalta ja näihin on otettava huomiota heti alkumetreillä.

Kongreettinen lopputulos on kokonaisuus, josta saa vaikutelman, kuin foorumi olisi ollut aina osa WIMMA Labin sivuja. Yleisilme on siis oltava samassa linjassa sivustojen kanssa ja olla käytettävyydeltään myös sointuva jo aikaisempaan sivuun. 


## 1.3 Rajaus ja liittymät

> Täsmennetään projektin tehtävää rajaamalla ulkopuolelle jäävät osat kohteena olevasta järjestelmästä tai kokonaishankkeesta. 
> Erikseen on syytä kuvata myös tehtävän suorittamista merkittävästi rajoittavat ulkoiset tekijät. Tässä myös täsmennetään ne 
> tehtäväkokonaisuudet, jotka nyt tehtävään osioon tulevat vielä todennäköisesti jossain vaiheessa liittymään, mutta joita ei 
> tämän projektin puitteissa kuitenkaan tulla toteuttamaan. Tyypillisiä tällaisia tehtäviä voisivat olla mm. käyttöympäristön
> rakentaminen ja koulutus. Muina rajauksina voisi olla esim. ohjelmiston käyttöliittymässä käytettävä kieli.

## 1.4 Oikeudet

>"Eri osapuolten oikeudet on määritelty projektisopimuksessa.” Ellei erillisessä sopimuksessa ole kerrottu oikeuksista työn tuloksiin, tulee ne ilmaista esim. tässä projektisuunnitelmassa. 

## 1.5 Termit ja määritelmät

>Tässä kappaleessa esitellään projektisuunnitelmassa esiintyvät määritelmät, termit ja lyhenteet. 

## 1.6 Projektiin liittyvät haasteet

>Tarkastellaan projektin tavoitteita ja laaditaan tarvittaessa tueksi erillinen SWOT-kuvaus, jossa tarkastellaan projektia ja sen toimintaympäristöä eri näkökulmista. 

**SWOT Analyysi**

```plantuml
@startmindmap
+ SWOT
++ VAHVUUDET
+++ Laaja osaaminen eri osa-alueilla
+++ Ammattitaitoa
+++ Kokenut tiimi
++ HEIKKOUDET
+++ Projekti hallitsija ekaa kertaa ohajimissa
+++ Tiimi on vieras ohjaajalle
++ MAHDOLLISUUDET
+++ Oppia paljon uutta projektin etenemisjärjestystä
+++ Vastoinkäymiset kääntyy opiksi
+++ Projekti valmistuu ajallaan
++ UHAT
+++ Deadlinessä ei pysytä
+++ Sairastumiset
+++ Tehdään jotain väärin
+++ Jotain olennaista jää huomaamatta
@endmindmap
```

## 2. Projektiorganisaatio

## 2.1 Organisaation esittely

![](../assets/work-to-do.png)

<!-- Kuka kuuluu projektiorganisaatioon? Onko projektiryhmän/tiimin lisäksi muita toimijoita?-->

Pyrimme toteuttamaan projektin täysin organisaatiomme sisällä, mutta tarvittaessa konsultoimme muita yhteistyökumppaneitamme ottamaan koppia erinäisistä tehtävistä, joihin ei mahdollisesti riitä tiimillä aika taikka osaaminen. Esimerkiksi laadunvalvonnallisissa tehtävissä saatamme ottaa yhteyttä muihin toimijoihin.

**Projektin eri osapuolet ja jäsenet**

Projektiin kuuluu myös muita jäseniä, jotka löytyy taulukon alta **"Tiimin esittely"** linkistä!

| Nimi | Organisaatio | Vastuu |
|:-:|:-:|:-:|
| Niko Kauppinen | CodeCerub Oy | Nuorempi projektipäällikkö, Projektinhallinta ja ohjaus, Projektin tiedotus|
| Arnold Suksi | CodeCerub Oy | Vanhempi projektipäällikkö, Projektin esimies |
| Carola Kettunen | CodeCerub Oy | Pääohjelmoija, Ohjelmointi esimies |
| Mirva Porkka | CodeCerub Oy | Asiakkaan yhteyshenkilö |
| Mauno Kara | CodeCerub Oy | Tietoturva päällikkö |
| Kari Pitkäniemi | WIMMA Lab | Asiakkaan edustaja |
| Teemu K | WIMMA Lab | Tekninen arkkitehti |
| Marko Rintamäki | WIMMA Lab | Tuoteomistaja |


[Tiimin esittely.](https://fi-a2022-ttc2070.pages.labranet.jamk.fi/ht1-AC8393-/core/10-Projektihallinta/esittely/)


**Projektiorganisaation rakenne MindMap-muodossa**

```plantuml
@startmindmap
+ Tuotos
++ Tuotantotiimi
+++ Arnold Suksi, Vanhempi projektipäällikkö
+++ Niko Kauppinen, Nuorempi projektipäällikkö
+++ Carola Kettunen, Pääohjelmoija/Arkkitehti
+++ Matti Urri, Ohjelmoija
+++ Kauno Koivisto, Ohjelmoija
-- Tilaaja
--- Tilaaja 1
++ Laadunvalvonta organisaatio(Voi olla myös ulkopuolinen toimija)
+++ Testipäällikkö
+++ Mauno Kara, Tietoturvatestaus
+++ Klaus Kähö, Käytettävyystestaaja
@endmindmap
```

## 2.2 Vastuut ja päätöksentekoprosessi

>Tähän kirjataan kaikkien projektiorganisaatioon kuuluvien (esim. johtoryhmä, projektipäällikkö, sihteeri, ryhmä, >ohjaajat) vastuut sekä päätöksentekoprosessi (esim. projektipäällikkö valmistelee ja esittää johtoryhmän päätettäväksi…)

>”Projektiryhmä suorittaa johtoryhmän projektille asettamat tehtävät käytettävissä olevien resurssien puitteissa. >Projektin aikana ryhmän päällikön ja sihteerin roolit kiertävät ryhmän sisällä siten, että jokainen ryhmän jäsen toimii >kerran kummassakin roolissa.”

>”Johtoryhmän muodostavat siihen valitut projektiryhmän, ohjaajien ja toimeksiantajan edustajat. Johtoryhmän kokouksiin >voidaan tarvittaessa kutsua myös muita henkilöitä, esim. asiantuntijoita.Johtoryhmän kokoonpano on esitelty >projektisopimuksen liitteessä <X>.” 

>Tukiryhmän tehtävänä on antaa projektiryhmälle sisällöllistä opastusta tehtävän suorittamiseksi. Kappaleessa tulee >esitellä projektin muut sidosryhmät (asiakas, ulkopuoliset konsultit, jne.) henkilötasolla. Asiakkaan mukana olevista >henkilöistä tulee mainita ainakin nimi, yhteystiedot, toimenkuva sekä rooli projektissa.


## 2.3. Projektin vaiheet ja taloudelliset tavoitteet

>tehtäväkokonaisuudet, osittelu ja vaiheistus, välitulokset, aikataulut ja resurssissuunnitelmat, budjetti

## 2.4. Laadun varmistus

>menetelmät, standardit, hyväksymismenettely, muutosten hallinta, dokumentointi, katselmoinnit, riskien hallinta, muut täydentävät suunnitelmat

## 2.5. Tiedonvälitys ja projektin etenemisen seuranta

>projektin aloitus, työtilat ja viestintävälineet, palaverikäytäntö ja yhteydenpito, raportointi ja tiedotus, projektikansio

## 2.6. Projektin päättyminen

>luovutus, käyttöönotto, ylläpito, projektin aineiston taltiointi, arkistointi, loppuraportti, projektin virallinen päättäminen

## 3. Projektin ajalliset tavoitteet	

## 3.1 Osittaminen ja vaiheistus

>Projektin etenemistä voidaan kuvata ns. GANTT-kaaviolla. Sen avulla voidaan esittää eri vaiheiden eteneminen aikajanalla, samalla voidaan osoittaa projektin eri vaiheisiin liittyvät kriittiset pisteet / etapit. Ohjelmistoprojekteissa karkea etenemisjärjestystä voi kuvata ohjelmistojen [SDLC](https://en.wikipedia.org/wiki/Systems_development_life_cycle )-mallilla.
Tästä voidaan nostaa esiin muutama oleellisia vaiheita kuten:

* Määrittely
* Suunnittelu
* Toteutus
* Testaus
* Luovutus

![](../assets/work-to-do.png)

**Esitetään vaiheet yksinkertaisen GANTT diagrammin avulla**

```plantuml
Project starts the 2022-8-20
[Projekti timeline] Starts 2022-8-20 and ends 2022-11-15 
[Määrittely] Starts 2022-8-20 and ends 2022-8-27
[Suunittelu] Starts 2022-8-27 and ends 2022-9-17
[Toteutus+suunnittelu] Starts 2022-9-17 and ends 2022-10-15
[Testaus+korjaus] Starts 2022-10-15 and ends 2022-11-5
[Hyväksyntätestaus] Starts 2022-11-5 and ends 2022-11-13
[Luovutus] Starts 2022-11-13 and ends 2022-11-15
```

![](../assets/work-to-do.png)

Päivitä linkit omaan projektiin liittyviksi!

* [Etappi 0](https://gitlab.labranet.jamk.fi/jamkit/project-templates/opf-core-template-v2/-/milestones/2)
* [Etappi 1](https://gitlab.labranet.jamk.fi/jamkit/project-templates/opf-core-template-v2/-/milestones/3)
* [Etappi 2](https://gitlab.labranet.jamk.fi/jamkit/project-templates/opf-core-template-v2/-/milestones/4)
* [Etappi 3](https://gitlab.labranet.jamk.fi/jamkit/project-templates/opf-core-template-v2/-/milestones/5)
* [Etappi 4](https://gitlab.labranet.jamk.fi/jamkit/project-templates/opf-core-template-v2/-/milestones/6)

>Projektin osittamisella tarkoitetaan projektin jakamista selkeisiin osakokonaisuuksiin ja niitä vastaaviin toteutuskokonaisuuksiin (osaprojekteihin, vaiheisiin, tehtäväkokonaisuuksiin ja tehtäviin). >Tutkimus- ja kehitysprojektien etenemiselle on tyypillistä lopputuloksen muodostuminen ja tavoitteen tarkentuminen vaihe vaiheelta. Projektin osituksen tulee perustua tähän lähtökohtaan (koskee myös >IT-instituutin opiskelijaprojekteja). 
>Projektin elinkaari voidaan jakaa erityyppisiin vaiheisiin. Kussakin vaiheessa tuotetaan määrätyt tuotteet, kuten selvitys, suunnitelmat, prototyyppi, laite jne. Kunkin vaiheen loppuun sovitaan arviointi, hyväksyntä tai katselmointi. Ohjelmistoprojekti jakautuu tyypillisesti seitsemään vaiheeseen: perustaminen, esitutkimus, analyysi, suunnittelu, toteutus, testaus ja lopettaminen. Joskus esitutkimus on oma projektinsa, joskus analyysi sisällytetään suunnitteluun jne. Testaus ei välttämättä ole oma vaiheensa, vaan se sisältyy kaikkiin vaiheisiin. Usein edetään inkrementaalisesti eli ensin suunnitellaan ja toteutetaan yksi asia kokonaisuudessaan ennen kuin edetään seuraavaan asiakokonaisuuteen. Ei ole yhtä ainutta ”oikeaa” vaihejakoa, mutta jos toimeksiantajalla on oma menetelmänsä ja siihen liittyvät mallipohjat, niin opiskelijaprojekteissa käytetään ensisijaisesti niitä. Yhä useammin käytetään ketterää sovelluskehitystä eli ohjelmisto tehdään 1-4 viikon sprinteissä.

>Mitä tavoitteita  / vaiheita projekti sisältää? (Lyhyt kuvaus kustakin)> <Mitä tuloksia kustakin vaiheesta syntyy? >

Seuraavassa käydään jokainen vaihe, niiden vaatimat aikaresurssit ja tulokset läpi lyhyesti. Vaiheet ja niiden tehtävät kuvataan tarkemmin vaihesuunnitelmissa. Parhaillaan meneillään olevasta vaiheesta tulee olla tiedossa tarkasti kuka tekee ja kuinka paljon työtä tämän vaiheen tehtävien suorittamiseksi. Myöhempien vaiheiden työmääräarviot voidaan esittää alkuvaiheessa karkealla tasolla, jota sitten projektin edetessä tarkennetaan yksityiskohtaiselle tasolle. Tämä tapahtuu jokaisen vaiheen lopussa, jolloin suunnitellaan tarkemmin seuraava vaihe.

Huom.: Seuraavassa on esitetty käynnistys- ja lopetusvaiheet. Kaikista projektin vaiheista, niiden kestoista ja työmääristä laaditaan myös nk. Gantt-kaavio (liitteenä), jossa näkyy myös vaiheiden väliset riippuvuudet ja tärkeimmät etapit (esim. johtoryhmän kokouspäivämäärät).

>Projektin eteneminen kannataa jakaa ns. tavoitteisiin/etappeihin. Näiden tehtävän on osoittaa ajanhetkeä, jollon jokin oleellinen projektin vaihe on tarkoitus saavuttaa. Projektille määritellyt etapit voidaan linkittää dokumentaation kanssa yhteen käyttäen apuna Issue/Milestone linkkejä avulla. *Katso esimerkit alla*




* [Etappi 0](https://gitlab.labranet.jamk.fi/jamkit/project-templates/fi-opf-2021-core-template-v2/-/milestones/1)

>esim. ryhmän webbisivut, tutustutaan tarkemmin toimeksiantoon, aloitetaan kohdealueeseen perehtyminen ja laaditaan projektisuunnitelma yhteistyössä toimeksiantajan edustajien kanssa. 
>Projektin käynnistämiseen kuuluu olennaisesti projektisuunnittelu ja suunnitteludokumenttien laatiminen sekä yhteydenpitokäytänteiden luominen toimeksiantajayrityksen kanssa. Vaiheen aikana tehdään
>Etappiin mennessä muodostetaan johtoryhmä, pidetään johtoryhmän kokous sekä allekirjoitetaan projektisopimus.

* [Etappi Z](https://gitlab.labranet.jamk.fi/jamkit/project-templates/fi-opf-2021-core-template-v2/-/milestones/3)

>Esimerkkinä Etappi Z , jossa tavoitteet on asetettu ennakkon esimerkkeinä: projektisuunnitelman hyväksyminen, tavoitteiden tarkistaminen

* [Etappi X](https://gitlab.labranet.jamk.fi/jamkit/project-templates/fi-opf-2021-core-template-v2/-/milestones)

>Sovittu etappi X, jossa suoritettaa esimerkisi katselmointi ja esitetään tilanneraportti

* [Etappi Y](https://gitlab.labranet.jamk.fi/jamkit/project-templates/fi-opf-2021-core-template-v2/-/milestones)


* [Etappi Z](https://gitlab.labranet.jamk.fi/jamkit/project-templates/fi-opf-2021-core-template-v2/-/milestones)

>”Lopettamisvaihe sisältää projektin päättämiseen liittyvät toimenpiteet. Vaiheen aikana projektiryhmä laatii projektin loppuraportin ja esityksen johtoryhmälle. Vaiheen aikana luovutetaan projektin tulos toimeksiantajalle, pidetään viimeinen johtoryhmän kokous viikolla X sekä puretaan projektin organisaatio. Lopettamisvaiheen tuloksena on projektin loppuraportti.”

## 3.2 Projektin alustavat kustannusarvio

![](../assets/work-to-do.png)

Kustannusarvion esittäminen taulukon avulla: 

![](kustannusarvio.JPG)

## 4. Laadunvarmistus

>Projektissa sovellettavat työmenetelmät, välineet, ohjeet ja standardit

>Tässä kappaleessa luetellaan kaikki käytettävät menetelmät, työkalut ja standardit versionumeroineen. Usein toimeksiantajalla on jokin menetelmä, jota projektiryhmän olisi syytä noudattaa. Toimeksiantaja voi määrittää myös noudatettavat dokumenttien ulkoasustandardit. Muussa tapauksessa projektiryhmä räätälöi IT-instituutin tarjoamista mallipohjista itselleen soveltuvan ja toimeksiantajan hyväksymän mallin.

>Opintojakso asettaa siis tietyt vaatimukset projektin seurantatyökaluille ja raportoinnille, jotka tulee ottaa huomioon. Opintojaksolla ei kuitenkaan pakoteta tiettyä tapaa käyttää työkaluja, joten niiden käytöstä on syytä tehdä suunnitelma tähän kohtaan.

>Projektin tiedon- ja versionhallinnan perusteet tulee selvittää, jotta kaikki projektin sidosryhmät tietävät dokumenttien uusimpien versioiden sijainnin. Projektisuunnitelmasta ja kaikista muistakin projektin keskeisistä dokumenteista tulee useita versioita, joihin pitää lisätä versiohistoria, jotta projektin kehityksen seuraaminen jälkikäteen on mahdollista. Mikäli jokin yksittäinen laite tai ohjelmisto nousee projektin toteutuksen kannalta kriittiseen asemaan, on tälle hyvä nimetä vastuuhenkilö, joka tuntee ko. laitteen tai ohjelmiston ryhmästä parhaiten. Ohessa on lista asioista, jotka kannattaa suunnitella ja dokumentoida: 

## 4.1 Väli- ja lopputulosten hyväksymismenettely

>Tähän kirjataan se hyväksymismenettely, mikä projektissa on sovittu.

## 4.2 Muutosten hallinta

>Kuvataan muutosten hallintaproseduuri projektinkäytäntöihin tai projektin tuloksiin liittyvien muutosten osalta.

## 4.3 Dokumentointi

>Kirjataan minne dokumentit tallennetaan/arkistoidaan, miten ne jaetaan ja kuka on vastuussa eri dokumenteista.

## 4.4 Riskien hallinta

>Listataan riskit, arvioidaan niiden vakavuus ja todennäköisyys ja koetetaan miettiä toimenpiteet kuinka vakavimmat/todennäköisimmät riskit voitaisiin ehkäistä jo ennalta. Lisäksi olisi hyvä olla suunnitelma kuinka toimitaan, jos riski toteutuu.
>Kirjataan alla olevaan taulukkoon projektiin kohdistuvat riskit ja pidetään niitä yllä tarpeen mukaan. Jokaiselle riskille annetaan yksilöllinen tunniste esim. RIS007, koska tämä helpottaa niiden käsittelyä eri tilanteissa.

Liitä seuraava osio tähän mukaan: [Riskienhallintataulukko](riskitaulukko.md)

## 4.5 Katselmointikäytäntö

>Luetellaan ja alustavasti aikataulutetaan projektin tuloskatselmukset laaditun toteutussuunnitelman pohjalta. Esitetään luettelomaisesti, mitä katselmuksia pidetään, alustava ajankohta, käsiteltävät asiat, osallistujat sekä käytännöt katselmointimateriaalin toimittamisesta (mitä, milloin, miten).

## 4.6 Projektisuunnitelmaa täydentävät suunnitelmat

>Tässä kohdassa mainitaan, mitä täydentäviä suunnitelmia on käytettävissä tai aiotaan projektin kuluessa laatia (esim. viestintä-, riskienhallinta-, testaus- ja käyttöönottosuunnitelma).

* Projektisopimus <!--(..//10-Projektinhallinta/projektisuunnitelma.md)-->
* Vaatimusmäärittely <!--(../20-Vaatimustenhallinta/vaatimusmaarittely.md)-->
* [Julkaisusuunnitelma](../40-Julkaisusuunnittelu/julkaisusuunnitelma.md)
* [Yleistestisuunnitelma](../40-Julkaisusuunnittelu/julkaisusuunnitelma.md)
* Viestintäsuunnitelma <!--(..//10-Projektinhallinta/viestintasuunnitelma.md)-->
* Riskihallintasuunnitelma <!--(../10-Projektinhallinta/riskihallinta-suunnitelma.md)-->
* [Muu annettu dokumentaatio]()


## 4.7 Suunnitelmien tarkistus- ja päivitysajankohdat 

>Projektisuunnitelman avulla reagoidaan poikkeamiin ja ympäristömuutoksiin, joten sitä päivitetään projektin aikana. Tähän kohtaan kirjataan ne ajankohdat, jolloin suunnitelman ajantasaisuus ainakin on tarkistettava.

## 4.8 Projektin keskeyttämiskriteerit

Oikeaoppiseen projektisuunnitelmaan kuuluu myös projektin keskeyttämiskriteerit. Näitä ei kuitenkaan opiskelijaprojekteissa käytetä, koska projekteissa käytetään tietty tuntimäärä tuloksen tekoon ja tulos luovutetaan sellaisena, kun se opintojakson päättyessä on. Projektiryhmä tekee kuitenkin jatkokehityssuunnitelman, josta mahdollinen uusi projekti jatkaa.

## 5. Tiedonvälitys ja projektin etenemisen seuranta (viestintäsuunnitelma)

## 5.1 Viestintäsuunnitelma

>Viestintäsuunnitelman tarkoituksena on määritellä X projektin yhteydessä käytetyt viestintämenetelmät ja kanavat. Selkeällä ja yhdenmukaisella viestinnällä varmistetaan >informaation kulku ja vaikutetaan projektin laatutavoitteiden toteutumiseen. Suunnitelma voidaan laatia osana projektisuunnitelmaa tai siihen voidaan viitata omana [alasivunaan](../10-Projektihallinta/viestintasuunnitelma.md)

>Listaa projektissa sovitut työtilat ja viestintävälineet, palaverikäytäntö ja yhteydenpito, raportointi ja tiedotus.

## 6. Projektin päättyminen

## 6.1 Lopputuotteen luovutus, käyttöönotto

>Projektin lopputuote tulee myös dokumentoida järkevällä tasolla. Osana lopputuotetta saattaa olla asiakkaalle tarjottavaa käyttöönottokoulutusta ja mahdollisesti asennus- tai käyttöönotto­palvelua. Mikäli koulutuksen rooli projektin kannalta on huomattava (esimerkiksi ohjelmiston käyttäjät eivät ole olleet mukana projektissa ja eivät tiedä miten järjestelmä toimii) tulee projektisuunnitelmaan liittää suunnitelma asiakkaalle tarjottavasta koulutuksesta. Lisäksi jos on tarpeen, tulee projektisuunnitelmaan liittää myös asennussuunnitelma ja käyttöönottosuunnitelma.

## 6.2 Projektin tuottaman aineiston taltiointi, arkistointi ja säilytysaika

>”Projektiryhmien dokumentaatiosta jäävä osa tallennetaan X-järjestelmään” 
>Toimeksiantajan kanssa tulee tarvittaessa voida sopia, mitkä dokumentit voidaan jättää opiksi seuraaville projekteille. 
>Tyypillisesti eri suunnitelmat ja loppuraportti sopivin osin ovat tällaisia dokumentteja. 

## 6.3 Projektin virallinen päättäminen

>On tärkeää määritellä milloin, mihin tai miten projekti päättyy. Projektin päätös voi olla tietty päivämäärä, tietty tuotteen valmiusaste, tietty työtuntimäärä, tietty kulutettu rahasumma, kun asiakas ottaa tuotteen käyttöön, takuuaika on umpeutunut tai kun asiakas hyväksyy tuotteen.

>”Projekti päättyy p.k.vvvv, jolloin projektisopimuksen voimassaoloaika päättyy.”

## 6.4 Lopetustilaisuus

>Yleensä projektit päätetään yhteiseen päätösseminaariin. Tähän kirjataan osallistujat ja ajankohta. 

* Saunailta :)?


## 6.5 Projektin loppuraportti

>Projektin loppuraportti laaditaan viimeiseen johtoryhmän kokoukseen mennessä.

