CentOS’da Kanboard Kurulumu
===========================

Centos 7
--------

PHP’yi ve Apache’ye kurun:

.. code:: bash

    yum install -y php php-mbstring php-pdo php-gd unzip wget

Varsayılan olarak, Centos 7, PHP 5.4.16 ve Apache 2.4.6 kullanır.

Apache’yi yeniden başlatın:

.. code:: bash

    systemctl restart httpd.service

Kanboard’u kurmak:

.. code:: bash

    cd /var/www/html

    # Download the latest release from https://github.com/kanboard/kanboard/releases
    wget https://github.com/kanboard/kanboard/archive/v<version>.zip

    unzip kanboard-<version>.zip
    chown -R apache:apache kanboard-<version>/data
    rm kanboard-<version>.zip

Centos 6.x
----------

PHP’yi ve Apache’yi kurun:

.. code:: bash

    yum install -y php php-mbstring php-pdo php-gd unzip wget

Varsayılan olarak, Centos 6.5, PHP 5.3.3 ve Apache 2.2.15’i kullanır.

Kısa etiketleri etkinleştirin:

-  Dosyayı düzenleyin ``/etc/php.ini``
-  Satırı değiştirin; ``short_open_tag = On``

Apache’yi yeniden başlatın:

.. code:: bash

    service httpd restart

Kanboard’u kurmak:

.. code:: bash

    cd /var/www/html

    # Download the latest release from https://github.com/kanboard/kanboard/releases
    wget https://github.com/kanboard/kanboard/archive/v<version>.zip

    unzip kanboard-<version>.zip
    chown -R apache:apache kanboard-<version>/data
    rm kanboard-<version>.zip

SELinux kısıtlamaları
---------------------

SELinux etkinleştirilmişse, Apache kullanıcısının dizin verilerine
yazabildiğinden emin olun:

.. code:: bash

    chcon -R -t httpd_sys_content_rw_t /var/www/html/kanboard/data

Sunucunuzu, SELinux’la olduğu gibi, Kanboard’un e-posta göndermelerine
ve harici ağ istekleri almasına izin verecek şekilde yapılandırmalarını
sağlayın:

.. code:: bash

    setsebool -P httpd_can_network_connect=1

LDAP, SMTP, Web kancaları veya herhangi bir üçüncü taraf entegrasyonu
kullanıyorsanız harici bağlantılara izin verilmesi gereklidir.

Notlar
------

Kanboard’un bazı özellikleri, günlük arka plan işleri çalıştırmanızı gerektirir.
