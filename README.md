# Veri-Analizi
Bu kodun amacı, süpermarket satışlarını etkileyen faktörleri anlamak, toplam satış değerini tahmin etmek ve farklı regresyon modellerinin performansını kıyaslamaktır. 
Analiz çıktıları, süpermarketlerin satış stratejileri hakkında kararlar almasına yardımcı olabilir.

# Veri
https://www.kaggle.com/datasets/aungpyaeap/supermarket-sales

# Veri Kümesi Hakkında
Kapsam:
Nüfusun yoğun olduğu şehirlerde süpermarketlerin sayısı artıyor ve piyasa rekabeti de yüksek. Bu veri kümesi, bir süpermarket şirketinin 3 farklı şubede 3 ay boyunca kaydedilen tarihi satış verilerini içermektedir. 
Bu veri kümesi ile öngörücü veri analitiği yöntemleri kolayca uygulanabilir.

# Özellik Bilgileri:
        Fatura Kimliği (Invoice id): Bilgisayar tarafından oluşturulan satış fişi fatura kimlik numarası
        Şube (Branch): Süper merkezin şubesi (A, B ve C olarak tanımlanan 3 şube mevcut)
        Şehir (City): Süpermarketlerin konumu
        Müşteri Türü (Customer type): Müşteri türü; üye kartı kullananlar için "Üyeler", kullanmayanlar için "Normal" olarak kaydedilmiştir.
        Cinsiyet (Gender): Müşterinin cinsiyeti
        Ürün Hattı (Product line): Genel ürün kategorileri - Elektronik aksesuarlar, Moda aksesuarları, Yiyecek ve içecekler, Sağlık ve güzellik, Ev ve yaşam tarzı, Spor ve seyahat
        Birim Fiyat (Unit price): Her bir ürünün fiyatı ($ olarak)
        Adet (Quantity): Müşterinin satın aldığı ürün sayısı
        Vergi (Tax): Müşterinin alışverişinde ödediği %5 vergi
        Toplam (Total): Vergi dahil toplam fiyat
        Tarih (Date): Alışveriş tarihi (Ocak 2019'dan Mart 2019'a kadar kayıtlar mevcut)
        Saat (Time): Alışveriş saati (10.00 ile 21.00 arası)
        Ödeme (Payment): Müşterinin kullandığı ödeme yöntemi (3 yöntem mevcut – Nakit, Kredi Kartı ve Elektronik Cüzdan)
        Maliyet (COGS): Satılan malın maliyeti
        Brüt Kar Marjı Yüzdesi (Gross margin percentage): Brüt kar marjı yüzdesi
        Brüt Gelir (Gross income): Brüt gelir
        Puanlama (Rating): Müşterinin genel alışveriş deneyimine ilişkin derecelendirmesi (1 ila 10 arasında bir ölçek)




