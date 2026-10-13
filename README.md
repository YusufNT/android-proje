# Ayet — Her Gün Bir Ayet

Kotlin ve Jetpack Compose ile hazırlanmış, Kur'an metnini çevrimdışı sunan Android uygulaması.

## Android Studio'da açma ve derleme

Projeyi Android Studio'da açın ve Gradle eşitlemesinin tamamlanmasını bekleyin. Komut satırından Windows'ta:

```powershell
.\gradlew.bat testDebugUnitTest
.\gradlew.bat assembleDebug
```

Kurulabilir deneme APK'sı `app\build\outputs\apk\debug\app-debug.apk` konumunda oluşturulur. Android SDK ve JDK 17 veya üzeri gerekir.

## İçerik kaynakları

- Arapça Uthmani metin: [Tanzil Project](https://tanzil.net/), sürüm 1.1. Tanzil'in sağladığı XML dosyasındaki telif/lisans bildirimi dosyanın içinde aynen korunmuştur. Metin değiştirilmeden dağıtılır.
- Türkçe meal: [Rowwad Translation Center / QuranEnc](https://quranenc.com/en/browse/turkish_rwwad), `turkish_rwwad` sürüm 1.0.4. Sağlayıcının kaynak, sürüm ve özgün belgeyi koruma koşulları için asıl XML dosyası değiştirilmeden saklanmıştır.

Uygulama açılırken kaynaklar eşleştirilir; 114 sure ve 6.236 Arapça/Türkçe ayet doğrulanmazsa okuma ekranı sessizce eksik veri göstermez.

## Kilit ekranı ve bildirimler

Android uygulamaların sistem kilit ekranını serbestçe değiştirmesine izin vermez. Otomatik ayetler, kullanıcı bildirim izni verdiğinde kilit ekranında gösterilebilen standart Android bildirimiyle sunulur; gerçek görünürlük ve gizlilik Android/cihaz ayarlarına bağlıdır. Uygulama ayetli duvar kâğıdını Android'in duvar kâğıdı API'siyle ana ekrana ve desteklenen sürümlerde kilit ekranına uygular. Zamanlama, pil tasarrufu nedeniyle gecikebilir.

Okuma konumu, geçmiş, favoriler ve ayarlar cihazda saklanır. Uygulama ayet verilerini sunmak için internet bağlantısı istemez.
