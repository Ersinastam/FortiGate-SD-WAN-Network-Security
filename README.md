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

<img width="1668" height="829" alt="image" src="https://github.com/user-attachments/assets/039c484b-bc92-4f7f-b5a5-b1479c1c2f57" />

<img width="1658" height="803" alt="image" src="https://github.com/user-attachments/assets/289a4bfe-830b-4b35-9415-fbd1c960a007" />
<img width="1646" height="345" alt="image" src="https://github.com/user-attachments/assets/fdfd9f8e-cad8-482e-a158-f0752ba0487b" />


<img width="1660" height="49" alt="image" src="https://github.com/user-attachments/assets/6c9d5230-04af-4f2f-b7bf-55f4f0416eb2" />

<img width="1654" height="734" alt="image" src="https://github.com/user-attachments/assets/01691f0f-c27a-4a57-8da2-16a673379ab8" />
<img width="1649" height="290" alt="image" src="https://github.com/user-attachments/assets/1a6f1bfe-43fb-4cc2-aef7-ad96275f8c97" />


<img width="1582" height="829" alt="image" src="https://github.com/user-attachments/assets/97a7c8b5-b6d5-4498-a188-41f40bd797dc" />
<img width="1653" height="242" alt="image" src="https://github.com/user-attachments/assets/d6cb25d7-2fbc-4aea-b8e7-bf926139577a" />


