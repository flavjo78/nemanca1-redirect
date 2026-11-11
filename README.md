# nemanca1-redirect

Sito minimo su GitHub Pages che rimanda `nemanca1.com` (senza www) a `https://www.nemanca1.com`,
conservando percorso e parametri. Serve perché il DNS del dominio sta su Tophost, che non permette
un CNAME sul dominio nudo né il redirect verso un sito esterno.

- `index.html` e `404.html`: stessa pagina, rimbalzo immediato via meta refresh + JavaScript.
- `CNAME`: dice a GitHub Pages quale dominio servire.

DNS su Tophost: record `A` di `@` verso gli IP di GitHub Pages (185.199.108.153, .109.153, .110.153, .111.153);
rimosso il record `AAAA` di `@`.
