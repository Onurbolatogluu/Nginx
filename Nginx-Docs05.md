# Proxy Host Header
![enter image description here](https://i.hizliresim.com/fwezz7l.png)

Varsayılan olarak, Reverse Proxy düzeyinde alınan ana bilgisayar başlığı backend sunucusuna iletilmez.

![enter image description here](https://i.hizliresim.com/lh5f987.png)

Backend sunucusu birden fazla web sitesi/etki alanı ile ilişkili bir uygulama barındırıyorsa, istemci tarafından istenen orijinal etki alanını bilmesinin hiçbir yolu yoktur.

![enter image description here](https://i.hizliresim.com/azbcob2.png)

**Reverse Proxy Level**

`proxy_set_header Host $host`
