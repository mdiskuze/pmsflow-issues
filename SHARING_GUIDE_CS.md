# PMS Flow - Návod na lokální sdílení (.pmsshare)

Tento návod popisuje, jak v praxi funguje lokální sdílení jen pro čtení pro scénáře:
- žena -> partner
- dcery -> matka (včetně více dcer)

Funkce je plně lokální, bez cloudu a bez účtu.

---

## 1. Co tohle sdílení dělá

- Odesílatel vytvoří soubor se snapshotem: `.pmsshare`.
- Příjemce soubor naimportuje do sekce **Sdílené profily**.
- Importovaný profil je oddělený od vlastních záznamů.
- Příjemce sdílená data vidí, ale neupravuje původní záznamy odesílatele.

---

## 2. Typické scénáře

### A) Žena sdílí partnerovi

Cíl: partner vidí kontext cyklu (odhad další menstruace, základní přehled), ale nic neupravuje.

Doporučené nastavení exportu:
- Zahrnout příznaky: volitelné (ON pokud se na tom oba shodnou)
- Zahrnout poznámky: většinou OFF (kvůli soukromí)

### B) Dcery sdílí matce

Cíl: matka vidí více sdílených profilů v jedné aplikaci.

Doporučený postup:
- Každá dcera exportuje ze svého zařízení/profilu.
- Matka naimportuje každý soubor do Sdílených profilů.
- Matka profily hned přejmenuje (např. „Anna“, „Eliška“).

---

## 3. Kroky odesílatele (telefon dcery/ženy)

1. Otevři `PMS Flow -> Sdílené profily`.
2. Klikni na `Exportovat sdílený snapshot (.pmsshare)`.
3. Volitelně nastav:
   - alias profilu,
   - zahrnout příznaky,
   - zahrnout poznámky.
4. Klikni na export.
5. Otevře se Android sdílecí nabídka. Vyber způsob přenosu.

Běžné způsoby přenosu:
- Nearby Share / Quick Share (Android -> Android)
- příloha v chatu (WhatsApp, Signal, Telegram)
- příloha e-mailu
- nahrání do Drive/Soubory a poslání odkazu
- Bluetooth přenos (starší zařízení)
- kopie přes USB do PC a potom do cílového telefonu

---

## 4. Kroky příjemce (telefon partnera/matky)

1. Ulož `.pmsshare` soubor lokálně (pokud přišel přes chat/e-mail).
2. Otevři `PMS Flow -> Sdílené profily`.
3. Klikni na `Importovat sdílený snapshot (.pmsshare)`.
4. Vyber soubor.
5. Potvrď import.
6. Otevři detail profilu, případně profil přejmenuj.
7. Volitelně nastav vztah (Partner / Dcera / Otec / Rodina / Jiné).

---

## 5. Workflow pro více dcer

Doporučené nastavení na telefonu matky:

1. Naimportovat první snapshot dcery.
2. Hned profil přejmenovat (např. „Dcera - Anna“).
3. Opakovat pro ostatní dcery.
4. U každého profilu nastavit vztah (doporučeno).
5. Používat filtr v seznamu Sdílených profilů.
6. Nastavit vhodné řazení (aktualizace/název/vztah).
7. Volitelně zapnout/vypnout:
   - **Uchovat historii snapshotů**
     - OFF: nový snapshot od stejné osoby aktualizuje existující profil.
     - ON: každý nový snapshot zůstane jako samostatná historická položka.

---

## 6. Jak fungují aktualizace souborů

- Každý odesílatel má ve snapshotu stabilní ID odesílatele.
- Když je `Uchovat historii snapshotů` OFF, novější snapshot od stejného odesílatele aktualizuje stávající profil.
- Když je ON, každý import se uloží jako nový záznam.

---

## 7. Poznámky podle verze Androidu

### Android 13+ (API 33+)
- Runtime oprávnění notifikací nemá vliv na sdílení souborů.
- Výběr/import funguje přes systémový dokument picker.
- Nearby Share / Quick Share bývá dostupný podle zařízení.
- `.pmsshare` lze otevřít i přímo do PMS ze Soubory/Drive/sdílecí nabídky (pokud vybereš PMS).

### Android 10-12
- Standardní chování sdílecí nabídky i dokument pickeru.
- Scoped storage tento flow neblokuje (aplikace používá content URI).

### Android 8-9
- PMS Flow je stále podporuje (min SDK 26).
- Sdílecí cíle se mohou lišit podle výrobce/OEM aplikací.
- Když přímé sdílení nefunguje dobře, použij e-mail nebo USB přenos.

### Rozdíly mezi výrobci (Samsung/Xiaomi/...)
- Názvy v share sheetu se liší (`Quick Share`, `Nearby Share`, vlastní správce souborů).
- Některé chat aplikace mohou přílohu změnit/poškodit; při problému poslat znovu přes Soubory/Drive/e-mail.

---

## 8. Soukromí a bezpečnost

- Pokud není potřeba, nech `Zahrnout poznámky = OFF`.
- Pro partner režim zvaž i `Zahrnout příznaky = OFF`.
- Profily přejmenuj, ať se nepletou.
- Staré nepotřebné sdílené profily smaž.
- Nesdílej snapshoty ve veřejných skupinách/kanálech.

---

## 9. Řešení problémů

### „Neplatný .pmsshare soubor"
- Ověř, že soubor má příponu `.pmsshare`.
- Udělej nový export a pošli znovu.

### „Checksum mismatch" / import odmítnut
- Soubor byl poškozen nebo upraven při přenosu.
- Požádej odesílatele o nový export a pošli jiným kanálem.

### Profil se neaktualizoval podle očekávání
- Zkontroluj přepínač `Uchovat historii snapshotů`.
- OFF = aktualizace existujícího profilu, ON = nová položka historie.

### Importovaný profil není vidět
- Otevři `Sdílené profily` ve spodní navigaci.
- Zkontroluj filtr (vyčisti text filtru).

### Špatné pořadí profilů v seznamu
- V sekci Sdílené profily klikni na řazení a vyber požadované pořadí.

---

## 10. Rychlý checklist pro reálné použití

- odesílatel exportoval `.pmsshare`
- příjemce importoval přes formát Sdílený snapshot
- profil je vidět v Sdílených profilech
- profil je přejmenovaný pro přehled
- je nastaven vztah
- je vybrané požadované řazení
- nastavení historie je ověřené
- nový snapshot byl jednou otestovaný (update nebo historie)
