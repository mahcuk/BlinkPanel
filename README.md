# BlinkPanel
================================================================================
 BlinkPanel
 Tabletiniz önüne geldiğinizde kendiliğinden uyansın, Home Assistant paneliniz
 hazır olsun.
================================================================================

BlinkPanel nedir?
-----------------
Duvara astığınız ya da standa koyduğunuz bir Android tableti Home Assistant
kontrol paneline çevirir. Tablet normalde uykuda durur. Önünden geçtiğinizde ya
da yaklaştığınızda ekran kendiliğinden açılır ve Home Assistant paneliniz
karşınıza çıkar. Uzaklaşınca ekran yine uykuya geçer.

Ne işe yarar?
  - Tableti sürekli açık tutmak zorunda kalmazsınız, ekran ve pil kazanır.
  - Işıkları, sensörleri, kameraları tek dokunuşla panelden yönetirsiniz.
  - Ekran uyurken bile "hazır" beklediği için panele beklemeden ulaşırsınız.


Neler gerekir?
--------------
  - Android 8.0 ve üzeri bir tablet (ön kameralı olması gerekir).
  - Çalışan bir Home Assistant (aynı Wi-Fi ağında).
  - Duvar tabletleri için tabletin prize bağlı olması önerilir.


--------------------------------------------------------------------------------
 KURULUM
--------------------------------------------------------------------------------

1) APK dosyasını tabletinize indirin.

2) İndirdiğiniz dosyaya dokunun. Android "bilinmeyen kaynaklardan yükleme"
   izni isteyebilir. İzin verip yüklemeyi tamamlayın.
   (Uygulama Play Store dışından yüklendiği için telefon ya da tablet bir uyarı
   gösterebilir. Bu normaldir.)

3) BlinkPanel'i açın. İlk açılışta sizi adım adım yönlendiren bir ekran gelir:

   a) "Hareket algılanınca ne açılsın?" sorusuna cevap verin:
        - Dahili panel: Home Assistant'ı uygulamanın içinde tam ekran açar.
          (Çoğu kişi için en kolay seçenek budur.)
        - Home Assistant uygulaması: Tabletinizde kurulu resmi Home Assistant
          uygulamasını açar.

   b) Dahili panel seçtiyseniz Home Assistant adresinizi yazın.
      Örnek: http://192.168.1.50:8123

   c) Hassasiyeti ayarlayın (sonra değiştirebilirsiniz).

   d) İzinleri verin. Her iznin yanındaki "İzin ver" düğmesine basın, verilince
      yeşil tik görünür:
        - Kamera: Önünüzdeki hareketi görmek için.
        - Bildirimler: Uygulamanın çalıştığını gösteren küçük bildirim için.
        - Diğer uygulamaların üzerinde göster: Ekran kapalıyken paneli açabilmesi
          için ÇOK ÖNEMLİ.
        - Pil optimizasyonunu kapat: Android'in uygulamayı arka planda
          kapatmasını engeller. Önerilir.
        - Kullanım erişimi: İsteğe bağlı. Home Assistant uygulaması modunu
          kullanıyorsanız ve ekranın açık kalmasını istiyorsanız verin.

   e) "Başla" düğmesine basın. Hepsi bu kadar.

4) Tabletin kendi ekran zaman aşımını kısa tutun (örneğin 1-2 dakika).
   Ekranı kapatmak için tabletin kendi uyku süresi kullanılır.


--------------------------------------------------------------------------------
 NASIL KULLANILIR?
--------------------------------------------------------------------------------

Kurulumdan sonra yapmanız gereken bir şey yok. Tablet uyurken önüne gelin,
ekran açılır ve panel görünür. Panelle işiniz bitince bekleyin, ekran kendiliğinden
kararır.

  - Ekran kapalıysa: hareket ekranı uyandırır ve paneli açar.
  - Ekran açık ve panel önündeyse: siz hareket ettiğiniz sürece ekran kararmaz.
  - Siz başka bir uygulama kullanıyorsanız: BlinkPanel araya girmez.

Ayarlara girmek için:
  - Panelin sağ alt köşesindeki soluk dişli simgesine dokunun, ya da
  - Bildirim çubuğundaki BlinkPanel bildiriminden "Ayarlar" düğmesine basın.


