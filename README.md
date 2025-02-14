Proje: Türkiye İller ve İzmirin İlçeleri Arası  Mesafe ve En Kısa Yol Hesaplama

Bu proje, Türkiye'deki 81 ilin arasındaki mesafeleri kullanarak en kısa kara yolunu hesaplamak için Dijkstra algoritmasını uygular. Ayrıca, rastgele şehir çiftleri arasındaki kuş uçuşu mesafesi ve kara yolu mesafesi arasındaki farkları analiz eder ve belirli ilçeler arasındaki komşuluk ilişkileri ve mesafeleri analiz eder.  
Dijkstra Algoritması kullanılarak en kısa yol hesaplanır ve kuş uçuşu ile karayolu mesafesi arasındaki farklar belirlenir.


İçerik:

Uzaklık Matrisi (distanceMatrix): Türkiye'deki 81 ilin arasındaki mesafeleri içeren bir matris oluşturulur.

Üçgen Matrisin Kare Matrise Dönüştürülmesi: İlk olarak üçgen matris formatındaki mesafeler tam kare matris haline getirilir.

İllerin Komşuluk Listesi (provinceWithNeigbour): İllerin birbirleriyle komşuluk ilişkileri belirlenir.

Komşu Olmayan İllerin Mesafesi: Komşu olmayan illere maksimum mesafe atanarak Dijkstra algoritmasına uygun hale getirilir.

Dijkstra Algoritması: İki şehir arasındaki en kısa mesafeyi bulmak için Dijkstra algoritması kullanılır.

Şehirler Arası Mesafe Hesaplamaları: Rastgele seçilen 10 şehir çifti için kuş uçuşu ve kara yolu mesafesi hesaplanır ve farkları gösterilir.

81 İlin 81 İle Olan Mesafe Karşılaştırmaları: Tüm şehir çiftleri için hesaplanan en kısa kara yolu mesafesi ile kuş uçuşu mesafesi arasındaki farklar karşılaştırılır.

Kullanılan Veri Yapıları:

Jagged Array (Üçgen Matris - triangleDistanceMatrix)

Bellek tasarrufu için üçgen matris formatında tutulur.Sonrasında kare matrise çevrilir.

Dictionary Yapısı (provinceWithNeigbour)

Her ilin komşularını içeren bir sözlük (Dictionary) kullanılır.

Dijkstra Algoritması İçin Matris (borderMatrix)

Komşu olmayan iller için int.MaxValue atanarak Dijkstra algoritması için uygun hale getirilir.

Örnek Kullanım

Kod çalıştırıldığında aşağıdaki işlemler yapılır:

Rastgele seçilen 10 şehir çifti için mesafe hesaplanır:

Ankara (06) - İstanbul (34): 450 km
İzmir (35) - Antalya (07): 330 km

Dijkstra algoritması ile en kısa kara yolu mesafesi bulunur ve kuş uçuşu mesafesiyle karşılaştırılır:

İstanbul - Ankara: Orijinal: 450 km, Hesaplanan: 490 km, Fark: 40 km
İzmir - Antalya: Orijinal: 330 km, Hesaplanan: 370 km, Fark: 40 km

Dijkstra Algoritması Açıklaması

Dijkstra algoritması, bir kaynak şehirden diğer tüm şehirlere en kısa mesafeyi bulur.

Başlangıç olarak tüm şehirlerin uzaklığı int.MaxValue olarak atanır.

Kaynak şehir için mesafe 0 olarak belirlenir.

En kısa mesafeye sahip şehir seçilir ve komşu şehirlerin mesafeleri güncellenir.

Tüm şehirler ziyaret edilene kadar bu işlem devam eder.

Belirtilen hedef şehir için minimum mesafe döndürülür.

Gereksinimler

C# ile geliştirilmiştir.

.NET Core veya .NET Framework destekleyen bir ortam gereklidir.

Çalıştırma

Projeyi çalıştırmak için:

# Visual Studio veya .NET CLI ile çalıştırılabilir.
dotnet run

