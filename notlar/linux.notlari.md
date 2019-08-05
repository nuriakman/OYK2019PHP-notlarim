

# Linux Notları

Linuxta ```halt``` veya ``` sudo shutdown now ```komutu bilgisayarı kapatır.
```sudo shutdown -r ```komutu restart ettirir. Zaman verebilirsin.

Ls -al komutunu kullanarak terminalde bulunduğumuz dizindeki dosyaların ve klasörlerin erişim izinlerini görebiliyoruz.

**owner** - Dosyanın/klasörün sahibi konumundadır. User komutları sadece user kullanıcısı için çalışır.
**group** - Barındırdığı klasör ya da dosyalara etki edebilen user’dan daha az yetkisi olan kısımdır.
**others **- Diğer kullanıcılar anlamına gelir. Genellikle en az yetkiye sahip olan kısımdır.

r - Read
w - Write
x - Execute

read - Dosya ya da  klasörleri okuyabilmeye, görüntüleyebilme izni verir.
write - Dosya ya da klasörleri yazabilme, editleyebilme izni verir.
execute - Dosya ya da klasörleri çalıştırabilme izni verir.
+ Operatörü - Bir dosyaya ya da klasöre herhangi bir izni vermek için kullanılan operatördür.
- Operatörü - Bir dosyaya ya da klasöre herhangi bir izni çıkarmak için kullanılan operatördür.

**Kullanıcı Detayları :**
u - Owner
g - Group
o - Others
a - All users



***Dosya izinlerini değiştirmek:***

Herhangi bir izni user, grup ya da other kullanıcılarına ekleyebilmek için + operatörü, aynı şekilde bir izin çıkartmak için de - operatörü kullanılır.

Herhangi bir dosyanın iznini değiştirmek için chmod komutu kullanılır.

 ```chmod o-rw file1```  file1 dosyasında others kısmından read(r) ve write (w) izinlerini çıkartır.

``` chmod g+rw file1``` file1 dosyasının ait olduğu gruba read® ve write(w) izinlerini ekler.

```lscpu``` komutu CPU hakkında bilgi almaya yarar.

```sudo apt purge``` komutu bilgisayarda o programla ilgili olan o zamana kadar ne yapıldıysa her şeyi kaldırır. Veritabanlarını , dataları tamamen siler.

```sudo apt remove``` komutu programı kaldırır.

```
Sudo apt upgrade
Sudo apt update
Sudo apt list —upgradable
Sudo apt remove
Sudo apt purge
```
```sudo apt purge```  komutu bilgisayarda o programla ilgili olan o zamana kadar ne yapıldıysa her şeyi kaldırır. Veritabanlarını , dataları tamamen siler.

``` ssh-keygen``` komutu ssh fingerprint verir.

--Push yaparken sistem Gitignore klasörünün altındaki dosyaları ignore eder. Projeye dahil etmez.

--.gitignore klasörü projenin root klasöründe olmalı. Ignore etmek istediğin dosyanın pathi yazarsın.

-- Linuxta dosya yükleme işlemi yaparken yazma işlemi yetkisi olması lazım. Windowsta böyle bir kavram yok ama macte ve linuxta grupta apache(www-data) ve write yetkisi olmalı.
