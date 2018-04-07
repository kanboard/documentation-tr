Windows Kurulum
===============

Windows Server ve Apache üzerinde Kurulum
-----------------------------------------

Bu kılavuz, bir Windows Server’da Apache ve PHP ile adım adım Kanboard
kurmanıza yardımcı olacaktır.

Not: 64 bitlik bir platformunuz varsa “x64” seçin, aksi halde 32-bit
sistemler için “x86” seçeneğini seçin.

Visual C ++ Yeniden Dağıtılabilir-Redistributable Kurulum
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

PHP ve Apache Visual Studio ile derlenmiştir, bu kütüphaneyi henüz
kurmadıysanız yüklemeniz gerekir.

1. Kitaplığı `resmi Microsoft web
   sitesinden <http://www.microsoft.com/en-us/download/details.aspx?id=30679>`__
   indirin.
2. Yükleyicilerden ``vcredist_x64.exe`` veya ``vcredist_x86.exe`` yi
   platformunuza göre çalıştırın

Apache kurulumu
~~~~~~~~~~~~~~~

1. Apache ikili-binary dosyasını `Apache
   Lounge <http://www.apachelounge.com/download/>`__ adresinden indirin.
2. Apache24 ü ``C:\Apache24`` klasörününe sıkıştırılmış dosyaları açın.

Sunucu adını tanımla
''''''''''''''''''''

``C:\Apache24\conf\httpd.conf`` dosyasını açın ve yönergeyi ekleyin:

::

    ServerName localhost

