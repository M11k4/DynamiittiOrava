# Ohjelmistoarkkitehtuuri (pohja)

|  |  |
|:-:|:-:|
| Dokumentti | Ohjelmiston arkkitehtuuri kuvaus-pohja |
| Laatija: | DynamiittiOrava |
| Versio: | 3.4 |
| Päivämäärä: | 29.11.2022 |

Tämä dokumentin pohjana käytetään alkuperäistä http://www.cs.tut.fi/ohj/dokumenttipohjat/pohjat/suunnittelu/hytt_drsuunnittelu.doc

*Kiitos alkuperäisen rungon laatijoille.*

# 1.JOHDANTO

### 1.1		Tarkoitus ja kattavuus

>Tällä sivulla avataan Dynamiitti Oravan syksyn 2022 projektin teknistä suunnitelmaa ja toteutusta, keskittymällä tuotoksen ominaisuuksiin. Tämän asiakirjan tarkoitus on kirjata projektin teknista tavoitetta ja kuvata tuotoksen ominaisuuksia. Tämä kuvaus on tarkoitettu DynamiittiOravan jäsenille viitteeksi ja sen kattavuus on suhteutettuna siihen tuntemukseen joka tiimin jäsenille muodostui projektin aikana.
>Luvuista 1,5-7 löytyy yleisiä ja sekalaisia huomioita projektin teknisestä puolesta. Luku 3 on asiakirjan ydin, jossa käydään läpi teknistä suunnitelmaa, eli sitä millaista sivustoa oikein rakennamme. Luku 4 kirjaa lopullisen sivuston ulkoasua, ominaisuuksia ja toiminnallisuutta.

### 1.2		Tuote ja ympäristö

>Tuotamme verkkosivuston toimeksiantajalle. GrafiTeam Oy haluaa selkeät sivut jolla heidän asiakkaat saavat tietoa yrityksestä ja tilattavista tuotteista. Sivuston tulee toimia yleisimmillä nettiselaimilla internetissä.

### 1.3		Määritelmät, merkintätavat ja lyhenteet 

>evästeet - verkkosivun lokaalisti tallentama tieto kävijän laitteelle.
>nettisivu - tuottamamme verkkosivusto joka lopulta tarjotaan toimeksiantajalle.
>palikka - viittaa Reactissa toteutettuihin verkkosivun osiin.
>palvelin - jokin osa jota jonkun pitäisi ymmärtää sivuston julkaisemiseksi.
>printti - sana jota toimeksiantaja suosi tuotteestaan, vrt painatus/painotuote/tulostus.
>turbiini - rakennuksen nimi jossa tiimimme pystyi tavata Jamkin Lutakon kampuksella.

### 1.4		Viitteet

>Ulkopuolisia dokumentteja joita hyödynsimme projektin aikana.

 * https://www.npmjs.com/package/react-responsive-carousel

>Testasimme lukuisia muita mahdollisia valmiita osia joita voisi hyödyntää sivustoa kootessa, mutta suurin osa jäi tien varteen. (Valmisosista tarkemmin alla, luvussa 5.)

## 2.		JÄRJESTELMÄN YLEISKUVAUS

>Nettisivu mainostaa ja julkistaa toimeksiantajan yhteystiedot ja tuotteita.

### 2.1		Sovellusalueen kuvaus

>Nettisivu julkaistaan julkisella palvelimella.

### 2.2		Järjestelmän liittyminen ympäristöönsä

>Nettisivu on itsenäinen kokonaisuus, vaikka toki sieltä on linkitys toimeksiantajan sosiaalisen median profiileihin.

### 2.3		Laitteistoympäristö

>Nettisivu toimii yleisimmillä ajantasaisilla internetselaimilla. Tämän lisäksi käyttäjällä tulee olla toimiva internetyhteys. Sivusto on kevyt eikä vaadi laitteilta merkittävää toimintakykyä. 

### 2.4		Ohjelmistoympäristö

>Nettisivu on rakennettu hajoitetulla kehitysprosessilla jakaen projektin eri versioita git-järjestelmän avulla. Kukin kehittäjä toimi omilla alustoillaan, esimerkiksi editorina käytettiin Visual Studio Code (ver. 1.73.1) Windows alustalla. Osana tätä kokonaisuutta toimi Node.js, josta oli myös höytyä automaattisen testauksen puolella.

### 2.5		Toteutuksen keskeiset reunaehdot

>Nettisivun tulee toimia vähintään 20 yhtäaikaisella kävijällä. Nettisivulla ei ole juurikaan interaktiivista sisältöä, niin tämä vaatimus ei ole raskas ja toteutuu palveluntarjoajan sopimuksesta. Nettisivulla ei ole suuria teknisiä turvallisuusriskejä. (Toimeksiantaja kuitenkin toivoi yhteystietonsa olevan selkeästi, mutkattomasti ja salauksetta näkyvillä sivuilla.)

### 2.6		Sopimukset ja standardit

