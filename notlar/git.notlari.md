# Git ve GitHub Notları

GitHub'ta yeni bi repo oluşturduğun zaman adresini kopyaladığında terminalde ```git clone``` komutuna yapıştırdığında projeyi bilgisayara alır.

```git log``` yazdığında hangi tarihi istiyorsan projede o veriyi verir.

```git log —oneline``` aynı çıktıyı tek satıda verir

```git checkout LOGID``` yazarsan logıd yazdığın ana döner(geçmişe)

```git checkout master``` projenin son güncel haline geri döner

Herhangi bir projeyi git projesin çevirmenin yolu git init yazmaktır.(repo oluşturmak olarak düşün)

```git add``` dosyanınadi

```git commit -m “açıklama”```

```git status``` yazınca hangi dosyada değişiklik yapıldığını gösterir

```git add``` o değişiklik yapılan dosyayı günceller

```git commit -m “açıklama”``` komutu da güncellenen dosyayı commit etmemizi sağlar

```git push``` pushlamaya yarar

```git pull`` komutuyla locale aldığın projelerde değişiklik olduysa değişiklikleri kaydeder.

```git reset —hard``` komutu dosyayı aldığın git pull haline geri döndürür.

-- Push yaparken sistem Gitignore klasörünün altındaki dosyaları ignore eder. Projeye dahil etmez. (gitignore.io)

-- .gitignore klasörü projenin root klasöründe olmalı. ignore etmek istediğin dosyanın pathi yazarsın.

``` ssh-keygen``` komutu ssh fingerprint verir.

Terminalde ```cat ~/.ssh/id_rsa.pub ```komutu çalıştırdıktan sonra gelen key değerini GitHub'ta new ssh key kısmına ekleyerek hesap eşleme yapabilirsin.Key değerini yapıştırdıktan sonra

```git config —global “user.email”```
```git config —global “user.name” ``` komutlarını çalıştırıp işlem tamamlanır.

## Forklanan Bir Projeyi Güncel Tutmak

- GitHub hesabınızda forkladığınız projeyi açın.

- Sağ tarafta bulunan **Compare**(Karşılaştır) butonuna tıklayın.

- Karşımıza çıkan ekranda **Try Switching the Base** linkine tıklayın. Bu linke tıkladıktan sonra proje sahibinin siz projeyi forkladıktan sonra yaptığı değişiklikleri göreceksiniz.

- Ekranda **Create Pull Request** (Yeni İstek Oluştur) butonuna tıklayın. Bir sonraki ekranda istek gönderirken **commit**(yorum) yazmak isterseniz buradaki forma yazın ve  **Create Pull Request** butonuna tıklayın.

- Bir sonraki sayfanın aşağısında **Merge Pull Request** ve **Confirm Merge** butonlarına tıkladıktan sonra projeniz güncellenecektir.
