# Risk Bazlı Zafiyet Yönetiminde CMDB ve Envanter Entegrasyonunun Stratejik Önemi

Zafiyet yönetimi uzun yıllardır kurumların siber güvenlik gündeminde. Ancak son yıllarda çıtanın çok daha yukarıya taşındığını görüyoruz: artık konu sadece zafiyetleri tespit etmek değil, **iş etkisi penceresinden bakarak doğru riski, doğru anda, doğru ekibe yönlendirmek**. Bu da bizi klasik zafiyet yönetiminden Risk Bazlı Zafiyet Yönetimi (RBVM) yaklaşımına taşıyor.

Tenable, zafiyetleri tespit etme ve önceliklendirme konusunda dünyadaki lider teknoloji üreticilerinden biri. Fakat çözümün sunduğu değerin gerçek anlamda fark yarattığı nokta, ürüne **kurumunuzun envanterini farklı kırılımlarda öğrettiğiniz** anda başlıyor.

## Teknik Raporların Sınırı: Business Context Eksikliği

İşletim sistemi, uygulama veya IP adresi bazlı raporlar; sistem yöneticileri, yama yönetimi ve operasyon ekipleri için son derece değerlidir. Ancak bu raporlar tek başına bir şeyi sunmaz: **iş bağlamı (business context).**

Bir CISO ya da CIO'nun masasına düşen "20.000 kritik zafiyet var" cümlesi, aslında çok az şey anlatır. Asıl sorulması gereken sorular şunlardır:

- Bu zafiyetlerin kaçı **production** ortamımda?
- Kaçı **ana bankacılık** sistemlerimi etkiliyor?
- Hangileri **internete açık** servislerimde?
- Şu an süren **X projesinin** kapsamındaki sistemlerde ne kadar risk var?

İşte bu noktada envanter zekâsı devreye girer.

## Otomatik Sınıflandırma: Tenable'ın Hazır Şablonları

Tenable Security Center üzerinde yer alan yüzlerce hazır şablon, envanterinizi siz hiçbir tanım yapmasanız bile otomatik olarak sınıflandırabilir. MSSQL sunucuları, Web sunucuları, ElasticSearch kümeleri, IP kameralar, yazıcılar gibi farklı teknolojiler ürün tarafından kendiliğinden gruplanır.

Bu, hızlı bir başlangıç için çok değerli bir kapasitedir. Ancak otomatik sınıflandırma yalnızca *teknolojiyi* tanır; **iş süreçlerinizi tanımaz.** Production ile test ortamını, ana bankacılık ile destek sistemlerini, kritik müşteri verisini barındıran sunucu ile dahili bir araç sunucusunu ayırt etmek size kalmıştır.

## Asset Tags: Envanter Bilginizi Ürüne Öğretmek

Tenable Security Center'ın **Asset Tags** özelliği tam da bu boşluğu doldurur. Kurumunuzdaki envanter tanımlamalarını — kritiklik seviyeleri, iş birimleri, lokasyonlar, projeler, uyumluluk kapsamları — ürüne öğrettiğiniz anda zafiyet verileri bambaşka bir anlam kazanır:

- Production sistemlerinizdeki istismara açık (exploitable) riskleri tek bakışta görebilirsiniz.
- Ana bankacılık sistemlerinizdeki yüksek seviye riskler, gürültünün arasında kaybolmaz.
- Belirli bir proje veya iş birimi kapsamındaki riskleri ayrıca raporlayabilirsiniz.
- PCI, KVKK veya ISO kapsamındaki varlıkları ayrı bir mercekle izleyebilirsiniz.

Bu yaklaşım, "20.000 zafiyet" gibi soyut bir rakamı, **karar alınabilir bir tabloya** dönüştürür.

## Tek Bir Asset Tag Üzerinden 20+ Analiz Aracı

Tenable Security Center, spesifik bir Asset Tag altındaki riskleri farklı kırılımlarda analiz edebileceğiniz yaklaşık 20 farklı araç sunar. Birkaç örnek:

- *"Production sistemlerimdeki zafiyetler hangi portlar üzerinde yoğunlaşıyor?"*
- *"Bu varlıklarda en çok hangi VLAN'larda risk birikiyor?"*
- *"Bu varlık grubunda en sık karşılaşılan zafiyet aileleri neler?"*
- *"Hangi sistemlerde hem kritik zafiyet hem de aktif istismar (exploit-in-the-wild) bilgisi var?"*

Tek bir tag'in arkasında bu kadar çeşitli analitik açabilmek, ekiplerinizin saatler süren manuel raporlama yükünü ortadan kaldırır ve karar süreçlerini hızlandırır.

## Görünürlükten Aksiyona: Remediation Planları

Risklerin görünür hale gelmesi başlı başına bir kazanım, ama yolun sonu değil. Bir sonraki adım, bu görünürlüğü **kapatma planlarına** dönüştürmektir.

Kurumsal yapılarda zafiyetler; değişiklik yönetimi (change management), etki analizi ve test süreçleri çerçevesinde oluşturulan remediation planları ile kapatılır. CMDB ve envanter verisinin temiz olduğu ortamlarda bu planlar:

- Doğru sistem sahibine atanır,
- Doğru bakım pencerelerine yerleştirilir,
- İş etkisi öngörülebilir biçimde yönetilir.

Bunun tersi — yani envanter bilgisinin dağınık, sahipsiz ve güncel olmadığı bir ortam — remediation süreçlerinin en sık çıkmaza girdiği noktadır.

## Sonuç: Envanter Yönetimi ile Entegrasyon Şart

Operasyonunuzda envanter yönetimi (CMDB veya kurumsal envanter veritabanı) ile bir entegrasyon kurmanızı kuvvetle öneririm. Burada açık konuşmak gerekir: **birçok kurumun tertemiz bir envanter verisi yok.** Bu belki hiçbir zaman da tam anlamıyla "tertemiz" olmayacak; çünkü envanter, doğası gereği son derece dinamik ve sürekli değişen bir süreç olarak yaşıyor.

Ancak bu tarz entegrasyonlar size iki büyük kazanç sağlar:

1. **Süreç olgunluğu:** Zafiyet platformu ile CMDB arasındaki sürekli senkronizasyon, envanter kalitesizliklerini gün yüzüne çıkarır ve zaman içinde envanter sürecinizi iyileştirmenize zemin hazırlar.
2. **Stratejik karar desteği:** Hepsinden önemlisi, kurumun tepe yöneticilerine teknik gürültüden arındırılmış, **iş bağlamına oturmuş bir risk değerlendirmesi** sunma imkânı verir.

Sonuç olarak; Tenable'ın güçlü tespit ve önceliklendirme yetenekleri, ancak iyi tanımlanmış bir envanter zekâsı ile birleştiğinde gerçek değerini ortaya koyar. Doğru entegrasyon kurulduğunda zafiyet yönetimi, bir IT operasyon başlığı olmaktan çıkar ve **kurumsal risk yönetiminin merkezindeki stratejik bir disipline** dönüşür.
