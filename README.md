
# Müşteri Kaybı Tahmin Projesi (Customer Churn Prediction)

Bu proje, müşteri kaybı (customer churn) tahminini gerçekleştirmek için veri ön işleme, görselleştirme, makine öğrenimi ve derin öğrenme yöntemlerini kullanarak geliştirilmiştir. Proje sürecinde veri analizi ve modelleme aşamaları detaylı şekilde ele alınmış, ardından elde edilen sonuçlar yorumlanmıştır.

## Gerekli Kütüphaneler

Projede kullanılan kütüphaneler:

- **pandas**: Veri işleme ve analiz için
- **numpy**: Sayısal işlemler için
- **scikit-learn**: Makine öğrenimi algoritmaları için
- **matplotlib**: Grafikler ve görselleştirme için
- **seaborn**: İleri düzey görselleştirmeler için
- **tensorflow**: Derin öğrenme için

## Veri Seti

Veri seti aşağıdaki özelliklerden oluşmaktadır:

- **age**: Müşterinin yaşı
- **gender**: Cinsiyet 
- **security_no**: Güvenlik numarası
- **region_category**: Bölge kategorisi 
- **membership_category**: Üyelik kategorisi 
- **joining_date**: Üyelik tarihi
- **joined_through_referral**: Tavsiye ile üye olma durumu
- **referral_id**: Tavsiye kimliği
- **preferred_offer_types**: Tercih edilen teklif türleri
- **medium_of_operation**: İşlem aracı
- **internet_option**: İnternet bağlantı seçeneği
- **last_visit_time**: Son ziyaret zamanı
- **days_since_last_login**: Son girişten bu yana geçen gün sayısı
- **avg_time_spent**: Ortalama harcanan zaman
- **avg_transaction_value**: Ortalama işlem değeri
- **avg_frequency_login_days**: Ortalama giriş sıklığı
- **points_in_wallet**: Cüzdandaki puan miktarı
- **used_special_discount**: Özel indirim kullanımı
- **offer_application_preference**: Teklif başvuru tercihi
- **past_complaint**: Geçmişteki şikayetler
- **complaint_status**: Şikayet durumu
- **feedback**: Geri bildirim
- **churn_risk_score**: Churn risk skoru

## Veri Ön İşleme ve Hazırlık

Aşağıdaki işlemler veri ön işleme aşamasında gerçekleştirilmiştir:

1. **Kütüphanelerin Yüklenmesi**: Pandas, Numpy, Seaborn, Matplotlib ve Scikit-learn kütüphaneleri yüklenmiştir.
2. **Veri Seti Yükleme**: Veri seti yüklenmiş ve ilk 10 satır görüntülenmiştir.
3. **Geçersiz Değerlerin Düzeltilmesi**: Geçersiz değerler NaN ile değiştirilmiş ve gereksiz sütunlar kaldırılmıştır.
4. **Eksik Verilerin Doldurulması**: Eksik veriler, sütunun mod veya medyanı ile doldurulmuştur.
5. **Tarih Formatı ve Kodlama**: Tarih formatları düzeltilmiş ve bazı kategorik sütunlar sayısal verilere dönüştürülmüştür.
6. **Kategorik Verilerin Sayısal Verilere Dönüştürülmesi**: Kategorik sütunlar sayısal verilere dönüştürülmüştür.
7. **Veri Kaydetme**: Sonuçlar, modellerde kullanılmak üzere kaydedilmiştir.

## Veri Görselleştirme

Veri görselleştirme aşamasında aşağıdaki analizler gerçekleştirilmiştir:

1. Yaş aralıklarına göre gruplandırma 
- 20-50 yaş arası bireyler, müşteri kitlesinin çoğunluğunu oluşturuyor ve yaş ilerledikçe müşteri sayısı belirgin şekilde azalıyor.

2. Bölge Kategorisine Göre Churn Risk Dağılımı:
- Şehir ve kasaba kategorilerinde churn riski daha yüksekken, köy kategorisinde daha düşük riski var.
- Coğrafi faktörler, kullanıcıların platformda kalmalarını etkileyebilir.

3. Üyelik Kategorisine Göre Churn Risk Dağılımı:
- Gold üyeler daha düşük churn riski gösteriyor, bu da üyeliklerin kullanıcı bağlılığını artırabileceğini gösteriyor.
- No Membership (Üyelik Yok) kategorisi yüksek churn riski taşıyor.

