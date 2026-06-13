# FlowVault — 14 päivän validointisuunnitelma

Tavoite: selvittää **14 päivässä ja 0 eurolla**, onko FlowVaultille kysyntää, ennen kuin
yhtään riviä appikoodia kirjoitetaan. Mittarina ei ole näyttökerrat vaan **sähköpostit** —
view on uteliaisuutta, email on sitoutumislupaus.

Skriptiviittaukset (#1–#15) → [scripts.md](scripts.md).

---

## 1. Postausaikataulu (1 video/päivä)

Strategian logiikka:
- **Päivät 1–2: pelkkää pain point -huumoria.** Laajin samaistumispinta, ei vaadi kontekstia.
  Näillä algoritmi oppii, kenelle sisältö kuuluu (räppärit/lauluntekijät), ja profiiliin
  kertyy katsojia ennen kuin esittäydyt.
- **Päivä 3: esittely (building in public).** Vasta kun joku jo katsoo. Tämä video kerää seuraajat.
- **Päivät 4–13: vuorottelu** kipu → arvo → rakentaminen. Kipu tuo reachin, arvo tuo savet
  ja seuraajat, building in public muuttaa seuraajat odottajiksi (= email-konversio).
- **Päivä 12: kommenttihaaste** ajetaan loppuvaiheessa, kun on jo yleisöä joka vastaa —
  engagement-piikki nostaa myös päivien 13–14 jakelua.
- **Päivä 14: paras toistettuna.** Älä keksi uutta — ota dataa.

| Päivä | Skripti | Tyyppi | Miksi tässä kohtaa |
|---|---|---|---|
| 1 | #3 Finding that one bar | Kipu | Universaalein kipu, vahvin POV-hook — paras avaus kylmälle yleisölle |
| 2 | #2 App-switch death loop | Kipu | FlowVaultin ydinkipu; vahvistaa algoritmille niche-signaalin |
| 3 | #7 Why I'm building this | BIP | Esittely kun ensimmäiset katsojat ovat olemassa → follow-piikki |
| 4 | #12 3-folder system | Arvo | Ensimmäinen save-magneetti; todistaa että tili antaa, ei vain pyydä |
| 5 | #1 Two ads deep | Kipu | Reach-päivä; biittien etsimiskipu pohjustaa päivän 6 ratkaisun |
| 6 | #10 The beat never stops | BIP | Ratkaisu edellisen päivän kipuun — kipu→ratkaisu-pari konvertoi |
| 7 | #13 Teleprompter trick | Arvo | Viikon paras jaettava; teaseraa Training Modea luontevasti |
| 8 | #4 New Recording 247 | Kipu | Viikko 2 auki samaistuttavimmalla formaatilla (näytön kuvaus) |
| 9 | #9 Section Navigator | BIP | Konkreettinen feature-demo — "tää on oikeesti tulossa" -uskottavuus |
| 10 | #14 4-bar loop method | Arvo | Syvin arvovideo; kerää saveja jotka nostavat profiilin painoarvoa |
| 11 | #5 Group chat ghostwriter | Kipu | Kevyt välipäivä; pitää reachin yllä ennen loppukirin haastetta |
| 12 | #11 Tell me what to build | BIP | Kommenttihaaste nyt kun yleisö vastaa — engagement-piikki loppuun |
| 13 | #6 Studio session, no bars | Kipu | Emotionaalisesti vahvin kipuvideo — pohjustaa viimeisen CTA:n |
| 14 | **Paras suorittaja uusiksi** | — | Kuvaa päivien 1–13 parhaiten toiminut video uudella hookilla + kovempi CTA ("first 100 get the keys") |
| varalla | #8 Beat sites feel like 2009 · #15 Check the BPM | BIP · Arvo | Varaskriptit: käytä jos jokin kuvaus epäonnistuu tai jaksat tuplapostata parhaina päivinä (pe–su) |

**Suomenkieliset versiot (#3, #7, #13):** postaa halutessasi samana päivänä "tuplana" tai
omalle FI-tilille. Suomi-rap-yleisö on pieni mutta tiivis — jos FI-versiot vetävät
selvästi paremmin, se on itsessään validointisignaali kotimarkkinasta.

**Postausrytmi:** sama kellonaika joka päivä, suositus klo 18–21 (EET) — EU-ilta ja
Pohjois-Amerikan iltapäivä osuvat päällekkäin. Vastaa jokaiseen kommenttiin ensimmäisen
tunnin aikana — varhainen engagement on TikTokin tärkein jakelusignaali.

---

## 2. Mitä lukuja seurataan

Kirjaa joka ilta taulukkoon (Sheets/Numbers riittää):

| Mittari | Lähde | Miksi |
|---|---|---|
| Videon näyttökerrat (24 h) | TikTok-analytiikka | Jakelun terveys — ei päämittari |
| Katseluprosentti & uudelleenkatselut | TikTok-analytiikka | Hookin laatu; alle 20 % = hook uusiksi |
| Savet + jaot | TikTok-analytiikka | Vahvin laatusignaali algoritmille ja sinulle |
| Seuraajakertymä | TikTok-profiili | Yleisön kasvu — odottajien raaka-aine |
| **Sivun kävijät (uniikit)** | GoatCounter (ks. README vaihe 6) | Funnelin keskikohta |
| **Email-liittymiset** | Formspree-dashboard | **Päämittari** |
| **Konversio-% (emailit / uniikit kävijät)** | laskettu | Kertoo toimiiko sivun viesti |
| Kommenttien laatu | käsin | "when can I get this?" -kommentit ovat kultaa — screenshottaa talteen |

Funneli: **video → profiili → biolinkki → sivu → email.** Jos luvut ovat huonot, korjaa
ensin se funnelin kohta, jossa pudotus on suurin — älä koko pakettia kerralla.

---

## 3. Go / no-go — päivän 14 illalla

Raja-arvojen perustelu: kylmällä TikTok-liikenteellä terve waitlist-sivu konvertoi
tyypillisesti ~10–25 % uniikeista kävijöistä. 40+ emailia kahdessa viikossa nollabudjetilla
riittää 10–15 käyttäjähaastatteluun ja beta-ryhmän siemeneksi — se on tarpeeksi
käynnistämään kehityksen. Alle 15 emailia tarkoittaa, ettei viesti tai kipu pure.

### ✅ GO — aloita MVP-kehitys (blueprintin mukaan)
**Molemmat** täyttyvät:
- **≥ 40 emailia** kerätty, JA
- **konversio ≥ 10 %** (emailit / uniikit kävijät)

…tai ohituskaista: **≥ 75 emailia** konversiosta riippumatta, TAI yksittäinen video
**> 100 k näyttöä** + selvä "when is this out?" -kommenttivirta.

Toimenpide: jatka postaamista (rytmi saa harventua 3×/vko), aloita kehitys blueprintistä,
lähetä waitlistille ensimmäinen "we're building" -sähköposti viikon sisällä.

### 🔁 ITEROI — 14 päivää lisää, yksi muuttuja kerrallaan
Jokin näistä:
- **15–39 emailia** — signaali on olemassa muttei vahva: jatka, tuplaa parhaiten toiminut formaatti.
- **Konversio < 10 % mutta kävijöitä > 300** — jakelu toimii, sivu ei: kirjoita hero-osio
  uusiksi (testaa kärkenä "the beat never stops" vs. "never lose a bar").
- **Konversio ≥ 10 % mutta kävijöitä < 200** — sivu toimii, jakelu ei: ongelma on hookeissa
  ja CTA:ssa, älä koske sivuun. Katso mitkä 3 videota toivat eniten profiilikäyntejä ja tee niistä variaatiot.

### ❌ NO-GO — tapa tai pivotoi
**Kaikki** kolme totta päivänä 14:
- **< 15 emailia**, JA
- **konversio < 5 %**, JA
- yksikään video ei ylittänyt **3 000 näyttöä** (= edes kipusisältö ei resonoi tälle yleisölle)

Toimenpide: älä rakenna appia tämän position varaan. Vaihtoehdot ennen lopullista hautaamista:
1. **Pivot positiointiin:** testaa 14 päivää pelkkää "never lose a bar" -kulmaa (organisointi)
   ilman biittimarkkinapaikkaa — kevyempi lupaus, eri sivun kärki.
2. **Pivot yleisöön:** sama kipu tuottajille ("your beats die in YouTube comments") —
   tuottajapuoli on joka tapauksessa tarpeen ennen julkaisua (Beta Producer -ohjelma).
3. Jos kumpikaan ei herätä mitään → idea hyllyyn, opit talteen, seuraava idea.

### Harmaan alueen sääntö
Jos luvut osuvat kriteerien väliin (esim. 35 emailia ja 9 % konversio): **ITEROI, älä GO.**
Fake doorin koko pointti on välttää rakentamasta heikon signaalin varaan — kahden viikon
lisätesti on halvempi kuin kahden kuukauden turha kehitys.

---

## 4. Päivittäinen 30 min -rutiini

1. **~15 min:** kuvaa ja postaa päivän video (skripti on valmis — älä hio yli 3 ottoa).
2. **10 min:** vastaa kaikkiin kommentteihin (eilen + tänään).
3. **5 min:** kirjaa eilisen videon luvut + Formspree/GoatCounter-tilanne taulukkoon.

Päivänä 7 välitarkistus: jos nollatasolla (ei yhtään emailia, ei yhtään videota > 1 000 näyttöä),
tarkista perusteet ennen jatkamista — onko biolinkki varmasti toiminnassa, aukeaako sivu
puhelimella, toimiiko lomake (testaa itse).
