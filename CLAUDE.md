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

### Google Play Console Account
- [x] Gmail kreiran: `vrapcici.developer@gmail.com`
- [x] Play Console account registriran kao organizacija "Udruga Vrapcici"
- [x] DUNS broj unesen
- [x] Website verifikacija prošla (udrugavrapcici.hr)
- [ ] **Identity verifikacija** - čeka se Google odobrenje (uploadana osobna iskaznica, traje 1-3 dana)
- [ ] **Phone verifikacija** - otključava se nakon identity verifikacije

## Što još treba napraviti

### Čeka se:
1. **Google identity verifikacija** (1-3 dana od 5.5.2026.)
2. **Phone verifikacija** (nakon identity)

### Kad verifikacija prođe:
1. **Kreirati app** u Play Console ("Create app")
   - Naziv: ZenUM
   - Jezik: Hrvatski
   - App type: App (ne game)
   - Free
2. **Popuniti Store listing**
   - Tekstovi su u `playstore/listing-tekstovi.md`
   - Upload screenshotova (8 komada iz SS pics foldera)
   - Upload feature graphic (`BannerZaPS.png`)
   - Upload ikone 512x512
   - Privacy Policy URL: `https://bandrax.github.io/ZenUM-1.0/privacy-policy.html`
3. **Content rating** upitnik (IARC)
4. **Target audience** - odabrati 18+
5. **Upload AAB** u Production track
6. **Submit za review**

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
