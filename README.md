# Naive Bayes ile Diyabet Tahmini
Bayes teoremi:

P ( A | B )= P ( B | A ) P ( A ) /P ( B )


P ( A | B ) = B olayı gerçekleştiğinde A olayının gerçekleşme olasılığı 

P ( A ) = A olayının gerçekleşme olasılığı

P ( B | A ) = A olayı gerçekleştiğinde B olayının gerçekleşme olasılığı 

P ( B ) = B olayının gerçekleşme olasılığı 

Naive Bayes sınıflandırıcısının temeli Bayes teoremine dayanır. lazy ( tembel ) bir öğrenme algoritmasıdır aynı zamanda dengesiz veri kümelerinde de çalışabilir. Algoritmanın çalışma şekli bir eleman için her durumun olasılığını hesaplar ve olasılık değeri en yüksek olana göre sınıflandırır. Az bir eğitim verisiyle çok başarılı işler çıkartabilir. Test kümesindeki bir değerin eğitim kümesinde gözlemlenemeyen bir değeri varsa olasılık değeri olarak 0 verir yani tahmin yapamaz. Bu durum genellikle Zero Frequency ( Sıfır Frekans ) adıyla bilinir. Bu durumu çözmek için düzeltme teknikleri kullanılabilir. En basit düzeltme tekniklerinden biri Laplace tahmini olarak bilinir.

# 1 - Gerekli Kütüphanelerin ve Veri Setinin Yüklenmesi

sklearn.naive_bayes: Naive Bayes algoritmasını kullanmak için gerekli kütüphane.

sklearn.metrics: Doğruluk ve karışıklık matrisi gibi performans metriklerini hesaplamak için kullanılan kütüphane.

sklearn.model_selection: Model seçimi için kullanılan kütüphane, GridSearchCV için gereklidir.

pandas: Veri işleme ve manipülasyonu için kullanılan kütüphane.

sklearn.preprocessing: Veri normalizasyonu için kullanılan kütüphane.

diabetes.csv: Diyabet veri setini içeren CSV dosyası.

# 2 - Veri Setinin Yüklenmesi

diabetes.csv dosyası pandas kullanılarak yüklenir.
Bağımlı değişken ("Outcome") ve bağımsız değişkenler (diğer özellikler) ayrılır.

# 3 - Modelin Eğitilmesi ve Test Edilmesi (Normalize Edilmemiş Veriler İçin)

Veri seti, eğitim ve test kümelerine bölünür.

Multinomial Naive Bayes modeli oluşturulur ve eğitilir.

Model, test kümesi üzerinde değerlendirilir.

Doğruluk ve karışıklık matrisi hesaplanır ve görselleştirilir.

# 4 - Modelin Fine-Tuning İşlemi (Normalize Edilmemiş Veriler İçin)

Veri seti, Min-Max Normalizasyonu kullanılarak normalize edilir.

Normalize edilmiş veri seti üzerinde model yeniden eğitilir.

Model, test kümesi üzerinde değerlendirilir.

Doğruluk ve karışıklık matrisi hesaplanır ve görselleştirilir.

# 5 - Verilerin Normalize Edilmesi ve Modelin Eğitilmesi

Veri seti, Min-Max Normalizasyonu kullanılarak normalize edilir.

Normalize edilmiş veri seti üzerinde model yeniden eğitilir.

Model, test kümesi üzerinde değerlendirilir.

Doğruluk ve karışıklık matrisi hesaplanır ve görselleştirilir.

# 6 - Modelin Fine-Tuning İşlemi 

GridSearchCV kullanılarak modelin hiperparametreleri ayarlanır.

En iyi hiperparametreler bulunur ve model yeniden eğitilir.

Yeniden eğitilmiş model, test kümesi üzerinde değerlendirilir.

Doğruluk ve karışıklık matrisi hesaplanır ve görselleştirilir.
