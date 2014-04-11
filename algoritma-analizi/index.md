#   Algoritma Analizi

.fx: first

ensr `<ensar.hamzacebi@bil.omu.edu.tr>`

http://ensr.github.io/

Nisan 2014

---

##  T(n)

-   Problemin boyutu

-   Algoritmada gerçekleştirilen işlem sayısı

        !python

        def sumOfN(n):
            sum = 0
            for i in range(1, n+1):
                sum = sum + 1
            return sum

---

##  Ardışıl (Sequential) Arama

-   Listede sırayla dolaş

-   Aranılan eleman ile karşılaştır

-   Eşleşme sağlandığında çık

---

##  İkil Arama

-   Listeyi küçükten büyüğe sırala

-   Listenin ortasındaki elemana git karşılaştır

-   Aranan eleman daha büyükse

        *   Sağdaki yarım listenin ortasına git

-   Aranan eleman daha küçükse

        *   Soldaki yarım listenin ortasına git

-   Eşleşma sağlanıncaya kadar devam et

---

##  Maliyet

-   n (liste boyu) küçükse bir kere sırala ikil ara

-   n büyükse sıralama maliyetli

-   Ardışıl arama yap

---

##  Hash (Çırpı)

-   Elemanları listeye çakışma olmayacak şekilde yerleştir

-   Daha sonra kolayca erişebileceğimiz şekilde

-   Bellek kullanımını minimuma düşür

-   Her eleman için bir slot belirle ve o slota kaydet

-   Yük oranı = (yerleştirilmiş eleman sayısı) / (liste boyutu)

-   Yük oranını olabildiğince 1'e yaklaştır

---

##  Mükemmel Çırpı

-   Çakışmanın sıfır olduğu hash'dir

-   Liste boyutu eleman sayısı kadardır

-   Yük oranı 1'dir 


