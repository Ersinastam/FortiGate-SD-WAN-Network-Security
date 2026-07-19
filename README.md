# FortiGate-SD-WAN-Network-Security

Bu proje, iki farklı ISP hattı üzerinde FortiGate SD-WAN mimarisi kullanılarak; uygulama bazlı dinamik yönlendirme, SLA tabanlı hat sağlığı kontrolü ve kurumsal trafik mühendisliği tekniklerini içermektedir

<img width="782" height="904" alt="image" src="https://github.com/user-attachments/assets/939b6725-9359-460f-89bc-64e414145957" />

# SD-WAN Nedir ve Neden Kullanıyoruz?

SD-WAN (Software-Defined Wide Area Network), geleneksel WAN mimarilerinin aksine, ağ trafiğini kontrol düzlemi (control plane) üzerinden yöneten yazılım tabanlı bir teknolojidir.

Projedeki Kullanım Amacımız:

Geleneksel yapılarda trafik genellikle statik rotalar üzerinden (sabit hatlardan) akar. Ancak bu projede SD-WAN'ı şu amaçlarla kurduk:

* Uygulama Odaklılık: Trafiğin sadece hedef IP'ye göre değil, içerdiği uygulamaya (Zoom, Teams, ERP vb.) göre ayırt edilerek en optimize yoldan gitmesini sağlamak.

* Akıllı Trafik Yönetimi: Hatların fiziksel durumunu (Up/Down) değil, "kalitesini" (Latency, Jitter, Loss) gerçek zamanlı izleyerek, kullanıcı deneyimini en üst seviyede tutmak.

* Maliyet ve Verimlilik: Kurumsal trafiği yüksek maliyetli/performanslı hatta, genel trafiği ise her iki hattı verimli kullanarak dağıtmak.

Bu proje ile geleneksel statik yönlendirme yerine, dinamik, esnek ve hat sağlığına duyarlı bir ağ altyapısı kurgulanmıştır.

<img width="1920" height="1181" alt="image" src="https://github.com/user-attachments/assets/57a901d6-b8e7-41c7-965d-729b0d70b010" />






