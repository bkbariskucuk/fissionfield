# Fissionfield

[En Güncel Sürüm](https://github.com/bkbariskucuk/fissionfield/releases/latest) · Linux x86_64 · AppImage

Serpent 2 Monte Carlo nötronik hesaplamaları için modern grafiksel kullanıcı arayüzü, gelişmiş reaktör geometri görselleştirme ve simülasyon analiz platformu.

---

## Kubuntu / Linux kurulumu

Uygulama menüsünde **Fissionfield** olarak görünmesi için kullanıcı kurucusunu çalıştırın. `sudo` gerekmez; kurucu yayımlanmış AppImage'i indirir, SHA256 doğrulaması yapar, menü kaydını ve tüm logo boyutlarını kurar. Projeleri ve ayarları korur. Kurucu için Python 3 gerekir (Kubuntu'da bulunur); uygulamanın kendisi bağımsızdır.

```bash
curl -fL -o /tmp/fissionfield-install.py \
  https://raw.githubusercontent.com/bkbariskucuk/fissionfield/main/install.py
python3 /tmp/fissionfield-install.py
```

AppImage kurulumdan sonra uygulama menüsünde paket adıyla görünür. Yeni **Fissionfield** paketleri `~/.local/share/fissionfield/application/` altına kurulur. Sadece AppImage'i indirmek/çalıştırmak menü kaydı oluşturmaz.

Daha önce indirdiğiniz resmî dosyayı kullanmak için ikinci komuta `--appimage /dosyanın/yolu/Fissionfield.AppImage` ekleyebilirsiniz; sürüm/hash doğrulaması yine yapılır.

---

## Öne Çıkan Yetenekler

* **Reaktör Çekirdek ve Geometri Görselleştirme:** Altıgen ve kare kafes yapılarında çekirdek, yakıt demeti ve pin düzeyinde etkileşimli görselleştirme.
* **Serpent Girdi Düzenleyici & Doğrulama:** Sözdizimi vurgulama, gerçek zamanlı hata kontrolü ve otomatik tamamlama.
* **Kapsamlı Analiz ve Grafik Çıktıları:** Akı (flux) dağılımları, güç pik faktörleri (PPF), yanma (depletion) ve reaktivite katsayısı görselleştirmeleri.
* **Termal-Hidrolik Şablonlama:** D6 altıgen simetrisi destekli kanal eşleme ve malzeme durum yönetimi.

---

## Sistem Gereksinimleri

* **İşletim Sistemi:** Linux x86_64 (Ubuntu 20.04+, Debian 11+, Fedora, Arch Linux ve türevleri).
* **Bağımlılıklar:** Herhangi bir Python, Conda veya ek kütüphane kurulumu gerekmez; tek bir bağımsız binary olarak çalışır.
* **Hesaplama Motoru:** Serpent 2 hesaplama motoru ve nükleer veri kütüphaneleri (ENDF/B, JEFF vb.) güvenlik ve lisans nedeniyle pakete dahil değildir.

---

## Hesap Erişimi

Fissionfield kurumsal güvenlik ve erişim standartlarına sahiptir. Uygulama ilk açıldığında sistem yöneticisi tarafından tanımlanmış kullanıcı adı ve parolanızla giriş yapmanız gerekir. Yeni hesap tanımlamaları ve panel yetkilendirmeleri yönetici tarafından gerçekleştirilir.

---

## Doğrulama (Opsiyonel)

İndirdiğiniz dosyanın bütünlüğünü sürümle birlikte sunulan `SHA256SUMS.txt` dosyasıyla teyit edebilirsiniz:

```bash
sha256sum -c SHA256SUMS.txt
```

---

## Lisans ve Yasal Uyarı

Fissionfield yazılımının tüm hakları saklıdır.  
Serpent, VTT Technical Research Centre of Finland tarafından geliştirilen bağımsız bir Monte Carlo reaktör fiziği kodudur. Fissionfield bağımsız bir kullanıcı arayüzü olup VTT ile resmi bir ortaklığı bulunmamaktadır.
