# Load Balancer
![enter image description here](https://www.journaldev.com/wp-content/uploads/2019/03/nginx-load-balancing.png)

Şirketiniz, tüm üretim trafiğine hizmet eden 1 sunucuya uygulama yükledi. Bu sunucu herhangi bir nedenle çökerse, tüm üretim trafiği etkilenir.

> Nginx, sunucularınızın kaynak kullanılabilirliğini ve verimliliğini artırmak için bir yük dengeleyici olarak yapılandırılabilir.

Bu yaklaşımda, birden çok sunucu kümesi oluşturursunuz.
Artık trafiği sunucular arasında dağıtmak için ek bir Yük Dengeleyici bileşeni eklersiniz.

Yük Dengeleyiciler, trafiği sunucular kümesi arasında dağıtmaktan başka birçok şey yapar.
Load Balancer'ların önemli bir özelliği, backend sunucularının Sağlık Kontrolü'dür.
Backend sunucularına dağıtılan birden çok algoritma vardır.
Yük Dengeleyiciler, SSL/TLS sonlandırmasını destekleyebilir.


**Upstream Bloğunun Önemi**

![enter image description here](https://i.hizliresim.com/ff3rmvf.png)

upstream bloğu, Trafiğin dağıtılmasını istediğiniz sunucu grubunu belirtmek için kullanılabilir.

**Örnek Yapılandırma**

![Örnek yapılandırma](https://i.postimg.cc/KYSdM5vD/Screen-Shot-2022-02-16-at-2-53-56-PM.png)



