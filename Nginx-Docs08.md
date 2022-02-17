# Traffic Distribution Methods

**Trafiğin Eşitsiz Dağılımı**

Server Weight, bir Load Balancer görevi gören Nginx ile upstream backend arasındaki istek akışını özelleştirmemize olanak tanır.

Örnek Yapılandırma;

![enter image description here](https://i.hizliresim.com/9emfkrm.png)

Bu yapılandırmada, her 3 istekten 2'si 10.139.0.4'e ve 1'i 10.139.0.3'e gönderilir.

**Least_conn**

    upstream backend {
       least_conn;
       server 10.1.0.101; 
       server 10.1.0.102;
       server 10.1.0.103;
    }

En az bağlantıya dayalı yük dengeleme, başka bir basit yöntemdir. Adından da anlaşılacağı gibi, bu yöntem istekleri o anda en az aktif bağlantıya sahip sunucuya yönlendirir. İsteklerin tamamlanmasının bazen daha uzun sürebileceği uygulamalarda, döngüsel denemeden daha adil çalışır.

least_conn bağlantı dengeleme yöntemini etkinleştirmek için, aşağıdaki örnekte gösterildiği gibi yukarı akış bölümünüze least_conn parametresini ekleyin.

![enter image description here](https://www.nginx.com/wp-content/uploads/2018/11/least-conn_power-of-two-choices.png)


[Load Balancing Methods Wiki](https://upcloud.com/community/tutorials/configure-load-balancing-nginx/)