>GrafiTeam Oy:n ja DynamiittiOravan välillä oli sanallainen ystävyyssopimus ilman suurempia vaatimuksia puolin tai toisin. DynamiittiOrava tarjoutui valmistamaan GrafiTeamille uudet nettisivut jotka GrafiTeam saisi käyttöönsä halutessaan.

>Nettisivua rakentaessa otimmi huomioon viranomaisten laatimia sääntöjä ja direktiivejä. Esimerkiksi evästevaatimukset tuottivat paljon keskustelua, vaikka lopulliselle sivulle päädyttiin olla käyttämättä evästeitä.

>DynamiittiOravan jäsenet saavat käyttää projektin jälkeen projektia omissa portfolioissaan, ainakin siltä osin kun tämä ei loukkaa tiimin jäsenten yksityissuojaa tai muuten esitä jäseniä huonossa valossa.

## 3.		ARKKITEHTUURIN KUVAUS

>Nettisivusto rakennetaan DynamiittiOravan osaamisen rajoissa, joka alkaa muttei rajoitu nettiteknologiohin HTML, JavaScript, React ja Node.js.

### 3.1		Suunnitteluperiaatteet

>Nettisivustosta laaditaan design-luonnoksia käyttäen Figma-työkalua. Sivuston osien tulee olla selkeät ja painoitus on uuden asiakkaan kokemuksessa. Sivujen tavoite on herättää uuden kävijän luottamus ja mielenkiinto ottaa yhteyttä GrafiTreamiin tilausta varten. Sivustolla esitelty tieto tulee olla totuudenmukaista ja selkeästi esittää GrafiTeamin toimintaa. Samalla DynamiittiOrava haluaa myös oppia jotain uutta käytetysta teknologiasta, eli emme vain tyydy kulkemaan sitä tuttua ja turvallisinta reittiä jos ideoimme jotain joka sopivassa määrin haastaa meitä ja muuten tähtää parempaan lopputulokseen sivun suhteen.

### 3.2	 	Ohjelmistoarkkitehtuuri, moduulit ja prosessit

(Work In Progress)
>Tässä kohdassa esitetään yksityiskohtaisesti ohjelmiston jako osajärjestelmiin, ohjelmiin, prosesseihin, moduuleihin, pakkauksiin ja/tai luokkiin. Lisäksi kuvataan moduulinen välistä kommunikointia esimerkiksi tapahtumasekvenssikaavioiden avulla.
Moduuleista erotellaan "valmisosat", eli muualta sellaisenaan tai muokaten napatut osat. Nämä seikat voi kuvata esim. moduulikaaviossa erilaisilla korostuskeinoilla.  
Tässä voidaan myös esittää nimeämiskäytäntöjä, viittauksia tyylioppaisiin yms. kaikkien moduulien toteutukseen liittyviä asioita.

## Suoritysympäristön (tuotanto) kuvaus

Käyttäjäkokemus:
1. Käyttäjä avaa sivuston GrafiTeam.fi.
2. Käyttäjä selaa sivustoa.
3. Käyttäjä ottaa yhteyttä GraTeamiin ja tilaa jotain.

Tekninen puoli käyttäjäkokemuksesta:
1. Sivusto latautuu palveluntarjoajalta käyttäjän laitteeseen.

### 3.3		Tietokantaarkkitehtuuri

>Nettisivulle ei tulekaan tietokantatoiminnallisuutta.

### 3.4	Virhe ja poikkeusmenettelyt

>Nettisivuilla ei ole implementoitu virheilmoituksia DynamiittiOravan puolesta.

### 3.5 Tuotekehitysympäristön kuvaus

>Kuvaa ainakin seuraavat:

* Kehitysympäristö
* Testiympäristö
* Ajo/suoritusympäristö
* Demoympäristö

>Eli miten nuo eri ympäristöt on toteutettu ko. projektissa

## Käytetyt työvälineet ja niiden versionumerot

(WORK IN PROGRESS)
* Kääntäjä xyz v1.0.1
* debuggeri zky v2.05
* Firefox 123

## 4.		MODUULI /LUOKKA/PROSESSIKUVAUKSET

>Tämän luvun lukurakenne suunnitellaan ohjelman arkkitehtuurin mukaiseksi: Jos yksitasoinen jaottelu riittää, käytetään tässä esitettyä tapaa (4.1 Moduuli X, 4.2 Moduuli Y…). Jos ohjelma jakaantuu esimerkiksi pakkauksiin, joiden sisällä on useita luokkia, kannattaa kullekin pakkaukselle tehdä oma kohtansa, jonka alakohdissa kukin luokka kuvataan. Pakkauksen kaikille luokille yhteiset asiat kuvataan luvun alussa, ja jos pakkauksella on rajapinta, myös se kuvataan tässä. Laajoissa hankkeissa kunkin pakkauksen tai osajärjestelmän sisäisestä rakenteesta kirjoitetaan erillinen suunnitteludokumentti.
Jokaisesta moduulista kuvataan sen tehtävä, liittymät muihin osiin, rajapinta sekä toteutusnäkökohdat. Tekniset yksityiskohdat täytyy selittää niin tarkasti, että kuvauksen perusteella pystytään suorittamaan moduulin testaus mustalaatikkotestauksena.

