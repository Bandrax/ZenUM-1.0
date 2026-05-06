# ZenUM - Projekt Status

## O projektu
ZenUM je wellness/mindfulness Android aplikacija razvijena za **Udrugu za unaprjeđenje mentalnog zdravlja "Vrapčići"** iz Slavonskog Broda. Projekt je financiran od strane Ministarstva znanosti, obrazovanja i mladih, u sklopu projekta "Mala škola psihijatrije u zajednici za buduće zdravstvene radnike".

- **Tech stack:** HTML/CSS/JS + Capacitor 8 za Android
- **App ID:** `com.dejansakic.zenum`
- **GitHub:** https://github.com/Bandrax/ZenUM-1.0

## Što je napravljeno

### Inicijalni kod (ZenUM 1.0 snapshot)
- Pushano originalno stanje aplikacije na GitHub kao prvi commit

### Pripreme za Play Store
- [x] Privacy Policy dodana u aplikaciju (in-app modal na "O projektu" ekranu)
- [x] Privacy Policy hostana na GitHub Pages: `https://bandrax.github.io/ZenUM-1.0/privacy-policy.html`
- [x] Canvas animacija optimizirana (zaustavlja se kad nije aktivna - štedi bateriju)
- [x] Naziv konzistentan "ZenUM" svuda (strings.xml)
- [x] Release signing konfiguriran u build.gradle
- [x] Keystore generiran: `zenum-upload-key.jks`
- [x] Signed AAB buildan: `android/app/build/outputs/bundle/release/app-release.aab`
- [x] Play Store listing tekstovi pripremljeni: `playstore/listing-tekstovi.md`
- [x] Feature graphic template: `playstore/feature-graphic.html`
- [x] Feature graphic finalni: `C:\Users\dsaki\Desktop\BannerZaPS.png` (1024x500)
- [x] 8 screenshotova: `C:\Users\dsaki\Desktop\Posao\Projekt ZenUM\SS pics\`
- [x] Ikona 512x512: `android/app/src/main/ic_launcher-playstore.png`
- [x] Release APK za testiranje: `C:\Users\dsaki\Desktop\ZenUM-v1.0.apk`
- [x] Svi materijali kopirani u folder: `C:\Users\dsaki\Desktop\za objavu zenUMa\`
- [x] GitHub Pages aktiviran za privacy policy (branch: main, folder: /docs)

### Google Play Console Account
- [x] Gmail kreiran: `vrapcici.developer@gmail.com`
- [x] Play Console account registriran kao organizacija "Udruga Vrapcici"
- [x] DUNS broj unesen
- [x] Website verifikacija prošla (udrugavrapcici.hr)
- [x] Identity verifikacija prošla (6.5.2026.)
- [x] Phone verifikacija prošla (6.5.2026.)

### Google Play Console - Objava aplikacije (6.5.2026.)
- [x] App kreiran u Play Console (ZenUM, Hrvatski, Free, Health & Fitness)
- [x] Package name registriran: `com.dejansakic.zenum`
- [x] `adi-registration.properties` dodana u assets za proof of ownership
- [x] Store listing popunjen (tekstovi, 8 screenshotova, feature graphic, ikona 512x512)
- [x] Privacy Policy URL postavljen: `https://bandrax.github.io/ZenUM-1.0/privacy-policy.html`
- [x] Content rating (IARC) upitnik završen
- [x] Target audience postavljen na 18+
- [x] Data safety deklaracija popunjena (app ne prikuplja podatke)
- [x] Ads declaration: no advertising ID
- [x] Release AAB uploadan u Production track (verzija 1, v1.0, 3.34 MB)
- [x] 177 zemalja odabrano za distribuciju (18.714 podržanih uređaja)
- [x] **Aplikacija poslana na Google review (6.5.2026.)**

## Što još treba napraviti

### Čeka se:
1. **Google review odobrenje** (obično 1-7 dana za nove aplikacije, poslano 6.5.2026.)

### Nakon odobrenja:
- Aplikacija će automatski biti dostupna na Play Store
- Provjeriti da se listing ispravno prikazuje
- Podijeliti Play Store link s Udrugom Vrapčići

## Važni podaci

### Keystore (ČUVATI - bez ovoga nema updatea!)
| Polje | Vrijednost |
|-------|-----------|
| Datoteka | zenum-upload-key.jks |
| Alias | zenum-upload |
| Lozinka | vrapcici2026 |

### Build komanda
```bash
cd android && cmd.exe //c "set ANDROID_HOME=C:\Users\dsaki\AppData\Local\Android\Sdk&& set JAVA_HOME=C:\Program Files\Android\Android Studio\jbr&& gradlew.bat bundleRelease"
```
AAB output: `android/app/build/outputs/bundle/release/app-release.aab`

### Capacitor sync (nakon promjena u www/)
```bash
cp www/index.html android/app/src/main/assets/public/index.html
cp www/img/* android/app/src/main/assets/public/img/
```

### Kontakt udruge
- Web: https://www.udrugavrapcici.hr/
- Email: info@udrugavrapcici.hr
- Adresa: Naselje Andrije Hebranga 6/30, 35000 Slavonski Brod
- Tel: +385 35 624 074
