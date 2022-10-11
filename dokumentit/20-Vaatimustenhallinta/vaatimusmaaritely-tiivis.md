# Vaatimusmäärittely

|  |  |
|:-:|:-:|
| Dokumentti | Vaatimusmääritelmä |
| Laatija: | *Taru* |
| Versio: | *0.2* |
| Päivämäärä: | 21.9.2022 |


# 1 Johdanto

## 1.1 Tarkoitus 

Tarkoituksena on luoda päivitetyt verkkosivut, josta yrityksen asiakkaat löytävät tietoa yrityksestä ja voivat jättää yhteydenotto pyynnön. Yhteydenotto lähtee sähköpostina (STMP) toimeksiantajan haluamaan sähköpostiosoitteeseen. 

## 1.2 Määritelmä 

Tämä dokumentti on tarkoitettu ensisijaisesti projektista vastaaville yrityksen työntekijöille, käyttäjille, kehittäjille, testaajille sekä dokumentin kirjoittajille. 

### Määritelmiä 

- Käyttäjä – yrityksen asiakas 
- Ylläpitäjä – henkilö, jolla on oikeudet luoda, muuttaa ja poistaa järjestelmän tietoja 
- Asiakas – yrityksen asiakas 
- SMTP - Simple Mail Transfer Protocol  
- Toimeksiantaja – työn tilaaja 
- Tekijät - Dynamiitti oravan henkilöstö 
- Poweruser - oikeudet antaa käyttöoikeuksia 
- Ylläpito-oikeus – saa lisätä, poistaa ja muokata sisältöä 
- Selaaja – ei saa lisätä, poistaa ja muokata sisältöä vain lukuoikeus 
- SLL - Secure sockets layer 
- CAPTCHA - Completely Automated Public Turing test to tell Computers and Humans Apart 


## 1.3 Rajaukset  

Koska yhteydenotto käyttää SMTP:tä ei tietokantaa tarvita. Rajapintoja/liittymiä ei tehdä muihin järjestelmiin. 

## 1.4 Johtoryhmä 

- Toimeksiantaja – Mika Kuurne 
- Projektipäällikkö - Taru Vuori 

## 1.5 Nimet 

- Ylläpitäjä - Toimitusjohtaja Santeri Kuurne 
- Toimeksiantaja – Tuotantopäällikkö Mika Kuurne 

### Dynamiitti orava, henkilöstö: 

- Projektipäällikkö Taru Vuori 
- Projektihallinta Niko Kauppinen 
- UI-suunnittelija ja frontend Beatrice Raitio 
- UI-suunnittelija ja frontend Miika Toukola 
- Frontend Joni Peltomäki  
- Backend Jose Toivainen 
- Testaaja Jari Blomroos 
- Testaaja Daniela Ferretti

# 2 Toiminnallinen määrittely 

## 2.1 Pakolliset ominaisuudet  

**p01.** Ylläpitäjä pääsee lisäämään, muuttamaan ja poistamaan tietoja ja kuvia, kun tarve tulee. 

**p02.** Yhteystietolomakkeeseen tarvitaan asiakkaan nimi, puhelin, sähköposti ja viesti. 

**p03.** Käytetään SMTP lomakkeentietojen (p02) lähettämiseen.  

## 2.2 Tärkeät ominaisuudet 

**T01.** Linkit Instagramiin ja Facebookiin, josta näkee yrityksen ottamia kuvia ja saa ajantasaistatietoa.  

**T02.** Lomakkeeseen pyydettävät tieto-otsikot on oltava kentän ulkopuolella. 


## 2.3 Valtuutustietojen tasot 

Verkkosivujen luonnin ajaksi projektipäälliköllä on poweruser käyttöoikeudet. Dynamiitti oravan muulla henkilöstöllä on ylläpito-oikeudet. 

## 2.4 Valvonnan seuranta ja arkistointi 

Kävijätietoja ei oteta talteen.  

## 2.5 Sertifiointivaatimukset 

SSL Löytyy ja se on Let’s encryptin kautta.   

## 2.6 Vaatimustenmukaisuus-, laki- tai sääntelyvaatimukset 

Evästeet – Ilmoitus sivulle, että se käyttää evästeitä, hyväksyntä ja muokkaukset evästeisiin tai tarjotaan vaihtoehtoa hyväksyä vain pakolliset evästeet. Meillä ei ole tarvetta evästeilmoitukselle, jos ei ole tiedon keräämistä. 

Vasteaika katso **3.3 Vasteaika **

## 2.7 Varmuuskopiointi ja palautus 

Palnetta.fi löytyy palvelu varmuuskopiointia varten. 


# 3 Ei-toiminnallinen määrittely 

## 3.1 Suorituskyky 

### Suorituskykyyn vaikuttavat asiat: 

- Laite millä sivua käytetään 
- Verkkoyhteys 
- Datan määrä 

Suorituskykyyn liittyvät tiedot löytyvät **3.2 Toimintavarmuus, 3.3 Vasteaika, 3.4 Saavutettavuus, 3.8 Ympäristö, 3.10 Käytettävyys,**  

## 3.2 Toimintavarmuus 

Verkkosivun on toimittava kun 50 henkilöä käyttää sivua yhtä aikaa 30 minuutin ajan. 

## 3.3 Vasteaika  

Vasteaika saa olla korkeintaan 2 sekuntia sivuston valinnan jälkeen. 

## 3.4 Saavutettavuus 

Sivun sisällön tulisi olla saavutettavissa ainakin yhden käyttäjän aistin avulla. Kuvat ja ei-tekstisisältöiset kuvailtaisiin vaihtoehtoisesti tekstillä näkövammaisia käyttäjiä varten. Sivun tulisi olla ymmärrettävää ja selkeää kieltä. Verkkosivun tulisi toimia eri alustoilla, selaimilla ja laitteilla, mukaan lukien avustava teknologia. Tekstin ja taustavärin konstraktin pitää olla selkeä ja olla vähintään saatavuusvaatimuksen tasoa 4,5-1 vaatimustaso AA. 

Lomakekentät on oltava selkeästi rajatut. 

## 3.5 Palautuvuus 

Palautettavuus hyvä. Planeetta.fi palvelu hoitaa. 

## 3.6 Kapasiteetti 

Planeetta.fi tulee tieto. Tämä ominaisuus ilmaisee järjestelmän tallennuskapasiteetin, joka riippuu sen tyypistä ja ominaisuuksista.  

## 3.7 Ympäristö 

### Asiat, jotka vaikuttavat käytettävyyteen: 

- Sähkökatkot 
- Luonnonkatastrofit, ilmastonmuutos 
- Tietomurto/ kyberhyökkäys

## 3.8 Yhteensopivuus 

Pitää toimi A browser which supports React/JavaScript, bacend: Flask 

## 3.9 Käytettävyys 

Käytettävyys sisältää osia **3.4 Saavutettavuus. ** 

Sivun käytettävyys tulisi olla helppoa, helposti muistettava ja miellyttävä. 

Sivun tulisi olla ymmärrettävää ja selkeää kieltä. Sivua tulisi pystyä käyttämään näppäinkomennoilla. Virheilmoitus esim. lomakkeen syötössä pitäisi ilmaista myös toisella tavalla kuin pelkästään punaisella reunalla (puna-vihersokeus).  

Käytettävyystestaus on suoritettava ennen sivuston julkaisua. 

## 3.10 Tietoturva 

SSL-sertifikaatti löytyy asiakkaan käyttämältä web hosting palvelusta. Katso kohta **2.6 Sertifiointivaatimukset.**  

Sähköpostin lähettämistä varten tulee Captcha tai jokin vastaava. 




