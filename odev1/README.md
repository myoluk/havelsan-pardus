# Havelsan Pardus ve Liman Teknoloji Kampı
---
## 1. Gün Ödevi

*1-* _Python kabuğu üzerinde basit fonksiyon geliştirme Uçbirim üzerinde python kabuğu açılmalı, python kabuğu üzerinde fibo (fibonacci dizisi için) kütüphanesini içeri aktararak, dizinin ilk 10 sayısını döndüren bir fonksiyon yazın._

Gerekli kütüphane: `pip install py-fibonacci`
```sh
python3
>>> from fibonacci import fibonacci
>>> fibonacci(10)
[0, 1, 1, 2, 3, 5, 8]
```


*2-* _Kullanıcı bazlı değil, sistem genelinde kalıcı bir çevre değişkeni tanımlanmak istense, hangi sistem dosyası kullanılabilir._

`.bashrc` dosyası kullanılabilir.
```sh
nano .bashrc
```
satır sonuna aşağıdaki satır yazılır ve kaydedilir:
> export degisken='Sistem genelinde degisken'

aşağıdaki komutlar ile değişken sistem genelinde çağrılabilir:
```sh
source .bashrc
echo $degisken
Sistem genelinde degisken
```


*3-* _LVM nedir araştırın._
> LVM (Logical Volume Manager / Mantıksal Hacim Yöneticisi), linux için mevcut disk alanının kolaylıkla yeni disk veya disk bölümleri ilave edilebilmesini, şekillendirilmesini sağlar.


*4-* _Dosya türlerinden Ext4 ve NTFS nedir araştırın._
> Ext4, linux tarafından; NTFS, windows tarafından desteklenen dosya sistemidir.
