# FlowVault — fake door -validointipaketti

Tämä repo sisältää kaiken, mitä FlowVaultin kysynnän validointi vaatii — ei riviäkään appikoodia.

| Tiedosto | Mikä se on |
|---|---|
| [index.html](index.html) | Landing page (julkaisuvalmis GitHub Pagesiin) |
| [styles.css](styles.css) | Sivun tyylit |
| [assets/og-image.png](assets/og-image.png) | Some-jakokuva (1200×630, placeholder — vaihdettavissa) |
| [scripts.md](scripts.md) | 15 TikTok/Shorts-käsikirjoitusta |
| [plan.md](plan.md) | 14 päivän julkaisusuunnitelma + go/no-go-rajat |
| [PROMPT.txt](PROMPT.txt) | Alkuperäinen tehtävänanto (saa poistaa julkaisusta) |

**Julkaisun polku:** 1) esikatsele → 2) Formspree-ID → 3) GitHub Pages → 4) OG-tagit → 5) seuranta → 6) biolinkki. Noin 30 min yhteensä.

---

## 1. Esikatselu paikallisesti

Tuplaklikkaa `index.html` — sivu aukeaa selaimeen sellaisenaan, build-steppiä ei ole.
Testaa myös mobiilileveys: selaimen DevTools (F12) → laitetila (Ctrl+Shift+M) → iPhone-koko.

> Lomake näyttää tässä vaiheessa virheen *"Form isn't connected yet"* — se on tarkoituksella,
> kunnes vaihe 3 on tehty.

## 2. Luo GitHub-repo ja pushaa

Osaat gitin, joten lyhyesti — PowerShellissä tämän kansion juuressa:

```powershell
git init
git add .
git commit -m "FlowVault fake door: landing page + content pack"
```

Luo sitten **github.com → New repository**:
- Nimi esim. `flowvault-landing` (nimi näkyy sivun URL:ssa!)
- **Public** (GitHub Pages on ilmainen vain julkisille repoille free-tierissä)
- Älä lisää README/gitignore-tiedostoja (repo tulee tyhjänä)

```powershell
git remote add origin https://github.com/OMA-KAYTTAJA/flowvault-landing.git
git branch -M main
git push -u origin main
```

## 3. Formspree käyttöön (email-keräys, ~5 min)

Formspreen ilmainen taso riittää testiin: **50 lähetystä / kk**, ei luottokorttia.
Jos waitlist ylittää 50/kk, se on hyvä ongelma — ja jo itsessään validointisignaali.

