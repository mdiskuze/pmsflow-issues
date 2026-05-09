# PMS Flow

A privacy-first menstrual cycle tracker for Android. Local data only,
no cloud sync, no ads, no paywalls.

This repository is **not the source code** — it's the public space for
release downloads, issue reports, feedback, and the user guide.

➡️ **[Latest release](../../releases/latest)** — install the APK directly,
or [open an issue](../../issues/new) to report a bug or suggest a feature.

---

## English

### What PMS Flow does

- **Tracks your cycle.** Log periods (with start and optional end), flow
  intensity per day, symptoms (cramps, mood, energy, mid-cycle pain,
  cervical mucus, basal body temperature, free-form notes), and pregnancies.
- **Predicts the next period and ovulation window.** The prediction is
  shown with a confidence level and an honest plus/minus range — wider
  for predictions further into the future.
- **Pinpoints ovulation when you log fertility signals.** When you log
  mid-cycle pain, fertile-type cervical mucus, or basal body temperature
  near the predicted ovulation, the app uses your observation to sharpen
  the day. You don't have to log any of these — they're optional.
- **Calendar with colour-coded days.** Period days, predicted period,
  fertile window, ovulation day, and pregnancy days are all distinct.
  A gradient on the fertile window shows day-by-day fertility.
- **Statistics and insights.** See your average cycle and period length,
  cycle variability, and trends over time. The full multi-year history
  stays visible — only the prediction model itself focuses on your most
  recent cycles, so it reacts faster when your cycle changes.
- **Notifications.** Optional reminders for period start, fertile window,
  symptom logging, and a once-per-cycle late-period nudge.
- **Backup and restore.** Export to CSV or JSON; import the same files
  back. Your data, your control.
- **Read-only sharing with a partner or family.** Generate a `.pmsshare`
  snapshot they can open in their own app — no account, no cloud.
  The receiver sees your shared data but can't change it.
- **App lock.** Optional biometric or PIN lock that triggers when the app
  goes to the background.

### Privacy

PMS Flow keeps everything **on your device**. No analytics, no ads, no
third-party tracking, no cloud sync. The app does not need network
permission for its core features — the only network request it ever
makes is the optional version-update check against this public release
list.

The on-device database is encrypted at rest on Android 15 and below.
On Android 16+, encryption is currently disabled because the underlying
library is not yet compatible with the new platform — the file is
still in the app's private storage where only this app can read it.

### How to report something

Bug, feature idea, usability feedback — open an issue here. When
reporting a bug, include:

- App version (for example `1.3.0`)
- Device model
- Android version
- Steps that lead to the problem
- What you expected to happen
- What actually happened
- A screenshot or short screen recording, if you can attach one

**Please don't paste personal data in issues** (health information,
names, emails, exported records). If you want to share a backup file
for diagnosis, we'll arrange a private channel.

### Security

Found something that looks like a security or privacy hole? Don't post
it publicly — contact the maintainer privately first.

---

## Česky

### Co PMS Flow umí

- **Sleduje tvůj cyklus.** Zaznamenávej menstruaci (začátek, volitelný
  konec), intenzitu krvácení po dnech, symptomy (bolesti, nálada,
  energie, ovulační bolest uprostřed cyklu, cervikální hlen, bazální
  tělesná teplota, vlastní poznámky) a těhotenství.
- **Předpovídá další menstruaci a okno ovulace.** Předpověď je zobrazena
  s úrovní jistoty a poctivým rozptylem ± dní — pro vzdálenější
  předpovědi širší.
- **Zpřesňuje den ovulace podle tvých záznamů plodnosti.** Když
  zaznamenáš ovulační bolest, plodný typ cervikálního hlenu nebo
  bazální tělesnou teplotu v okolí předpovídané ovulace, aplikace tu
  konkrétní událost využije k zúžení okna na konkrétní den. Žádný
  z těchto záznamů není povinný — jsou volitelné.
- **Kalendář s barevně odlišenými dny.** Menstruační dny, předpovídaná
  menstruace, plodné okno, den ovulace a dny těhotenství jsou
  rozlišitelné. Barevný gradient v plodném okně ukazuje pravděpodobnost
  otěhotnění po jednotlivých dnech.
- **Statistiky a přehledy.** Průměrná délka cyklu, délka menstruace,
  variabilita, trendy v čase. Plnou víceletou historii máš stále
  viditelnou — predikční model se ale zaměřuje na nedávné cykly, takže
  rychleji reaguje, když se ti cyklus mění.
- **Notifikace.** Volitelné připomenutí menstruace, plodného okna,
  záznamu symptomů a jednorázové upozornění při zpožděné menstruaci.
- **Záloha a obnova.** Export do CSV nebo JSON; import stejných souborů
  zpět. Tvá data, tvoje kontrola.
- **Sdílení s partnerem/rodinou jen ke čtení.** Vygeneruješ snímek
  `.pmsshare`, který si otevřou ve své vlastní aplikaci — bez účtu,
  bez cloudu. Příjemce vidí sdílená data, ale nemůže je změnit.
- **Zámek aplikace.** Volitelné odemykání otiskem prstu / obličejem nebo
  PINem při návratu z pozadí.

### Soukromí

PMS Flow drží všechno **u tebe v telefonu**. Žádná analytika, žádné
reklamy, žádný tracking třetích stran, žádná cloudová synchronizace.
Aplikace pro svou hlavní funkci nepotřebuje připojení k internetu —
jediné, co kdy na síť posílá, je volitelná kontrola dostupnosti nové
verze proti tomuto veřejnému seznamu.

Databáze v telefonu je na Androidu 15 a starším šifrovaná. Na
Androidu 16+ je šifrování zatím vypnuté, protože použitá knihovna
není kompatibilní s novou platformou — soubor je nicméně stále uložen
v privátním úložišti aplikace, kam má přístup jen ona.

### Jak něco nahlásit

Chyba, nápad, zpětná vazba — otevři issue tady. Když hlásíš chybu,
přidej prosím:

- Verzi aplikace (např. `1.3.0`)
- Model telefonu
- Verzi Androidu
- Postup, který k problému vede
- Co jsi očekávala
- Co se ve skutečnosti stalo
- Screenshot nebo krátké video, pokud je můžeš přiložit

**Prosím nelep do issue osobní údaje** (zdravotní informace, jména,
e-maily, exportované záznamy). Pokud potřebuješ poslat zálohu pro
diagnostiku, domluvíme privátní kanál.

### Bezpečnost

Pokud najdeš něco, co vypadá jako bezpečnostní nebo soukromá díra,
nepiš to prosím veřejně — kontaktuj nejdřív tvůrce soukromou cestou.
