---
layout: article
key: page-about
---
# Our Team

{% for author in site.data.authors %}

## {{ author[1].name }}

{{ author[1].bio }}

Email: [{{ author[1].email }}](mailto:{{ author[1].email }})

Website: [{{ author[1].website }}]({{ author[1].website }}){:target="_blank"}

{:.social-links}

* {: .social-link if author[1].twitter }[Twitter](https://twitter.com/{{ author[1].twitter }})
* {: .social-link if author[1].github }[GitHub](https://github.com/{{ author[1].github }})
* {: .social-link if author[1].linkedin }[LinkedIn](https://linkedin.com/in/{{ author[1].linkedin }})
* {: .social-link if author[1].instagram }[Instagram](https://instagram.com/{{ author[1].instagram }})
* {: .social-link if author[1].youtube }[YouTube](https://youtube.com/@{{ author[1].youtube }})

### Cryptocurrencies

* {: .crypto if author[1].crypto.btc }Bitcoin (BTC): {{ author[1].crypto.btc }}
* {: .crypto if author[1].crypto.eth }Ethereum (ETH): {{ author[1].crypto.eth }}
* {: .crypto if author[1].crypto.xmr }Monero (XMR): {{ author[1].crypto.xmr }}

{% endfor %}