1. Mene [formspree.io](https://formspree.io) → **Sign up** (ilmainen tili).
2. Vahvista sähköpostisi.
3. Dashboard → **+ New form** → nimeä esim. *FlowVault waitlist*.
4. Formspree näyttää endpointin muotoa:
   `https://formspree.io/f/mqkvabcd` ← tuo 8-merkkinen loppuosa on **form ID**.
5. Avaa `index.html` ja korvaa **molemmat** `PLACEHOLDER_ID`-esiintymät omalla ID:lläsi
   (hero-lomake + sivun alaosan lomake — hae editorissa `PLACEHOLDER_ID`, osumia on 2).
6. Commitoi ja pushaa muutos.

**Testaa:** avaa sivu, syötä oma sähköpostisi → näkyy *"You're on the list"* → kirjaudu
Formspreehen ja varmista, että lähetys näkyy dashboardissa. Ensimmäinen lähetys saattaa
vaatia vahvistuksen Formspreen sähköpostista (reCAPTCHA/verify) — tee tämä testi itse
**ennen** ensimmäisen videon julkaisua.

> Lähetyksen mukana tulee `placement`-kenttä (hero/footer) — siitä näet kumpi lomake
> sivulla konvertoi.

## 4. Julkaise GitHub Pagesiin (~5 min + odotus)

1. Avaa repo github.comissa → **Settings** (ylävalikko) → vasemmasta sivupalkista **Pages**.
2. Kohta **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: **main**, kansio: **/ (root)** → **Save**
3. Odota 1–5 min. Päivitä sivu — yläreunaan ilmestyy osoite:
   `https://OMA-KAYTTAJA.github.io/flowvault-landing/`
4. Avaa osoite **puhelimella** ja testaa lomake vielä kerran oikeassa ympäristössä.

Jatkossa jokainen `git push` päivittää sivun automaattisesti (~1 min viive).

## 5. Viimeistele OG-tagit (some-jakojen esikatselu)

`index.html`:n `<head>`-osiossa on neljä kohtaa, joissa lukee `USERNAME.github.io/REPO`
— korvaa ne oikealla Pages-osoitteellasi (hae editorissa `USERNAME`).

Jakokuva `assets/og-image.png` (1200×630) on mukana placeholder-versiona. Kun haluat
paremman: tee 1200×630 px kuva (esim. Canva, haku "OG image"), tallenna samalla nimellä
samaan paikkaan. Testaa jaon ulkonäkö: [opengraph.xyz](https://www.opengraph.xyz).

## 6. Kävijäseuranta — pakollinen go/no-go-laskentaan (~5 min)

Ilman kävijämäärää et voi laskea konversiota ([plan.md](plan.md) § 3). Kevyin ilmainen
työkalu on [GoatCounter](https://www.goatcounter.com) — ei evästeitä, ei banneria, ilmainen
ei-kaupalliseen käyttöön.

1. Luo tili → valitse "code", esim. `flowvault` → saat osoitteen `https://flowvault.goatcounter.com`.
2. Avaa `index.html`, etsi kommentoitu GoatCounter-lohko `<head>`:in lopusta.
3. Poista kommenttimerkit ja vaihda `OMA-KOODI` → omaksi koodiksesi.
4. Pushaa → käy sivulla → kävijän pitäisi näkyä GoatCounter-dashboardissa ~minuutissa.

Seuraa dashboardista **uniikkeja kävijöitä** (visits), ei sivulatauksia.

## 7. TikTok-biolinkki

1. TikTok → profiili → **Edit profile** → Website → liitä Pages-osoitteesi.
   (Jos kenttä ei ole näkyvissä: vaihda Business-tiliin asetuksista — ilmaista — tai pidä
   linkki bio-tekstissä, kunnes kenttä aukeaa.)
2. Kuvaa [scripts.md](scripts.md):n video #3 ja postaa [plan.md](plan.md):n aikataululla. Päivä 1 alkaa siitä.

---

## Vianetsintä

| Ongelma | Korjaus |
|---|---|
| Pages-osoite antaa 404 | Odota 5 min; tarkista Settings → Pages, että branch on `main` ja kansio `/ (root)`. Tiedoston nimen on oltava täsmälleen `index.html`. |
| Sivu näkyy ilman tyylejä | `styles.css` puuttuu reposta tai polku muuttunut — molempien pitää olla repon juuressa. |
| Lomake: "Form isn't connected yet" | `PLACEHOLDER_ID` on yhä vaihtamatta — muista molemmat lomakkeet (2 esiintymää). |
| Lomake: "Something broke" | Form ID väärin, tai Formspree-lomake vahvistamatta — kirjaudu Formspreehen ja katso formin tila. |
| Formspree ei näytä lähetyksiä | Ensimmäinen lähetys vaatii joskus vahvistuksen sähköpostista; tarkista myös spam-kansio. |
| OG-kuva ei näy jaossa | OG-osoitteiden pitää olla absoluuttisia (`https://...`) — tarkista vaihe 5. Some-palvelut cachettavat: testaa opengraph.xyz:lla. |
| Haluan oman domainin | Toimii myöhemminkin: Settings → Pages → Custom domain. Älä säädä tätä validointivaiheessa — github.io-osoite kelpaa. |

## Mitä tästä EI löydy (tarkoituksella)

Appikoodia, Supabasea, Stripeä tai React Nativea ei ole vielä olemassa. Ne rakennetaan
vasta, jos [plan.md](plan.md):n GO-kriteerit täyttyvät päivänä 14. Sovellusvision
kokonaiskuvaus on erillisessä blueprint-dokumentissa.
