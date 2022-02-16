# Nginx : Health Check
**Health Check**

![enter image description here](https://miro.medium.com/max/1400/1*jCyoGFOZdWPBbfvyNuhdJQ.png)

Health check, bir upstream grubundaki HTTP sunucularının sağlığını izlemek için kullanılır. Belirli bir sunucu yanıt vermiyorsa, Nginx ona istenenleri göndermeyi durdurur.

**Health Checks Türleri**

Nginx tarafından desteklenen iki tür sağlık kontrolü:

- Active Health Checks (Nginx Plus)
- Passive Health Checks

**Active Health Checks**

Nginx Plus, her sunucuya özel sağlık kontrolü (health check) istekleri göndererek bir upstream sunucusunun sağlığını ve geri dönüş HTTP kodlarını periyodik olarak kontrol edebilir. Herhangi bir iletişim hatası veya zaman aşımı varsa veya 2xx veya 3xx dışında bir kodla yanıt alırsa, upstream sunucusu sağlıksız olarak işaretlenir.

**Passive Health Checks**

Passive Health Checks (Pasif Sağlık Kontrollerinde) Nginx, istemci ile upstream sunucusu arasındaki iletişimi izler. Upstream sunucusu yanıt vermiyorsa veya bağlantıları reddediyorsa, pasif durum denetimi sunucunun sağlıksız olduğunu değerlendirecektir.

Nginx, önceki isteğin başarısız bir yanıtı olması durumunda belirli bir sunucuya yeni istek göndermeyi durdurma yeteneğine sahiptir.

**Önemli Parametreler**

![enter image description here](https://i.hizliresim.com/br8jpfw.png)

Başarısız upstream sunucularına giden trafiği kontrol etmek için upstream bloğunda aşağıdaki iki parametre ayarlanabilir.

- max_fails : Sunucunun kullanılamaz olarak işaretlenmesi için fail_timeout süresi boyunca gerçekleşmesi gereken başarısız denemelerin sayısını ayarlar.
- fail_timeout : Sunucunun kullanılamıyor olarak işaretlenmesi için başarısız denemelerin sayısının ve ayrıca sunucunun kullanılamaz olarak işaretlenmesi için gereken süreyi ayarlar.
