## 1. Sivusto ja sen käyttäjät

- Toiminnot: 
  Sivustolla kaikki informaatio yhdellä samalla sivulla. Navigaatio (ylös-alas) toimii hiirellä tai nuolinäppäimillä. 
  Sivuston alaosasta pääsee linkkien kautta yrityksen Instagramiin ja Facebookiin. 
  Ainoa erillinen toiminto on yhteydenottolomake, johon potentiaalinen asiakas jättää nimensä ja sähköpostiosoitteensa.


- Kohderyhmä/ end-user:
  Sivuston kohderyhmä on Grafiteamin asiakkaat ja potentiaaliset asiakkaat. 
  Asiakkaita ovat yritykset, jotka tarvitsevat mainostauluja ja muita painopalveluita oman yrityksensä markkinointia varten.

        
## 2. Testaustrategia

**Functional testing** (suoritetaan manuaalisesti)
   * Sivulla navigointi
   * Linkkien toimivuus
   * Yhteydenottolomakkeen toimivuus
   * Käytettävyystestaus (testiryhmä, 6 henkilöä)

   

**Non-Functional testing** (suoritetaan testityökaluilla ja manuaalisesti)
   * Sivuston responsiivisuus (manuaalisesti, Google ja Safari developer tool)
   * Selaimien ja laitteiden yhteensopivuus
   * API-testaus (Postman)
   * Suorituskykytestaus (Postman)
   * Saavutettavuustestaus (Accessibilitychecker)

        
## 3. Testauksen tavoitteet

   Testauksella varmistetaan, että:
   - kaikki toiminnot toimivat halutulla tavalla
   - sivusto on responsiivinen
   - sivusto on suorituskyvyltään riittävä (ks. vaatimusmääritelmä)
   - sivusto täyttää EU:n saavutettavuuskriteerit

        
## 4. Testauksen kriteerit

   Testausta jatketaan, kunnes kohdassa 3 mainitut tavoitteet ovat täyttyneet ja koodin työstäminen on loppunut. 
   Jos koodiin tehdään vielä muutoksia, suoritetaan jatkotestausta, kunnes sivusto on valmis ja testausvaatimukset täyttyvät. 
   Kun vaatimusmäärittelyssä ja testauksen tavoitteissa mainitut kohdat on testattu, ominaisuudet todettu toimiviksi/riittäviksi ja koodin työstäminen lopetettu, testaus päättyy.

        
## 5. Resurssit (testaajat, työtunnit, testiryhmä)

| Testaaja | Tunnit | Testiryhmä? |
|:-:|:-:|:-:|
| Jari Blomroos | TBA | TBA |
| Daniela Ferretti | TBA | TBA |

 
## 6. Testausympäristöt (selaimet, laitteet ja muut muuttujat)

   Testaus suoritetaan yleisimmiten käytetyillä selaimilla. Varmistamme toimivuuden siis [Chrome, Edge, Firefox, Safari ja Opera selaimilla.](https://en.wikipedia.org/wiki/Usage_share_of_web_browsers#Summary_tables) 
   Tämän lisäksi varmistamme myös, että sivusto pyörii laitteilla, joita asiakkaat/käyttäjät käyttävät sivustolla käymiseen. Tarkoittaen pöytäkoneita, kannettavia ja puhelimia (Android&iOS) mutta pääasiallinen keskittyminen on Windows, Linux ja Mac koneissa. 
        
## 7. Laadi Road Map prosessille

        
## 8. Dokumentaatio (miten ja millä dokumentoidaan?)

   GitLab-ympäristö tarjoaa projektillemme tarpeelliset työkalut dokumentointiin (issues, milestones, test cases). Pyrimme toimimaan [CI/CD](https://en.wikipedia.org/wiki/CI/CD) menetelmän mukaisesti.
