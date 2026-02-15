# 🏭 PROFESYONEl ÜRETİM TAKİP SİSTEMİ v2.0

## 🎯 Sistem Özellikleri

### 🔐 Güvenlik
- **Rol Bazlı Erişim**: Yönetici ve Çalışan rolleri
- **Şifre Korumalı Giriş**: Her kullanıcı için özel şifre
- **Oturum Yönetimi**: Güvenli session handling

### 👨‍💼 Yönetici (Yusuf Yalçıntaş)
- **Kullanıcı Adı**: `yusuf`
- **Şifre**: `yusuf123`
- **Yetkiler**:
  - Tüm verileri görüntüleme
  - Detaylı raporlar ve analiz
  - Çalışan performans karşılaştırmaları
  - Dashboard ve grafikler
  - Excel export

### 👷 Çalışanlar
Her çalışan kendi kullanıcı adı ve şifresi ile giriş yapar:
- **Ahmet Öz**: `ahmet` / `ahmet123`
- **Barış Korkut**: `baris` / `baris123`
- **Burak Uçman**: `burak` / `burak123`
- *(Diğer tüm çalışanlar için: isim / isim123)*

**Çalışan Yetkileri**:
- Sadece kendi verilerini görüntüleme
- Veri girişi yapma
- Kendi performansını takip etme

## 📂 Dosya Yapısı

```
📁 Üretim Takip Sistemi
├── index.html              # Giriş sayfası (Login)
├── dashboard.html          # Ana dashboard ve uygulama
├── data-loader.js          # Gerçek Excel verilerini yükleyen script
├── manifest.json           # PWA yapılandırması
└── README.md              # Bu dosya
```

## 🚀 Kurulum

### 1. Hızlı Test (Lokal)
```bash
# Dosyaları indirin
# index.html dosyasını tarayıcıda açın
# Giriş yapın ve test edin
```

### 2. Web Sunucusuna Yükleme (Önerilen)

