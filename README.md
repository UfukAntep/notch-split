# NotchSplit

**Herhangi bir pencereyi çentiğe (notch) sürükleyerek macOS'te ekranı bölün.**

NotchSplit, MacBook'unuzun çentiğini bir pencere yöneticisine dönüştürür. Klavye kısayolu ezberlemek yok, küçük yeşil düğmelerin üzerinde beklemek yok: pencereyi tutun, ekranın üstüne, çentiğe götürün, bırakın.

Bu repo **kullanıma hazır uygulamayı** içerir. **Tamamen ücretsizdir** ve **kapalı kaynaktır** — kaynak kodu paylaşılmaz, yalnızca derlenmiş macOS çıktısı (`.dmg`) burada yayınlanır.

---

## 📥 İndir

**[NotchSplit-1.0.0.dmg](NotchSplit-1.0.0.dmg)** indir (432 KB)

### Kurulum

1. `.dmg` dosyasını açın, **NotchSplit**'i **Applications** klasörüne sürükleyin.
2. Applications klasöründen NotchSplit'i açın.
3. macOS *"Apple doğrulayamadı"* uyarısı gösterirse: **Bitti**'ye basın, ardından **Sistem Ayarları › Gizlilik ve Güvenlik** bölümünün en altında **Yine de Aç**'a tıklayın.
   *(Bu uyarı, App Store dışı ve ücretsiz bir uygulama olduğu için çıkar. NotchSplit internete bağlanmaz, sürücü yüklemez; yalnızca pencere taşımak için Erişilebilirlik API'sini kullanır.)*
4. Sorulduğunda **Erişilebilirlik** iznini verin: **Sistem Ayarları › Gizlilik ve Güvenlik › Erişilebilirlik**.
5. Menü çubuğundaki çentik simgesine tıklayıp dilinizi seçin (20 dil arasından), sonra herhangi bir pencereyi çentiğe sürükleyin.

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

## 🪶 Performans

Bu Mac'te (Apple Silicon, macOS 27) ölçülmüştür:

| Metrik | NotchSplit |
| --- | --- |
| RAM (boşta) | **12 MB** |
| CPU (boşta) | **%0.0** |
| Uygulama boyutu | **756 KB** |
| Bağımlılık | Yok (3. parti kütüphane, Electron, web view yok) |

### Rakiplerle karşılaştırma — RAM / CPU / boyut

> Rakip verileri her uygulamanın kendi resmi sitesinden, GitHub deposundan veya Mac App Store kaydından derlenmiştir (2026-11-10). Güvenilir, kamuya açık bir rakam **bulunamayan** hücreler "—" ile işaretlenmiştir — tahmini sayı verilmemiştir.

| Uygulama | Fiyat | Boyut | Idle RAM | Idle CPU |
| --- | --- | --- | --- | --- |
| **NotchSplit** | **Ücretsiz** | **756 KB** | **12 MB** | **%0.0** |
| Rectangle | Ücretsiz | 4.96 MB | ~14 MB | %0.0 |
| Magnet | $4.99 | 3.2 MB | — | — |
| Moom (Classic) | $6.99 | 5.2 MB | — | — |
| BetterSnapTool | $1.99 | 3.3 MB | — | — |
| Loop | Ücretsiz | 24.0 MB | — | ~%0.5 |
| Rectangle Pro | $9.99 | — | — | — |
| Divvy | $13.99 | 1.3 MB | — | — |

### Rakiplerle karşılaştırma — dil desteği

| Uygulama | Dil sayısı |
| --- | --- |
| Rectangle | 33 |
| **NotchSplit** | **20** |
| Loop | 14 |
| BetterSnapTool | 9 |
| Magnet / Moom / Divvy | 1 (yalnızca İngilizce) |

NotchSplit'in desteklediği diller: English, Türkçe, Deutsch, Français, Español, Italiano, Português, Nederlands, Русский, Українська, Polski, Svenska, 简体中文, 繁體中文, 日本語, 한국어, العربية, हिन्दी, Bahasa Indonesia, Tiếng Việt.

---

## 💻 Gereksinimler

- macOS 13 Ventura veya üstü
- Çentikli bir MacBook (çentiksiz Mac'lerde ekranın üst orta kenarı aynı şekilde çalışır)

## 🔒 Gizlilik ve güvenlik

NotchSplit internete hiç bağlanmaz, veri toplamaz, analitik göndermez. Yalnızca pencereleri taşımak/boyutlandırmak için macOS'un Erişilebilirlik API'sini kullanır. Uygulama hardened runtime ile imzalıdır; sembolleri ve hata ayıklama bilgileri kaldırılmıştır.

## 📄 Lisans

Kullanımı tamamen ücretsizdir. Kaynak kodu kapalıdır ve paylaşılmaz; uygulamanın izinsiz dağıtılması, değiştirilmesi veya tersine mühendislik yapılması yasaktır.

---

<sub>Sürüm 1.0.0 · SHA-256: `e771a5c46546faf30be7767df2b1508c973514a046850ed4daaedf76689491fa`</sub>
