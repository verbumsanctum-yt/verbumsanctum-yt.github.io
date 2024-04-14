---
layout: article
titles:
  en      : &EN       About
  en-GB   : *EN       About
  en-US   : *EN       About
  en-CA   : *EN       Aboot
  en-AU   : *EN       About
key: page-about
---

<div>
  <h1>Our Team</h1>
</div>
{% for author in site.data.authors %}
<div class="author-profile">
  <h2>{{ author[1].name }}</h2>
  <p>{{ author[1].bio }}</p>
  <p>Email: <a href="mailto:{{ author[1].email }}">{{ author[1].email }}</a></p>
  <p>Website: <a href="{{ author[1].website }}" target="_blank">{{ author[1].website }}</a></p>
  <ul class="social-links">
    {% if author[1].twitter %}
    <li><a href="https://twitter.com/{{ author[1].twitter }}">Twitter</a></li>
    {% endif %}
    {% if author[1].github %}
    <li><a href="https://github.com/{{ author[1].github }}">GitHub</a></li>
    {% endif %}
    {% if author[1].linkedin %}
    <li><a href="https://linkedin.com/in/{{ author[1].linkedin }}">LinkedIn</a></li>
    {% endif %}
    {% if author[1].instagram %}
    <li><a href="https://instagram.com/{{ author[1].instagram }}">Instagram</a></li>
    {% endif %}
  </ul>
  <div>
    <h3>Cryptocurrencies:</h3>
    <ul>
      {% if author[1].crypto.btc %}
      <li>Bitcoin (BTC): {{ author[1].crypto.btc }}</li>
      {% endif %}
      {% if author[1].crypto.eth %}
      <li>Ethereum (ETH): {{ author[1].crypto.eth }}</li>
      {% endif %}
      {% if author[1].crypto.xmr %}
      <li>Monero (XMR): {{ author[1].crypto.xmr }}</li>
      {% endif %}
    </ul>
  </div>
</div>
{% endfor %}
