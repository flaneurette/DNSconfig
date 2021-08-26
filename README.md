# DNSconfig
Generic DNS configuration. (Be mindful of the reversed arpa address, which reverses the IP)


            Raw AXFR output
            ; domain.tld
            ;
            domain.tld.	172800	IN	SOA	ns1.dns.tld. hostmaster.dns.tld. (
                      2021082607	;serial
                      86400		;refresh
                      7200		;retry
                      3600000	;expire
                      86400	)	;minimum
            domain.tld.	28800	IN	A	1.0.0.127
            domain.tld.	28800	IN	NS	ns1.dns.tld.
            domain.tld.	28800	IN	NS	ns2.dns.tld.
            domain.tld.	28800	IN	NS	ns3.dns.tld.
            domain.tld.	28800	IN	NS	ns4.dns.tld.
            domain.tld.	28800	IN	NS	ns5.dns.tld.
            domain.tld.	28800	IN	SPF	"domain.tld IN TXT v=spf1 ip4:1.0.0.127 a:hostmaster.dns.tld"
            domain.tld.	172800	IN	TXT	google-site-verification=XXXXXXXXXXXXXX
            domain.tld.	14400	IN	TXT	"v=spf1 +a +mx +ip4:1.0.0.127 ~all"
            mail.domain.tld.	14400	IN	CNAME	domain.tld.
            mail.domain.tld.	14400	IN	MX	10 domain.tld.
            mail.domain.tld.	86400	IN	PTR	127.0.0.1.in-addr.arpa.
            mx.domain.tld.	14400	IN	MX	10 domain.tld.
            spf.domain.tld.	86400	IN	TXT	"domain.tld  IN TXT v=spf1 ip4:1.0.0.127 a:hostmaster.dns.tld"
            www.domain.tld.	28800	IN	A	1.0.0.127
            _dmarc.domain.tld.	86400	IN	TXT	"v=DMARC1; p=none; rua=mailto:info@domain.tld;"
