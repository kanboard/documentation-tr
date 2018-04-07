Projeler
========

Proje Tipleri
-------------

İki tür proje vardır:

+--------------+-------------------------------------------------------+
| Tip          | Açıklama                                              |
+==============+=======================================================+
| Takım        | Kullanıcı ve grup yönetimi ile proje                  |
| Projesi      |                                                       |
+--------------+-------------------------------------------------------+
| Özel proje   | Yalnızca bir kişiye ait olan projede, kullanıcı       |
|              | yönetimi yoktur                                       |
+--------------+-------------------------------------------------------+

-  Yalnızca Yöneticiler ve Uygulama Yöneticileri ekip projeleri
   oluşturabilir.
-  Özel projeler herkes tarafından oluşturulabilir.

Proje İzinleri
--------------

Her proje birbirinden izole edilmiş ve birbirinden ayrılmıştır. Proje
erişimine proje sahibi tarafından izin verilmelidir.

Her kullanıcı ve her gruba ayrı bir rol atanabilir.

-  Proje Müdürü
-  Proje Üyesi
-  Proje Görüntüleyicisi

Yalnızca yöneticilerin her şeye erişimi vardır.

Rol atamaları **Proje Ayarları> İzinler** ’den ulaşılabilir:

.. figure:: /_static/project-permissions.png
   :alt: Project Permissions

Özel projeler izin tanımlayamaz.


Projeleri Oluşturma
-------------------

Kanboard birden fazla projeyi idare edebilir. İki tür proje vardır:

-  Takım projeleri
-  Tek bir kullanıcı için özel proje

Birden fazla kullanıcı için proje oluşturma
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Yalnızca yöneticiler ve proje yöneticileri bu projeleri oluşturabilir
-  Kullanıcı yönetimi mevcut

Gösterge tablosundan **Yeni proje** bağlantısını tıklayın:

.. figure:: /_static/new-project.png
   :alt: Project creation form

Çok kolay, sadece projeniz için bir isim bulmanız gerekiyor!

Özel proje oluşturma
~~~~~~~~~~~~~~~~~~~~

-  Herkes özel bir proje yaratabilir
-  Burda kullanıcı yönetimi **YOK**.
-  Projeye yalnızca sahibi ve yöneticiler erişebilir

Gösterge tablosundan **Yeni özel proje** bağlantısını tıklayın.

Başka bir projeden projeler oluşturma
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Yeni bir proje oluşturduğunuzda, başka bir projenin özelliklerini
çoğaltmayı seçebilirsiniz:

-  İzinler
-  Eylemler
-  Swimlanes
-  Katagori
-  Görevler

Projeleri Düzenleme
-------------------

Projeler yeniden adlandırılabilir ve istediğiniz zaman devre dışı
bırakılabilir.

Bir projeyi yeniden adlandırmak için soldaki “Projeyi düzenle”
bağlantısına tıklamanız yeterlidir.

.. figure:: /_static/project-edition.png
   :alt: Project edition

-  Başlangıç tarihi ve bitiş tarihi proje Gantt grafiğini oluşturmak
   için kullanılır
-  Tanım, panoda ve proje listeleme sayfasında araç ipucu olarak görünür
-  Yöneticiler ve proje yöneticileri, “Özel proje” onay kutusunu
   değiştirerek özel bir projeyi birden fazla kullanıcı projesine
   dönüştürebilirler.
-  Birden fazla kullanıcı projesini özel bir projeye
   dönüştürebilirsiniz.

Not: Bir projeyi özel yaptığınızda, mevcut tüm kullanıcılar projeye hâlâ
erişebilir. Kullanıcı listesini ihtiyaçlarınıza göre ayarlayın.

Projeleri Kaldırma
------------------

Bir projeyi kaldırmak için, projenin müdürü veya yönetici olmanız
gerekir.

**“Proje ayarları”** ’na gidin ve sol taraftaki menüden, en alttaki
**“Kaldır”** seçeneğini seçin.

.. figure:: /_static/project-remove.png
   :alt: Removing Projects

Bir projeyi kaldırmak, bu projeye ait tüm görevleri kaldırır.

Pano ve görev paylaşımı
-----------------------

Varsayılan olarak, panolar özel durumdadır, ancak panoyu herkese açık
yapmak mümkündür.

Bir genel kurul **değiştirilemez; salt-okunur bir erişimdir**. Bu erişim
rasgele belirteç (random token) tarafından korunur, yalnızca doğru
URL’ye sahip kullanıcılar panoyu görebilir.

Genel panolar her 60 saniyede bir otomatik olarak yenilenir. Görev
ayrıntıları salt okunur haldedir.

Kullanım örnekleri:

-  Panonuzu kuruluşunuz dışındaki biriyle paylaşın
-  Panoyu ofiste geniş bir ekranda görüntüle

Herkese açık erişimi etkinleştir
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Projenizi seçin, ardından “Herkese açık erişim” i tıklayın ve “Herkese
açık erişimi etkinleştir” düğmesini tıklayın.

.. figure:: /_static/project-enable-sharing.png
   :alt: Enable public access

Genel erişim etkinleştirildiğinde, birkaç bağlantı oluşturulur:

-  Genel pano görünümü
-  RSS beslemesi abonelik bağlantısı
-  iCalendar abonelik bağlantısı

.. figure:: /_static/project-disable-sharing.png
   :alt: Disable public access

Ayrıca, herkese açık erişimi istediğiniz zaman devre dışı
bırakabilirsiniz.

Her seferinde, kamu erişimini etkinleştirir veya devre dışı
bırakırsanız, yeni bir rastgele belirteç (random token) üretilir. \*\*
Önceki bağlantıları artık çalışmayacak \**.


