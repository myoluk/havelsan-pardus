# rDNS (reverse DNS) Nedir/Neden Kullanılır?

### DNS Nedir?
- **DNS** (Domain Name System / Alan Adı Sistemi), IP adreslerini daha anlaşılabilir yapan bir adlandırma sistemidir. Örneğin; [duckduckgo.com](https://duckduckgo.com) adresi aslında [40.114.177.156](40.114.177.156) IP adresine karşılık gelen bir alan adıdır. Öyle ki bu IP adres ile yine duckduckgo.com adresine gidilebilir. Yani alan adı, bir IP adresine karşılık gelmektedir. Alan adına ping gönderilerek karşılık gelen IP adresi bulunabilir:
```
ping duckduckgo.com
```

### rDNS Nedir?
- **rDNS** (reverse DNS / ters DNS) de ise bunun tam tersi, yani IP adresi alan adına karşılık gelmektedir. IP adresine karşılık gelen alan adı çözümlenirken PTR kayıtları (PTR records) kullanılır.

- rDNS çözümlemesi, IPv4 ve IPv6 için farklı yöntemler kullanır. IPv4 için `in-addr.arpa` özel alan adını, IPv6 için `ip6.arpa` özel alan adını kullanır.

- IPv4 için örnek verecek olursak; [8.8.4.4](https://8.8.4.4) IP adresinin ters alan adı (rDNS) çözümlemesi için PTR kayıtlarında `4.4.8.8.in-addr.arpa` aranır ve kayıt, [dns.google](https://dns.google) ile eşleşir. 

### rDNS Neden Kullanılır?
- DNS, alan adlarını IP ile eşleştirir ve bu IP adresi ile eşleşen birden fazla alan adı olabilir. Yani alan adı ile IP adresi arasında çoktan-bire eşleşme vardır.

- rDNS ise IP adresini alan adı ile eşleştirir ve IP adresleri tekil olduğundan yalnız bir alan adı ile eşleşir. Yani alan adı ile IP adresi arasında bire-bir eşleşme vardır.

- rDNS ile sağlanan bire-bir eşleşmeler ileti onayı, günlük kaydı (logging), e-posta için anti-spam tekniği olarak kullanılabilir.

### Dipnot:
Havelsan Liman uygulamasında domain oluştururken '*Domain'e katılamadınız!*' hatası alırsanız, istemci cihazda rdns özelliğini kapatmayı deneyiniz. Linux istemciler için:
`/etc/krb5.conf` dosyasından `rdns=false` yapılarak kapatılabilir.

*Kaynak ve detaylı bilgi için:*
*[https://en.wikipedia.org/wiki/Reverse_DNS_lookup](https://en.wikipedia.org/wiki/Reverse_DNS_lookup)*
