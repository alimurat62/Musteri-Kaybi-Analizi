
# Customer Churn Prediction - Deep Learning Model

## 1. Veri Önişleme

### 1.1 Veri Önişleme Sonuçlarının Yorumları

Veri ön işleme aşaması, modelin başarısı için kritik bir adımdır. Bu adımda, eksik veriler, aykırı değerler, kategorik verilerin işlenmesi ve özelliklerin ölçeklendirilmesi gibi işlemler yapılmıştır. Bu işlemler sonucunda elde edilen verilerin model için uygun hale gelmesi sağlanmıştır. Aşağıdaki adımlar ve sonuçları veri ön işleme sürecinde önemli rol oynamaktadır:

- **Eksik Verilerin İşlenmesi**: Eksik verilerin ortalama, medyan veya başka uygun stratejilerle doldurulması, modelin daha sağlıklı sonuçlar vermesini sağlar. Eksik veri, modelin doğruluğunu olumsuz etkileyebilir.

- **Kategorik Verilerin Sayısal Veriye Dönüştürülmesi**: Kategorik değişkenlerin sayısal verilere dönüştürülmesi (örneğin, One Hot Encoding veya Label Encoding) modelin öğrenmesini kolaylaştırır.

- **Özellik Ölçeklendirme**: Özelliklerin ölçeklendirilmesi (örneğin, StandardScaler kullanarak) derin öğrenme modellerinin daha hızlı ve doğru bir şekilde eğitim almasını sağlar. Özellikle farklı ölçeklere sahip özellikler, modelin öğrenme sürecini zorlaştırabilir.

Sonuç olarak, veri ön işleme süreci doğru bir şekilde tamamlanmış ve veriler modelin öğrenmesi için uygun hale getirilmiştir.

## 2. Veri Görselleştirme

### 2.2 Veri Görselleştirmenin Sonuçlarının Yorumları

Veri görselleştirme, verilerdeki desenleri ve ilişkileri anlamak için önemli bir adımdır. Görselleştirme ile aşağıdaki unsurlar gözlemlenebilir:

- **Veri Dağılımı**: Özelliklerin dağılımını incelemek, verilerdeki dengesizlikleri veya uç değerleri (outliers) tespit etmeye yardımcı olur. Bu tür analizler, veri temizleme sürecinde yol gösterici olabilir.

- **Korelasyon Matrisi**: Özellikler arasındaki ilişkilerin görselleştirilmesi, hangi özelliklerin modelin tahminlerine daha fazla katkı sağladığını anlamamıza yardımcı olur. Yüksek korelasyonlu özellikler birbirinin yerine kullanılabilir, bu da modelin karmaşıklığını azaltabilir.

- **Churn Dağılımı**: Müşteri kaybı (churn) ile ilgili verilerin görselleştirilmesi, churn oranlarını, demografik faktörleri ve diğer özelliklerle olan ilişkilerini anlamamıza yardımcı olur. Bu görselleştirmeler, hedef değişkenin (churn) tahminini etkileyebilecek önemli faktörlerin belirlenmesine olanak tanır.

Veri görselleştirmeleri, verinin daha iyi anlaşılmasına ve sonraki analiz adımlarında doğru kararlar alınmasına yardımcı olmuştur.

## 3. Customer Churn Prediction

### 3.1 Customer Churn Prediction Sonuçlarının Yorumlanması

Müşteri kaybı (churn) tahmin modeli, müşterilerin bir hizmeti terk etme olasılıklarını tahmin etmeye yönelik olarak inşa edilmiştir. Modelin başarısı, aşağıdaki performans metrikleri ile değerlendirilmiştir:

- **Doğruluk (Accuracy)**: Model, eğitim verisi üzerinde %81, test verisi üzerinde ise %84 doğruluk oranlarına ulaşmıştır. Bu, modelin büyük oranda doğru tahminler yaptığını gösterir.

- **Kayıp (Loss)**: Eğitim kaybı %0.41'den %0.16'ya düşerken, test kaybı %0.36'dan %0.17'ye gerilemiştir. Kayıp değerinin düşmesi, modelin optimizasyonunun başarılı olduğunu ve hataların azaldığını gösterir.

