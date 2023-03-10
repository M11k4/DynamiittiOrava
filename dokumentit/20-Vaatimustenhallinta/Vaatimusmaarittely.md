# Vaatimusmäärittely

|  |  |
|:-:|:-:|
| Dokumentti | Vaatimusmääritelmä |
| Laatija: | *Taru* |
| Versio: | *0.4* |
| Päivämäärä: | 21.9.2022 |


# 1 Johdanto

## 1.1 Tarkoitus 

Tarkoituksena on luoda päivitetyt verkkosivut, josta yrityksen asiakkaat löytävät tietoa yrityksestä ja voivat ottaa yhteyttä yritykseen puhelimitse sekä sähköpostitse.  

## 1.2 Määritelmä 

Tämä dokumentti on tarkoitettu ensisijaisesti projektista vastaaville yrityksen työntekijöille, käyttäjille, kehittäjille, testaajille sekä dokumentin kirjoittajille. 

### Määritelmiä 

- Käyttäjä – yrityksen asiakas 
- Ylläpitäjä – henkilö, jolla on oikeudet luoda, muuttaa ja poistaa järjestelmän tietoja 
- Asiakas – yrityksen asiakas   
- Toimeksiantaja – työn tilaaja 
- Tekijät - Dynamiittioravan henkilöstö 
- Poweruser - oikeudet antaa käyttöoikeuksia 
- Ylläpito-oikeus – saa lisätä, poistaa ja muokata sisältöä 
- Selaaja – ei saa lisätä, poistaa ja muokata sisältöä vain lukuoikeus 
- SLL - Secure sockets layer 


## 1.3 Rajaukset  

Rajapintoja/liittymiä ei tehdä muihin järjestelmiin. 

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


## 2.2 Tärkeät ominaisuudet 

**T01.** Linkit Instagramiin ja Facebookiin, josta näkee yrityksen ottamia kuvia ja saa ajantasaistatietoa.  


## 2.3 Valtuutustietojen tasot 

Verkkosivujen luonnin ajaksi projektipäälliköllä on poweruser-käyttöoikeudet. Dynamiittioravan muulla henkilöstöllä on ylläpito-oikeudet. 

## 2.4 Valvonnan seuranta ja arkistointi 

Kävijätietoja ei oteta talteen.  

## 2.5 Sertifiointivaatimukset 

SSL Löytyy ja se on Let’s encryptin kautta.   

## 2.6 Vaatimustenmukaisuus-, laki- tai sääntelyvaatimukset 

Evästeet – Ilmoitus sivulle ei tarvita. Sivulla ei ole evästeitä.

Vasteaika katso **3.3 Vasteaika **


# 3 Ei-toiminnallinen määrittely 

## 3.1 Suorituskyky 

### Suorituskykyyn vaikuttavat asiat: 

- Laite, millä sivua käytetään 
- Verkkoyhteys 
- Datan määrä 

Suorituskykyyn liittyvät tiedot löytyvät **3.2 Toimintavarmuus, 3.3 Vasteaika, 3.4 Saavutettavuus, 3.8 Ympäristö, 3.10 Käytettävyys,**  

## 3.2 Toimintavarmuus 

Verkkosivun on toimittava kun 50 henkilöä käyttää sivua yhtä aikaa 30 minuutin ajan. 

## 3.3 Vasteaika  

Vasteaika saa olla korkeintaan 2 sekuntia sivuston valinnan jälkeen. 

## 3.4 Saavutettavuus 

Sivun sisällön tulisi olla saavutettavissa ainakin yhden käyttäjän aistin avulla. Kuvat ja ei-tekstisisältöiset kuvailtaisiin vaihtoehtoisesti tekstillä näkövammaisia käyttäjiä varten. Sivun tulisi olla ymmärrettävää ja selkeää kieltä. Verkkosivun tulisi toimia eri alustoilla, selaimilla ja laitteilla, mukaan lukien avustava teknologia. Tekstin ja taustavärin konstraktin pitää olla selkeä ja olla vähintään saatavuusvaatimuksen tasoa 4,5-1 vaatimustaso AA. 


## 3.5 Kapasiteetti 

Planeetta.fi:stä tulee tieto. Tämä ominaisuus ilmaisee järjestelmän tallennuskapasiteetin, joka riippuu sen tyypistä ja ominaisuuksista.  

## 3.6 Ympäristö 

### Asiat, jotka vaikuttavat käytettävyyteen: 

- Sähkökatkot 
- Luonnonkatastrofit, ilmastonmuutos 
- Tietomurto/ kyberhyökkäys

## 3.7 Yhteensopivuus 

Pitää toimia selaimella, joka tukee Reactia ja JavaScriptiä.

## 3.8 Käytettävyys 

Käytettävyys sisältää osia **3.4 Saavutettavuus. ** 

Sivun käytettävyys tulisi olla helppoa, helposti muistettavaa ja miellyttävää. 

Sivun tulisi olla ymmärrettävää ja selkeää kieltä. Sivua tulisi pystyä käyttämään näppäinkomennoilla. Virheilmoitus esim. lomakkeen syötössä pitäisi ilmaista myös toisella tavalla kuin pelkästään punaisella reunalla (puna-vihersokeus).  

Käytettävyystestaus on suoritettava ennen sivuston julkaisua. 

## 3.9 Tietoturva 

SSL-sertifikaatti löytyy asiakkaan käyttämästä web hosting -palvelusta. Katso kohta **2.6 Sertifiointivaatimukset.**  


# 4 Kohderyhmät

## 4.1 Kävijäprofilointi

Kävijäprofilointi voidaan käsittää tarvetta etsiviin ihmisiin. Tämä voidaan jakaa kahteen eri ryhmään.

- Yritysasiakkaat
- Yksityiset asiakkaat

Jokainen kävijä on mahdollinen asiakas. 

## 4.2 Yritysasiakkaat

Yritysasiakkaat hankkivat palveluita pääsääntöisesti oman yritystoimintansa tueksi. Yritysasiakkailla tilatun tuotteen käyttötarkoitus on markkinoida omia tuotteita tai palveluita. Yritysasiakkaat saattavat tilata myös huomattavasti suurempia määriä, kuin yksityiset asiakkaat. Tietenkin löytyy myös poikkeuksia.

## 4.3 Yksityiset asiakkaat

Yksityiset asiakkaat hankkivat palveluita yksityiselämään esimerkiksi koristeellisista syistä, kuten erilaiset kutsukortit, veneiden teippaukset jne. Voi löytyä tottakai poikkeuksia. 


