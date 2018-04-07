LDAP Yapılandırma Parametreleri
===============================

Kullanılabilir LDAP parametrelerinin listesi aşağıdadır:

+-----------------------+------------+---------------------------------+
| Parametre             | Varsayılan | Açıklama                        |
|                       | değer      |                                 |
+=======================+============+=================================+
| ``LDAP_AUTH``         | false      | LDAP kimlik doğrulamasını       |
|                       |            | etkinleştir                     |
+-----------------------+------------+---------------------------------+
| ``LDAP_SERVER``       | Empty      | LDAP sunucusu ana makine adı    |
+-----------------------+------------+---------------------------------+
| ``LDAP_PORT``         | 389        | LDAP server port                |
+-----------------------+------------+---------------------------------+
| ``LDAP_SSL_VERIFY``   | true       | ``ldaps://`` stil URL’si için   |
|                       |            | sertifikayı doğrulama           |
+-----------------------+------------+---------------------------------+
| ``LDAP_START_TLS``    | false      | LDAP başlangıç TLS’i            |
|                       |            | etkinleştir                     |
+-----------------------+------------+---------------------------------+
| ``LDAP_USERNAME_CASE_ | false      | Kanboard, yinelenen             |
| SENSITIVE``           |            | kullanıcılardan kaçınmak için   |
|                       |            | ldap kullanıcı adını küçük      |
|                       |            | harflerle yazmaktadır           |
|                       |            | (veritabanı büyük/küçük harf    |
|                       |            | duyarlıdır)                     |
+-----------------------+------------+---------------------------------+
| ``LDAP_BIND_TYPE``    | anonymous  | Bağ türü: “anonim”, “kullanıcı” |
|                       |            | veya “vekil”                    |
+-----------------------+------------+---------------------------------+
| ``LDAP_USERNAME``     | null       | Kullanıcı moduyla kullanılacak  |
|                       |            | proxy modu veya kullanıcı adı   |
|                       |            | kalıbıyla kullanılacak LDAP     |
|                       |            | kullanıcı adı                   |
+-----------------------+------------+---------------------------------+
| ``LDAP_PASSWORD``     | null       | Proxy modu için kullanılacak    |
|                       |            | LDAP şifresi                    |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_BASE_DN`` | Empty      | Kullanıcılar için LDAP DN       |
|                       |            | (Örnek:                         |
|                       |            | “CN=Kullanıcılar,DC=kanboard,DC |
|                       |            | =yerel”)                        |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_FILTER``  | Empty      | Kullanıcı hesabı ararken        |
|                       |            | kullanılacak LDAP deseni        |
|                       |            | (Örnek:                         |
|                       |            | “(&(objectClass=user)(sAMAccoun |
|                       |            | tName=%s))”)                    |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_ATTRIBUTE | uid        | Kullanıcı adı için LDAP         |
| _USERNAME``           |            | özelliği (Örnek:                |
|                       |            | “samaccountname”)               |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_ATTRIBUTE | cn         | Kullanıcı tam adı için LDAP     |
| _FULLNAME``           |            | özelliği (Örnek: “displayname”) |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_ATTRIBUTE | mail       | Kullanıcı e-postası için LDAP   |
| _EMAIL``              |            | özelliği                        |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_ATTRIBUTE | memberof   | Kullanıcı profilinde gruplar    |
| _GROUPS``             |            | bulmak için LDAP özniteliği     |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_ATTRIBUTE | Empty      | Kullanıcı fotoğrafını bulmak    |
| _PHOTO``              |            | için LDAP özniteliği (jpegPhoto |
|                       |            | veya thumbnailPhoto)            |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_ATTRIBUTE | Empty      | Kullanıcı dili için LDAP        |
| _LANGUAGE``           |            | özniteliği (preferredlanguage), |
|                       |            | kabul edilen dil biçimi “fr-FR” |
+-----------------------+------------+---------------------------------+
| ``LDAP_USER_CREATION``| true       | Otomatik LDAP kullanıcı         |
|                       |            | yaratmayı etkinleştir           |
+-----------------------+------------+---------------------------------+
|``LDAP_GROUP_ADMIN_DN``| Empty      | Yöneticiler için LDAP DN        |
|                       |            | (Örnek:                         |
|                       |            | “CN=Kanboard-Admins,CN=Users,DC |
|                       |            | =kanboard,DC=local”)            |
+-----------------------+------------+---------------------------------+
| ``LDAP_GROUP_MANAGER_ | Empty      | Müdürler için LDAP DN (Örnek:   |
| DN``                  |            | “CN=Kanboard                    |
|                       |            | Managers,CN=Users,DC=kanboard,D |
|                       |            | C=local”)                       |
+-----------------------+------------+---------------------------------+
|``LDAP_GROUP_PROVIDER``| false      | Proje izinleri için LDAP grup   |
|                       |            | sağlayıcısını etkinleştirin     |
+-----------------------+------------+---------------------------------+
| ``LDAP_GROUP_BASE_DN``| Empty      | Gruplar için LDAP Tabanı DN     |
|                       |            |                                 |
+-----------------------+------------+---------------------------------+
| ``LDAP_GROUP_FILTER`` | Empty      | LDAP grup filitresi (Örnek:     |
|                       |            | “(&(objectClass=group)(sAMAccou |
|                       |            | ntName=%s*))“)                  |
+-----------------------+------------+---------------------------------+
| ``LDAP_GROUP_USER_FIL | Empty      | Kanboard, tanımlandıysa,        |
| TER``                 |            | LDAP_GROUP_BASE_DN ’deki        |
|                       |            | kullanıcı gruplarını bu filtre  |
|                       |            | ile arayacaktır, yalnızca       |
|                       |            | posixGroups için kullanışlıdır  |
|                       |            | (Örnek:                         |
|                       |            | ``(&(objectClass=posixGroup)(me |
|                       |            | mberUid=%s))``)                 |
+-----------------------+------------+---------------------------------+
| ``LDAP_GROUP_ATTRIBUT | cn         | Grup adı için LDAP özniteliği   |
| E_NAME``              |            |                                 |
+-----------------------+------------+---------------------------------+

Notlar:

-  LDAP nitelikleri küçük harflerle yazılmış olmalıdır
