<h1 align="center">🎬 Java Swing - Adam Asmaca (Hangman)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white" alt="Java">
  <img src="https://img.shields.io/badge/Apache_NetBeans-1B6AC6?style=for-the-badge&logo=apache-netbeans&logoColor=white" alt="NetBeans">
  <img src="https://img.shields.io/badge/Swing-GUI-4CAF50?style=for-the-badge" alt="Swing">
  <img src="https://img.shields.io/badge/I/O-File_Operations-ff69b4?style=for-the-badge" alt="File IO">
</p>

<p align="center">
  <b>Dosya işlemleri (File I/O), hata yönetimi ve "Defensive Programming" (Savunmacı Programlama) prensipleri kullanılarak geliştirilmiş, Sinema & Gerilim temalı gelişmiş bir Java masaüstü oyunudur.</b>
</p>

<br>

## 📌 Proje Hakkında
Bu proje, standart bir adam asmaca oyununun ötesine geçerek bir yazılımın arka planda log tutma, veri saklama ve eksik dosyaları kendi kendine onarma gibi mühendislik standartlarını barındıracak şekilde tasarlanmıştır. Proje arayüzü sekme (JTabbedPane) mantığıyla 3 ana modüle ayrılmıştır.

## 🚀 Öne Çıkan Özellikler

- 🛡️ **Kendi Kendini Onaran Veri Havuzu:** Oyun, kelimeleri `C:\P2Oyun\TXTDosyalar\kelimeler.txt` dosyasından okur. Kullanıcı veya sistem bu dosyayı yanlışlıkla silerse program çökmez; Exception Handling devreye girer ve 30 kelimelik sinema temalı yeni bir dosyayı anında kendi kendine oluşturur.
- ⏱️ **Entegre Timer (Kronometre):** Oyun başlar başlamaz aktifleşen ve oyun bitiminde otomatik duran hassas zamanlayıcı.
- 🔒 **Güvenlik ve Loglama:** Sisteme ilk girişte şifre belirlenir. Başarılı ve başarısız tüm giriş denemeleri anlık olarak `log.txt` dosyasına kaydedilir ve oyun içinden takip edilebilir.
- 💾 **Kalıcı Skor Tablosu:** Oynanan oyunların tarih, süre ve kazanma/kaybetme durumları `oyunlar.txt` dosyasına yazılır ve `JTable` ile anlık olarak listelenir.
- 🛑 **Anti-Hile Sistemi:** Oyun sonuçlandığı anda tüm TextField ve Button erişimleri (setEnabled) kapatılarak hile yapılması engellenir.

<br>

## 📂 Proje Dizin Yapısı

Program ilk çalıştığında C diskinde aşağıdaki ağaç yapısını otomatik olarak inşa eder:

```text
C:\P2Oyun\
├── 📁 TXTDosyalar
│   ├── 📄 log.txt (Giriş hareketleri)
│   ├── 📄 oyunlar.txt (Geçmiş maç skorları)
│   └── 📄 kelimeler.txt (Kendi kendini onaran kelime havuzu)
└── 📁 Resimler
    └── 🖼️ 1.png, 2.png ... 7.png (Dinamik darağacı çizimleri)
```

## 💾 Veri Yönetimi ve Kalıcılık (File I/O)

Proje, veritabanı bağımsız çalışabilmek için kendi dosya sistemini kullanır:
* **`kelimeler.txt` :** Sinema, polisiye ve psikolojik gerilim temalı kelimelerin tutulduğu dinamik veri havuzudur. Silinmesi durumunda kendi kendini yeniden oluşturur.
* **`oyunlar.txt` :** Oynanan her oyunun süresini ve sonucunu kalıcı olarak saklar. Tablo ekranı (JTable) verilerini anlık olarak buradan okur.
* **`log.txt` :** Sisteme yapılan başarılı veya hatalı tüm giriş denemelerini güvenlik amacıyla kayıt altında tutar.


## 🛠️ Kullanılan Teknolojiler

| Kategori | Teknoloji / Kütüphane |
| :--- | :--- |
| **Dil** | `Java (JDK 8+)` |
| **Arayüz Geliştirme** | `Java Swing (JFrame, JPanel, JTabbedPane, JTable)` |
| **Veri Yönetimi** | `File`, `FileReader`, `FileWriter`, `BufferedReader`, `BufferedWriter` |
| **Geliştirme Ortamı** | `Apache NetBeans IDE` |

## 📸 Ekran Görüntüleri

> **Not:** Sistem arayüzüne ve güvenlik loglarına ait görseller aşağıda yer almaktadır.

### Giriş ve Güvenlik Aşamaları
| İlk Giriş Ekranı | Şifre Doğru Girildiğinde | Şifre Yanlış Girildiğinde |
| :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/0c89f40e-2305-481d-8891-87093aac9cbd" width="300"> | <img src="https://github.com/user-attachments/assets/cc0eeec0-3ebb-4359-8ae5-32c21823932c" width="300"> | <img src="https://github.com/user-attachments/assets/98825122-1f70-4205-8a0e-17a1aa5e334d" width="300"> |

<br>

### Oyun İçi Ana Modüller
| 🎮 Oyun Ekranı | 🏆 Skorlar Tablosu | 📝 Sistem Logları |
| :---: | :---: | :---: |
| <img src="https://github.com/user-attachments/assets/d835292f-fe8b-4f49-b1b6-aace7bc51ec9" width="300"> | <img src="https://github.com/user-attachments/assets/6e5ff255-918f-4b98-9955-68199fda8b89" width="300"> | <img src="https://github.com/user-attachments/assets/7981b350-a66d-41b8-adcf-ed7b428e2589" width="300"> |
