Analizler
=========

Her projenin bir analiz bölümü vardır. Kanboard’u nasıl kullandığınıza
bağlı olarak, şu raporları görebilirsiniz:

Kullanıcı yeniden bölümlendirme
-------------------------------

.. figure:: /_static/user-repartition.png
   :alt: User repartition

   User repartition

Bu pasta grafik kullanıcı başına atanan açık görev sayısını gösterir.

Görev dağıtımı
--------------

.. figure:: /_static/task-distribution.png
   :alt: Task distribution

   Task distribution

Bu pasta grafiği, sütun başına açık görev sayısına genel bir bakış
sunar.

Kümülatif akış diyagramı
------------------------

.. figure:: /_static/cfd.png
   :alt: Cumulative flow diagram

   Cumulative flow diagram

-  Bu grafik, zaman içindeki her bir sütun için toplu olarak görev
   sayısını gösterir.
-  Her gün, her bir sütun için toplam görev sayısı kaydedilir.
-  Kapatılan görevleri hariç tutmak istiyorsanız global proje
   ayarları seçeneğini değiştirin.

Not: Grafiği görmek için en az iki güne kadar veri içermeniz gerekir.

Geribildirim (Burndown) tablosu
-------------------------------

.. figure:: /_static/burndown-chart.png
   :alt: Burndown chart

   Burndown chart

Her proje için `geribildirim (Burndown)
tablosu <#geribildirim-burndown-tablosu>`__
(http://en.wikipedia.org/wiki/Burn_down_chart) mevcuttur.

-  Bu çizelge, zamana karşı yapılan işin grafik bir temsilidir.
-  Kanboard, bu diyagramı oluşturmak için karmaşıklığı veya
   öykü(olay-hikaye) noktasını kullanır.
-  Her gün, her sütunun öykü(olay-hikaye) puanlarının toplamı
   hesaplanır.

Her sütuna harcanan ortalama süre
---------------------------------

.. figure:: /_static/average-time-spent-into-each-column.png
   :alt: Average time spent into each column

   Average time spent into each column

Bu grafik, son 1000 görev için her bir sütuna harcanan ortalama süreyi
gösterir.

-  Kanboard, veriyi hesaplamak için görev geçişlerini kullanır.
-  Harcanan zaman, görev kapanıncaya kadar hesaplanır.

Ortalama Teslim ve Döngü Süresi
-------------------------------

.. figure:: /_static/average-lead-cycle-time.png
   :alt: Average time spent into each column

   Average time spent into each column

Bu grafik, son 1000 görevin zaman içindeki ortalama teslim ve döngü
süresini göstermektedir.

-  Teslim zamanı, görev yaratma ve tamamlanma tarihi arasındaki
   zamandır.
-  Döngü süresi, görevin belirtilen başlangıç tarihi ile bitiş tarihine
   kadar olan zamandır.
-  Görev kapalı değilse, tamamlanma tarihi yerine geçerli saat
   kullanılır.

Bu metrikler, tüm proje için her gün hesaplanır ve kaydedilir.

Not: Doğru istatistikleri elde etmek için günlük-daily
cronjob çalıştırmayı unutmayın.
