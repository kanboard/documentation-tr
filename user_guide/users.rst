Kullanıcılar
============

Kullanıcı Rolleri
-----------------

Uygulama Rolleri
~~~~~~~~~~~~~~~~

Her Kanboard kullanıcısı bu rollerden birine sahiptir:

+--------+-------------------------------------------------------------+
| Rol    | Açıklama                                                    |
+========+=============================================================+
| Yöneti | Her şeye erişim                                             |
| ci     |                                                             |
+--------+-------------------------------------------------------------+
| Müdür  | Ekip projeleri oluşturabilir, ancak uygulama ayarlarını     |
|        | değiştiremezsiniz                                           |
+--------+-------------------------------------------------------------+
| Kullan | Sadece özel projeler yaratabilir                            |
| ıcı    |                                                             |
+--------+-------------------------------------------------------------+

Proje Rolleri
~~~~~~~~~~~~~

Her bir proje ekip projesi her kullanıcıya ve gruba farklı bir rol
atayabilir:

+--------------+-------------------------------------------------------+
| Rol          | Açıklama                                              |
+==============+=======================================================+
| Proje Müdürü | Proje ayarlarını değiştirebilir, Gantt grafiğine ve   |
|              | raporlara erişebilir                                  |
+--------------+-------------------------------------------------------+
| Proje Üyesi  | Görevler oluşturabilir ve panoyu kullanabilir         |
+--------------+-------------------------------------------------------+
| Proje        | Panoya ve görevlere salt okunur                       |
| Görüntüleyic |                                                       |
| i            |                                                       |
+--------------+-------------------------------------------------------+

Kullanıcılara bir dizi kısıtlama uygulamak için özel proje rolleri
oluşturulabilir.

Kullanıcı Tipleri
-----------------

Kanboard’da iki tür kullanıcı vardır:

+----------+-----------------------------------------------------------+
| Tip      | Açıklama                                                  |
+==========+===========================================================+
| Yerel    | Kullanıcı şifresini Kanboard’un veritabanında saklar      |
| Kullanıc |                                                           |
| ı        |                                                           |
+----------+-----------------------------------------------------------+
| Uzak     | Kullanıcı kimlik bilgileri başka bir sistem tarafından    |
| Kullanıc | yönetilir (Örnek: LDAP sunucusu)                          |
| ı        |                                                           |
+----------+-----------------------------------------------------------+

Uzak kullanıcılara örnekler:

-  LDAP kullanıcısı
-  Ters proxy ile kimlik doğrulamasına tabi tutulmuş kullanıcılar

Grup Yönetimi
=============

Kanboard’da her kullanıcı bir veya daha fazla gruba üye olabilir. Bir
grup bir takım ya da bir organizasyon gibidir.

Yalnızca yöneticiler yeni gruplar oluşturabilir ve kullanıcıları
atayabilir.

Gruplar **Kullanıcı yönetimi>Tüm Grupları Görüntüle** ’den
yönetilebilir. Buradan, gruplar oluşturabilir ve kullanıcıları
atayabilirsiniz.

.. figure:: /_static/groups-management.png
   :alt: Group Management

Dış kimlik, çoğunlukla harici grup sağlayıcıları için kullanılır.
Kanboard otomatik olarak grupları LDAP sunucularından senkronize
et için bir LDAP grup sağlayıcısı sağlar.


Yeni kullanıcı ekle
-------------------

Yeni bir kullanıcı eklemek için bir yönetici olmalısınız.

1. Sağ üst köşedeki açılır menüden **Kullanıcı Yönetimi** seçeneğine
   gidin
2. Üst kısımda bir bağlantı var **Yeni yerel kullanıcı** veya **Yeni
   uzak kullanıcı**
3. Formu doldurun ve kaydedin.

.. figure:: /_static/new-user.png
   :alt: New user

Bir **yerel kullanıcı** oluşturduğunuzda, en azından bu değerleri
belirtmeniz gerekir:

-  **kullanıcı adı**: Bu, kullanıcının benzersiz tanımlayıcısıdır
   (giriş)
-  **şifre**: Kullanıcınızın şifresi en az 6 karakter olmalıdır

**uzak kullanıcı** için yalnızca kullanıcı adı zorunludur.

Kullanıcıları düzenle
---------------------

**kullanıcılar** menüsüne gittiğinizde, kullanıcıların listesine
sahipsiniz. Bir kullanıcıyı değiştirmek için **bağlantıyı-link düzenle**
ye tıklayınız.

-  Normal bir kullanıcısanız, yalnızca kendi profilinizi
   değiştirebilirsiniz
-  Herhangi bir kullanıcıyı düzenleyebilmek için bir yönetici olmak
   zorundasınız.

Kullanıcıları kaldır
--------------------

**kullanıcılar** menüsünden **kaldır** bağlantısını tıklayın. Bu
bağlantı, yalnızca siz yönetici iseniz görünür.

Belirli bir kullanıcıyı kaldırırsanız, **bu kişiye atanan görevler
işlemden sonra atanmamış olacaktır**.

Çift-Kademeli Kimlik Doğrulama
------------------------------

Her kullanıcı `Çift-Kademeli Kimlik Doğrulama two-factor
authentication <http://en.wikipedia.org/wiki/Two_factor_authentication>`__
yı aktyif edebilir. Başarılı bir oturum açtıktan sonra, kullanıcıya
Kanboard’a erişim izni vermeleri için bir kerelik kod (6 karakter)
istenecektir.

Bu kod, genellikle akıllı telefonunuza takılı olan uyumlu bir yazılım
tarafından sağlanmalıdır.

Kanboard, [RFC 6238] (http://tools.ietf.org/html/rfc6238) içinde
tanımlanan [Zamana Dayalı Bir Zamanlık Şifre Algoritması Time-based
One-time Password Algorithm]
(http://en.wikipedia.org/wiki/Time-based_One-time_Password_Algorithm)
kullanır.

Standart TOTP sistemi ile uyumlu birçok yazılım bulunmaktadır. Örneğin,
şu uygulamaları kullanabilirsiniz:

-  `Google
   Authenticator <https://github.com/google/google-authenticator/>`__
   (Android, iOS, Blackberry)
-  `FreeOTP <https://freeotp.github.io/>`__ (Android, iOS)
-  `OATH Toolkit Araç Seti <http://www.nongnu.org/oath-toolkit/>`__
   (Unix/Linux’da Komut satırı yardımcı programı)

Bu sistem çevrimdışı çalışabilir ve mutlaka cep telefonunuz olması
gerekmez.

Kurmak
~~~~~~

1. Kullanıcı profilinize git
2. Sol tarafta **İki faktörlü kimlik doğrulama** seçeneğini tıklayın ve
   kutuyu işaretleyin
3. Sizin için gizli bir anahtar oluşturulur.

.. figure:: /_static/2fa.png
   :alt: 2FA

-  TOTP yazılımında gizli anahtarı kaydetmeniz gerekir. Akıllı telefon
   kullanıyorsanız, en kolay çözüm QR kodunu FreeOTP veya Google
   Authenticator ile taramaktır.
-  Her sefer yeni bir oturum açtığınızda, yeni bir kod sorulur
-  Oturumunuzu kapatmadan önce cihazınızı test etmeyi unutmayın

Bu özelliği her etkinleştirirken / devre dışı bıraktığınızda yeni bir
gizli anahtar oluşturulur.
