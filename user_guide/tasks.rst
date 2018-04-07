Görevler
========

Görevler Oluşturma
------------------

Panodan, sütun adının yanındaki artı işaretini tıklayın:

.. figure:: /_static/task-creation-board.png
   :alt: Task creation from the board

Sonra görev oluşturma formu görünür:

.. figure:: /_static/task-creation-form.png
   :alt: Task creation form

Alan açıklamaları:

-  **Başlık**: Panoda görünecek olan görevinizin başlığı.
-  **Tanım**: Markdown biçimini destekleyen
   açıklama.
-  **Etiketler**: Görevlerle ilişkili etiketler listesi.
-  **Başka bir görev oluştur**: Benzer bir görev oluşturmak istiyorsanız
   bu kutuyu işaretleyin (bazı alanlar önceden doldurulacaktır).
-  **Renk**: Kartın rengini seçin.
-  **Atanan**: Görev üzerinde çalışacak kişi.
-  **Kategori**: Göreve yalnızca bir kategori atanabilir (yalnızca
   projelerde kategori varsa görünür).
-  **Kolon**: Görevin oluşturulacağı kolon, göreviniz kolonun en altına
   yerleştirilir.
-  **Öncelik**: Görev önceliği, aralık proje ayarlarında tanımlanabilir,
   varsayılan değerler P0 - P3’tür.
-  **Karmaşıklık**: Çevik proje yönetimi (Scrum) ’da kullanılan
   karmaşıklık veya hikaye puanları, ekibe hikayenin ne kadar zor
   olduğunu anlatan bir sayıdır. Çoğu zaman insanlar Fibonacci serisini
   kullanıyor.
-  **Referans**: Görev için harici kimlik, örneğin başka bir sistemden
   gelen bilet numarası olabilir
-  **Orijinal Tahmin**: Görevi tamamlamak için tahmini saat.
-  **Geçen Süre**: Görev üzerinde geçen süre.
-  **Başlangıç ​​Tarihi**: Bu bir tarih saati alanıdır.
-  **Bitiş Tarihi**: Vadesi geçmiş görevler kırmızı geçerlilik süresine
   sahip olacak ve yaklaşan bitiş tarihleri panoda siyah olacaktır.
   Tarih seçiciye ek olarak birkaç tarih biçimi kabul edilir.

Önizleme bağlantısıyla görev açıklamasının Markdown sözdiziminden
dönüştürülmesini görebilirsiniz.

Görevleri çoğaltmak ve taşımak
------------------------------

Bir görevi aynı projeye çoğalt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Görev görünümüne gidin ve soldaki **Çoğalt** seçeneğini belirleyin.

.. figure:: /_static/task-duplication.png
   :alt: Task Duplication

Orijinalle aynı özelliklere sahip yeni bir görev oluşturulur.

Görevi başka bir projeye çoğalt
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Görev görünümüne gidin ve **Başka bir projeye çoğalt** seçeneğini seçin.

.. figure:: /_static/task-duplication-another-project.png
   :alt: Task Duplication Another Project

Açılır menüde yalnızca üye olduğunuz projeler gösterilecektir.

Görevleri kopyalamadan önce, Kanboard kaynak ve hedef proje arasında
ortak olmayan hedef özellikleri soracaktır.

Temelde şunları tanımlamanız gerekir:

-  Hedef kulvar
-  Sütun
-  Kategori
-  Atanan kişi

Görevi başka bir projeye taşıma
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Görev görünümüne gidin ve **Başka bir projeye taşı** öğesini seçin.

Bir görevi başka bir proje çalışmasına çoğaltma ile aynı şekilde
taşıdığınızda, görevin yeni özelliklerini seçmeniz gerekir.

Çoğaltılan alanların listesi
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Çoğaltılmış özelliklerin listesi aşağıda:

-  title
-  description
-  date_due
-  color_id
-  project_id
-  column_id
-  owner_id
-  score
-  category_id
-  time_estimated
-  swimlane_id
-  recurrence_status
-  recurrence_trigger
-  recurrence_factor
-  recurrence_timeframe
-  recurrence_basedate


