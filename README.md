# Python-MongoDB 🍃🍃🍃🍃
MongoDB için hazırladığım notlar.. <br>
[Kaynak](https://www.w3schools.com/python/python_mongodb_getstarted.asp)
# İçerik:
- [Giriş](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#giri%C5%9F)
- [NoSQL - MongoDB Nedir?](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#nosql-nedir-)
- [NoSQL Veritabanı Özellikleri](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#nosql-veritaban%C4%B1-%C3%B6zellikleri)
- [NoSQL Veritabanı Türleri](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#nosql-veritaban%C4%B1-t%C3%BCrleri)

<img width="2451" alt="mdb-vs-sql" src="https://user-images.githubusercontent.com/120065120/215347383-a9f102b0-fcd6-409c-88a7-0610230f6f9d.png">

<!-- Table -->
<table>
<thead><th>RDMS</th><th>NoSQL</th></thead>
<tbody><tr><td>Dikeyde ölçeklenebilir, yatayda ölçeklenmesi zordur.</td><td>Koaly bir şekilde yatayda yada dikeyde ölçeklenebilir.Dağıtık sistemler için uygundur.</td></tr>
<tr><td>Anlık veri tutarlılığı sunar.</td><td>Nihai veri tutarlılığı sunar.</td></tr>
<tr><td>Olgunluk seviyesi yüksektir.Yetişmiş uzman bulmak kolaydır.</td><td>RDMS kadar olgun değildir.Yetişmiş uzman bulmak zordur.</td></tr>
<tr><td>Lisans ücretleri yüksek.</td><td>Lisans ücretleri düşük.</td></tr></tbody>
</table>

# Giriş
MongoDB, PostgreSQL - MySQL gibi ilişkisel veritabanlarından farklı olarak NoSQL veritabanı olarak sınıflandırılan bir veritabanıdır.
## NoSQL - MongoDB Nedir ?
**NoSQL**
- RDMS de **tablo ve sütunlar** ilişkili tutulurken **NoSQL** de **JSON** formatında tutulurlar.
- NoSQL de read-write işlemleri RDMS  ye göre çok daha hızlıdır.
- Büyük veri alanında NoSQL çok fazla kullanılmaktadır.
**MongoDB**
- Açık kaynak kodlu.
- NoSQL veri tabanı.
- Her kayıt bir döküman olup JSON formatında tutulur.

## NoSQL Veritabanı Özellikleri 
NoSQL veritabanı; esnek, yüksek performanslı, çok fonksiyonlu, ölçeklenebilir veritabanına ihtiyaç duyan mobil, web ve oyun gibi birçok uygulama türü için başarılı bir veritabanı çözümüdür.

- **Esnektir**: NoSQL, sağladığı esnek şemalar sayesinde daha hızlı ve daha fazla yineleme özelliğine sahip yazılımlar geliştirmeye olanak tanır. Yapılandırılmamış ya da yarı yapılandırılmış veriler için NoSQL veritabanları oldukça uygun çözümlerdir.
- **Ölçeklenebilir**: NoSQL, dağıtılmış donanım kümeleri kullanılarak ölçek genişlemesi sağlanabilecek şekilde tasarlandığından, pahalı ve kalıcı sunucuların kullanım zorunluluğunu ortadan kaldırır.
- **Yüksek Performansa Sahiptir**: Belirli veri modelleri ve erişim desenleri ile optimize edilen NoSQL veritabanları, benzer fonksiyonların ilişkisel veritabanları ile gerçekleştirilmesine oranla daha yüksek performans sağlamaktadır.
- **Yüksek İşlevselliğe Sahiptir**: Sağladığı veri türleri ve API’ler, ilgili veri modeline göre hazırlandığından, NoSQL veritabanları yüksek işlevsellik oranına sahiptir.
- **Kolay Taşınabilirliğe Sahiptir**: NoSQL veritabanına ait veriler disk ya da hafıza kartında kolaylıkla taşınabilmektedir.
- **Tanımlama Kolaylığı Sağlar**: Diğer veritabanlarının birçoğunda olduğu gibi verileri satırlar halinde saklayarak ve diğer tablolarla ilişkilendirerek tanımlama yapılmaya gerek olmayan NoSQL veritabanlarında veriler JSON veya XML biçiminde saklanabilmektedir.

## NoSQL Veritabanı Türleri
Belge Veritabanları: Belge veritabanları, uygulama kodlarında kullanılan aynı belge modelini kullandığından, veritabanında veri depolanmasını ve sorgulama işlemini kolaylaştırır.

- **Grafik Veritabanları**: Bağlı veri kümeleriyle çalışan uygulamalar oluşturmayı ve çalıştırmayı amaçlayan grafik veritabanları, sosyal ağlar, öneri altyapıları, dolandırıcılık işlemlerini algılama ve bilgi grafikleri gibi birçok alanda kullanılmaktadır.

- **Anahtar-Değer**: Yüksek oranda bölümlendirilebilen ve diğer veritabanı türlerinin ulaşamayacağı boyutlarda yatay ölçeklendirmeye olanak sağlayan anahtar-değer veritabanları IoT, oyun ve reklamcılık gibi alanlarda sıklıkla kullanılmaktadır.

- **Arama**: Uygulamaların birçoğu, yazılım geliştiricilerin sorun çözmelerine yardımcı olabilmek amacıyla günlükler tutar. NoSQL yarı yapılandırılmış günlükleri ve ölçümleri dizine ekleyip biriktirir ve bunlarda arama yaparak, makineler tarafından oluşturulan veriler için gerçek zamanlı sayılabilecek bir hızda görselleştirme ve analiz yapılmasına olanak tanır.

- **Bellek İçi**: Reklam teknolojisi ve oyun uygulamalarının puan tabloları, oturum bilgilerinin yer aldığı depolar ve gerçek zamanlı analitik gibi çok yüksek hızlarda yanıt alınması gereken ve her an yüksek trafik oluşabilen uygulamaların zamanında ve sorunsuz bir şekilde çalışmasını sağlar.