--------------------------------------------------------------------------------
 AYARLAR (KISACA)
--------------------------------------------------------------------------------

Hareket hassasiyeti
  1-10 arası bir kaydırma çubuğu. Sağa kaydırdıkça küçük hareketlerde bile ekran
  açılır. Çok sık ya da yanlışlıkla açılıyorsa sola kaydırın.

Ekran açık kalma süresi
  Hareket durduktan sonra ekranın kaç saniye açık kalacağı (varsayılan 30 sn).

Yakınlık sensörü
  Tabletinizde varsa, elinizi yaklaştırınca ekran anında uyanır. Kamerayla
  birlikte çalışır. Sensör yoksa bu seçenek pasif görünür.

Başka uygulama açıkken de paneli aç
  Kapalıysa (önerilen) siz başka bir uygulama kullanırken BlinkPanel araya girmez.

Tablet açılınca otomatik başlat
  Açarsanız BlinkPanel'i tabletin ana ekranı olarak seçmeniz istenir. Böylece
  tablet yeniden başlayınca da, Ana Ekran tuşuna basınca da BlinkPanel açılır.


--------------------------------------------------------------------------------
 EKRAN KORUYUCU (İSTEĞE BAĞLI)
--------------------------------------------------------------------------------

Hareket olmadığında ekran kapanmadan önce seçtiğiniz resimler yumuşak geçişle
döner, dilerseniz saat de görünür. Dokunduğunuzda ya da hareket ettiğinizde panele
geri dönülür. Varsayılan olarak KAPALIDIR.

Resim eklemek için:
  Ayarlar > Ekran koruyucu > "Resim ekle". Açılan dosya seçicisinden (Dosyalar,
  Google Fotoğraflar, Drive vb.) birden fazla resim seçin. Resimler uygulamanın
  içine kopyalanır; galeriden silseniz de çalışmaya devam eder (en fazla 60 resim).
  Resimler tablette değilse önce USB ile, Drive/Fotoğraflar ile ya da tarayıcıdan
  tabletinize aktarın.

Neler ayarlayabilirsiniz?
  - Kaç saniye hareketsizlikten sonra başlasın (varsayılan 60 sn)
  - Resim kaç saniyede bir değişsin (varsayılan 15 sn)
  - En fazla kaç dakika çalışsın (varsayılan 10 dk, 0 = sınırsız). Süre dolunca
    ekran normal şekilde uykuya geçer.
  - Parlaklık (varsayılan %30)
  - Saati göster (isteğe bağlı), 24 saat ya da 12 saat biçimi
  - Resmi ekrana doldur (kenarlar kırpılabilir) ya da tamamını göster

Ne zaman çalışmasın? (hepsi isteğe bağlı)
  - Gece saatlerinde: Örneğin 23:00-07:00 arası çalışmaz. İsterseniz bu saatlerde
    hareket ekranı hiç uyandırmasın seçeneğini de açabilirsiniz.
  - Oda karanlıksa: Işıklar kapalıyken çalışmaz (tabletinizde ışık sensörü
    gerekir).
  - Evde kimse yokken: Belirlediğiniz süre (varsayılan 2 saat) hareket olmazsa
    durur.


--------------------------------------------------------------------------------
 İPUÇLARI
--------------------------------------------------------------------------------

  - Tableti kameranın önü açık olacak şekilde yerleştirin. Kameranın önünde
    sallanan perde, TV ışığı ya da yansıma yanlış açılmalara neden olabilir.
  - Ekran çok sık açılıyorsa hassasiyeti düşürün, hiç açılmıyorsa artırın.
  - Tabletin parlaklığını ve ekran zaman aşımını duvardaki kullanımınıza göre
    ayarlayın.
  - Tableti sürekli şarjda tutacaksanız, üreticinin "pil koruma / şarjı %80'de
    sınırla" gibi bir ayarı varsa açmak pil ömrünü uzatır.


--------------------------------------------------------------------------------
 SORUN GİDERME
--------------------------------------------------------------------------------

