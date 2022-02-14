# Basics Nginx

![enter image description here](https://www.ruraldock.com/images/20190303165944572.png?%20X-oss-process=image/watermark,%20type_ZmFuZ3poZW5naGVpdGk,%20shadow_10,%20text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3lwcDkxenI%20=,%20size_16,%20color_FFFFFF,%20t_70)
log_format = Günlüklerin ve ilgili parametrelerin biçimini tanımlar.
access_log = Kullanıcıların web sunucunuza yaptığı isteklerin listesi.

**Nginx CLI**

Nginx, belirli işlemleri gerçekleştirmek için çeşitli komut satırı seçenekleri sunar.

**Seçenekler ve Açıklama**

 1. -v = Sürümü yazdır.
 2. -V = Nginx sürümünü yazdır, Derleyici sürümü ve parametreleri yapılandır.
 3. -t = Çalıştırmayın, sadece yapılandırma dosyasını test edin.
 4. -c = Nginx'in varsayılan yerine hangi yapılandırma dosyasını kullanması gerektiğini belirtin.

**Include**

![enter image description here](https://i.hizliresim.com/8fctye3.png)

Tüm yapılandırmayı tek bir nginx.conf dosyasına eklerseniz, daha uzun vadede yönetmek büyük ve zor olacaktır.
![enter image description here](https://miro.medium.com/max/1400/1*Jg-UHj1APjUBAsq4ZUO_-g.png)
Bunu aşmak için, konfigürasyona başka bir dosya dahil eden include direktifini kullanıyoruz.

**Server Blocks**

Nginx, yapılandırma ayrıntılarını gruplamak ve birden çok etki alanını tek bir sunucuda barındırmak için sunucu bloklarını kullanır.

![enter image description here](https://user-images.githubusercontent.com/32312712/61088623-b004c980-a430-11e9-8a8b-eb78856c90d9.png)

Varsayılan sunucu blokları, tek bir alan tabanlı web sitesi için yeterince iyi olabilir. Birden çok etki alanı tabanlı web siteleri için birden çok sunucu bloğu oluşturmamız gerekir.