Görevleri kapatma
-----------------

Bir görev kapatıldığında, panodan gizlenir.

Bununla birlikte, her zaman arama durumundaki **status:closed**
sorgusunu kullanarak kapalı görev listesine her zaman erişebilir veya
filtre açılır menüsünden **Kapalı görev** seçeneğini belirleyin.

Bir görevi kapatmak için panodaki görev açılır menüsünden iki farklı yol
vardır:

.. figure:: /_static/menu-close-task.png
   :alt: Close a task from drop-down menu

Veya görev ayrıntı görünümündeki görev yan çubuğu menüsünden:

.. figure:: /_static/closing-tasks.png
   :alt: Close task

Not: Bir görevi kapattığınızda, tamamlanmayan alt görevlerin tamamı
“Bitti” durumuna değiştirilir.

Ekran görüntüleri ekleme
------------------------

Zaman kazanmak için görüntüleri doğrudan Kanboard’a kopyalayıp
yapıştırabilirsiniz. Bu görüntüler göreve ek olarak yüklenir.

Bu, örneğin, bir sorunu tarif etmek için ekran görüntülerinin alınması
için özellikle yararlıdır.

Açılır menüye tıklayarak veya görev görünümü sayfasında doğrudan ekran
görüntüleri ekleyebilirsiniz.

.. figure:: /_static/dropdown-screenshot.png
   :alt: Drop-down screenshot menu

Yeni bir görüntü eklemek için ekran görüntüsünü alın ve CTRL+V veya
Command+V ile yapıştırın:

.. figure:: /_static/task-screenshot.png
   :alt: Screenshot page

Mac OS X’te ekran görüntüleri almak için şu klavye kısayolları
kullanabilirsiniz:

-  Command-Control-Shift-3: Ekranın ekran görüntüsünü alın ve kopya
   panoya kaydedin
-  Command-Control-Shift-4, sonra bir alan seçin: Alanın ekran
   görüntüsünü alın ve panoya kaydedin.
-  Command-Control-Shift-4, daha sonra boşluk bırakın, sonra bir
   pencereyi tıklatın: Bir pencerenin ekran görüntüsünü alın ve panoya
   kaydedin

Ek açıklamaları ve şekilleri içeren ekran görüntüleri almak için
kullanılabilecek birkaç üçüncü taraf uygulaması da vardır.

**Not: Bu özellik tüm tarayıcılarda çalışmaz.** Şu hata yüzünden Safari
ile çalışmaz:https://bugs.webkit.org/show_bug.cgi?id=49141

Etiketler
---------

Kanboard ile, bir veya birçok etiketi görevle ilişkilendirebilirsiniz.
Etiketleri genel olarak tüm projeler için veya yalnızca belirli bir
proje için tanımlayabilirsiniz.

.. figure:: /_static/tags-board.png
   :alt: Tags on the board

Görev formundan istediğiniz etiketleri girebilirsiniz:

.. figure:: /_static/tags-task.png
   :alt: Tags form

Otomatik tamamlama formu, kullanılabilir etiketleri önermek için
görünür.

Etiketleri doğrudan görev formundan da oluşturabilirsiniz. Varsayılan
olarak, bir görev formundan etiketler oluşturduğunuzda, bunlar geçerli
projeyle ilişkilendirilir:

.. figure:: /_static/tags-projects.png
   :alt: Project Tags

Tüm etiketler proje ayarlarında yönetilebilir.

Etiketleri tüm projeler için genel olarak tanımlamak için uygulama
ayarlarına gidin:

.. figure:: /_static/tags-global.png
   :alt: Global Tags

Görevleri etiketler temelinde aramak için “tag” özelliğini kullanmanız
yeterlidir:

.. figure:: /_static/tags-search.png
   :alt: Search Tags

Tekrar eden görevler
--------------------

