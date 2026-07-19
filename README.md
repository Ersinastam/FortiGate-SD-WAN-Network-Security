# FortiGate-SD-WAN-Network-Security

Bu proje, iki farklı ISP hattı üzerinde FortiGate SD-WAN mimarisi kullanılarak; uygulama bazlı dinamik yönlendirme, SLA tabanlı hat sağlığı kontrolü ve kurumsal trafik mühendisliği tekniklerini içermektedir

<img width="782" height="904" alt="image" src="https://github.com/user-attachments/assets/939b6725-9359-460f-89bc-64e414145957" />

# SD-WAN Nedir ve Neden Kullanıyoruz?

SD-WAN (Software-Defined Wide Area Network), geleneksel WAN mimarilerinin aksine, ağ trafiğini kontrol düzlemi (control plane) üzerinden yöneten yazılım tabanlı bir teknolojidir.

### Projedeki Kullanım Amacımız:

Geleneksel yapılarda trafik genellikle statik rotalar üzerinden (sabit hatlardan) akar. Ancak bu projede SD-WAN'ı şu amaçlarla kurduk:

* Uygulama Odaklılık: Trafiğin sadece hedef IP'ye göre değil, içerdiği uygulamaya (Zoom, Teams, ERP vb.) göre ayırt edilerek en optimize yoldan gitmesini sağlamak.

* Akıllı Trafik Yönetimi: Hatların fiziksel durumunu (Up/Down) değil, "kalitesini" (Latency, Jitter, Loss) gerçek zamanlı izleyerek, kullanıcı deneyimini en üst seviyede tutmak.

* Maliyet ve Verimlilik: Kurumsal trafiği yüksek maliyetli/performanslı hatta, genel trafiği ise her iki hattı verimli kullanarak dağıtmak.

Bu proje ile geleneksel statik yönlendirme yerine, dinamik, esnek ve hat sağlığına duyarlı bir ağ altyapısı kurgulanmıştır.

### Kritik İş Uygulamaları için SD-WAN Trafik Yönetimi

<img width="1920" height="1181" alt="image" src="https://github.com/user-attachments/assets/57a901d6-b8e7-41c7-965d-729b0d70b010" />

Bu kural, Zoom, Microsoft Teams ve Cisco Webex gibi gecikmeye duyarlı (latency-sensitive) iş uygulamalarının trafik akışını yönetmektedir. Lowest Cost (SLA) stratejisi ile yapılandırılan bu politika; Google_Dns üzerinden anlık olarak izlenen hat kalitesi (jitter, latency, packet loss) verilerini baz alır. Böylece, kritik görüşmelerin her zaman en yüksek performanslı WAN hattı üzerinden gerçekleştirilmesi sağlanarak, hat kaynaklı kopmaların önüne geçilmiş ve kullanıcı deneyimi garanti altına alınmıştı

### Misafir Ağı (Guest Network) İçin Trafik İzolasyonu

<img width="1920" height="775" alt="image" src="https://github.com/user-attachments/assets/e828a095-5607-4b92-8d0c-4cbc91cc985a" />

Kurumsal ağın güvenliğini ve ana iş trafiğinin performansını korumak amacıyla, misafir kullanıcılar için özel bir trafik politikası oluşturulmuştur. Bu politika, misafir trafiğini Manual stratejisi ile yedek hat (WAN2) üzerinden yönlendirerek, ana hattın (WAN1) kapasitesini kurumsal ihtiyaçlara (ERP, Zoom, Teams vb.) ayırmaktadır. Böylece, misafir kullanıcıların yoğun internet kullanımı kurumsal operasyonlarda herhangi bir darboğaza (bottleneck) sebebiyet vermemektedir.

### Genel İnternet Trafiği için Yük Dengeleme (Load Balancing)

<img width="1920" height="1139" alt="image" src="https://github.com/user-attachments/assets/a06525c9-9d00-4cf5-b021-ce5e39ebc097" />


Kurumsal ağdaki tüm VLAN segmentlerinden (VLAN10, VLAN20) çıkan ve özel bir kurala takılmayan genel internet trafiği, Maximize Bandwidth (SLA) stratejisi ile yönetilmektedir. Bu yapılandırma; her iki WAN hattının (WAN1 ve WAN2) toplam bant genişliğini verimli bir şekilde kullanarak yük dengelemesi sağlar. Required SLA target olarak tanımlanan Google_Dns üzerinden hat sağlığı sürekli denetlenmekte; bu sayede hatlardan birinde performans kaybı yaşanması durumunda trafik, otomatik olarak sağlıklı olan hat üzerinden akmaya devam ederek ağ sürekliliği (High Availability) sağlanmaktadır.

