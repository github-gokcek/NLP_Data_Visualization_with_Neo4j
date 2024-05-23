# Web Sitesi Analizleri ve Bilgi Grafiği
<br></br>
## Amaç
Bu çalışmanın temel araştırma sorusu, "Kurumsal firma siteleri kullanıcı verimliliğini ve amaca hizmet etme açısından nasıl değerlendirilebilir?" şeklindedir. Bu bağlamda, çalışmanın amacı, doğal dil işleme teknikleri kullanarak sitelerin verimlilik analizini yapmak ve kullanıcı deneyimini iyileştirmek için somut önerilerde bulunmaktır.
<br></br>
## Giriş
 - Bir websitesi şirketi temsil eder. Websitesi genellikle ürün vehizmetleri tanıtmak ve satışları
 artırmak için kullanılır.
 - Ancak, websitesi zamanla değişir ve düzensiz hale gelebilir. Bu nedenle, websitesinin düzenli olarak değerlendirilmesi önemlidir
 - Ticari SEO araçlarının yanı sıra kodlama bilgisiyle websitesinin analiz edilip iyileştirilmesi mümkündür.
<br></br>
## Yöntem
- Bu projede, doğal dil işleme (NLP) teknikleri kullanılarak sitelerin içerikleri analiz edilecektir.
- Bu analizler sonucunda, sitelerin hangi bölümlerinin kullanıcılar tarafından daha sık ziyaret edildiği, hangi içeriklerin kullanıcılar tarafından daha değerli bulunduğu gibi veriler elde edilecektir.
- Bu veriler grafik şemaları ile görselleştirilecek ve sitelerin verimliliği hakkında net bir tablo sunulacaktır.
<br></br>
## Kaynaklar ve Literatür Taraması
Bu çalışma, mevcut literatürde yer alan kurumsal web sitelerinin verimliliği ve kullanıcı deneyimi ile ilgili araştırmalara dayanmaktadır. Ayrıca, doğal dil işleme tekniklerinin verimlilik analizlerinde nasıl kullanılabileceğine dair örnekler ve yöntemler incelenecektir.

### Analiz Yöntemleri 
- Web sitesi analizleri için kullanılan yöntemler arasında Google Analytics, Hotjar ve A/B testleri bulunmaktadır. Bu yöntemler, web sitesinin etkili bir şekilde analiz edilmesini sağlar
-  Biz bu yazıda NPL modelleri ve Neo4j GDS/GDB sistemleri ile analizlerde bulunacağız
- Bunların dışında <b>100</b>'lerce algoritma ve <b>1000</b>'lerce model vardır. 
<br></br>
## Sonuç ve Tartışma
Elde edilen analiz sonuçları, kurumsal firma sitelerinin verimliliğini artırmak için uygulanabilecek stratejiler ve öneriler sunacaktır. Bu stratejiler, sitelerin kullanıcı dostu hale getirilmesi, içeriklerin optimize edilmesi ve genel kullanıcı deneyiminin iyileştirilmesi için rehberlik edecektir.

Bu proje, kurumsal firma sitelerinin verimlilik analizine yönelik yenilikçi bir yaklaşım sunarak, sitelerin kullanıcılar için daha etkili ve verimli hale getirilmesine katkı sağlayacaktır.
<br></br>
## Süreç
- <b>Keyword</b> ve <b>SentenceTransformer</b>'a ihtiyacımız var. Bu modellere Hugging Face üzerinden erişeceğiz.
- Modellerimiz olduğuna göre işlenecek verilere erişmek için Selenium aracılığı ile gerekli verileri çekeceğiz.
- Bu Verileri <b>Neo4j GDB</b> üzerinde toplayacağız.
- Veriler üzerinde istediğim <b>Graph</b> ve <b>Analiz</b> fonksiyonları ile anlamlı verilerçıkartmaya çalışacağız.

### Bilgi Grafiği Kullanımı
- Bilgi grafiği, web sitesi analizlerinin sonuçlarını görsel olarak temsil etmek için kullanılır. Bu grafiğin amacı, <b>verilerin anlaşılmasını</b> ve <b>karar verme sürecini kolaylaştırmayı</b> sağlamaktır.
- Bu çıktıyı sonradan <b>Neo4j</b> üzerinde görüntüleceğiz

<br></br>
<div align="center">
<b>Örnek Analiz Sonucu</b>
<p >
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/ca0cdda4-9bfc-412d-9494-12b2e2c3712c"/>
</p>

