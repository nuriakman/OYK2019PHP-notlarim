# OYK2019PHP
![özgür yazılım yaz kampı](https://kamp.linux.org.tr/2019/yaz/wp-content/themes/oyk-wp-theme/assets/images/oyk2019logo.png)


#### Özgür yazılım yaz kampı Php sınıfında kendi aldığım ders notları

10 , 192 , 172 ile başlayan IP’ler localdir.

Top level domain sitenin temel uzantısı demektir. örn: .com, .gov, .edu, .net

DNS = Site adresini IP adresine çevirir, rehber gibidir.

```lscpu``` komutu linux’ta cpu hakkında bilgi almaya yarar.

```sudo apt purge``` komutu bilgisayarda o programla ilgili olan o zamana kadar ne yapıldıysa her şeyi kaldırır. Veritabanlarını , dataları tamamen siler.

```sudo apt remove``` komutu programı kaldırır.

```
Sudo apt upgrade
Sudo apt update
Sudo apt list —upgradable
Sudo apt remove
Sudo apt purge
```

GitHub'ta yeni bi repo oluşturduğun zaman adresini kopyaladığında terminalde ```git clone``` komutuna yapıştırdığında projeyi bilgisayara alır.

```git add dosyanınadi```

```git commit -m “açıklama”```

```git status``` yazınca hangi dosyada değişiklik yapıldığını gösterir

```git add``` o değişiklik yapılan dosyayı günceller

```git push``` pushlamaya yarar

```sudo apt purge```  komutu bilgisayarda o programla ilgili olan o zamana kadar ne yapıldıysa her şeyi kaldırır. Veritabanlarını , dataları tamamen siler.


``` ssh-keygen``` komutu ssh fingerprint verir.

Terminalde ```cat ~/.ssh/id_rsa.pub ```komutu çalıştırdıktan sonra gelen key değerini GitHub'ta new ssh key kısmına ekleyerek hesap eşleme yapabilirsin.Key değerini yapıştırdıktan sonra

```git config —global “user.email”```
```git config —global “user.name” ``` komutlarını çalıştırıp işlem tamamlanır.

Push yaparken sistem Gitignore klasörünün altındaki dosyaları ignore eder. Projeye dahil etmez.

.gitignore klasörü projenin root klasöründe olmalı. Ignore etmek istediğin dosyanın pathi yazarsın.

```<pre> ``` tagleri ile satır ve sütunları daha düzgün gösterir. Genelde ```sprintf```  ile yazılır.

Linuxta ```halt``` veya ``` sudo shutdown now ```komutu bilgisayarı kapatır.
```sudo shutdown -r ```komutu restart ettirir. Zaman verebilirsin.

form select içerisinde ```autocomplete=“off”``` daha önce yazdığım inputlar gözükmez.
```<input type=“” required>``` yazarsan php devreye girmeden html inputları kontrol eder.

- SQL Komutlarının Bazıları

--LIKE % kullanımı içerisinde "an" ifadesi geçen bütün şehirleri listeler.
 ```SELECT * FROM sehirler WHERE sehir_adi LIKE %an% ```

-- Hatırlamadığın harfleri için _ karakteri kullanabilirsin.
 ```SELECT * FROM sehirler WHERE sehir_adi LIKE %an__a% ```


-- DISTINCT dediğimiz için arabalar tablosunda yakit sütunundaki her yakıt türünden birer tane seçerek gösterir.

``` SQL
SELECT DISTINCT yakit FROM arabalar
```

-- GROUP BY diyerek sıraladığımız zaman aynı veritabanında tekrar eden satırları bize göstermez.
``` SQL
SELECT kelime1, kelime2
FROM esanlam
GROUP BY kelime1, kelime2
```
-- Bu veritabanında tekrar eden satırları bulmak için yazdığımız kod
``` SQL
SELECT kelime1, kelime2
FROM esanlam
GROUP BY kelime1, kelime2
COUNT(*) > 1
```
-- Çift olan kayıtların bilgisinin çekilmesi max(id) ya da min(id) bakarak seçilebilir.
``` SQL
SELECT MAX(id) as id
FROM esanlam
GROUP BY kelime1, kelime2
COUNT(*) > 1
```



-- Çift kayıtların silinmesi
``` SQL
DELETE FROM esanlam
WHERE id IN(
SELECT * FROM (
SELECT MAX(id) AS id FROM esanlam
GROUP BY kelime1, kelime2
HAVING COUNT(*) > 1 )
AS SILINECEKLER )```