4. Üyelik Kategorisine Göre Ortalama Harcanan Zaman:
- Premium üyelik kategorisi, en yüksek ortalama zaman harcamayı gösteriyor.

5. Şikayet Durumuna Göre Churn Risk Dağılımı:
- Şikayet durumu olan kullanıcıların churn riski daha yüksek.

6. Tavsiye Durumuna Göre Churn Risk Dağılımı:
- Tavsiye yoluyla üye olan kullanıcılar, daha yüksek churn riski taşıyor.

7. Churn Riskine Göre Tercih Edilen Teklif Türleri:
- Gift Vouchers/Coupons kullanıcıları daha fazla churn riski gösteriyor.

8. Cinsiyete Göre Ortalama Harcama:
- Cinsiyet farkı olmadan benzer harcama eğilimleri gözlemleniyor.

9. İnternet Seçeneğine Göre Ortalama Harcama:
- Fiber Optic ve Mobile Data kullanıcıları daha yüksek harcama yapıyor.

10. Ortalama Zaman Harcama ve Şikayet Durumu:
- Şikayet durumu olmayan kullanıcılar daha fazla zaman harcıyor.

11. Cüzdan Puanlarına Göre Churn Riski:
- Cüzdan puanları arttıkça churn riski azalıyor.

12 .Özel İndirim Kullanımına Göre Ortalama Giriş Sıklığı:
- Özel indirimlerin giriş sıklığı üzerinde önemli bir etkisi yok.

13. Korelasyon Matrisi:
- Yaş, cinsiyet, bölge kategorisi gibi değişkenler arasında düşük korelasyonlar gözlemleniyor, ancak üyelik kategorisi ve churn riski skoru arasında güçlü negatif bir ilişki var.

## Derin Öğrenme Modeli

- **Doğruluk Değeri (Accuracy)**: İlk eğitim doğruluğu %81 iken, son doğruluk değerleri eğitim setinde %93.3 ve test setinde %92.5'e yükselmiştir.
- **Kayıp (Loss)**: Eğitim kaybı 0.41'den 0.16'ya düşerken, test kaybı ise 0.36'dan 0.17'ye düşmüştür.
- **Karışıklık Matrisi ve Sınıflandırma Raporu**: Gerçek pozitif, yanlış pozitif, doğru negatif ve yanlış negatif değerleri gözlemlenmiştir. Precision, recall ve f1-score değerleri %92-93 seviyelerinde çıkmıştır.
- **ROC AUC Değeri**: Modelin ayrım gücü güçlü olup, ROC AUC değeri 0.97'dir.

## Makine Öğrenmesi Modelleri

1. **Lojistik Regresyon**:
   - Ortalama doğruluk: %80
   - Test doğruluğu: %79
   - Çapraz doğrulama sonuçları: [0.795, 0.801, 0.795, 0.806, 0.802]
   - Sınıflandırma metrikleri: Precision %80, recall %73 (Churn olmayan), Precision %79, recall %85 (Churn).

2. **Random Forest**:
   - Ortalama doğruluk: %93
   - Test doğruluğu: %93
   - Çapraz doğrulama sonuçları: [0.929, 0.928, 0.931, 0.928, 0.933]
   - Sınıflandırma metrikleri: Precision %95, recall %89 (Churn olmayan), Precision %91, recall %96 (Churn).

## Modellerin Karşılaştırılması

- **Derin Öğrenme**: Yüksek doğruluk ve düşük kayıp ile güçlü performans gösteriyor.
- **Makine Öğrenmesi**: Lojistik Regresyon basit ve açıklanabilir, ancak karmaşık müşteri davranışlarını modellemede zorlanıyor. Random Forest ise daha güçlü ve daha doğru sonuçlar veriyor.

## Sonuçlar ve Öneriler

- Derin öğrenme modeli yüksek doğruluk oranları ile başarılı sonuçlar verirken, makine öğrenmesi modellerinden Random Forest, müşteri kaybı tahmininde daha etkili oldu.
- Bu model, müşteri churn önleme stratejilerinde daha verimli bir araç olabilir.

- Bu proje, müşteri kaybı tahminini yapmak için derin öğrenme modellerini kullanarak başarılı sonuçlar elde etmeyi amaçlamaktadır. 
- Bu süreçteki her aşama, veri bilimi ve makine öğrenmesi alanındaki en iyi uygulamalarla şekillendirilmiş ve sonuçlar oldukça tatmin edici olmuştur.

