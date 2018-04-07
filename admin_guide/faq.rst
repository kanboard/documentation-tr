Sıkça Sorulan Sorular (F.A.Q. -S.S.S.)
======================================

Kanboard için bir web barındırma sağlayıcısı önerebilir misiniz?
----------------------------------------------------------------

Kanboard, herhangi bir büyük VPS barındırma sağlayıcısı ile iyi çalışır;
`Digital Ocean <https://www.digitalocean.com/?refcode=4b541f47aae4>`__,
`Linode <https://www.linode.com/?r=4e381ac8a61116f40c60dc7438acc719610d8b11>`__
veya `Gandi <https://www.gandi.net/>`__ gibi.

En iyi performansa sahip olmak için, Kanboard’un varsayılan olarak
Sqlite’i kullanması nedeniyle hızlı disk G/Ç(I/O)’si olan bir sağlayıcı
seçin. Paylaşılan bir NFS bağlama noktası kullanan barındırma
sağlayıcılarından kaçının.

“Sisteminizde uygun bir CSPRNG yüklü değil” “There is no suitable CSPRNG
installed on your system” hatası; ———————————————————————–

PHP <7.0 kullanıyorsanız, openssl uzantısının etkinleştirilmesini
sağlamanız gerekir veya eğer bir ``open_basedir`` kısıtlaması ile
kısıtlanmışsa uygulamadan ``/dev/urandom`` alanına erişilebilir
olmalıdır.

Sayfa bulunamadı ve URL yanlış görünüyor (&amp;)
------------------------------------------------

-  URL, ``?controller=auth&action=login&redirect_query=`` yerine
   ``/?controller=auth&amp;action=login&amp;redirect_query=`` gibi
   görünüyor.
-  Kanboard, “Sayfa bulunamadı” hatası döndürür

Bu sayı PHP yapılandırmanızdan geliyor, ``arg_separator.output`` değeri
PHP’nin varsayılanı değil, bunu düzeltmenin farklı yolları var:

Eğer yapabiliyorsanız, doğrudan ``php.ini`` dosyanızdaki değeri
değiştirin:

::

    arg_separator.output = "&"

Değeri ``.htaccess`` ile geçersiz kılın:

::

    php_value arg_separator.output "&"

Aksi takdirde, Kanboard değeri doğrudan PHP’de geçersiz kılmaya
çalışacaktır.

API ve Apache + PHP-FPM ile kimlik doğrulama başarısızlığı
----------------------------------------------------------

Apache altındaki php-cgi, varsayılan olarak HTTP temel
kullanıcı/şifre’sini PHP’ye geçirmiyor. Bu geçici çözümün çalışması için
aşağıdaki şu satırları ``.htaccess`` dosyanıza ekleyin:

::

    RewriteCond %{HTTP:Authorization} ^(.+)$
    RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]

eAccelerator ile bilinen sorunlar
---------------------------------

Kanboard, `eAccelerator <http://eaccelerator.net>`__ ile çok iyi
çalışmıyor. Buna sebep boş bir sayfa veya bir Apache çökmesi olabilir:

::

    [Wed Mar 05 21:36:56 2014] [notice] child pid 22630 exit signal Segmentation fault (11)

Bu sorunu önlemenin en iyi yolu, eAccelerator’ı devre dışı bırakmak veya
hangi dosyaların önbelleklemek istediğinizi ``eaccelerator.filter``
yapılandırma parametresiyle el-ile manuel olarak tanımlamaktır.

`eAccelerator projesi ölü gibi görünüyor ve 2012’den beri
güncellenmedi <https://github.com/eaccelerator/eaccelerator/commits/master>`__.
`OPcache <http://php.net/manual/en/intro.opcache.php>`__ ile
paketlendiğinden PHP’nin son sürümüne geçmenizi öneririz.

Neden minimum gereksinim PHP 5.3.3’tir?
---------------------------------------

Kanboard, parolaları şifrelemek için ``password_hash ()`` işlevini
kullanır, ancak bu işlev yalnızca PHP >= 5.5 için kullanılabilir.

Bununla birlikte, `eski PHP
sürümleri <https://github.com/ircmaxell/password_compat#requirements>`__
için bir arka port var. Bu kütüphane, en azından PHP 5.3.7’nin doğru
çalışmasını gerektiriyor.

Görünüşe göre, Centos ve Debian arka-port güvenlik güncellemeleri yaptı,
böylece PHP 5.3.3 tamam olmalıdır.

Kanboard v1.0.10 ve v1.0.11, en azından PHP 5.3.7 gerektirir, ancak bu
değişiklik, Kanboard >= v1.0.12 ile PHP 5.3.3 ile uyumlu olacak şekilde
geri döndürülmüştür

Kanboard PHP yerel-local dahili web sunucusu ile nasıl test edilir?
-------------------------------------------------------------------

Eğer localhost üzerinde Apache gibi bir web sunucusu kurmak
istemiyorsanız. `PHP’nin gömülü web sunucusu
ile <http://www.php.net/manual/en/features.commandline.webserver.php>`__
test edebilirsiniz:

.. code:: bash

    unzip kanboard-VERSION.zip
    cd kanboard
    php -S localhost:8000
    open http://localhost:8000/
