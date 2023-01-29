# Python-MongoDB 🍃🍃🍃🍃
MongoDB için hazırladığım notlar.. <br>
[Kaynak](https://www.w3schools.com/python/python_mongodb_getstarted.asp)
![MongoDB_Logo svg](https://user-images.githubusercontent.com/120065120/215358239-4c22ed81-3bfe-46af-962b-b885b63359ce.png)

# İçerik:
- [Giriş](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#giri%C5%9F)
- [NoSQL - MongoDB Nedir?](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#nosql-nedir-)
- [NoSQL Veritabanı Özellikleri](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#nosql-veritaban%C4%B1-%C3%B6zellikleri)
- [NoSQL Veritabanı Türleri](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#nosql-veritaban%C4%B1-t%C3%BCrleri)
- [Başlangıç - Kurulum](https://github.com/erkamesen/Python-MongoDB/edit/main/README.md#ba%C5%9Flang%C4%B1%C3%A7---kurulum)

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

## Başlangıç - Kurulum
Öncelikle python ile mongodb bağlantısını yapmak için pymongo library mizi indirelim.
Windows:
```
pip install pymongo 
```
Linox - MacOS
```
pip3 install pymongo
```
MongoDB yi localde veya dileğe göre cloud üzerinde çalıştırabiliriz.Biz cloud üzerinde çalıştıracağımızdan [Atlas](https://www.mongodb.com/cloud/atlas/register)a kayıt olup bize verilen 512 mb lık ücretsiz kısımdan faydalanıcaz. Eğer siz localde kullanmak istiyorsanız [buradan](https://www.mongodb.com/) indirebilirsiniz. 
Eğer cloud üzerinde kullanacaksanız mail üzerinden gelen onay linkine tıklayıp kayıdı tamamlıyoruz.

### Cluster Oluşturma

- [Atlas](https://www.mongodb.com/cloud/atlas/register) a gidip üye olun, daha önce üye olduysanız giriş yapabilirsiniz. <br>
- Üye olup giriş yaptıktan sonra, “Clusters” sekmesi altında “Build a Database” butonuna tıklayın. <br>
![Seçim_043](https://user-images.githubusercontent.com/120065120/215360005-31b8dd51-0eb3-4c1d-9f20-784cdc083130.png)
***
- Çıkan seçenekler arasında “Free” altındaki “Create” butonuna tıklayın. <br>
![Seçim_044](https://user-images.githubusercontent.com/120065120/215360016-7e6298be-26f8-4522-9653-4f06597bd040.png)
***
- Clusterınızı Amazon AWS, Google veya Azure Cloud sağlayıcılarından herhangi birinde saklayabilirsiniz. Region olarak Frankfurt bize direkt bağlı bir hub olduğu için Frankfurt seçmeniz hız açısından faydalı olabilir. <br>
- Seçimlerinizi yaptıktan sonra “Create Cluster” butonuna tıklayın. <br>
![Seçim_051](https://user-images.githubusercontent.com/120065120/215360271-01aad569-62dc-48b5-94df-8c428673eae5.png)
***
- Bir kullanıcı yaratmak için bilgilerimizi giriyoruz. Ardından Create User diyip listeye ekliyoruz.
![Seçim_048](https://user-images.githubusercontent.com/120065120/215360019-54fb0d03-6c7c-4f97-a4c7-49569eeb8210.png)
***
- Cloud Environment seçip IP adresi eşlenmediyse IP adresi girip lsiteye ekliyoruz.
![Seçim_![Seçim_050](https://user-images.githubusercontent.com/120065120/215360025-87026d72-bfd4-4d6c-b4d9-d1728f38e72a.png)
049](https://user-images.githubusercontent.com/120065120/215360023-0f0486a1-0a4d-4673-9e6f-442b68a1c9b6.png)
***
- "Finish and Close" ve ardından "Go to Databases" diyerek clusterımıza gidiyoruz. Açılması bir müddet zaman alabilir.
![Seçim_050](https://user-images.githubusercontent.com/120065120/215360522-2a460355-5073-47d9-8804-ef9a602e793a.png)
***
## Bağlantı 

- Cluster hazır olduğunda aşağıdaki gibi görünmesi lazım. Buradan “CONNECT” tuşuna basıyoruz.
![Seçim_052](https://user-images.githubusercontent.com/120065120/215360790-7b2ec2c0-3f64-46b4-aae3-076de92edf68.png)
***
- "Connect your application" seçeneğini seçiyoruz.
![Seçim_053](https://user-images.githubusercontent.com/120065120/215360843-94031ae0-e04c-45bc-a21e-7f224262b270.png)
***
- Pythonı ve ardından kullanacağımız sürümü seçiyoruz. Kodu kopyalayıp python kodumuza yapıştırabiliriz.<password> kısmını user eklerken kullandığımız password ile değiştirmeyi unutmayalım.
![Seçim_055](https://user-images.githubusercontent.com/120065120/215360892-91e9b9bf-67f7-4b1f-8be5-9fce31c14f64.png)
***
Artık editörümüze geçebiliriz.
```
import pymongo 
from pymongo import MongoClient #MongoClient sınıfımızı import ediyoruz.
```

MongoClient sınıfına parametre olarak siteden kopyaladığımız bağlantıyı veriyoruz ve myclient adında bir nesne oluşturuyoruz.
```
myclient = MongoClient("mongodb+srv://erkamesen:<yourpassword>@cluster1.dumyfbl.mongodb.net/?retryWrites=true&w=majority") #python ile bağlama
```

myclient["veritabanıAdı"] ile clodumuzuda veritabanını oluşturuyoruz ve db adında bir değişkene atıyoruz. <br>
db["collectionAdı"] ile bir collection oluşturarak bunu new_collection adında bir değişkene atıyoruz ve collection ımızı başarı ile oluşturduk.
```
db = myclient["veritabanıAdı"] #Veritabanı oluşturma
new_collection = db["collectionAdı"] #collection oluşturma veya bağlanma
```