#### Netlify ile Ücretsiz Hosting:
1. [netlify.com](https://netlify.com)'a gidin
2. "Drop" alanına tüm dosyaları sürükleyin
3. Otomatik link alın (örn: `uretim-takip.netlify.app`)
4. Bu linki çalışanlarla paylaşın

#### GitHub Pages:
1. GitHub repository oluşturun
2. Dosyaları yükleyin
3. Settings > Pages > Deploy from branch
4. Link: `username.github.io/repo-name`

### 3. Mobil Kurulum (PWA)

#### iPhone:
1. Safari'de uygulamayı açın
2. Paylaş (⬆️) > Ana Ekrana Ekle
3. Uygulama ana ekranda görünür

#### Android:
1. Chrome'da uygulamayı açın
2. Menü (⋮) > Ana ekrana ekle
3. Ya da "Yükle" bildirimi gelir

## 📊 Dashboard Özellikleri

### Yönetici Dashboard
1. **Genel Bakış**
   - Günlük toplam üretim
   - Ortalama performans
   - Aktif çalışan sayısı
   - Toplam duruş süreleri

2. **Performans Grafikleri**
   - 7/30/90 günlük trend grafiği
   - Çalışan bazlı karşılaştırmalar
   - Pres bazlı verimlilik

3. **Detaylı Raporlar**
   - Çalışan performans raporu
   - Vardiya analizi
   - Pres ve fason takibi
   - Duruş süreleri analizi

4. **Veri Yönetimi**
   - Excel export
   - Filtreleme ve arama
   - Tarih aralığı seçimi

### Çalışan Dashboard
1. **Kişisel Performans**
   - Bugünkü üretim
   - Kendi performans yüzdesi
   - Geçmiş performans grafiği

2. **Veri Girişi**
   - Basit form arayüzü
   - Pres 1 ve Pres 2 için ayrı alanlar
   - Otomatik hesaplamalar

## 🎨 Özellikler

### Dashboard Bileşenleri
- 📊 **Real-time KPI Cards**: Anlık metrikler
- 📈 **Interactive Charts**: Chart.js ile profesyonel grafikler
- 📋 **Data Tables**: Sıralanabilir ve filtrelenebilir tablolar
- 🎯 **Performance Indicators**: Renkli performans göstergeleri
- 🔍 **Advanced Filters**: Tarih, çalışan, vardiya filtreleri

### Teknik Özellikler
- ✅ Responsive tasarım (mobil, tablet, desktop)
- ✅ Offline çalışma (PWA)
- ✅ Gerçek zamanlı veri güncellemesi
- ✅ LocalStorage ile veri saklama
- ✅ Session yönetimi
- ✅ Rol bazlı içerik kontrolü

## 💾 Veri Yönetimi

### Veri Kaynakları
1. **İlk Yükleme**: 80+ gerçek kayıt (Excel'den)
2. **Yeni Girişler**: Kullanıcıların girdiği veriler
3. **Yedekleme**: LocalStorage (tarayıcı hafızası)

### Veri Güvenliği
- Şifrelenmiş oturum yönetimi
- Her kullanıcı sadece yetkili verileri görür
- Otomatik oturum kapatma (güvenlik)
- Yedekleme ve geri yükleme özelliği

## 📱 Kullanım Senaryoları

### Senaryo 1: Vardiya Başı (Çalışan)
1. Uygulamaya giriş yap
2. "Veri Gir" sekmesine tıkla
3. Pres bilgilerini gir
4. Üretim miktarını kaydet
5. Duruş sürelerini işaretle

### Senaryo 2: Günlük Kontrol (Yönetici)
1. Dashboard'u aç
2. Günlük metrikleri gözden geçir
3. Performans grafiklerini incele
4. Düşük performanslı alanları belirle
5. Gerekli aksiyonları al

### Senaryo 3: Haftalık Rapor
1. Raporlar sekmesine git
2. "Bu Hafta" filtresini seç
3. Çalışan bazlı karşılaştırma yap
4. Excel'e aktar
5. Ekiple paylaş

## 🔧 Özelleştirme

### Renk Teması Değiştirme
`dashboard.html` dosyasında CSS variables:
```css
:root {
    --primary: #1e40af;     /* Ana renk */
    --success: #16a34a;     /* Başarı rengi */
    --warning: #f59e0b;     /* Uyarı rengi */
    --danger: #dc2626;      /* Hata rengi */
}
```

### Yeni Kullanıcı Ekleme
`index.html` dosyasında USERS objesine ekleyin:
```javascript
'kullanici_adi': {
    password: 'sifre123',
    name: 'Tam Adı',
    role: 'worker',
    avatar: '👷'
}
```

## 📈 Performans Metrikleri

### Hesaplama Formülleri
```
Performans (%) = (Üretilen Adet / Hedef Adet) × 100
Verimlilik = (Çalışılan Süre - Duruş) / Çalışılan Süre × 100
Günlük Performans = (Pres1 Perf + Pres2 Perf) / 2
```

### Performans Seviyeleri
- 🟢 **Mükemmel** (100%+): Hedefin üzerinde
- 🔵 **İyi** (80-99%): Hedef civarında
- 🟡 **Orta** (60-79%): Geliştirilmeli
- 🔴 **Zayıf** (<60%): Acil aksiyon gerekli

## 🆘 Sorun Giderme

### Giriş Yapamıyorum
- Kullanıcı adı ve şifrenizi kontrol edin
- Büyük/küçük harf duyarlılığına dikkat edin
- Tarayıcı önbelleğini temizleyin

### Veriler Görünmüyor
- Sayfa yenileyin (F5)
- LocalStorage'ı kontrol edin
- Farklı tarayıcı deneyin

### Grafikler Yüklenmiyor
- İnternet bağlantınızı kontrol edin
- Chart.js CDN'inin yüklendiğinden emin olun
- Tarayıcı konsolunu kontrol edin

## 🔄 Güncellemeler

### v2.0 (Şubat 2026)
- ✅ Rol bazlı yetkilendirme sistemi
- ✅ Şifre korumalı giriş
- ✅ Profesyonel dashboard
- ✅ Gerçek Excel verilerini import
- ✅ Gelişmiş filtreleme ve raporlama
- ✅ Mobil responsive tasarım
- ✅ PWA desteği

### Planlanan (v3.0)
- ☁️ Bulut senkronizasyonu (Firebase)
- 🔔 Push bildirimleri
- 📧 Otomatik email raporları
- 👥 Kullanıcı yönetimi paneli
- 📱 Native mobil uygulama
- 🤖 AI destekli tahminler

## 💡 İpuçları

1. **Düzenli Veri Girişi**: Her vardiya sonunda veri girin
2. **Yedekleme**: Haftada bir Excel export yapın
3. **Analiz**: Haftalık trendleri takip edin
4. **Paylaşım**: Ekiple düzenli dashboard inceleyin
5. **Güncelleme**: Tarayıcıyı güncel tutun

## 📞 Destek

Sorularınız veya önerileriniz için:
- **Yönetici**: Yusuf Yalçıntaş
- **Email**: [email korunuyor]
- **GitHub Issues**: Teknik sorunlar için

## 📄 Lisans

© 2026 Tüm hakları saklıdır.
Bu sistem özel olarak geliştirilmiştir.

---

**Başarılı üretimler dileriz! 🏭✨**