Apache hizmetini-service kur
''''''''''''''''''''''''''''

Bir komut istemi açın (``cmd.exe``) ve ``C:\Apache24\bin`` dizinine
gidin:

.. code:: bash

    cd C:\Apache24\bin

    # Windows hizmetini-service yükle
    httpd.exe -k install

ApacheMonitor’i kur
'''''''''''''''''''

-  ``C:\Apache24\bin\ApacheMonitor.exe`` dosyasına çift tıklayın veya
   başlangıç klasörüne koyun.
-  Simgesine sağ tıklayın ve Apache’yi başlatın.

Apache kurulumunu kontrol edin
''''''''''''''''''''''''''''''

http://localhost/ adresine giderseniz, “It works! / Çalışıyor!” metniyle
birlikte boş bir sayfa görmeniz gerekir.

PHP kurulumu
''''''''''''

1. PHP’nin son kararlı sürümünü `resmi PHP web
   sitesinden <http://windows.php.net/download/>`__ indirin, **İş
   Parçası Güvenli-Thread Safe** sürümünü seçin ve Apache ile aynı yapı
   türünü kullanın: x86 or x64
2. ``C:\php`` klasörüne sıkıştırılmış dosyaları açın
3. PHP klasörüne gidin ve ``php.ini-production`` dosyasını ``php.ini``
   olarak yeniden adlandırın

``php.ini`` yi düzenleyin:

Uzantı dizininindeki yorum işaretlerini-Uncomment kaldırın:

.. code:: ini

    extension_dir = "C:/php/ext"

Şu PHP modüllerininden yorum işaretlerini-Uncomment kaldırın:

.. code:: ini

    extension=php_gd2.dll
    extension=php_ldap.dll
    extension=php_mbstring.dll
    extension=php_openssl.dll
    extension=php_pdo_sqlite.dll

Saat dilimini ayarlayın:

.. code:: ini

    date.timezone = Europe/Istanbul

Desteklenen saat dilimlerinin listesi `PHP
belgeleri <http://php.net/manual/en/timezones.america.php>`__ adresinde
bulunabilir.

Apache için PHP modülünü yükleyin:

Şu yapılandırmayı ``C:\Apache24\conf\httpd.conf`` dosyasına ekleyin:

::

    LoadModule php5_module "c:/php/php5apache2_4.dll"
    AddHandler application/x-httpd-php .php

    # configure the path to php.ini
    PHPIniDir "C:/php"

    # change this directive
    DirectoryIndex index.php index.html

Apache’yi yeniden başlatın.

PHP kurulumunuzu test edin:

``C:\Apache24\htdocs`` klasöründe ``phpinfo.php`` adlı bir dosya
oluşturun:

.. code:: php

    <?php

    phpinfo();

    ?>

http://localhost/phpinfo.php adresine gidin ve PHP kurulumunuzla ilgili
tüm bilgileri görmelisiniz.

Kanboard kurulumu
~~~~~~~~~~~~~~~~~

-  Zipli dosyayı indirin
-  Sıkıştırılmış arşiv dosyasının ``C:\Apache24\htdocs\kanboard``
   klasöründe sıkıştırmasını açın
-  Kanboard’u kullanmak için http://localhost/kanboard/ adresini web
   tarayıcınızı açın
-  Varsayılan kimlik bilgileri **kullanıcı adı:admin/şifre:admin**

Windows üzerinde IIS ile Yükleme
--------------------------------

Bu kılavuz, Kanboard’un IIS ve PHP ile Windows Server’da adım adım
kurulmasına yardımcı olacaktır.

PHP kurulumu
~~~~~~~~~~~~

-  IIS’yi sunucunuza yükleyin (yeni bir rol ekleyin ve CGI/FastCGI’yi
   etkinleştirmeyi unutmayın)
-  Resmi belgeleri izleyerek PHP’yi kurun:

   -  `Microsoft IIS 5.1 ve IIS
      6.0 <http://php.net/manual/tr/install.windows.iis6.php>`__
   -  `Microsoft IIS 7.0 ve
      sonrası <http://php.net/manual/en/install.windows.iis7.php>`__
   -  `PHP for Windows burada
      mevcuttur <http://windows.php.net/download/>`__

PHP.ini
'''''''

En azından bu uzantıları ``php.ini`` dosyanızda bulmanız gerekir:

.. code:: ini

    extension=php_gd2.dll
    extension=php_ldap.dll
    extension=php_mbstring.dll
    extension=php_openssl.dll
    extension=php_pdo_sqlite.dll

Gerekli PHP uzantılarının tam listesi gereksinimler sayfasında dır.

Saat dilimini ayarlamayı unutmayın:

.. code:: ini

    date.timezone = Europe/Istanbul

Desteklenen saat dilimleri listesi `PHP
belgelerinde <http://php.net/manual/tr/timezones.europe.php>`__
bulunabilir.

Notlar:

-  PHP <5.4 kullanıyorsanız, php.ini dosyanızdaki kısa etiketleri
   etkinleştirmeniz gerekir
-  Yukarıda belirtilen gerekli php uzantılarını etkinleştirmeyi
   unutmayın
-  “MSVCP110.dll kütüphanesi eksik / the library MSVCP110.dll is
   missing” konusunda bir hata alırsanız, Microsoft web sitesinden
   Visual Studio için Visual C ++ Yeniden Dağıtılabilir (Visual C++
   Redistributable for Visual Studio) dosyasını indirmeniz gerekebilir.

IIS Modülleri
~~~~~~~~~~~~~

Kanboard arşivi(sıkıştırılmış dosya) URL yeniden yazma özelliğini etkinleştirmek için bir
``web.config`` dosyası içerir. Bu yapılandırma `IIS için yeniden yazma
modülü-Rewrite module for
IIS <http://www.iis.net/learn/extensions/url-rewrite-module/using-the-url-rewrite-module>`__
gerektirir.

Yeniden yazma modülünüz yoksa, IIS’den bir dahili sunucu hatası (500)
alırsınız. Kanboard’da okunabilir-hoş URL’lerle sahip olmak
istemiyorsanız ``web.config`` dosyasını kaldırabilirsiniz.

Kanboard kurulumu
~~~~~~~~~~~~~~~~~

-  Zip-arşivi(sıkıştırılmış dosya) dosyasını indirin
-  Arşivi(sıkıştırılmış dosya) ``C:\inetpub\wwwroot\kanboard`` klasörüne
   sıkıştırılmış dosyaları açınız
-  veri ’dizininin IIS kullanıcısı tarafından yazılabilir olduğundan
   emin olun
-  Kanboard’u kullanmak için web tarayıcınızı açın http: // localhost /
   kanboard /
-  Varsayılan kimlik bilgileri **admin/admin**
