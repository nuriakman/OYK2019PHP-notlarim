
# PHP Notları


Phpde büyük küçük harf önemi yoktur. Değişkenler büyük küçüük harfe duyarlıdır.
Nokta(.) birleştirme operatörüdür.

```$a=5``` ve ```$b=“5”``` ```if($a == $b)``` dersen true döner ```if($a === $b)``` dersen false döner. Int ve string karşılaştırması yapmak için === kullanarak yap.


```explode(“;”, $degisken)``. değişkeni ; e göre ayırır

```implode(“-”, Dizi)``Dizi aralarına - koyarak birleştirir.

**Count** - dizide kaç tane eleman olduğunu söyler

**Strrev** - stringi tersten yazar


```<pre> ``` tagleri ile satır ve sütunları daha düzgün gösterir. Genelde ```sprintf```  ile yazılır.


form select içerisinde ```autocomplete=“off”``` daha önce yazdığım inputlar gözükmez.
```<input type=“” required>``` yazarsan php devreye girmeden html inputları kontrol eder.


**Session** bir başka sayfada tanımlanana değişkeni kullanmak ve belirli bir süre o değişkeni arka planda kaydetmek için session kullanılır. ```$_SESSION[]```olarak yazılır. Bir sayfada session değişkeni kullanabilmek için sayfanın en başında ```session_Start();``` yazmamız gerekir.

Herhangi bir dosyanın içine ```include```kullanarak başka bir dosya import ettiğinde içeri verdiğin parametre dosyası kayıtlı olmasa bile çalışır hata vermez ama ```require```kullanarak import ettiğinde o dosya yoksa hata verir.

```phpinfo();```komutu bilgisayarda o an yüklü olan php sürümü ile ilgili bilgi verir. Değişiklik yapmak istenirse php.ini dosyasından yapılabilir.

```PHP
mb_internal_encoding(“UTF-8");
if (function_exists('date_default_timezone_set')) {
    date_default_timezone_set('Europe/Istanbul');  // Saat dilimini ayarlayalım...
} else {
    putenv("TZ=Europe/Istanbul"); // Zaman Dilimini TÜRKİYE'ye göre ayarla.
}
```
Yapmaya başladığın projelerin başına bunu yazarsan default olarak zamanı Avrupa-İstanbul ve dili de UTF-8 Türkçe karakterlere duyarlı olarak ayarlar.

### MySqli ve PDO
Mysql ile başlayan bütün komutlar güvenlik açığı bulundurduğu için mysqli komutları kullanılır. Php 7den sonra mysqli kullanmaya başlanır.Mysqli kullanıyorsanı oracle a geçmek zor çünkü kodda mysql geçen her yeri değiştirmen gerekir.


PDO kullanarak bağlanırsan mysqlden oracle a geçtiğinde arka planda veritabanına bağlanmayla olan bölümde sadece bağlantı tanımını değiştirirsin. Pdo sana hangi tür veritabanı kullanacağını sorar. Bağlantı noktasını tanımlarsın ve diğer kodları tanımlamaya gerek yok hangi türü seçersen ona uygun tanımları çalıştırır. Mysql seçersen mysql kodlarını kullanarak çalıştırır.

```mysqli_real_escape_string``` kod içerisinde tek tırnak çift tırnak yani php kod akışını bozacak karakterler varsa bu karakterleri phpnin okuyacağı şekle dönüştürüyor. Değişken içeridine ‘ ifadesi varsa bunu fark edip ./ karakterine dönüştürüyor. Bu şekilde olmasa php tırnaklara duyarlı olduğu için kod açığı ortaya çıkabilir. Güvenlik için mysqli_real_escape_String komutunu kullanırsak iyi olur.
