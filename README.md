# CampSpringRentACar
Kodlama.io
![image](https://user-images.githubusercontent.com/63293055/221370840-03affad8-1a67-43e8-aa90-5ea72330e218.png)

#  ARAÇ KİRALAMA SİSTEMİ 
<p>Bu projemde spring boot kullanarak java ile bir araba kiralama
otomasyon projesi geliştirme amacıyla başlamış bulunmaktayım. Bu projemde n katmanlı mimari yapısı kullanarak
projemi SOLID prensiplerine uygun bir şekilde CODE REFACTORING yaparak ilerleme sağlayacağım.<p/>

### :loud_sound::boom: GÜNCELLEME(25.02.2023)
:purple_circle: projeyi katmanlı mimari olarak gerekli katmanlar yazıldı.

:purple_circle: Bu katmanların her birine Brand nesnesi ile ilgili entity nesnesi oluşturulup
gerekli servis elemanları yazıldı.

:purple_circle: Projeye lombok ve swagger.ui kullanımı için gerekli eklentiler dahil edildi.

:purple_circle: Projede response request pattern'e göre classlar oluşturuldu.

:purple_circle: Core katmanı yazılarak projeye modelmapper eklendi.

:purple_circle:Controller kısmında gerekli operasyonlar sağlanarak Brand nesnesine ait ekleme,silme,
güncelleme ve id işlemine göre brand listeleme işlemleri başarılı bir şekilde test edildi.

![image](https://user-images.githubusercontent.com/63293055/221396209-4b6e8198-f4ea-4674-a101-7a0845db9680.png)
![image](https://user-images.githubusercontent.com/63293055/221396225-2bdaa9db-9030-4bf4-8be1-1bfd6a195bb1.png)
![image](https://user-images.githubusercontent.com/63293055/221396274-267b28e5-4e37-46d5-8683-778b458177e6.png)


## İçindekiler
 ### BUSİNESS KATMANI

Bu katmanda iş kodlarımı yazdım.
  + [Abstract:open_file_folder:  :(İlgili soyut Sınıflarımı içerir.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/business/abstracts)
     + BrandService.java
   
   + [ Concrete:open_file_folder: : (Somut sınıflarımı içerir.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/business/concretes)
     + BrandManager.java
  
   + [Requests:open_file_folder:  :(Bu dosya projedeki request pattern'lere uygun yazım için ilgili classları içeren dosyamız.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/business/requests)
     + CreateBrandRequests.java
     + UpdateBrandRequest.java
     
   + [Responses:open_file_folder: :(Bu dosya projedeki response pattern'lere uygun yazım için ilgili classları içeren dosyamız.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/business/responses)
      + GetAllBrandsResponse.java
      + GetByIdBrandResponse.java
     
   ###  CORE KATMANI
Evrensel kodlarımızı kullandığımız  katmanımızdır.  
Core katmanı diğer katmanları referans almaz.
+ [mappers:open_file_folder:  :(Bu katmanda mapper dosyası ile ModelMapper işlevlerini sağlayacak classlar yer almaktadır.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/core/utilities/mappers)
  + ModelMapperManager.java
  + ModelMapperService.java
  
 ### DATA ACCESS KATMANI 
Veriye ulaşmak için yazdığım katman kısacası SQL kodlarımın mevcut olduğu katman.

 + [Abstract:open_file_folder:  :(İlgili soyut Sınıflarımı içerir. Bu klasörde bulunan repository classlarında ilişkisel model (veritabanı modeli) ile nesne modeli(Java nesnesi) arasında bir köprü oluşturan JPA kullanılmıştır. )](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/dataAccess/abstracts)
  + BrandRepository

### ENTİTİES
 Bu katman yardımcı katmanımdır. Veri tabanına ait nesneleri tutar.
+ [Concrete:open_file_folder:  : (Somut sınıflarımı içerir.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/entities/concretes)
   + Brand.java

###  WebAPI  
[Sadece veri transferi için kullanılır.RestFull mimarisini destekleyen katmandır. bu katmandaki Controller gelen bütün istekleri karşılar.(RESFUL: Http protokolü:Bir kaynağa ulaşmak için izlediğimiz yol diyebiliriz.)](https://github.com/kadernur/CampSpringRentACar/tree/main/rentACar/src/main/java/kodlama/io/rentACar/webApi/controllers)
 + BrandsController.java
     
     
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