Özel Proje Rolleri
------------------

Bu role ait kişiler üzerinde belirli kısıtlamalar dizisi uygulamak için
özel proje rolleri oluşturabilirsiniz. Bu özel roller her proje için
tanımlanmıştır.

Özel rol, proje üyesi rolünden devralır. Örneğin, birini bir işlemi
takip etmeye zorlamak için özel bir rol oluşturmak isteyebilirsiniz.
Görevleri yalnızca “Devam etmekte olan iş” sütunundan “Bitti” sütununa
taşımanıza izin verilen bir grup insana sahip olabilirsiniz.

Mevcut kısıtlamalar
~~~~~~~~~~~~~~~~~~~

-  Proje Kısıtlamaları:

   -  Görev oluşturulmasına izin verilmiyor
   -  Bir görevi kapatmak veya açmak yasaktır
   -  Görevin taşınmasına izin verilmiyor

-  Sütun Kısıtlamaları:

   -  Görev oluşturulması sadece belirli bir sütun için **izin** verilir
   -  Görev oluşturulması yalnızca belirli bir sütun için **engel**
      lenir
   -  Bir görevi kapatmak veya açmak için sadece belirli bir sütuna
      **izin** verilir
   -  Bir görevi kapatmak veya açmak için yalnızca belirli bir sütun
      için **engel** lenir

-  Görevleri yalnızca belirtilen sütunlar arasında taşıma

Yapılandırma
~~~~~~~~~~~~

1) Yeni bir özel rol oluştur
''''''''''''''''''''''''''''

Proje ayarlarından, **Özel Roller** menüsünde soldaki simgesini tıklayın
ve sayfanın üst kısmında **Yeni özel rol ekleyin** seçeneğini tıklayın.

.. figure:: /_static/new_custom_role.png
   :alt: New custom role

   New custom role

Rol için bir isim verin ve formu gönderin.

2) Rol için bir sınırlama ekleyin
'''''''''''''''''''''''''''''''''

Burada farklı kısıtlamalar vardır:

-  Proje kısıtlamaları
-  Sürükle ve bırak kısıtlamaları
-  Sütun kısıtlamaları

Yeni bir kısıtlama eklemek için tabloda açılır menüye tıklayabilirsiniz:

.. figure:: /_static/add_new_restriction.png
   :alt: Add a new restriction

3) Kısıtlamalar listesi
'''''''''''''''''''''''

.. figure:: /_static/example-restrictions.png
   :alt: List of restrictions

Örneğin, bu rol yalnızca “Geri Kayıt-Backlog” sütununda görevler
oluşturabilir ve görevleri “Hazır” ve “Devam etmekte olan” sütunları
arasında taşımak mümkündür.

4) Rolü birine atayın
'''''''''''''''''''''

Sol menüdeki “izinler” bölümüne gidin ve istenen rolü kullanıcıya
atayın.

.. figure:: /_static/custom_roles.png
   :alt: Custom project role

Örnekler
~~~~~~~~

Kullanıcıların yalnızca belirli sütunlarda görev oluşturmasına izin ver
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure:: /_static/example-restriction-task-creation.png
   :alt: Example restriction task creation

-  Bu role ait kullanıcılar, yalnızca “Geri Kayıt-Backlog” sütununda
   yeni görevler oluşturabilir.
-  2 kuralın kombinasyonu önemlidir, aksi takdirde bu işe yaramaz.

Kullanıcıların görev durumunu yalnızca belirli sütunlarda değiştirmelerine izin ver
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure:: /_static/example-restriction-task-status.png
   :alt: Example restriction task status

-  Bu role ait olan kullanıcılar, “Geri Kayıt-Backlog” sütunundaki görev
   durumunu değiştirebilecek.
-  Durum açık olan görevler tahta üzerinde görünür ve durum kapalı olan
   görevler varsayılan olarak tahtada gizlidir.

Kullanıcıların belirli bir sütundaki görev durumunu değiştirmesine izin verme
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure:: /_static/example-restriction-task-status-blocked.png
   :alt: Example column restriction

Bu role ait kullanıcılar, “Tamamlandı” sütunundaki görev durumunu
değiştiremez. Ancak diğer sütunlarda da mümkün olacaktır.

Kullanıcıların görevleri yalnızca belirli sütunlar arasında taşımasına izin ver
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''

.. figure:: /_static/example-restriction-task-drag-and-drop.png
   :alt: Example restriction task drag and drop

Bu role ait kullanıcılar, görevleri yalnızca “Hazır” ve “Devam etmekte
olan” sütunları arasında taşıyabilir.

Özel Filtreler
--------------

Özel filtreler, herhangi bir arama sorgusunu kaydetmenize izin verir. Bu
şekilde, varsayılan filtreleri kolayca genişletebilir ve en çok
kullanılan arama sorguları kaydedebilirsiniz.

-  Özel filtreler proje tarafından saklanır ve içerik oluşturucuyla
   ilişkilendirilir.
-  Oluşturan proje yöneticisi ise, filtreyi diğer proje üyeleri ile
   paylaşmayı seçebilir.

Filtre oluşturma
~~~~~~~~~~~~~~~~

İşlem açılır menüsüne veya proje ayarlarına gidin ve **özel filtreler**
öğesini seçin:

.. figure:: /_static/custom-filter-creation.png
   :alt: Custom Filter Creation

Filtrenizi oluşturduktan sonra, panoda varsayılan filtrelerin yanında
görünecektir:

.. figure:: /_static/custom-filter-dropdown.png
   :alt: Custom Filter Dropdown