- **Karışıklık Matrisi**: Gerçek Pozitifler (True Positives) ve Gerçek Negatifler (True Negatives) oranları oldukça yüksekken, yanlış pozitifler (False Positives) ve yanlış negatifler (False Negatives) oranları düşük çıkmıştır. Bu durum, modelin doğru sınıflandırmalar yapma konusunda başarılı olduğunu gösterüyor.

- **Precision, Recall ve F1-Score**: Precision, recall ve f1-score değerleri %92-93 seviyelerinde. Bu da modelin churn sınıfını doğru bir şekilde tahmin ettiğini ve churn olmayan sınıfı da iyi ayırt ettiğini gösteriyor.

Sonuç olarak, müşteri kaybı tahmin modeli başarılı sonuçlar elde etmiş olup, müşterilerin kaybedilme riskini doğru bir şekilde tahmin etmektedir.

## 4. Müşteri Kaybı Tahmininde Derin Öğrenme

### 4.4 Müşteri Kaybı Tahmininde Derin Öğrenme Sonuçlarının Yorumlanması

Derin öğrenme modeli (Yapay Sinir Ağı), müşteri kaybı tahminini daha hassas bir şekilde yapabilmek için kullanılmaktadır. Modelin performansı, aşağıdaki metriklerle değerlendirilmiştir:

- **Doğruluk Değeri (Accuracy)**: Eğitim ve test doğruluğu değerleri sırasıyla %93.3 ve %92.5'e ulaşmıştır. Bu, modelin iyi genelleme yapabildiğini ve overfitting (aşırı öğrenme) yapmadığını gösteriyor.

- **Kayıp (Loss)**: Eğitim kaybı %0.41'den %0.16'ya, test kaybı ise %0.36'dan %0.17'ye düşmüştür. Bu, modelin öğrenme sürecinde önemli bir iyileşme sağladığını ve hataların azaldığını gösteriyor.

- **Karışıklık Matrisi ve Sınıflandırma Raporu**: Gerçek pozitifler (True Positives) ve gerçek negatifler (True Negatives) oldukça yüksek. Yanlış pozitif ve yanlış negatif oranlarının düşük olması, modelin her iki sınıfı da doğru bir şekilde ayırt etme konusunda başarılı olduğunu gösteriyor.

- **ROC AUC Değeri**: 0.97 ile oldukça yüksek bir AUC değeri elde edilmiştir. Bu, modelin sınıflar arasındaki ayrımı oldukça iyi yapabildiğini gösteriyor.

- **Ortalama Tahmin Edilen Değerler ve Pozitiflerin Oranı**: Modelin tahmin ettiği pozitiflik oranları, gerçek pozitiflik oranlarıyla paralellik göstermektedir. Bu, modelin kalibrasyonunun iyi olduğunu ve tahminlerin doğru olduğunu işaret eder.

Sonuç olarak, derin öğrenme modeli müşteri kaybını başarılı bir şekilde tahmin edebilmiş ve yüksek doğruluk oranlarına ulaşmıştır.

---

## Özet

Bu proje, müşteri kaybı tahminini yapmak için derin öğrenme modellerini kullanarak başarılı sonuçlar elde etmeyi amaçlamaktadır. Aşağıda yapılan işlemlerin özeti verilmiştir:

- **Veri Ön İşleme**: Eksik verilerin doldurulması, kategorik verilerin sayısal verilere dönüştürülmesi ve özelliklerin ölçeklendirilmesi işlemleri başarılı bir şekilde yapılmıştır.
- **Veri Görselleştirme**: Verilerin görselleştirilmesi, verinin yapısını ve ilişkilerini anlamaya yardımcı olmuş ve modelin daha iyi hazırlanmasını sağlamıştır.
- **Customer Churn Prediction**: Müşteri kaybı tahmin modeli doğruluk oranı yüksek, kayıp değeri düşük ve performans metrikleri tatmin edici sonuçlar sunmuştur.
- **Derin Öğrenme**: Derin öğrenme modeli, müşteri kaybı tahmininde yüksek doğruluk oranları ve düşük kayıp değerleriyle başarılı sonuçlar elde etmiştir.

Bu süreçteki her aşama, veri bilimi ve makine öğrenmesi alanındaki en iyi uygulamalarla şekillendirilmiş ve sonuçlar oldukça tatmin edici olmuştur.
