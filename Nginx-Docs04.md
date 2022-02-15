# X-Real-IP
Sorun nedir?

![enter image description here](https://i.hizliresim.com/ff1k2z8.png)

Varsayılan olarak, backend sunucusu, Reverse Proxy sunucusundan gelen tüm istekleri alır ve tüm erişim günlükleri Nginx IP'ye sahip olur. İstemci IP düzeyinde yapılması gereken birçok kullanım durumu için bu bir sorun olacaktır.

![enter image description here](https://i.hizliresim.com/mlz22dj.png)

İşleri Yapmanın İdeal Yolu Bu yaklaşımda, sunucuyu, gerçek İstemci IP'sinin backend sunucusunun erişim günlük dosyasında günlüğe kaydedileceği şekilde yapılandırırsınız.

> Yapılandırma;

 **Reverse Proxy Side**

`nano /etc/nginx/conf.d/proxy.conf`

`proxy_set_header X-Real-IP $remote_addr;`

**Backend Server Side**

`nano /etc/nginx/nginx.conf`

`"$http_x_real_ip"`

**Example Log Format**
`        log_format  main  '$remote_addr - $remote_user [$time_local] "$request" '
                          '$status $body_bytes_sent "$http_referer" '
                          '"$http_user_agent" "$http_x_forwarded_for" "$http_x_real_ip"';

        access_log /var/log/nginx/access.log main;`

