# Reverse Proxy

![enter image description here](https://avinetworks.com/wp-content/uploads/2020/01/reverse-proxy-server-diagram_1.png)
Reverse Proxy, bir veya daha fazla sunucudan bir istemci adına kaynakları alan bir proxy sunucusu türüdür.

Reverse proxy ne yapabilir?

Reverse proxy, aşağıdakiler gibi birçok kullanım durumu elde etmek için kilit rol oynayabilir:

 - Orijinal arka uç sunucularının varlığını gizler.
 - Arka uç sunucuları web tabanlı saldırılara, DOS'a ve çok daha fazlasına karşı koruyabilir.
 - Harika önbelleğe alma işlevi sağlayabilir.
 - İçeriği sıkıştırarak optimize edebilir.
 - SSL Sonlandırma proxy'si olarak hareket edebilir.
 - Yönlendirme isteği ve daha fazlası.
 - İstek, URI'ye göre yönlendirilebilir.

**proxy_pass**
![enter image description here](https://i.hizliresim.com/skny7qs.png)

> proxy_pass yönergesi, isteği yönergeyle birlikte belirtilen proxy sunucusuna iletir.

![enter image description here](https://i.hizliresim.com/bizphhy.png)

> Using multiple proxy_pass statements and redirecting by URI.

[Reverse Proxy Docs](https://www.imperva.com/learn/performance/reverse-proxy/)