<b>Örnek Grafik Sonucu</b>
<p >
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/0c75cb25-e779-45c2-b168-fc9f0bd12d21"/>
</p>
</div>

## Yapılabilitesi
-  Sitemizin ne kadar dış bağlantı verdiğini görmek ve buna göre bir aksiyon almak isteyebiliriz. Örneğin;
<p align="center">
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/41cc8a72-36b6-45f6-8eaa-ae3115ded23e"/>
</p>

- <b>Ölü bağlantıları</b> test etmek iyi bir fikir olabilir. Ölü bağlantılar <b>404</b> status kodu gönderen içi boş bağlantılardır. Unutulmuş veya bozulmuş olabilirler bunları tespit etmek performansı iyileştirecektir. Biz önceden yaptığımız analiz sırasında biliyoruz ki Neo4j için 9000 bağlantıdan 241 tane ölü bağlantı var.</b>

- Çoğu web sitesi, kullanıcıları nihai hedeflerine ulaşmaları için yönlendirmek üzere tasarlanmıştır. Örneğin, bir e-ticaret sitesinde bu hedef genellikle bir satın alma işlemi olabilir. Ancak, bazı durumlarda kullanıcıların istenilen hedefe ulaşması karmaşık ve uzun olabilir. Örneğin, <a hreF="https://neo4j.com/docs">Neo4j Doc</a> sayfasına gelen bir kullanıcının <a href="https://console.neo4j.io">Console Neo4j</a> <b>adresine gitmek için dört farklı bağlantıya tıklaması gerekebilir.</b> Bu durum, kullanıcı deneyimini olumsuz etkileyebilir ve potansiyel müşteri kaybına yol açabilir. Bu nedenle, bağlantı analizi yaparak ve web sayfalarının önemini sıralamak için merkezilik algoritmaları kullanarak kullanıcı yolculuğunu optimize edebiliriz. Bu analizler, kullanıcıların hedeflerine daha hızlı ve kolay ulaşmalarını sağlayarak müşteri memnuniyetini artırabilir.
<p align="center">
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/b9cbee3b-6d73-4f3b-ac87-b56b0a977333"/>
</p>
Buradan anlayabiliyoruz ki en çok dış bağlantıyı <b>developer/kb</b> uzantısı veriyor. Bir iyileştirme planlanıyor ise en çok kişiye ulaşması bakımından en önce buradan başlanmalıdır

-  Google Bağlantı analizi için dış bağlantıları direkt kullanmanın eksik kalabileceğinin farkındaydılar ve PageRank algoritmasını geliştirdiler. Peki Bu algoritma bize ne söylüyor.

<p align="center">
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/18974bc4-f676-4641-b949-d8278b838ad2"/>  
</p>

 <b>Developer/kb</b> yerini koruyor. Yani bu **öngürülerimizi** doğruluyor. Diğer **ilk 4'ün** yer değiştirmesi ise odağımızı bu tarafa kaydırmak için bir işaret.

-  Anahtar kelimeler arama motoru optimizasyonu için çok önemlidir. Doğru kelimeleri doğru yerde kullandığımızdan emin miyiz? Sitemizdeki keyword'lere bir göz atalım Sitemizdeki **keyword**'lere bir göz atalım:

<p align="center">
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/08c8f77d-1b35-49e8-ae21-19953d35f304"/>
</p>

**Sonuçlar beklendik gözüküyor. Ancak Java'nın bu kadar çok kullanılması ayrı bir dikkati hakkediyor.**

-  **HAS_KEYWORD** ilişkilerine bakıp daha fazla
 bilgi edinmeye çalışmak bize fazlasıyla bilgi
 verebilir.
 1. Sayfa ve düğümler arasında **HAS_KEYWORD** ilişkisi kuralım.
 2. Birlikte sıkça görülen anahtar kelimeler arasında **CO_OCCUR** ( tekrarlama) ilişkisi oluşturalım
 3. **Louvain** yöntemi gibi bir topluluk algılama algoritması çalıştıralım

<p align="center">
  <img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/5e9a39b6-5018-4e15-a563-e8dd9873ee00"/>
</p>
<div align="center">
<b>Beklenen Sonuç</b>
</div>
<p align="center"><img src="https://github.com/github-gokcek/NLP_Data_Visualization_with_Neo4j/assets/149272091/fce713ed-67a6-499d-9fe9-54de05df0593" /></p>

<br></br>
# Proje Dahilindeki Kişiler
- Ali Asker GÖKÇEK (195541015)
- Burak Furkan ERKEMEN (195541040)
