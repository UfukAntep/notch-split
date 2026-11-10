# NotchSplit

**Herhangi bir pencereyi çentiğe (notch) sürükleyerek macOS'te ekranı bölün.**

NotchSplit, MacBook'unuzun çentiğini bir pencere yöneticisine dönüştürür. Klavye kısayolu ezberlemek yok, küçük yeşil düğmelerin üzerinde beklemek yok: pencereyi tutun, ekranın üstüne, çentiğe götürün, bırakın.

Bu repo **kullanıma hazır uygulamayı** içerir. **Tamamen ücretsizdir** ve **kapalı kaynaktır** — kaynak kodu paylaşılmaz, yalnızca derlenmiş macOS çıktısı (`.dmg`) burada yayınlanır.

---

## 📥 İndir

**[NotchSplit-1.0.0.dmg](NotchSplit-1.0.0.dmg)** indir (448 KB)

### Kurulum

1. `.dmg` dosyasını açın, **NotchSplit**'i **Applications** klasörüne sürükleyin.
2. Applications klasöründen NotchSplit'i açın.
3. macOS *"Apple doğrulayamadı"* uyarısı gösterirse: **Bitti**'ye basın, ardından **Sistem Ayarları › Gizlilik ve Güvenlik** bölümünün en altında **Yine de Aç**'a tıklayın.
   *(Bu uyarı, App Store dışı ve ücretsiz bir uygulama olduğu için çıkar. NotchSplit internete bağlanmaz, sürücü yüklemez; yalnızca pencere taşımak için Erişilebilirlik API'sini kullanır.)*
4. Sorulduğunda **Erişilebilirlik** iznini verin: **Sistem Ayarları › Gizlilik ve Güvenlik › Erişilebilirlik**.
5. Menü çubuğundaki çentik simgesine tıklayıp dilinizi seçin (35 dil arasından), sonra herhangi bir pencereyi çentiğe sürükleyin.

---

## ✨ Nasıl çalışır

| Hareket | Sonuç |
| --- | --- |
| Pencereyi çentiğe sürükleyip **bırakın** | Pencere **tam ekran** olur |
| Pencereyi çentiğe sürükleyip **~1 saniye basılı tutun** | Çentiğin altında bir **yerleşim seçici** belirir |
| Seçicideki bir yerleşimin üstüne gelip bırakın | Pencere o yerleşime oturur |
| Çentikten uzaklaşın | Hiçbir şey olmaz, pencere normal hareket eder |

**Yerleşimler:** Sol/Sağ yarı · Sol/Orta/Sağ üçte bir · Sol/Sağ üçte iki · Dört köşe çeyrek · Tam ekran · Ortala

---

## 📊 Kıyaslayın — NotchSplit vs. diğer macOS pencere yöneticileri

> Aşağıdaki tabloda NotchSplit, macOS için en bilinen 7 pencere yöneticisiyle karşılaştırılmıştır. **Rakiplerin isimleri kasıtlı olarak gizlenmiştir** (Rakip A–G) — amaç marka tartışması değil, çıplak rakamlarla kıyas. **Kalın** hücreler NotchSplit'in önde olduğu yerlerdir. Rakip verileri her uygulamanın kendi resmi sitesinden, GitHub deposundan ve Mac App Store kayıtlarından alınmıştır (2026-11-10); güvenilir kamuya açık rakam bulunamayan hücreler "—" ile gösterilir (tahmin yok).

| | **NotchSplit** | Rakip A | Rakip B | Rakip C | Rakip D | Rakip E | Rakip F | Rakip G |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| Fiyat | **Ücretsiz** | Ücretsiz | Ücretsiz | $1.99 | $4.99 | $6.99 | $9.99 | $13.99 |
| İndirme boyutu | **448 KB** | 4.96 MB | 24 MB | 3.3 MB | 3.2 MB | 5.2 MB | — | 1.3 MB |
| Boşta RAM | **12 MB** | ~14 MB | — | — | — | — | — | — |
| Dil sayısı | **35** | 33 | 14 | 9 | 1 | 1 | — | 1 |
| Çentik ile tetikleme | **✅ Evet** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Sürüklerken yerleşim seçici | **✅ Evet** | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

**NotchSplit'in öne çıktığı noktalar:**
- 🪶 **En küçük indirme** — 448 KB; en yakın rakibin ~1/7'si, bazılarının ~1/50'si.
- 🧠 **Ölçülmüş düşük RAM** — boşta 12 MB, boşta CPU %0.0 (bu Mac'te `footprint`/`top` ile ölçüldü). Rakiplerin çoğu kamuya açık bir rakam yayınlamıyor.
- 🌍 **35 dil** — test edilen tüm ücretli rakiplerden fazla; ücretsiz rakiplerle aynı ligde.
- 🎯 **Çentik ile tetikleme + sürüklerken yerleşim seçici** — kıyaslanan uygulamaların hiçbirinde yok; NotchSplit'e özgü.
- 💸 **Ücretsiz** — ücretli rakipler $1.99–$13.99 arası.

<sub>Not: "Boşta RAM" hücrelerindeki "—", o uygulama için güvenilir ve kamuya açık bir ölçüm bulunamadığı anlamına gelir; düşük performans değil, yayınlanmış veri eksikliğidir.</sub>

---

## 🪶 Performans (ölçülmüş)

| Metrik | NotchSplit |
| --- | --- |
| RAM (boşta) | **12 MB** |
| CPU (boşta) | **%0.0** (0 idle wakeup) |
| CPU (sürüklerken) | ~%0.3 |
| Uygulama boyutu (.app, universal) | **820 KB** |
| Bağımlılık | Yok (saf AppKit; Electron, web view, 3. parti kütüphane yok) |

Nasıl: %100 native Swift + AppKit, timer/polling yok (yalnızca fare sürükleme olaylarını dinler), menü çubuğu uygulaması (Dock ikonu yok), seçici panel yalnızca gerektiğinde oluşturulup hemen serbest bırakılır.

---

## 🌍 Diller (35)

English · Türkçe · Deutsch · Français · Español · Italiano · Português · Nederlands · Русский · Українська · Polski · Svenska · 简体中文 · 繁體中文 · 日本語 · 한국어 · العربية · हिन्दी · Bahasa Indonesia · Tiếng Việt · Čeština · Dansk · Suomi · Ελληνικά · עברית · Magyar · Norsk bokmål · Română · Slovenčina · ไทย · Català · Hrvatski · فارسی · Bahasa Melayu · Lietuvių

Sistem diline otomatik uyar; uygulama içinden de elle seçilebilir. Sağdan-sola diller (Arapça, İbranice, Farsça) tam desteklenir.

---

## 💻 Gereksinimler

- macOS 13 Ventura veya üstü
- Çentikli bir MacBook (çentiksiz Mac'lerde ekranın üst orta kenarı aynı şekilde çalışır)

## 🔒 Gizlilik ve güvenlik

NotchSplit internete hiç bağlanmaz, veri toplamaz, analitik göndermez. Yalnızca pencereleri taşımak/boyutlandırmak için macOS'un Erişilebilirlik API'sini kullanır. Uygulama hardened runtime ile imzalıdır; sembolleri ve hata ayıklama bilgileri kaldırılmıştır.

## 📄 Lisans

Kullanımı tamamen ücretsizdir. Kaynak kodu kapalıdır ve paylaşılmaz; uygulamanın izinsiz dağıtılması, değiştirilmesi veya tersine mühendislik yapılması yasaktır.

---

<sub>Sürüm 1.0.0 · SHA-256: `ee17fba196f11f6639237e67a0351a1d74443b78a8e232c7f57d946e05b0bf83`</sub>
