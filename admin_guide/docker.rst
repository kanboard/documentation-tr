Docker ile Kanboard nasıl çalıştırılır?
=======================================

Kanboard, `Docker <https://www.docker.com>`__ ile kolayca
çalıştırabilir.

Disk görüntü-image boyutu yaklaşık **70MB** olup aşağıdakileri içerir:

-  `Alpine Linux <http://alpinelinux.org/>`__
-  `Süreç yöneticisi S6 <http://skarnet.org/software/s6/>`__
-  Nginx
-  PHP 7

Kanboard cronjob’u her gece yarısı çalışıyor. URL yeniden yazma,
birlikte gelen yapılandırma dosyasında etkinleştirilmiştir.

Kapsayıcı-konteyner çalışırken, bellek kullanımı yaklaşık **30MB**
civarındadır.

Kararlı sürümü kullanmak
------------------------

Kanboard’un en kararlı sürümünü elde etmek için **stable** etiketini
kullanın:

.. code:: bash

    docker pull kanboard/kanboard
    docker run -d --name kanboard -p 80:80 -t kanboard/kanboard:stable

Geliştirme sürümünü kullanmak (otomatik yapı)
---------------------------------------------

Depodaki her yeni taahhüt, `Docker
Hub <https://registry.hub.docker.com/u/kanboard/kanboard/>`__ üzerinde
yeni bir yapı oluşturur.

.. code:: bash

    docker pull kanboard/kanboard
    docker run -d --name kanboard -p 80:80 -t kanboard/kanboard:latest

**latest** etiketi, Kanboard’un **geliştirme versiyonudur-development
version**, risk almak kendi sorumluluğunuzdadır.

Kendi Docker görüntü-image oluşturun
------------------------------------

Kendi görüntü-image inızı oluşturmak için Kanboard havuzunda-repository
bir ``Dockerfile`` var. Kanboard havuzunda-repository klonlayın ve
aşağıdaki komutu çalıştırın:

.. code:: bash

    docker build -t youruser/kanboard:master .

veya

.. code:: bash

    make docker-image

Bağlantı noktası 80 üzerinde arka planda kapsayıcı-konteyner çalıştırmak
için:

.. code:: bash

    docker run -d --name kanboard -p 80:80 -t youruser/kanboard:master

Cilt-Volumes
------------

Kapsayıcınıza-konyetner 2 cilt bağlayabilirsiniz:

-  Veri klasörü: ``/var/www/app/data``
-  Eklentiler-Plugins klasörü: ``/var/www/app/plugins``

`Resmi Docker belgeleri <https://docs.docker.com/storage/volumes/>`__
’da açıklandığı gibi, ana makineye bir hacim bağlamak için ``-v``
parametresi-bayrağını kullanın.

Kapsayıcınızı-Konteyner Yükseltme
---------------------------------

-  Yeni görüntü-image koy
-  Eski kapsayıcı-konteyner çıkarın
-  Aynı ciltlere sahip yeni bir kapsayıcı-konteyner yeniden başlat

Ortam Değişkenleri
------------------

Ortam değişkenleri, Kanboard konteyner (Docker) olarak kullanıldığında
yararlı olabilir.

+------+---------------------------------------------------------------+
| Deği | Tanım                                                         |
| şken |                                                               |
+======+===============================================================+
| DATA | ``[Veritabanı türü]://[kullanıcı adı]:[şifre]@[host]:[port]/[ |
| BASE | veritabanı adı]``,                                            |
| _URL | örnek: ``postgres://foo:foo@myserver:5432/kanboard``          |
+------+---------------------------------------------------------------+
| DEBU | Hata ayıklama modunu etkinleştir/devre dışı bırak: “true”     |
| G    | veya “false”                                                  |
+------+---------------------------------------------------------------+

Yapılandırma dosyaları
----------------------

-  Kapsayıcı-konteyner da zaten ``/var/www/app/config.php`` de bulunan
   özel bir yapılandırma dosyası bulunmaktadır.
-  Kendi yapılandırma dosyanızı veri hacmine kaydedebilirsiniz:
   ``/var/www/app/data/config.php``.

Kaynaklar
---------

-  `Resmi Kanboard
   görüntü-image <https://registry.hub.docker.com/u/kanboard/kanboard/>`__
-  `Docker belgeleri <https://docs.docker.com/>`__
-  `Dockerfile kararlı sürümü <https://github.com/kanboard/docker>`__
-  `Dockerfile dev
   sürümü <https://github.com/kanboard/kanboard/blob/master/Dockerfile>`__
