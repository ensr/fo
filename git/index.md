#   Git

.fx: first

Ensar Hamzaçebi `<ensar.hamzacebi@bil.omu.edu.tr>`

Fatma Tercan `<fatma.tercan@bi.omu.edu.tr>`

Mart 2014

---

##  Git Nedir

-   Dağınık Versiyon Kontrol Sistemi

-   Kod deposu çok merkezden yönetilebilir

-   Open source


---


##  Çözüm Üretilen Problemler

-   Kodlar güvenli bir şekilde saklanır

-   Projede birden çok kullanıcı değişiklik yapabilir

-   Karışıklıkların önüne geçilir

---

##  Çözüm Üretilen Probemler

-   Ne zaman hangi değişiklik yapıldı görülür

-   Offline olarak çalışılabilir

-   Gereksinimlere göre projede dallanma yapılır

---

##  Git Alternatifleri

-   CVS (Concurrent Version System)

-   SVN

-   BitKeeper

-   Mercurial

-   Perforce

-   Bazaar

-   Saire

---

##  Avantajlar

-   Hızlıdır

-   Merkezil değil dağınıktır

-   Disk alanı verimli kullanılır

-   Conflict oluşma riski oldukça azdır

-   Veri kaybı olmaz

-   Öğrenmesi kolaydır

---

##  Dezavantajlar

-   ???

---

##  Geliştiriciler

-   Linus Torvalds

-   Junio Hamano

---

##  Kurulum

        !sh

        $ sudo apt-get install git

-   Debian/Ubuntu üzerinde kurulum bu şekildedir

---

##  Depo Oluşturma

github.com'dan depo oluşturma

-   create -> New repostory

-   Deponun adı girilir

-   Public/Private seçilir

-   Create repository tıklanır

---

##  Depo Oluşturma

-   Yerelde boş bir dizin oluşturulur ve dizine girilir

-   Depo ilklenir (initializing)

        !sh

        $ git init

-   `.git` otomatik olarak oluşturulur

        *   Depo ile ilgili bilgiler tutulur

        *   ???

---

##  Depoya Dosya Ekleme

-   Bütün depoyu ekleme

        !sh

        $ git add .

-   Belirli bir dosyayı ekle

        !sh

        $ git add <dosya_adi>

---

##  Yerelde Değişiklikleri Kaydetme

-   `git commit` kullanılır

        !sh

        $ git commit -a -m "<metin>"

---

##  Uzaktaki Depoya Gönderme

-   `git push` ile gönderilir

-   master dalına push etme

        !sh

        $ git push origin master

-   gh-pages dalına push etme

        !sh

        $ git push origin gh-pages

---

##  Uzak Depodan Yerelin Güncellenmesi

        !sh

        $ git pull

---

##  Mevcut Dizini Depo Yapma

-   Github'da repo oluştur

-   Yereldeki mevcut dizinde:

        !sh

        $ touch README.md

        $ git init

        $ git add README.md

        $ git commit -m "first commit"

        $ git remote add origin git@github.com:ensr/gitDeneme.git

        $ git push -u origin master

---

##  Depo Klonlama

-   Github'daki depoyu klonlama

        !sh

        $ git clone git@github.com:<hesap>/<depo>.git

---

##  SSH Protokolü

-   En çok kullanılan erişim yöntemi

-   Depoyu oku - Depoya yaz

-   Erişim güvenlidir

-   Tüm data şifrelenir

-   Sadece kendi makinenizden erişim mümkün

---

##  Git Protokolü

-   Erişim güvenliği yok

-   Depo herkes tarafından clonlanabilir

-   Depo'ya push yapılamaz (read-only accses)

-   En hızlı erişim yöntemi

---

##  Http/s Protokolü

-   Kurulumu kolay

-   read-only accses

-   ???

---

##  Yeni Dal Oluşturma

-   Yeni dal oluşturma `branch` ile yapılır

        !sh

        $ git branch <yeni_dal_adı>

---

##  Dallar Arası Geçiş

-   İstenilen dala `checkout` ile geçilir

        !sh

        $ git checkout <dal_adı>

-   Dalı oluştur ve dala geç

        !sh

        $ git checkout -b <yeni_dal_adı>

---

##  Dalları Birleştirmek

-   Önce master dalına geçilir

        !sh

        $ git checkout master

-   Dallar birleştirilir

        !sh

        $ git merge <dal_adi>

---

##  Yapılandırma Dosya ve Dizinleri

-   `/etc/gitconfig` sistemdeki tüm kullanıcıların ayarlarını tutar

        !sh

        $ git config --system <komut>

-   `~/.gitconfig` kullaniciya özeldir

        !sh

        $ git config --global<komut>

-   `<yerel_depo>/.git/config` bulundğu depoya özeldir

    *   Diğer ayarları override eder

    *   `.git/config` `/etc/gitconfig`'den daha baskındır

---
