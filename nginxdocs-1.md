# Nginx Docs - 1

Nginx yapılandırma dosyası, Nginx'in hangi istekleri çalıştıracağına ve işleyeceğine bağlı olarak çeşitli ayarlardan oluşur.

![enter image description here](https://image.slidesharecdn.com/igorsysoev-nginx-140117075821-phpapp02/95/2013-igor-sysoev-nginx-origen-evolucin-y-futuro-php-conference-argentina-4-638.jpg?cb=1390973748)

Nginx'in bir Main process ve bir veya daha fazla worker process vardır. Main process(sürecin) temel amacı, yapılandırma dosyalarını okumak ve değerlendirmek ve ayrıca çalışan işlemleri sürdürmektir. Worker process, isteklerin fiili olarak işlenmesini gerçekleştirir.

    root       15511       1  0 Feb07 ?        00:00:00 nginx: master process /usr/sbin/nginx -g daemon on; master_process on;
    www-data   15513   15511  0 Feb07 ?        00:00:00  \_ nginx: worker process
    www-data   15514   15511  0 Feb07 ?        00:00:00  \_ nginx: worker process
    www-data   15515   15511  0 Feb07 ?        00:00:00  \_ nginx: worker process
    www-data   15516   15511  0 Feb07 ?        00:00:00  \_ nginx: worker process

**Önemli Yapılandırma Yönergeleri;**

user : worker processes tarafından kullanılan kullanıcı kimlik bilgilerini tanımlar;

worker processes : worker processes sayısını tanımlar. Bunu mevcut CPU çekirdeklerinin sayısına ayarlamak iyi bir başlangıç olacaktır ("auto" değeri onu otomatik olarak algılamaya çalışacaktır)

error_log : Hata Günlüğü dosyasının yolu.

pid : Main process işlem ID'sini saklayacak bir dosya tanımlar.

```
