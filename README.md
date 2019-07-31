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







