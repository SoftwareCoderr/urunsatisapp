Proje iskeleti oluşturuldu ve ilk commit eklendi(Commit1)

Login Page, HomePage ve authentication yapıları işlendi.(Commit2)

✅ İş Paketi 1: .NET MAUI ile Proje Başlatma, LiteDB Entegrasyonu ve ActivityIndicator Kullanımı
Açıklama: Proje .NET MAUI altyapısı ile başlatıldı. Yerel veritabanı olarak LiteDB kullanıldı. Kullanıcı verileri ve ürün bilgileri, cihaz içinde saklanacak şekilde MyContext sınıfı ile yapılandırıldı.
Katkısı: Uygulama internetsiz ortamda bile çalışabilir hale getirildi. LiteDB ile performanslı ve bağımsız veri yönetimi sağlandı. ActivityIndicator ile işlem sürecinde kullanıcıya geri bildirim sunuldu.

✅ İş Paketi 2: AuthHelper, MyContext ve GenericRepository Tasarımı
Açıklama: MyContext.cs ile LiteDB bağlantı yapısı oluşturuldu. GenericRepository.cs ve IGenericRepository.cs ile tüm veri işlemleri (Ekleme, Silme, Güncelleme, Listeleme) soyutlandı.
Katkısı: Kod tekrarını önleyen, genişletilebilir ve sade bir yapı kuruldu. Tüm veriler tek bir repository yapısı üzerinden kontrol edilebilir hale geldi.

✅ İş Paketi 3: Giriş Sayfası Tasarımı ve Trigger Yapısı
Açıklama: LoginPage.cs dosyasında kullanıcı giriş ekranı oluşturuldu. Entry kontrolleri ile kullanıcı adı ve şifre girişi sağlandı. Trigger kullanılarak, kullanıcı bilgilerinin eksik girilmesi durumunda “Giriş Yap” butonu pasif hale getirildi.
Katkısı: Kullanıcı deneyimini artıran, hatalı girişlerin önüne geçen, sade ve fonksiyonel bir giriş arayüzü oluşturuldu.

✅ İş Paketi 4: TapGestureRecognizer, Bind, ICommand, GetUser ile MVVM Etkileşimi
Açıklama: Entry, CheckBox gibi UI bileşenleri ViewModel ile bağlandı. LoginCommand üzerinden giriş işlemi kontrol edildi. Kullanıcının girdiği bilgilere göre veritabanından doğrulama yapılması sağlandı.
Katkısı: MVVM mimarisi oturtuldu. UI ile iş mantığı birbirinden ayrıldı, test edilebilir ve sürdürülebilir bir yapı kuruldu.

✅ İş Paketi 5: “Beni Hatırla” (Remember) ve Kayıt Sayfası (Register) İşlemleri
Açıklama: Kullanıcının oturum bilgilerini uygulamayı yeniden açtığında hatırlamak amacıyla SecureStorage kullanılarak şifreli bir şekilde cihazda veri saklandı. Ayrıca RegisterPage üzerinden kullanıcı kaydı yapılabilmesi için kullanıcı adı, şifre gibi bilgiler alınıp LiteDB üzerinden kaydedildi.
Katkısı: Kullanıcı, giriş ekranını tekrar tekrar doldurmadan uygulamayı rahatça kullanabiliyor. Aynı zamanda kullanıcı verilerinin güvenliği artırıldı. Kayıt ekranı sayesinde uygulama çok kullanıcıya uygun hale getirildi.

✅ İş Paketi 6: TabBar ve FlyoutItem Entegrasyonu
Açıklama: Uygulamanın temel gezinti yapısı için alt tarafta TabBar, yan menü için FlyoutItem kullanıldı. Sayfalar arasında geçiş ve menü yönetimi kolaylaştırıldı.
Katkısı: Kullanıcıların uygulama içinde farklı sayfalar (ürünler, sepet, kategoriler vb.) arasında hızlı ve sezgisel şekilde geçiş yapabilmesi sağlandı. UI/UX kalitesi artırıldı.

✅ İş Paketi 7: Mapper ve Opacity Geçiş Efektleri Ekleme
Açıklama: Sayfalar arası geçişlerde Opacity (saydamlık) animasyonları ile yumuşak geçiş efektleri uygulandı. Mapper kullanılarak model sınıflar ile ViewModel arasındaki dönüşümler otomatik hale getirildi.
Katkısı: Uygulama daha görsel ve profesyonel bir kullanıcı deneyimi sundu. Kod karmaşıklığı azaltıldı ve ViewModel-Model geçişleri standartlaştırıldı.

✅ İş Paketi 8: Converters ve Ürün Yönetimi Modülü Geliştirme
Açıklama: Uygulamada IValueConverter arayüzü kullanılarak bool → visibility, string → renk, stok sayısı → etiket durumu gibi dönüşümler tanımlandı. Ürün ekleme, düzenleme, silme gibi işlemler için özel sayfalar ve ViewModel yapıları geliştirildi. Product modeli üzerinden LiteDB ile tam entegre veri akışı sağlandı.
Katkısı: Görsel dönüşümler merkezi olarak kontrol edilebilir hale geldi; UI dinamikleşti. Ürünlerin listelenmesi, filtrelenmesi ve güncellenmesi tek bir yapıdan yönetildi. Yönetici dostu bir panel yapısı oluşturuldu.
