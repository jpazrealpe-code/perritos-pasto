---
layout: default
title: Inicio
---

<section class="hero">
  <div class="hero__content">
    <span class="kicker">Pasto • Fundación</span>
    <h1>El arte de rescatar peluditos</h1>
    <p class="lead">
      Rescatamos, cuidamos y buscamos hogar para perritos en situación de abandono.
      Tu apoyo se convierte en comida, veterinario y hogares de paso.
    </p>

    <div class="hero__actions">
      <a class="btn btn--primary" href="{{ site.baseurl }}/adopta">🐶 Adopta un peludo</a>
      <a class="btn btn--ghost" href="{{ site.baseurl }}/ayudar">❤️ Dona con Nequi</a>
    </div>
  </div>

  <div class="hero__media">
    <img src="{{ site.baseurl }}/assets/img/hero.jpg" alt="Perritos Pasto">
  </div>
</section>

<section class="donations">
  <div class="donations__card">
    <h2>Apoya nuestra labor</h2>
    <p class="small">Tu aporte ayuda con alimento, medicamentos, transporte y esterilizaciones.</p>

    <div class="donations__methods">
      <div class="method">
        <div class="method__title">Nequi</div>
        <div class="method__text">Aquí va tu número Nequi</div>
      </div>
      <div class="method">
        <div class="method__title">QR</div>
        <div class="method__text">Sube tu QR a <code>assets/img/qr-nequi.png</code></div>
      </div>
    </div>

    <a class="btn btn--primary" href="{{ site.baseurl }}/ayudar">Ver donaciones</a>
  </div>
</section>

<section class="section">
  <div class="section__head">
    <h2>Nuestra misión</h2>
    <p class="small">
      Brindar atención y protección a perritos vulnerables, y promover adopción responsable.
    </p>
  </div>

  <div class="grid grid--3">
    <div class="card card--soft">
      <h3>Lo que hacemos</h3>
      <p>Rescate, atención veterinaria, recuperación y búsqueda de hogar definitivo.</p>
    </div>
    <div class="card card--soft">
      <h3>Lo que queremos</h3>
      <p>Fomentar esterilización, respeto por la vida y cero maltrato animal.</p>
    </div>
    <div class="card card--soft">
      <h3>Nuestra meta</h3>
      <p>Cada adopción responsable cambia dos vidas: la de ellos y la tuya.</p>
    </div>
  </div>
</section>

<section class="impact">
  <div class="impact__box">
    <div class="impact__number">+ 100</div>
    <div class="impact__text">Peluditos rescatados (pon tu número real cuando lo tengas)</div>
  </div>
</section>

<section class="section">
  <div class="section__head">
    <h2>Haz parte del cambio</h2>
    <p class="small">Cuatro formas rápidas de ayudar.</p>
  </div>

  <div class="grid grid--4">
    <div class="card">
      <h3>Adopta</h3>
      <p>Conoce a tu alma gemela y dale un hogar.</p>
      <p><a href="{{ site.baseurl }}/adopta">Ver adopciones →</a></p>
    </div>

    <div class="card">
      <h3>Apoya</h3>
      <p>Donaciones con Nequi para alimento y veterinario.</p>
      <p><a href="{{ site.baseurl }}/ayudar">Donar →</a></p>
    </div>

    <div class="card">
      <h3>Hogar de paso</h3>
      <p>Un lugar temporal mientras encuentran familia.</p>
      <p><a href="{{ site.baseurl }}/ayudar">Quiero ser hogar →</a></p>
    </div>

    <div class="card">
      <h3>Difunde</h3>
      <p>Comparte sus historias y jornadas en redes.</p>
      <p><a href="{{ site.baseurl }}/contacto">Ver redes →</a></p>
    </div>
  </div>
</section>

<section class="section">
  <div class="section__head section__headRow">
    <div>
      <h2>Perritos en adopción</h2>
      <p class="small">Se cargan desde <code>_perritos</code>.</p>
    </div>
    <a class="btn btn--ghost" href="{{ site.baseurl }}/adopta">Ver todos →</a>
  </div>

  <div class="grid grid--3">
    {% assign adoptables = site.perritos | slice: 0, 3 %}
    {% for p in adoptables %}
    <div class="card">
      {% if p.foto %}<img src="{{ p.foto | prepend: site.baseurl }}" alt="Foto de {{ p.nombre }}">{% endif %}
      <h3>{{ p.nombre }}</h3>
      <p class="small">
        <span class="pill">{{ p.edad }}</span>
        <span class="pill">{{ p.tamano }}</span>
        <span class="pill">{{ p.ciudad }}</span>
      </p>
      <p>{{ p.excerpt }}</p>
      <p><a href="{{ p.url | prepend: site.baseurl }}">Ver ficha →</a></p>
    </div>
    {% endfor %}
  </div>
</section>

<section class="section">
  <div class="section__head section__headRow">
    <div>
      <h2>Blog</h2>
      <p class="small">Actualizaciones y casos.</p>
    </div>
    <a class="btn btn--ghost" href="{{ site.baseurl }}/historias">Ver blog →</a>
  </div>

  <div class="grid grid--3">
    {% for post in site.posts limit:3 %}
    <div class="card">
      <h3><a href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a></h3>
      <p class="small">{{ post.date | date: "%d/%m/%Y" }}</p>
      <p>{{ post.excerpt }}</p>
    </div>
    {% endfor %}
  </div>
</section>
