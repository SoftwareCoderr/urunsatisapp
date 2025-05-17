```diff

➕Proje iskeleti oluşturuldu ve ilk commit eklendi(Commit1)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

➕Login Page, HomePage ve authentication yapıları işlendi.(Commit2)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

✅- İş Paketi 1: .NET MAUI ile Proje Başlatma, LiteDB Entegrasyonu ve ActivityIndicator Kullanımı
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Proje .NET MAUI altyapısı ile başlatıldı. Yerel veritabanı olarak LiteDB kullanıldı. Kullanıcı verileri ve ürün bilgileri, cihaz içinde saklanacak şekilde MyContext sınıfı ile yapılandırıldı.

✴️Katkısı: Uygulama internetsiz ortamda bile çalışabilir hale getirildi. LiteDB ile performanslı ve bağımsız veri yönetimi sağlandı. ActivityIndicator ile işlem sürecinde kullanıcıya geri bildirim sunuldu.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

✅ İş Paketi 2: AuthHelper, MyContext ve GenericRepository Tasarımı
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: MyContext.cs ile LiteDB bağlantı yapısı oluşturuldu. GenericRepository.cs ve IGenericRepository.cs ile tüm veri işlemleri (Ekleme, Silme, Güncelleme, Listeleme) soyutlandı.

✴️Katkısı: Kod tekrarını önleyen, genişletilebilir ve sade bir yapı kuruldu. Tüm veriler tek bir repository yapısı üzerinden kontrol edilebilir hale geldi.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

✅ İş Paketi 3: Giriş Sayfası Tasarımı ve Trigger Yapısı
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: LoginPage.cs dosyasında kullanıcı giriş ekranı oluşturuldu. Entry kontrolleri ile kullanıcı adı ve şifre girişi sağlandı. Trigger kullanılarak, kullanıcı bilgilerinin eksik girilmesi durumunda “Giriş Yap” butonu pasif hale getirildi.

✴️Katkısı: Kullanıcı deneyimini artıran, hatalı girişlerin önüne geçen, sade ve fonksiyonel bir giriş arayüzü oluşturuldu.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 4: TapGestureRecognizer, Bind, ICommand, GetUser ile MVVM Etkileşimi
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Entry, CheckBox gibi UI bileşenleri ViewModel ile bağlandı. LoginCommand üzerinden giriş işlemi kontrol edildi. Kullanıcının girdiği bilgilere göre veritabanından doğrulama yapılması sağlandı.

✴️Katkısı: MVVM mimarisi oturtuldu. UI ile iş mantığı birbirinden ayrıldı, test edilebilir ve sürdürülebilir bir yapı kuruldu.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 5: “Beni Hatırla” (Remember) ve Kayıt Sayfası (Register) İşlemleri
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Kullanıcının oturum bilgilerini uygulamayı yeniden açtığında hatırlamak amacıyla SecureStorage kullanılarak şifreli bir şekilde cihazda veri saklandı. Ayrıca RegisterPage üzerinden kullanıcı kaydı yapılabilmesi için kullanıcı adı, şifre gibi bilgiler alınıp LiteDB üzerinden kaydedildi.

✴️Katkısı: Kullanıcı, giriş ekranını tekrar tekrar doldurmadan uygulamayı rahatça kullanabiliyor. Aynı zamanda kullanıcı verilerinin güvenliği artırıldı. Kayıt ekranı sayesinde uygulama çok kullanıcıya uygun hale getirildi.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 6: TabBar ve FlyoutItem Entegrasyonu
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Uygulamanın temel gezinti yapısı için alt tarafta TabBar, yan menü için FlyoutItem kullanıldı. Sayfalar arasında geçiş ve menü yönetimi kolaylaştırıldı.

✴️Katkısı: Kullanıcıların uygulama içinde farklı sayfalar (ürünler, sepet, kategoriler vb.) arasında hızlı ve sezgisel şekilde geçiş yapabilmesi sağlandı. UI/UX kalitesi artırıldı.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 7: Mapper ve Opacity Geçiş Efektleri Ekleme
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Sayfalar arası geçişlerde Opacity (saydamlık) animasyonları ile yumuşak geçiş efektleri uygulandı. Mapper kullanılarak model sınıflar ile ViewModel arasındaki dönüşümler otomatik hale getirildi.

✴️Katkısı: Uygulama daha görsel ve profesyonel bir kullanıcı deneyimi sundu. Kod karmaşıklığı azaltıldı ve ViewModel-Model geçişleri standartlaştırıldı.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 8: Converters ve Ürün Yönetimi Modülü Geliştirme
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Uygulamada IValueConverter arayüzü kullanılarak bool → visibility, string → renk, stok sayısı → etiket durumu gibi dönüşümler tanımlandı. Ürün ekleme, düzenleme, silme gibi işlemler için özel sayfalar ve ViewModel yapıları geliştirildi. Product modeli üzerinden LiteDB ile tam entegre veri akışı sağlandı.

✴️Katkısı: Görsel dönüşümler merkezi olarak kontrol edilebilir hale geldi; UI dinamikleşti. Ürünlerin listelenmesi, filtrelenmesi ve güncellenmesi tek bir yapıdan yönetildi. Yönetici dostu bir panel yapısı oluşturuldu.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 9: FlexLayout ve BindableLayout Entegrasyonu
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


◉Açıklama: Ürün kartları ve kategori etiketlerinin esnek şekilde yerleşmesini sağlamak amacıyla FlexLayout kullanıldı. Aynı veri kaynağından birden fazla öğe üretmek için BindableLayout.ItemsSource ile ViewModel verileri bağlandı.

✴️Katkısı: Ekran boyutundan bağımsız, esnek ve akıllı yerleşim sağlandı. UI elemanları daha yönetilebilir hale geldi ve kullanıcı dostu bir arayüz oluşturuldu.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 10: GridItemsLayout ve Expander ile Listeleme Geliştirme
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


◉Açıklama: Ürün listeleme ekranında grid yapısı kullanılarak ızgara formunda kart yerleşimi sağlandı (GridItemsLayout). Ayrıca her ürün kartında detayların gizlenip açılabilmesi için Expander yapısı uygulandı.

✴️Katkısı: Kullanıcı, aynı anda birden fazla ürünü kolayca görebildi. Gerekli detaylara ancak istenildiğinde erişim sağlanarak sade ve bilgi yoğunluğu kontrollü bir arayüz elde edildi.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 11: Sepet (Basket) Sayfası Oluşturma
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Kullanıcının sepete eklediği ürünlerin listelendiği özel bir sayfa geliştirildi. Her ürün için adet, fiyat ve toplam hesaplandı. ObservableCollection kullanılarak sepet dinamik hale getirildi.

✴️Katkısı: Gerçek zamanlı toplam fiyat güncellenmesi, ürün silme, adet değiştirme gibi işlemler sorunsuz hale geldi. Kullanıcı, satın alma öncesi tüm detayları görüp düzenleyebildi.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


✅ İş Paketi 12: SkiaSharp, LottieView, Dinamik Veriler ve Ödeme Entegrasyonu
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

◉Açıklama: Sayfa geçişlerinde ve işlem süreçlerinde görsel geri bildirim vermek için LottieView animasyonları ve SkiaSharp çizim bileşenleri entegre edildi. Dinamik olarak gelen ürün verileri UI'ya otomatik bağlandı. Ödeme ekranı oluşturuldu ve işlemin tamamlandığına dair kullanıcıya animasyonlu onay sunuldu.

✴️Katkısı: Uygulamanın profesyonel görünüm düzeyi artırıldı. Kullanıcılar işlem akışında net yönlendirmeler aldı ve geri bildirimler sayesinde güvenli işlem algısı oluştu. Son kullanıcı deneyimi üst seviyeye taşındı.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

