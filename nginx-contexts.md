# Welcome to StackEdit!

Contexts Temelleri

Context Temelleri, Nginx yapılandırma dosyası çeşitli bağlamlara (bölümlere) bölünmüştür. Her context, Nginx'in yönünü kontrol etmek için kendi yönergelerini içerir. 

![enter image description here](https://i.imgur.com/8f6riC6l.jpg)


Main Context

Tamamen bağlam bloklarının dışında bulunan herhangi bir Yönergenin "Main" context içerisinde yaşadığı söylenir. Main Context, tüm uygulamayı temel düzeyde etkileyen ayrıntıları yapılandırmak için kullanılır.

![enter image description here](https://image.slidesharecdn.com/nginx2-170327073647/95/introduction-to-nginx-15-638.jpg?cb=1490600331)

Event Context

Nginx'in bağlantıları genel düzeyde nasıl ele aldığını tanımlar Worker_Connections, bir worker process tarafından açılabilen maksimum eşzamanlı bağlantı sayısını ayarlar.

HTTP Context

Bu context öncelikle üretim ortamlarında çalışacaksınız. Bu context, HTTP veya HTTPS bağlantılarının ve ilişkili parametrelerin nasıl ele alınacağını tanımlamak için gerekli tüm yönergeleri ve diğer context'leri içerir.
