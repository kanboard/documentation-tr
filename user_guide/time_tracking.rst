Zaman izleme
============

Zaman izleme bilgileri, görev seviyesinde veya alt görev seviyesinde
tanımlanabilir.

Görev zamanı izleme
-------------------

.. figure:: /_static/task-time-tracking.png
   :alt: Task time tracking

Görevlerin iki alanı vardır:

-  Tahmini zaman
-  Harcanan zaman

Bu değerler çalışma saatlerini temsil eder ve manuel olarak ayarlanması
gerekir.

Alt görev zaman izleme
----------------------

.. figure:: /_static/subtask-time-tracking.png
   :alt: Subtask time tracking

Alt görevlerin “geçen süre” ve “zaman tahmini” alanları da vardır.

Bu alanların değerini değiştirdiğinizde **görev zaman izleme değerleri
otomatik olarak güncellenir ve tüm alt görev değerlerinin toplamı haline
gelir**.

Kanboard, her bir alt görev durumu değişikliği arasındaki zamanı ayrı
bir tabloda kaydeder.

-  Alt görev durumunu **todo** dan **devam eden** ne olarak değiştirme
   başlangıç zamanını günlüğüne kaydeder
-  Alt görev durumu **devam eden** dan **tamamlanmış** olarak
   değiştirildiğinde, bitiş saati günlüğe kaydedilir, ancak alt görevin
   ve görevin geöen süresi de güncellenir

Tüm kayıtların dökümü görev görünümü sayfasında görünür:

.. figure:: /_static/task-timesheet.png
   :alt: Task timesheet

Her bir alt görev için zamanlayıcı, istediği zaman durdurulabilir /
başlatılabilir:

.. figure:: /_static/subtask-timer.png
   :alt: Subtask timer

-  Zamanlayıcı, alt görev durumuna bağlı değildir
-  Zamanlayıcıyı her başlatışınızda, zaman takibi tablosunda yeni bir
   kayıt oluşturulur
-  Saati durdurduğunuz her sefer, bitiş tarihi saat izleme tablosuna
   kaydedilir
-  Hesaplanan geçen süre en yakın çeyreğe yuvarlanır (sadece Kanboard <
   1.0.32 için)