Ekran hareketle açılmıyor
  - "Diğer uygulamaların üzerinde göster" iznini verdiniz mi? (Ayarlar ekranında
    yeşil tik olmalı.)
  - Pil optimizasyonunu BlinkPanel için kapatın.
  - Bazı markalar (Xiaomi, Huawei, Samsung vb.) arka plandaki uygulamaları
    kapatır. Tabletin ayarlarında BlinkPanel için "arka planda çalışmaya izin
    ver" / "otomatik başlat" seçeneğini açın.
  - Bildirim çubuğunda "Hareket algılama aktif" bildirimi görünüyor mu? Yoksa
    uygulamayı bir kez açın.

Ekran çok sık ya da yanlışlıkla açılıyor
  - Hassasiyeti düşürün (sola kaydırın).
  - Kameranın görüş alanında hareket eden bir şey (perde, TV, yansıma) olmasın.

Ekran kilidi (PIN / desen) istiyor
  - Tabletin kilidi "Yok" ya da "Kaydırma" ise ekran doğrudan açılır. PIN, desen
    ya da parola varsa Android güvenlik gereği önce onu sorar. Bunu uygulama
    atlayamaz.

Home Assistant açılmıyor
  - Adresi kontrol edin (örn. http://192.168.1.50:8123). Tablet ve Home Assistant
    aynı Wi-Fi ağında olmalı.
  - Bağlantı koparsa uygulama 15 saniyede bir kendiliğinden yeniden dener.

"Kullanım erişimi" izni verilemiyor / "Kısıtlı ayar" uyarısı çıkıyor
  Android 13 ve üstünde, Play Store dışından yüklenen uygulamalarda bazı izinler
  ilk başta engellenir. Çözüm:
    Ayarlar > Uygulamalar > BlinkPanel > sağ üstte üç nokta (⋮) > "Kısıtlı
    ayarlara izin ver". Sonra Kullanım erişimi sayfasına tekrar gidin.
  Bu izin isteğe bağlıdır, vermezseniz uygulama yine çalışır.

Ekran koruyucu açılmıyor
  - Ayarlarda açık olduğundan ve en az bir resim ya da saat seçili olduğundan
    emin olun.
  - Gece saati, karanlık oda ya da "evde kimse yok" ayarı devrede olabilir.
  - Home Assistant uygulaması modunda ekran koruyucu kısıtlıdır. Dahili panel
    modunda daha sorunsuz çalışır.


--------------------------------------------------------------------------------
 GİZLİLİK
--------------------------------------------------------------------------------

  - Kamera görüntüsü kaydedilmez, saklanmaz ve hiçbir yere gönderilmez.
    Uygulama yalnızca "önümde hareket var mı?" sorusunu yanıtlamak için görüntüyü
    anlık olarak kontrol eder ve hemen siler.
  - İnternet bağlantısı yalnızca sizin yazdığınız Home Assistant adresini yüklemek
    için kullanılır. Reklam, izleme ya da veri toplama yoktur.
  - Ayarlarınız ve resimleriniz yalnızca tabletinizde saklanır.


--------------------------------------------------------------------------------
 BİLMENİZ GEREKENLER
--------------------------------------------------------------------------------

  - Uygulama arka planda kamerayı kullandığı için pil tüketir. En iyi sonucu
    prize bağlı duvar tabletlerinde verir. Pille çalışan bir tablette şarjın
    daha hızlı azalabileceğini unutmayın.
  - Farklı tablet markalarında ve Android sürümlerinde davranış biraz değişebilir.
  - Ekranı kapatmak için tabletin kendi uyku süresi kullanılır.
  - Hareket algılama basit bir ışık/görüntü karşılaştırmasıdır. Ani ışık
    değişimlerinde yanlışlıkla ekran açılabilir.
  - BlinkPanel resmi bir Home Assistant ürünü değildir. Home Assistant adı ve
    logosu sahiplerinin ticari markasıdır.


Sorun yaşarsanız lütfen tablet modelinizi, Android sürümünüzü ve ne olduğunu
yazarak bildirin. Geri bildirimleriniz uygulamayı geliştirmeme yardımcı olur.

Keyifli kullanımlar!