### 4.1		Moduuli X (kustakin moduulista oma alakohtansa 4.i)

### 4.1.1		Yleiskuvaus 

>Moduulin nimi:
Moduulin tyyppi: (luokka, funktio, prosessi, pakkaus, alijärjestelmä, kirjasto)
Yleiskuvaus: Lyhyt kuvaus moduulista – miksi se on olemassa, mitä se tekee.
Asiakkaat: mitkä/minkä tyyppiset osat järjestelmästä tarvitsevat tämän osan palveluita (yleiskäyttöisen komponentin tapauksessa tämä kohta puuttuu).
Riippuvuudet ja liittymät muihin moduuleihin: Kuvataan lyhyesti, miten moduuli käyttää hyväkseen muita moduuleita ja palveluita ympäristössään (voi usein yhdistää yleiskuvaukseen).

### 4.1.2		Rajapinta yleisesti

>Kuvataan yleisesti moduulin tarjoamat palvelut ja rajapintafunktioiden yhteiset ominaisuudet (esimerkiksi virhetilanteiden käsittely). Joissain tapauksissa kannattaa antaa esimerkkejä moduulin käytöstä kuvaamalla asiakkaan ja moduulin välinen kommunikointi esimerkiksi tapahtumasekvenssikaaviona. Tässä mainitaan myös rajapinnasta mahdollisesti ulos näkyvät vakiot yms. määrittelyt, mahdolliset kapasiteettirajoitukset ja niiden muuttaminen, moduulin tallettamat tilatiedot jne.

### 4.1.3	 	Rajapintafunktiot

>Tässä kuvataan erikseen omassa alakohdassaan jokainen rajapintafunktio:

  * Funktion nimi
  * Funktion parametrit ja paluuarvo
  * Toiminta: mitä funktio tekee
  * Esiehdot: kuvataan, mikä ohjelman tilan pitää olla ennen funktion kutsua.
  * Jälkiehdot: kuvataan, mikä ohjelman tila on funktion kutsun jälkeen (mm. sivuvaikutukset).
  * Virhetilanteet: poikkeukset ja muut virhetilanteet, toiminta kun esiehdot eivät kutsuttaessa pidä paikkaansa

### 4.1.4	 	Moduulin toteutus

Tarvittaessa voidaan antaa ohjeita toteutusta varten, esimerkiksi:
  * Ajatuksia moduulin sisäisten tietorakenteiden toteutuksesta.
  * Ajatuksia käytettävistä algoritmeista. 
  * Tiedossa olevat mahdollisesti uudelleenkäytettävät komponentit.
  * Mikäli moduuli on monimutkainen, voidaan käyttää pseudokoodia, aktiviteettikaavioita yms. Tarvittaessa voidaan tehdä erillinen moduulisuunnitteludokumentti.

### 4.1.5	 	Virhekäsittely

>Kuvataan virheiden ja poikkeusten käsittely moduulitasolla.

## 5.		VALMISOSAT JA ERITYISET TEKNISET RATKAISUT

>Nettisivut pääasiassa rakennettiin itse suhteellisen pohjalta. Toki hyödynsimme esimerkiksi Reactia ja sen kirjastoja. Näistä selkein palikka joka tuli käyttöön, on gallerian karuselli. (Katso tarkemmin linkkiä yllä, luvusta 2.)

>Nettisivulla ei poiketa silmäänpistävästi tavanomaisista nettisivujen toimintatavoista tai teknisistä ratkaisuista. Suojaukset, varmistukset, toipumiset ja siirrettävyys riippuvat sivuston nykyisestä palveluntarjoajasta. Sivuston ylläpito jää toimeksiantajan harteille ja heillä itsellään on back-end puoleen tarvittavat tunnukset.
	
## 6.	HYLÄTYT RATKAISUVAIHTOEHDOT

>Nettisivun ensimmäisiä design versioita ei toteutettu kun DynamiittiOrava ei saanut ehdotelman vaatimia materiaaleja toimeksiantajalta. Sivustolla ei täten ole suuressa visuaalisessa roolissa kuvia toimeksiantajan tuotteista ja toteutuksista.

>Google Analytics oli käytössä (evästeiden kera) sivuston aikaisemmilla versioilla, joten tutkimme kuinka tätä halutaan hyödyntää uudessa toteutuksessa. Toimeksiantaja kuitenkin priorisoi myös itselleen helppoa ylläpitoa joten GA-päivityksiä ja ilmaisen käytön muuttumista ennakoiden, tehtiin päätös jättää tämä työkalu pois sivustolta.

>Nettisivuista on vain suomenkielinen toteutus kun toimeksiantaja ei halunnut vetää puoleensa ulkomaalaisia tilaajia tässä vaiheessa.

## 7.	JATKOKEHITYSAJATUKSIA

>Nettisivuston lataamisajan parantamiseen voisi paneutua.
>Nettisivun värimaailma voisi vaihdella juhlapyhien mukaan.
>Nettisivun hakukoneoptimointia voisi kehittää.
>Nettisivulla voisi olla sarjakuvia.






  
