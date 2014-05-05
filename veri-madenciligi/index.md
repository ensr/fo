#   Veri Madenciliği

.fx: first

ensr `<ensar.hamzacebi@bil.omu.edu.tr>`

http://ensr.github.io/

Mayıs 2014

---

##  Soru - Cevap Algoritması

![Soru Cevap Algoritması](media/ibm)

---

##  Standardization

-   Bu bölümde kullanıcı sorusu insert edilir

-   Standardization üç aşamadan oluşur

    *   Tüm soruyu kontrol et ve bütün harfleri küçük yap

    *   Tüm ekstra kelimeleri(ve, ile, de, da) çıkart

    *   Tüm kelimeleri analiz et ve sonlarındaki ekleri sil

---

##  Sentence Processing

-   Bir önceki aşamadan gelen kelimeler incelenir

-   Kelimelerin yapısına bakılarak sorunun tipi belirlenir

-   Soru tipi baz alınarak cevabın türü de belirlenir

---

##  Retrieval System

-   Veritabanından rastgele cümleler çekilir

-   Çekilen cümleler Ranking system'a gönderilir

---

##  Ranking System

-   Veritabanından çekilen cümlelerin sıralandığı aşama

-   Sıralama yapılırken aşağıdakilere bakılır:

    *   Soru cümlesindeki kelimeler ile cevap cümlesindeki kelimelerin uyumu

    *   Soru cümlesinin tipi ile cevap cümlesinin tipinin uyumuna

-   Sıralama işlemi beş aşamadan oluşur

---

##  Adım 1: Initial evaluation

-   Her cevap cümlesi için iki değişken tutulur (fit1, fit2)

-   fit1 : Kelimelerin karşılaştırılma sonucu

-   fit2 : Cümle tiplerinin karşılaştırılma sonucu

        Global fitness(i)= (Fit1(i)*W1) +(Fit2(i)*W2)

-   W1=0.4 W2=0.6 sabit sayılar

---

##  Adım 2: Sorting

-   Her cevap cümlesi Globall fitness değerine göre bir listede sıralanır

-   Bubble Sort kullanılır

---

##  Adım 3: Mutation

-   Mutation işlemi artifical immune algoritması ile yapılır

-   Fitness değeri 1.1 den dazla ise bir kere yapılır

-   0.4 ile 1.0 arası ise dört kez yapılır

-   0 ile 0.3 arası ise altı kez yapılır

---

##  algoritma

---

##  Adım 4: Second Evaluation

-   num_iter sayısı kere yukarıdaki adımlar tekrarlanır

---

##  Adım 5: Return Answer

-   Global fitness değeri en yüksek olan cevap olarak döndürülür

---

##  Display Final Answer

-   Yanlış cevapların döndürüllmesinin engellendiği kısımdır

-   Global fitness' ı 1 olan cevaplar yanlış olabilir

-   1.1 den küçük ise <NOT FOUND> döndürülür




