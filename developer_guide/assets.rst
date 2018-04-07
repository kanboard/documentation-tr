Varlıklarğ-assets (Javascript ve CSS dosyaları) nasıl oluşturulur
=================================================================

Stil sayfası ve Javascript dosyaları bir araya getirilir ve küçültülür.

-  Orijinal CSS dosyaları ``assets/css/src/*.css`` klasöründe saklanır
-  Orijinal Javascript kodu ``assets/js/src/*.js`` klasöründe saklanır
-  ``assets/*/vendor.min.*`` birleştirilmiş ve küçültülmüş harici
   bağımlılıklardır
-  ``assets/*/app.min.*`` birleştirme ve küçültülmüş uygulama kaynak
   kodu

Gereksinimler
-------------

-  ``npm`` ile `NodeJS <https://nodejs.org/>`__

Javascript ve CSS dosyalarını oluşturma
---------------------------------------

Kanboard, öğeleri oluşturmak için `Gulp <http://gulpjs.com/>`__ ve
bağımlılıkları yönetmek için `Bower <http://bower.io/>`__ kullanır. Bu
araçlar, projeye NodeJS bağımlılıkları olarak yüklenir.

Her şeyi çalıştır
~~~~~~~~~~~~~~~~~

.. code:: bash

    make static

``vendor.min.js`` ve ``vendor.min.css`` leri oluşturun
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: bash

    gulp vendor

``app.min.js`` oluşturun
~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: bash

    gulp js

``app.min.css`` oluşturun
~~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: bash

    gulp css

Notlar
------

Varlıkların oluşturulması Kanboard’un arşivinden mümkün değildir,
havuzun klonlamanız gerekir.
