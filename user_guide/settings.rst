Ayarlar
=======

Uygulama ayarları
-----------------

Uygulama için bazı parametreler ayarlar sayfasında değiştirilebilir. Bu
ayarları yalnızca yöneticiler değiştirebilir.

Sağ üstteki **Ayarlar** menüsüne gidin, ardından soldaki **Uygulama
ayarları** seçeneğini seçin.

.. figure:: /_static/application-settings.png
   :alt: Uygulama ayarları

Uygulama URL
~~~~~~~~~~~~

Bu parametre, e-posta bildirimleri için kullanılır. E-postalarınızda
altbilgi(footer) alanı, Kanboard görevine bir bağlantı içerir.

Dil
~~~

Uygulama dili her an değiştirilebilir. Dil, tüm kullanıcılar için
belirlenecek.

Saat dilimi
~~~~~~~~~~~

Varsayılan olarak, Kanboard UTC’yi saat dilimi olarak kullanır, ancak
kendi saat dilimini tanımlayabilirsiniz. Liste, web sunucunuz tarafından
desteklenen tüm saat dilimlerini içerir.

Tarih formatı
~~~~~~~~~~~~~

Tarih alanlarında kullanılan girdi biçimi, örneğin görevler için son
tarih.

Kanboard, 4 farklı format sunuyor:

-  DD/MM/YYYY
-  MM/DD/YYYY (varsayılan)
-  YYYY/MM/DD
-  MM.DD.YYYY

`ISO 8601 <http://en.wikipedia.org/wiki/ISO_8601>`__ biçimi daima kabul
edilir (YYYY-MM-DD veya YYYY_MM_DD).

Özel Stil(CSS) Sayfası
~~~~~~~~~~~~~~~~~~~~~~

Kanboard varsayılan stilini geçersiz kılmak veya geliştirmek için kendi
CSS’nizi yazın.

Proje Ayarları
--------------

Sağ üstte bulunan **Ayarlar** menüsüne gidin, ardından soldaki **Proje
ayarları** seçeneğini seçin.

.. figure:: /_static/project-settings.png
   :alt: Project settings

Yeni projeler için varsayılan sütunlar
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Varsayılan sütun adlarını buradan değiştirebilirsiniz. Her zaman aynı
sütunlara sahip projeler oluşturmanız yararlıdır.

Her sütun adı virgül ile ayrılmalıdır.

Varsayılan olarak, Kanboard şu sütun adlarını kullanır: Bekleme
Listesi(Backlog), Hazır, İşlemde ve Tamamlandı.

Yeni projeler için varsayılan kategoriler
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Kategoriler uygulama için genel değildir, ancak bir projeye bağlıdır.
Her proje farklı kategorilere sahip olabilir.

Bununla birlikte, her zaman tüm projeleriniz için aynı kategorileri
oluşturursanız, burada otomatik olarak oluşturulacak kategorilerin
listesini tanımlayabilirsiniz.

Bir kullanıcı için aynı anda yalnızca bir alt görev almasına izin ver
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Bu seçenek etkinleştirildiğinde, bir kullanıcı o anda yalnızca bir alt
görevle çalışabilir.

Başka bir alt görev “devam ediyor” durumuna sahipse, kullanıcı bu
iletişim kutusunu görür:

.. figure:: /_static/subtask-user-restriction.png
   :alt: Subtask user restriction

   Subtask user restriction

Tetikleme otomatik olarak alt görev zamanı izleme
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Bu seçenek etkinleştirilirse, bir alt görev durumu “devam ediyor”
   olarak değiştirildiğinde, zamanlayıcı otomatik olarak başlayacaktır.
-  Zaman izlemeyi kullanmıyorsanız bu seçeneği devre dışı bırakın.

Kümülatif akış diyagramında kapalı görevleri dahil et
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Bu seçenek etkinleştirilirse, kapalı görevler kümülatif akış şemasına
   dahil edilir.
