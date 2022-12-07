# Ohjelmistoarkkitehtuuri

|  |  |
|:-:|:-:|
| Dokumentti | Ohjelmiston arkkitehtuuri kuvaus |
| Laatija: | DynamiittiOrava |
| Versio: | 3.5 |
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
 * https://www.framer.com/motion/

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

> Kukin kehittäjä käytti omalla koneellaan sopivia kehitystyökaluja, erityisesti Visual Studio Code.

## 4.		MODUULI/LUOKKA/PROSESSIKUVAUKSET

> Projektimme pyrki olemaan selkeä ja helppokäyttöinen nettisivusto. Tässä luvussa kuvaillaan sivuston toimintaa ja kosketetaan myös visuaaliseen ilmeeseen. Nämä asiathan ovat myös selkeästi ja nopeasti nähtävissä ja koettavissa kun menee katsomaan sivua, joten tämä kuvaus pyrkii tukemaan tuota kokemusta ja vahvistamaan, että mahdolliset huomiot sivusta ovat tarkoituksellisia.
> Kommentoiti visuaaliseen puoleen voisi vielä kehittää, mutta sanottakoon tässä, että sivulla on panostettu responsiivisuuteen tämän aspektin kohdalla.

### 4.1		React-komponentit

### 4.1.1	 Yleiskuvaus

>Sivusto koostuu useammasta komponentista jotka tuodaan yhteen luomaan koko sivusto. Vaikka lopputulos on suhteellisen yksinkertainen, on taustalla käytetty monenlaista ja yleistä metodologiaa.

### 4.1.2 Frontpage

>Tämän komponentin kävijä kohtaa ensimmäisenä sivulla. Erityisesti täältä löytyy myös nappi jolla kävijä voi suoraan navigoida Ota Yhteyttä osioon.

### 4.1.3 Nav-valikko

>Tästä komponentista käyttäjä voi nopeasti navigoida sivun osien välillä. Osiot joihin on linkit ovat Palvelumme, Yrityksemme sekä Ota Yhteyttä -osio. Näiden lisäksi on kuvakkeet toimeksiantajan sosiaalisen median tileille Instagramiin ja Facebookiin.

### 4.1.4 Palvelumme

>Tässä osiossa näkyy toimeksiantajan tarjoamia palveluita nopeallakin katsastuksella.
>Teknisellä puolella tästä osiosta voisi irroittaa omaksi komponentiksi Tuotteet-osion, ja tähän olemassa olevaan komponenttiin jäisi näiden alle jäävien komponenttien järjestely tai hallinnointi.
>Osion alaosassa on nappi joka paljastaa Gallerian näkyviin, tai piilottaa sen jos se on jo näkyvissä.

### 4.1.5 Galleria

>Tämä palikka näyttää kävijälle kuvia toimeksiantajan aikaisemmista tuotoksista. Galleria pyörii automaattisesti kuvien välillä. Kuvat ovat järjestetty aakkosjärjestykseen tiedostonimen perusteella.

### 4.1.6 Asiakkaitamme

>Tässä kappaleessa on useampi toimeksiantajan asiakkaita listattuna.

### 4.1.7 Yrityksemme

>Tässä pykälässä kuvaillaan toimeksiantajan yritystä ja toimintaa.

### 4.1.8 Ota Yhteyttä

>Täällä näkyy toimeksiantajan yhteystiedot.

### 4.1.2		Rajapinta yleisesti

>Yhteisiä osiota komponenttien välillä löytyy CSS-määrittelyistä ja nappien toiminnallisuudesta. Sivustoa luodessa pyrittiin luomaan yhtenevä tunne eri komponenttien välillä.

### 4.1.3	 	Rajapintafunktiot

>Sivujen taustalla toimii muutama funktio ja React-koukkuja.

* handleClick() vuoroin paljastaa ja piilottaa Gallerian. Koukut tässä palikassa pitävät kirjaa siitä, kumpi tila sivustolla on aktiivinen.

### 4.1.4	 	Moduulien toteutus

>Komponentit ovat omissa tiedostoissaan ja jokaisella on myös oma CSS-tiedostonsa erityismääritteitään varten. Jaettuja resursseja komponenttien välillä ovat Animations.js ja GlobalStyle.js.

### 4.1.5	 	Virhekäsittely

>Katso luku 3.4.

## 5.		VALMISOSAT JA ERITYISET TEKNISET RATKAISUT

>Nettisivut pääasiassa rakennettiin itse suhteellisen pohjalta. Toki hyödynsimme esimerkiksi Reactia ja sen kirjastoja. Näistä selkein palikka joka tuli käyttöön, on gallerian karuselli. (Katso tarkemmin linkkiä yllä, luvusta 2.) Käytimme myös Framer Motion -animaatioita ja Font Awesome -kuvakkeita.

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






  
