# 💻 Lokal Sunucu Kurulumu (İnternet Gerekmez)

## Neden Lokal?
- ✅ SSL hatası yok
- ✅ İnternet gerekmez
- ✅ Hemen çalışır
- ✅ Aynı ağdaki cihazlar erişebilir (WiFi)

## YÖNTEM 1: Python ile (ÇOK KOLAY)

### Windows için:
1. **Dosyaların olduğu klasöre gidin**
   - Örnek: `C:\Masaüstü\Üretim Takip`

2. **Klasörde Shift + Sağ Tık yapın**
   - "PowerShell penceresini burada aç" seçin

3. **Şu komutu yazın:**
   ```
   python -m http.server 8080
   ```
   ENTER'a basın

4. **Tarayıcıda açın:**
   ```
   http://localhost:8080
   ```

5. **Aynı WiFi'deki telefonlardan:**
   - Bilgisayarınızın IP adresini bulun (ipconfig komutundan)
   - Örnek: `http://192.168.1.100:8080`

### Mac için:
1. **Terminal'i açın**
2. **Klasöre gidin:**
   ```
   cd ~/Desktop/Üretim\ Takip
   ```
3. **Sunucuyu başlatın:**
   ```
   python3 -m http.server 8080
   ```
4. **Tarayıcıda açın:**
   ```
   http://localhost:8080
   ```

## YÖNTEM 2: Chrome Web Server (DAHA KOLAY)

### Adım 1: Extension Yükleyin
1. Chrome'u açın
2. Chrome Web Store'a gidin
3. "Web Server for Chrome" aratın
4. "Chrome'a Ekle" tıklayın

### Adım 2: Klasörü Seçin
1. Extension'ı açın
2. "CHOOSE FOLDER" tıklayın
3. Üretim Takip klasörünü seçin

### Adım 3: Başlatın
1. "Web Server: STARTED" olsun
2. Verilen linke tıklayın (örnek: http://127.0.0.1:8887)

## YÖNTEM 3: VS Code Live Server (Geliştiriciler için)

1. VS Code indirin ve kurun
2. Live Server extension'ını yükleyin
3. index.html'e sağ tık > "Open with Live Server"

## 📱 Aynı Ağdaki Telefonlardan Erişim

### Bilgisayarınızın IP'sini Bulun:

**Windows:**
1. CMD açın
2. `ipconfig` yazın
3. "IPv4 Address" altındaki numarayı not alın
4. Örnek: 192.168.1.100

**Mac:**
1. Terminal açın
2. `ifconfig | grep inet` yazın
3. 192.168 ile başlayan IP'yi not alın

### Telefondan Bağlanın:
```
http://BILGISAYAR-IP:8080
```
Örnek: `http://192.168.1.100:8080`

## ⚠️ Önemli Notlar

- Bilgisayar açık olmalı
- Aynı WiFi ağında olmalısınız
- Windows Firewall izin vermeli

## 🔥 Firewall İzni (Windows)

Eğer bağlanamıyorsa:
1. Windows Güvenlik Duvarı'nı açın
2. "Güvenlik duvarı üzerinden uygulama veya özelliğe izin ver"
3. Python veya Chrome'u bulun ve işaretleyin

## ✅ Avantajlar

- SSL sorunu yok
- İnternet gerekmez
- Aynı ofistekileri erişebilir
- Ücretsiz
- Hemen çalışır