-  Bu seçenek devre dışı bırakılırsa, yalnızca açık görevler dahil
   edilir.
-  Bu seçenek tablonun “toplam” sütununu etkiler
   “project_daily_column_stats”

Pano ayarları
-------------

Sağ Üst menüden **Ayarlar** menüsüne gidin, ardından soldaki **Pano
ayarları** seçimini yapın.

.. figure:: /_static/board-settings.png
   :alt: Board settings

Görev öne çıkarma
~~~~~~~~~~~~~~~~~

Bu özellik, yakın zamanda bir görev taşındığında görevin çevresinde bir
gölge görüntüler.

Bu özelliği devre dışı bırakmak için 0 değerini, varsayılan olarak 2 gün
(172800 saniye) olarak ayarlayın.

2 günden beri taşınan herşey görevin çevresinde gölgeli olacaktır.

Heskese açık paylaşılan Pano(public board) için yenileme aralığı
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Bir panoyu paylaştığınızda, sayfa her 60 saniyede otomatik olarak
varsayılan olarak yenilenir.

Özel Pano için yenileme aralığı
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Web tarayıcınız bir tahtada açık olduğunda, bir şey bir başkası
tarafından değiştirildiğinde Kanboard her 10 saniyede bir kontrol eder.

Teknik olarak bu süreç Ajax yoklaması ile yapılır.

Takvim ayarları
---------------

**Ayarlar** menüsüne gidin, ardından soldaki **Takvim ayarları**
seçeneğini seçin.

.. figure:: /_static/calendar-settings.png
   :alt: Calendar settings

Kanboard’da iki farklı takvim vardır:

-  Proje takvimi
-  Kullanıcı takvimi (dashboard-gösterge tablosundan kullanılabilir)

Proje takvimi
~~~~~~~~~~~~~

Bu takvim, oluşturulma tarihi veya başlangıç tarihine dayanan bitiş
tarihi ve görevleri olan görevleri gösterir.

Görevleri oluşturma tarihe göre göster
''''''''''''''''''''''''''''''''''''''

-  Takvim etkinliğinin başlangıç tarihi, görevin oluşturulma tarihidir.
-  Etkinliğin bitiş tarihi tamamlanma tarihidir.

Görevleri başlangıç tarihine göre göster
''''''''''''''''''''''''''''''''''''''''

-  Takvim etkinliğinin başlangıç tarihi, görevin başlangıç tarihidir.
-  Bu tarih el-ile manuel olarak tanımlanabilir.
-  Etkinliğin bitiş tarihi tamamlanma tarihidir.
-  Başlama tarihi yoksa, görev takvimde görünmez.

Kullanıcı takvimi
~~~~~~~~~~~~~~~~~

Bu takvim yalnızca kullanıcıya atanan görevleri ve isteğe bağlı olarak
alt görev bilgisini gösterir.

Alt görevleri zaman izlemeye göre göster
''''''''''''''''''''''''''''''''''''''''

-  Takvimdeki alt görevleri zaman izleme tablosunda kaydedilen
   bilgilerden görüntüleyin.
-  Kullanıcı zaman çizelgesiyle kesişme noktası da hesaplanır.

Alt görev tahminlerini göster (gelecek çalışmaların tahmini)
''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

-  Alt görevler için “todo” statüsünde ve tanımlanmış “tahmini” değerli
   gelecekteki çalışmalarının tahmini gösterilir.

Bağlantı ayarları
-----------------

Görev ilişkileri, uygulama ayarlarından değiştirilebilir (*\* Ayarlar>
Bağlantı ayarları \**)

.. figure:: /_static/link-labels.png
   :alt: Link Labels

Her etiketin zıt bir etiketi olabilir. Herhangi bir zıtlık yoksa, etiket
iki yönlü olarak değerlendirilir.

.. figure:: /_static/link-label-creation.png
   :alt: Link Label Creation
