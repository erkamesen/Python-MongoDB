# Python-MongoDB 🍃🍃🍃🍃
MongoDB için hazırladığım notlar.. <br>
[Kaynak](https://www.w3schools.com/python/python_mongodb_getstarted.asp)
![MongoDB_Logo svg](https://user-images.githubusercontent.com/120065120/215358239-4c22ed81-3bfe-46af-962b-b885b63359ce.png)

# İçerik:
1. [Giriş](https://github.com/erkamesen/Python-MongoDB#giri%C5%9F)
2. [NoSQL - MongoDB Nedir?](https://github.com/erkamesen/Python-MongoDB#nosql---mongodb-nedir-)
3. [NoSQL Veritabanı Özellikleri](https://github.com/erkamesen/Python-MongoDB#nosql-veritaban%C4%B1-%C3%B6zellikleri)
4. [NoSQL Veritabanı Türleri](https://github.com/erkamesen/Python-MongoDB#nosql-veritaban%C4%B1-t%C3%BCrleri)
5. [Başlangıç - Kurulum](https://github.com/erkamesen/Python-MongoDB#ba%C5%9Flang%C4%B1%C3%A7---kurulum) <br>
5.1 [Cluster Oluşturma](https://github.com/erkamesen/Python-MongoDB#cluster-olu%C5%9Fturma) <br>
5.2 [Bağlantı](https://github.com/erkamesen/Python-MongoDB#ba%C4%9Flant%C4%B1) 
6. [Insert(Veri Ekleme) Sorgusu](https://github.com/erkamesen/Python-MongoDB#insertveri-ekleme-sorgusu) <br>
6.1 [insert_one()](https://github.com/erkamesen/Python-MongoDB#insert_one) <br>
6.2 [insert_many()](https://github.com/erkamesen/Python-MongoDB#insert_many)
7. [Find(Veri Bulma) Sorgusu](https://github.com/erkamesen/Python-MongoDB#findveri-bulma-sorgusu) <br>
7.1 [find_one()](https://github.com/erkamesen/Python-MongoDB#find_one) <br>
7.2 [find()](https://github.com/erkamesen/Python-MongoDB#find) <br>
7.3 [find() ile Belirli Verileri Çekme](https://github.com/erkamesen/Python-MongoDB#find-ile-belirli-verileri-%C3%A7ekme)
8. [Query(Filtreleme Sorugları)](https://github.com/erkamesen/Python-MongoDB#queryfiltreleme-sorgular%C4%B1) <br>
8.1 [Advanced Query](https://github.com/erkamesen/Python-MongoDB#advanced-query)
9. [Sort(Sıralama) Sorgusu](https://github.com/erkamesen/Python-MongoDB#sorts%C4%B1ralama-sorgusu)
10. [and - or Sorguları](https://github.com/erkamesen/Python-MongoDB#and---or-sorgular%C4%B1) <br>
10.1 [and](https://github.com/erkamesen/Python-MongoDB#and) <br>
10.2 [or](https://github.com/erkamesen/Python-MongoDB#or)
11. [Update(Güncelleme) Sorguları](https://github.com/erkamesen/Python-MongoDB#updateg%C3%BCncelleme-sorgular%C4%B1) <br>
11.1 [update_one()](https://github.com/erkamesen/Python-MongoDB#update_one) <br>
11.2 [update_many()](https://github.com/erkamesen/Python-MongoDB#update_many)
12. [Limit Sorguları](https://github.com/erkamesen/Python-MongoDB#limit-sorgular%C4%B1)
13. [Delete Sorguları](https://github.com/erkamesen/Python-MongoDB#delete-sorgular%C4%B1) <br>
13.1 [delete_one()](https://github.com/erkamesen/Python-MongoDB#delete_one) <br>
13.2 [delete_many()](https://github.com/erkamesen/Python-MongoDB#delete_many)
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
### Bağlantı 

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

## Insert(Veri Ekleme) Sorgusu
### insert_one()
Bir kayıdı yani MongoDB'de çağrıldığı şekliyle bir dökümanı bir collection a eklemek için insert_one() yöntemini kullanırız.
insert_one() yönteminin ilk parametresi, eklemek istediğiniz belgedeki her alanın adlarını ve değerlerini içeren bir sözlüktür.

```
myclient = MongoClient("mongodb+srv://erkamesen:<yourpassword>@cluster1.dumyfbl.mongodb.net/?retryWrites=true&w=majority") #python ile bağlama
db = myclient["mydatabase"] #Veritabanı oluşturma
new_collection = db["customers"] #collection oluşturma veya bağlanma
--- 
new_data = {"name":"Erkam","City":"Karabük"}
x = new_collection.insert_one(new_data)
```
![Seçim_056](https://user-images.githubusercontent.com/120065120/215444999-28c7e38c-f749-497b-9b8a-768c9d79fedb.png)

insert_id

```
print(x.inserted_id)
Result : 63d79461665fd3f1737213b1
```
---
### insert_many()
MongoDB'deki bir collection a birden çok döküman eklemek için insert_many() yöntemini kullanırız.
insert_many() yönteminin ilk parametresi, eklemek istediğiniz verileri içeren sözlükleri içeren bir listedir:

```
mylist = [
  { "name": "Amy", "address": "Apple st 652"},
  { "name": "Hannah", "address": "Mountain 21"},
  { "name": "Michael", "address": "Valley 345"},
  { "name": "Sandy", "address": "Ocean blvd 2"},
  { "name": "Betty", "address": "Green Grass 1"},
  { "name": "Richard", "address": "Sky st 331"},
  { "name": "Susan", "address": "One way 98"},
  { "name": "Vicky", "address": "Yellow Garden 2"},
  { "name": "Ben", "address": "Park Lane 38"},
  { "name": "William", "address": "Central st 954"},
  { "name": "Chuck", "address": "Main Road 989"},
  { "name": "Viola", "address": "Sideway 1633"}
]
new_collection.insert_many(mylist)
```
Burda her bir row için otomatik bir unique ID verilecek istersek bunu kendimiz de belirtebiliriz.
```
# ID ye göre ekleme yapma 
new_list_with_id = [
    {"_id":1, "name": "Erkam", "address": "Karabük"},
    {"_id":2, "name": "Ensar", "address": "İstanbul"},
    {"_id":3, "name": "Duygu", "address": "Ankara"},
    {"_id":4, "name": "Enes", "address": "İstanbul"},
    {"_id":5, "name": "Ulaş", "address": "Sakarya"},
    {"_id":6, "name": "Onur", "address": "Isparta"},
    {"_id":7, "name": "Çelik", "address": "Bolu"},
    
]
new_collection.insert_many(new_list_with_id)
```

## Find(Veri Bulma) Sorgusu
MongoDB'de bir koleksiyondaki verileri bulmak için SQL de ki SELECT ifadesinin yerine MongoDB de find() ve find_one() yöntemlerini kullanırız.

### find_one()
MongoDB'deki bir koleksiyondan veri seçmek için find_one() yöntemini kullanabiliriz. Bu bize ilk satırda ki kayıdı verecektir.

```
x = new_collection.find_one()
print(x)
# {'_id': ObjectId('63d79904c5c7052da8b7bc6e'), 'name': 'Amy', 'address': 'Apple st 652'}
```
### find()
find() yöntemi, seçimdeki tüm kayıtları bize döndürür.
find() yönteminin ilk parametresi bir sorgu nesnesidir. Bu örnekte, parametre vermeyerek koleksiyondaki tüm kayıtları seçen boş bir sorgu nesnesi kullanıyoruz. Özetle SQL de ki *SELECT komutu için find() methodunun parametresini boş bırakmamız yeterlidir.

```
for x in new_collection.find():
  print(x) 
 """
{'_id': ObjectId('63d79904c5c7052da8b7bc6e'), 'name': 'Amy', 'address': 'Apple st 652'}
{'_id': ObjectId('63d79904c5c7052da8b7bc6f'), 'name': 'Hannah', 'address': 'Mountain 21'}
{'_id': ObjectId('63d79904c5c7052da8b7bc70'), 'name': 'Michael', 'address': 'Valley 345'}
{'_id': ObjectId('63d79904c5c7052da8b7bc71'), 'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'_id': ObjectId('63d79904c5c7052da8b7bc72'), 'name': 'Betty', 'address': 'Green Grass 1'}
{'_id': ObjectId('63d79904c5c7052da8b7bc73'), 'name': 'Richard', 'address': 'Sky st 331'}
{'_id': ObjectId('63d79904c5c7052da8b7bc74'), 'name': 'Susan', 'address': 'One way 98'}
{'_id': ObjectId('63d79904c5c7052da8b7bc75'), 'name': 'Vicky', 'address': 'Yellow Garden 2'}
{'_id': ObjectId('63d79904c5c7052da8b7bc76'), 'name': 'Ben', 'address': 'Park Lane 38'}
{'_id': ObjectId('63d79904c5c7052da8b7bc77'), 'name': 'William', 'address': 'Central st 954'}
{'_id': ObjectId('63d79904c5c7052da8b7bc78'), 'name': 'Chuck', 'address': 'Main Road 989'}
{'_id': ObjectId('63d79904c5c7052da8b7bc79'), 'name': 'Viola', 'address': 'Sideway 1633'}
{'_id': 1, 'name': 'Erkam', 'address': 'Karabük'}
{'_id': 2, 'name': 'Ensar', 'address': 'İstanbul'}
{'_id': 3, 'name': 'Duygu', 'address': 'Ankara'}
{'_id': 4, 'name': 'Enes', 'address': 'İstanbul'}
{'_id': 5, 'name': 'Ulaş', 'address': 'Sakarya'}
{'_id': 6, 'name': 'Onur', 'address': 'Isparta'}
{'_id': 7, 'name': 'Çelik', 'address': 'Bolu'}"""
```

### find() ile Belirli Verileri Çekme
find() yönteminin ikinci parametresi, sonuca hangi alanların dahil edileceğini açıklayan bir nesnedir.
Bu parametre isteğe bağlıdır ve atlanırsa tüm alanlar sonuca dahil edilir.

```
# id yi getirme ismi ve adresi getir
for x in new_collection.find({},{ "_id": 0, "name": 1, "address":1}):
  print(x) 
"""
{'name': 'Amy', 'address': 'Apple st 652'}
{'name': 'Hannah', 'address': 'Mountain 21'}
{'name': 'Michael', 'address': 'Valley 345'}
{'name': 'Sandy', 'address': 'Ocean blvd 2'}
{'name': 'Betty', 'address': 'Green Grass 1'}
"""
```
```
# Sadece isimleri getir
for x in new_collection.find({},{ "_id": 0, "name": 1}):
  print(x) 
"""
# Sadece isimleri getir
for x in new_collection.find({},{ "_id": 0, "name": 1}):
  print(x) 
# Sadece isimleri getir
for x in new_collection.find({},{ "_id": 0, "name": 1}):
  print(x) 
{'name': 'Amy'}
{'name': 'Hannah'}
{'name': 'Michael'}
{'name': 'Sandy'}
{'name': 'Betty'}
"""
```

## Query(Filtreleme) Sorguları
Bir koleksiyondaki belgeleri bulurken, bir sorgu nesnesi kullanarak sonuca filtre uygulayabilirsiniz.
find() yönteminin ilk bağımsız değişkeni bir sorgu nesnesidir ve aramayı sınırlandırmak için kullanılır.

```
myquery = { "address": "İstanbul" }
mydoc = new_collection.find(myquery)

for x in mydoc:
  print(x) 
"""
{'_id': 2, 'name': 'Ensar', 'address': 'İstanbul'}
{'_id': 4, 'name': 'Enes', 'address': 'İstanbul'}
"""
```

### Advanced Query

Daha detaylı sorgular için not ortalamalarının tutulduğu bir collection açalım.
ve içerisine liste şeklinde notlarımızı yükleyelim
```
mydb = db["notlar"]
notlar = [{"Adı":"Ali","Ortalama":63},
          {"Adı":"Ayşe","Ortalama":82},
          {"Adı":"Mehmet","Ortalama":18},
          {"Adı":"Duygu","Ortalama":41},
          {"Adı":"Buse","Ortalama":72},
          {"Adı":"Orhan","Ortalama":26},
          {"Adı":"Kerim","Ortalama":65},
          {"Adı":"Mustafa","Ortalama":23},
          {"Adı":"Şule","Ortalama":75},
          {"Adı":"Baran","Ortalama":91},
          {"Adı":"Kaan","Ortalama":74},
          {"Adı":"Osman","Ortalama":62},
          {"Adı":"Banu","Ortalama":84},
          {"Adı":"Burhan","Ortalama":36},
          {"Adı":"Oğuz","Ortalama":63},
          {"Adı":"Ali","Ortalama":75}
         ]
mydb.insert_many(notlar)
# <pymongo.results.InsertManyResult at 0x7f23655cff10>
```
![Seçim_057](https://user-images.githubusercontent.com/120065120/215504853-f3ea065a-b9be-4cf7-bd1e-5fcefc0e8382.png)

Şimdi 50 ve üzeri not alanların dersi geçtiğini baz alalım ve buna göre greater than, less than i kodlarımıza ekleyelim.
```
$gt = greater than ">"
$gte = greater than equal ">="
$lt = less than "<"
$lte = less than equal "<="
$ne = not equal "!="
$in = Karşısına gelen liste içindeki value ları getirir { field: { $in: [<value1>, <value2>, ... <valueN> ] } }
$nin = Karşısına gelen liste içindeki value lar haricini getirir { field: { $nin: [<value1>, <value2>, ... <valueN> ] } }
```
DERSİ GEÇENLERİN İSİMLERİ:
```
for x in mydb.find({"Ortalama": { "$gte": 50 }},{"_id":0, "Adı":1}):
    print(x)
"""
{'Adı': 'Ali'}
{'Adı': 'Ayşe'}
{'Adı': 'Buse'}
{'Adı': 'Kerim'}
{'Adı': 'Şule'}
{'Adı': 'Baran'}
{'Adı': 'Kaan'}
{'Adı': 'Osman'}
{'Adı': 'Banu'}
"""   
```
DERSTEN KALANLARI ISIMLERİ VE NOTLARI
```
for x in mydb.find({"Ortalama": { "$lt": 50 }},{"_id":0}):
    print(x)
"""
{'Adı': 'Mehmet', 'Ortalama': 18}
{'Adı': 'Duygu', 'Ortalama': 41}
{'Adı': 'Orhan', 'Ortalama': 26}
{'Adı': 'Mustafa', 'Ortalama': 23}
{'Adı': 'Burhan', 'Ortalama': 36}
"""
```
## Sort(Sıralama) Sorgusu

Sonucu artan veya azalan düzende sıralamak için sort() yöntemini kullanırız.
sort() yöntemi, "fieldname" için bir parametre ve "yön" için bir parametre alır (artan yön, varsayılan yöndür).

```
sort("name", 1) #ascending ( Artan Yön )
sort("name", -1) #descending ( Azalan Yön )
```
Ortalamalar için ARTAN YÖN
```
# Ortalamalar için ARTAN YÖN
for x in mydb.find({},{"_id":0}).sort("Ortalama"):
    print(x)
"""
{'Adı': 'Mehmet', 'Ortalama': 18}
{'Adı': 'Mustafa', 'Ortalama': 23}
{'Adı': 'Orhan', 'Ortalama': 26}
{'Adı': 'Burhan', 'Ortalama': 36}
{'Adı': 'Duygu', 'Ortalama': 41}
{'Adı': 'Osman', 'Ortalama': 62}
{'Adı': 'Ali', 'Ortalama': 63}
{'Adı': 'Kerim', 'Ortalama': 65}
{'Adı': 'Buse', 'Ortalama': 72}
{'Adı': 'Kaan', 'Ortalama': 74}
{'Adı': 'Şule', 'Ortalama': 75}
{'Adı': 'Ayşe', 'Ortalama': 82}
{'Adı': 'Banu', 'Ortalama': 84}
{'Adı': 'Baran', 'Ortalama': 91}
"""
```
Ortalamalar için AZALAN YÖN
```
for x in mydb.find({},{"_id":0}).sort("Ortalama", -1):
    print(x)
"""
{'Adı': 'Baran', 'Ortalama': 91}
{'Adı': 'Banu', 'Ortalama': 84}
{'Adı': 'Ayşe', 'Ortalama': 82}
{'Adı': 'Şule', 'Ortalama': 75}
{'Adı': 'Kaan', 'Ortalama': 74}
{'Adı': 'Buse', 'Ortalama': 72}
{'Adı': 'Kerim', 'Ortalama': 65}
{'Adı': 'Ali', 'Ortalama': 63}
{'Adı': 'Osman', 'Ortalama': 62}
{'Adı': 'Duygu', 'Ortalama': 41}
{'Adı': 'Burhan', 'Ortalama': 36}
{'Adı': 'Orhan', 'Ortalama': 26}
{'Adı': 'Mustafa', 'Ortalama': 23}
{'Adı': 'Mehmet', 'Ortalama': 18}
"""
```

## and - or Sorguları

 ```
 and: find({$and:[{sorgu1:beklenen1},{sorgu2:beklenen2}]})
 or: find({$or:[{sorgu1:beklenen1},{sorgu2:beklenen2}]})
 ```


### and 
liste içindeki sorguların hepsinin doğru olduğu kayıdı getirir.

ORTALAMASI 63 olanları getir
```
for x in mydb.find({"Ortalama":63},{"_id":0}):
    print(x)
"""
{'Adı': 'Ali', 'Ortalama': 63}
{'Adı': 'Oğuz', 'Ortalama': 63}
"""
```
ORTALAMASI 63 ve ADI ALİ olanları getir
```
for x in mydb.find({"$and":[{"Ortalama":63},{"Adı":"Ali"}]},{"_id":0}):
    print(x)
# {'Adı': 'Ali', 'Ortalama': 63}
```

### or
liste içindeki sorguların hepsini getirir.

ORTALAMASI 63 yada ADI ALİ olanları getir
```
for x in mydb.find({"$or":[{"Ortalama":63},{"Adı":"Ali"}]},{"_id":0}):
    print(x)
"""
{'Adı': 'Ali', 'Ortalama': 63}
{'Adı': 'Oğuz', 'Ortalama': 63}
{'Adı': 'Ali', 'Ortalama': 75}
"""
```

## Update(Güncelleme) Sorguları


### update_one()
Bir kaydı veya MongoDB tabiri ile dökümanı update_one() yöntemini kullanarak güncelleyebilirsiniz.
update_one() yönteminin ilk parametresi, hangi belgenin güncelleneceğini tanımlayan bir sorgu nesnesidir.
İkinci parametre, belgenin yeni değerlerini tanımlayan bir nesnedir.
Not: Sorgu birden fazla kayıt bulursa, yalnızca ilk oluşum güncellenir.

my_query = {"eski kayıt":"eski deger"}
new_values = {"$set":{"eski kayıt":"yeni deger"}}
update_one(my_query, new_values)

```
# Banu Ortalama 84 geldi. şimdi bunun notunu 100 ile güncelleyelim.
my_query = {"Ortalama":84}
new_values = {"$set":{"Ortalama":100}}
mydb.update_one(my_query, new_values)
# 100 olarak değiştirdik kontrol edelim
mydb.find_one({"Ortalama":100})

```
### update_many()
uygulama aşamasında update_one() dan hiç bir farkı yok.
Sorgunun koşullarını karşılayan tüm dökümanları güncellemek için update_many() yöntemini kullanırız.

AF GELDİ ! ORTALAMASI 50 den AZ OLAN HERKESİ GEÇİRİYORUZ
```
my_query = {"Ortalama":{"$lt":50}}
new_values = {"$set":{"Ortalama":50}}
mydb.update_many(my_query, new_values)
for x in mydb.find({},{"_id":0}):
    print(x)
"""
{'Adı': 'Ali', 'Ortalama': 63}
{'Adı': 'Ayşe', 'Ortalama': 82}
{'Adı': 'Mehmet', 'Ortalama': 50}
{'Adı': 'Duygu', 'Ortalama': 50}
{'Adı': 'Buse', 'Ortalama': 72}
{'Adı': 'Orhan', 'Ortalama': 50}
{'Adı': 'Kerim', 'Ortalama': 65}
{'Adı': 'Mustafa', 'Ortalama': 50}
{'Adı': 'Şule', 'Ortalama': 75}
{'Adı': 'Baran', 'Ortalama': 91}
{'Adı': 'Kaan', 'Ortalama': 74}
{'Adı': 'Osman', 'Ortalama': 62}
{'Adı': 'Banu', 'Ortalama': 100}
{'Adı': 'Burhan', 'Ortalama': 50}
{'Adı': 'Oğuz', 'Ortalama': 63}
{'Adı': 'Ali', 'Ortalama': 75}
"""
```

> update_one() karşılayan ilk kayıdı değiştirir. update_many() ise tüm karşılayan kayıtları.

## Limit Sorguları
Sonucu sınırlamak için limit() yöntemini kullanırız.
limit() yönteminin alacağı parametre ile kaç döküman döndüreceğini belirleriz.

HEPSİ
```
for x in mydb.find():
    print(x)
"""
{'_id': ObjectId('63d7dba343737eb5fa87bfb3'), 'Adı': 'Ali', 'Ortalama': 63}
{'_id': ObjectId('63d7dba343737eb5fa87bfb4'), 'Adı': 'Ayşe', 'Ortalama': 82}
{'_id': ObjectId('63d7dba343737eb5fa87bfb5'), 'Adı': 'Mehmet', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfb6'), 'Adı': 'Duygu', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfb7'), 'Adı': 'Buse', 'Ortalama': 72}
{'_id': ObjectId('63d7dba343737eb5fa87bfb8'), 'Adı': 'Orhan', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfb9'), 'Adı': 'Kerim', 'Ortalama': 65}
{'_id': ObjectId('63d7dba343737eb5fa87bfba'), 'Adı': 'Mustafa', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfbb'), 'Adı': 'Şule', 'Ortalama': 75}
{'_id': ObjectId('63d7dba343737eb5fa87bfbc'), 'Adı': 'Baran', 'Ortalama': 91}
{'_id': ObjectId('63d7dba343737eb5fa87bfbd'), 'Adı': 'Kaan', 'Ortalama': 74}
{'_id': ObjectId('63d7dba343737eb5fa87bfbe'), 'Adı': 'Osman', 'Ortalama': 62}
{'_id': ObjectId('63d7dba343737eb5fa87bfbf'), 'Adı': 'Banu', 'Ortalama': 100}
{'_id': ObjectId('63d7dba343737eb5fa87bfc0'), 'Adı': 'Burhan', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfc1'), 'Adı': 'Oğuz', 'Ortalama': 63}
{'_id': ObjectId('63d7dba343737eb5fa87bfc2'), 'Adı': 'Ali', 'Ortalama': 75}
"""
```

ilk 5 i 
```
for x in mydb.find().limit(5):
    print(x)
"""
{'_id': ObjectId('63d7dba343737eb5fa87bfb3'), 'Adı': 'Ali', 'Ortalama': 63}
{'_id': ObjectId('63d7dba343737eb5fa87bfb4'), 'Adı': 'Ayşe', 'Ortalama': 82}
{'_id': ObjectId('63d7dba343737eb5fa87bfb5'), 'Adı': 'Mehmet', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfb6'), 'Adı': 'Duygu', 'Ortalama': 50}
{'_id': ObjectId('63d7dba343737eb5fa87bfb7'), 'Adı': 'Buse', 'Ortalama': 72}
"""
```

## Delete Sorguları
### delete_one()
Bir belgeyi silmek için, delete_one() yöntemini kullanırız.
delete_one() yönteminin ilk parametresi, hangi belgenin silineceğini tanımlayan bir sorgu nesnesidir.

Not: Sorgu birden fazla belge bulursa yalnızca ilk geçtiği yer silinir.
İsmi ayşe olan biri var mı diye kontrol ediyoruz
```
for x in mydb.find({"Adı":"Ayşe"}):
    print(x)
"""
{'_id': ObjectId('63d7dba343737eb5fa87bfb4'), 'Adı': 'Ayşe', 'Ortalama': 82}
"""
```
1 adet Ayşe var şimdi biz bunu silmek istiyoruz.Öncelikle kod kalabalığı olmasın diye kaydımızı alıp değişkene atayalım.
```
myquery = {"Adı":"Ayşe"}
```
Şimdi delete_one() ile silebiliriz.
```
mydb.delete_one(myquery)
# <pymongo.results.DeleteResult at 0x7f23655ced70>
```
Kontrol edelim.
```
mydb.find_one({"Adı":"Ayşe"})
# None
```

### delete_many()
Birden fazla dökümanı silmek için, delete_many() yöntemini kullanın.

NOTU 50 OLANLARI SİLİYORUZ.ÖNCE KONTROL EDELİM
```
for x in mydb.find({"Ortalama":50},{"_id":0}):
    print(x)
"""
{'Adı': 'Mehmet', 'Ortalama': 50}
{'Adı': 'Duygu', 'Ortalama': 50}
{'Adı': 'Orhan', 'Ortalama': 50}
{'Adı': 'Mustafa', 'Ortalama': 50}
{'Adı': 'Burhan', 'Ortalama': 50}
"""
```
Silinecek kayıdımızı değişkene atıyoruz.
```
myquery = {"Ortalama":50}
```
Silme işlemini gerçekleştiriyoruz.
```
mydb.delete_many(myquery)
# <pymongo.results.DeleteResult at 0x7f23655ce800>
```
Tekrar kontrol edelim
```
for x in mydb.find({"Ortalama":50},{"_id":0}):
    print(x)
# None
```


