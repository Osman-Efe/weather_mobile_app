# Weather Buddy ☁️

## Kısa Açıklama
Weather Buddy, kullanıcının o anki konum verilerini kullanarak anlık hava durumu bilgilerini gösteren, modern ve şık arayüze sahip bir Flutter uygulamasıdır. Uygulama, **OpenWeatherMap API** üzerinden veri çekmekte ve **BLoC (Business Logic Component)** tasarım desenini kullanarak state yönetimini sağlamaktadır. Kullanıcılar sıcaklık, hava durumu durumu (güneşli, yağmurlu vb.), gün doğumu ve gün batımı gibi detayları dinamik grafikler eşliğinde görebilirler.

## Kullanılan Teknolojiler ve Sürümler
* **Flutter Sürümü:** 3.0.0 veya üzeri (Dart 3 uyumlu)
* **State Management:** `flutter_bloc`
* **Veri Kaynağı:** `weather` (OpenWeatherMap API Wrapper)
* **Konum Servisleri:** `geolocator`
* **Tasarım:** `glassmorphism` efektleri ve `CustomPainter` kullanımı

## Çalıştırma Adımları

Uygulamayı yerel makinenizde çalıştırmak için aşağıdaki adımları takip edin:

### 1. Ön Hazırlık
* Bilgisayarınızda Flutter SDK'nın yüklü olduğundan emin olun (`flutter doctor` komutu ile kontrol edebilirsiniz).
* Bir OpenWeatherMap hesabı oluşturun ve kendi **API Key**'inizi alın.

### 2. API Key Yapılandırması
Projenin çalışması için `lib/data/my_data.dart` (veya ilgili veri dosyası) içerisine API anahtarınızı tanımlayın:
```dart
const String apiKey = "BURAYA_KENDI_API_KEYINIZI_YAZIN";

3. Bağımlılıkları Yükleme
Terminali açın ve proje dizinine giderek paketleri indirin:
flutter pub get

4. İzinlerin Kontrolü
Uygulamanın konuma erişebilmesi için gerekli izinlerin tanımlandığından emin olun:

Android: android/app/src/main/AndroidManifest.xml içine ACCESS_FINE_LOCATION iznini ekleyin.

iOS: ios/Runner/Info.plist içine NSLocationWhenInUseUsageDescription anahtarını ekleyin.

5. Uygulamayı Başlatma
Bir emülatör veya gerçek cihaz bağladıktan sonra şu komutu çalıştırın:
flutter run