Kanban metodolojisine uymak için, tekrar eden görevler bir tarih
tabanında değil, panoda olaylara dayanır.

-  Seçilen olaylar gerçekleştiğinde, tekrar eden görevler panonun ilk
   sütununa kopyalanır
-  Teslim tarihi otomatik olarak yeniden hesaplanabilir
-  Her görev, onu oluşturan üst görevin görev no(id) ve oluşturulmuş alt
   görevin kaydını tutar

Yapılandırma
~~~~~~~~~~~~

Görev görünüm sayfasına gidin veya panodaki açılır menüyü kullanın,
ardından **Tekrarı düzenleyin** seçeneğini belirleyin.

.. figure:: /_static/recurring-tasks.png
   :alt: Recurring task

Halen yeni tekrar eden bir görev oluşturan 3 tetikleyici vardır:

-  Bir görevi ilk sütundan taşıma
-  Görevin son sütuna taşınması
-  Görevi kapatmak

Son tarihler, mevcut görev üzerinde ayarlanmışsa, verilen gün, ay veya
yıl faktörü ile yeniden hesaplanabilir. Yeni vade tarihinin hesaplanması
için temel tarih, mevcut vade tarihi veya işlem tarihi olabilir.

İç Görev Bağlantıları
---------------------

Görevler önceden tanımlanmış ilişkilerle birlikte birbirine
bağlanabilir:

.. figure:: /_static/internal-task-links.png
   :alt: Task Links

Bu görevler projeler arasında bağlamak için de mümkündür.

Varsayılan ilişkiler şunlardır:

-  **alakalı**
-  **bloklar** \| tarafından engellendi
-  **tarafından engellendi**\ \| bloklar
-  **çoğaltır** \| tarafından çoğaltılan
-  **tarafından çoğaltılan** \| çoğaltır
-  **bir çocuğun** \| bir ebeveyni
-  **’nın ebeveyni** \| bir çocuğu
-  **dönüm noktası hedefliyor** \| bir dönüm noktası
-  **bir dönüm noktası** \| dönüm noktasını hedeflemek
-  **düzeltmeler** \| tarafından düzeltildi
-  **tarafından düzeltildi** \| düzeltmeler

Bu etiketler uygulama ayarlarından değiştirilebilir.

Görev Geçişleri
---------------

Bir görevin sütunlar arasındaki her hareketi veritabanına kaydedilir.

.. figure:: /_static/task-transitions.png
   :alt: Task Transitions

Görev görünümünden ulaşılabilir, şu bilgileri görebilirsiniz:

-  Eylem tarihi
-  Kaynak kolonu
-  Hedef kolon
-  Yürütücü (görevi yerine getiren kullanıcılar)
-  Başlangıç kolonunda geçen süre


Görevler için analiz
--------------------

Her görev, görev görünümünde sol menüden erişilebilen bir analiz
bölümüne sahiptir.

Teslim ve döngü süresi
~~~~~~~~~~~~~~~~~~~~~~

.. figure:: /_static/task-lead-cycle-time.png
   :alt: Lead and cycle time

-  Teslim zamanı, görev yaratma ve tamamlanma tarihi arasındaki zamandır
   (görev kapatıldı).
-  Döngü süresi, başlangıç tarihi ile tamamlanma tarihi arasındaki
   zamandır.
-  Görev kapalı değilse, tamamlanma tarihi yerine geçerli saat
   kullanılır.
-  Başlangıç tarihi belirtilmemişse, çevrim süresi hesaplanmaz.

Not: Görevi seçtiğiniz kolona taşıdığınızda başlangıç tarihini otomatik
olarak tanımlamak için otomatik bir eylem yapılandırabilirsiniz.

Her bir kolonda geçen süre
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: /_static/time-into-each-column.png
   :alt: Time spent into each column

-  Bu grafik, görev için her bir kolonda geçen toplam süreyi gösterir.
-  Geçen süre, görev kapanıncaya kadar hesaplanır.
