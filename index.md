---
layout: default
title: Inicio
---

<section class="hero">
  <div class="hero__content">
    <span class="kicker">Fundación ángeles con corazón • Pasto</span>
    <h1>Fundación ángeles con corazón</h1>
    <p class="lead">
      Rescatamos, cuidamos y conectamos perritos con hogares responsables.
      Tu ayuda se convierte en comida, veterinario, transporte y hogares de paso.
    </p>

    <div class="hero__actions">
      <a class="btn btn--primary" href="{{ site.baseurl }}/adopta">🐶 Adopta</a>
      <a class="btn btn--ghost" href="{{ site.baseurl }}/ayudar">❤️ Dona con Nequi</a>
      <a class="btn btn--ghost" href="https://wa.me/573006608605" target="_blank" rel="noopener">💬 WhatsApp</a>
    </div>

    <div class="hero__mini">
      <div class="mini">
        <div class="mini__title">Adopción responsable</div>
        <div class="mini__text">Proceso claro + seguimiento.</div>
      </div>
      <div class="mini">
        <div class="mini__title">Rescate y recuperación</div>
        <div class="mini__text">Apoyo real en casos vulnerables.</div>
      </div>
      <div class="mini">
        <div class="mini__title">Pasto</div>
        <div class="mini__text">Impacto local y comunitario.</div>
      </div>
    </div>
  </div>

  <div class="hero__media">
    <img src="{{ site.baseurl }}/assets/img/hero.png" alt="Fundacion angeles con corazón - Rescate y adopción">
    <div class="hero__badge">
      <div class="badge__title">¿Quieres ayudar ahora?</div>
      <div class="badge__text">Dona con Nequi o comparte un perrito en redes.</div>
      <a class="btn btn--small btn--primary" href="{{ site.baseurl }}/ayudar">Ir a Donaciones</a>
    </div>
  </div>
</section>

<section class="donations">
  <div class="donations__card">
    <h2>Apoya nuestra labor</h2>
    <p class="small">
      Las donaciones cubren alimento, medicamentos, consultas, transporte y esterilización.
      Cada aporte suma 💛
    </p>

    <div class="donations__methods">
      <div class="method">
        <div class="method__title">Nequi</div>
        <div class="method__text">Pega aquí tu número Nequi</div>
      </div>

      <div class="method">
        <div class="method__title">QR Nequi</div>
        <div class="method__text">Sube el QR a <code>assets/img/qr-nequi.png</code></div>
      </div>

      <div class="method">
        <div class="method__title">Contacto</div>
        <div class="method__text">
          <a href="https://wa.me/573006608605" target="_blank" rel="noopener">WhatsApp 300 6608605</a>
        </div>
      </div>
    </div>

    <div class="hero__actions">
      <a class="btn btn--primary" href="{{ site.baseurl }}/ayudar">❤️ Ver Donaciones</a>
      <a class="btn btn--ghost" href="{{ site.baseurl }}/proceso">📋 Proceso de adopción</a>
    </div>
  </div>
</section>

<section class="section">
  <div class="section__head">
    <h2>Nuestra misión</h2>
    <p class="small">
      Proteger y mejorar la vida de perritos vulnerables, promoviendo una comunidad más consciente y solidaria.
    </p>
  </div>

  <div class="grid grid--3">
    <div class="card card--soft">
      <h3>Rescate</h3>
      <p>Atendemos casos de abandono, maltrato o riesgo, coordinando ayuda inmediata cuando es posible.</p>
    </div>
    <div class="card card--soft">
      <h3>Recuperación</h3>
      <p>Cuidados veterinarios, medicina y hogar de paso para que vuelvan a estar bien.</p>
    </div>
    <div class="card card--soft">
      <h3>Adopción</h3>
      <p>Proceso responsable para asegurar hogares definitivos y seguros.</p>
    </div>
  </div>
</section>

<section class="impact">
  <div class="impact__box">
    <div class="impact__number">+100</div>
    <div class="impact__text">
      Peluditos rescatados (puedes cambiar este número por el real cuando quieras)
    </div>
  </div>
</section>

<section class="section">
  <div class="section__head">
    <h2>¿Cómo puedes ayudar?</h2>
    <p class="small">Cuatro maneras simples de apoyar esta causa.</p>
  </div>

  <div class="grid grid--4">
    <div class="card">
      <h3>Adopta</h3>
      <p>Dale un hogar a un peludito que lo necesita.</p>
      <p><a href="{{ site.baseurl }}/adopta">Ver perritos →</a></p>
    </div>

    <div class="card">
      <h3>Dona</h3>
      <p>Nequi: comida, veterinario, medicamentos y transporte.</p>
      <p><a href="{{ site.baseurl }}/ayudar">Donar →</a></p>
    </div>

    <div class="card">
      <h3>Hogar de paso</h3>
      <p>Recibe temporalmente a un peludito mientras se recupera.</p>
      <p><a href="{{ site.baseurl }}/ayudar">Quiero ayudar →</a></p>
    </div>

    <div class="card">
      <h3>Difunde</h3>
      <p>Comparte publicaciones y adopciones en tus redes.</p>
      <p><a href="{{ site.baseurl }}/contacto">Ver redes →</a></p>
    </div>
  </div>
</section>

<section class="section">
  <div class="section__head section__headRow">
    <div>
      <h2>Perritos en adopción</h2>
      <p class="small">Se cargan automáticamente desde <code>_perritos</code>.</p>
    </div>
    <a class="btn btn--ghost" href="{{ site.baseurl }}/adopta">Ver todos →</a>
  </div>

  <div class="grid grid--3">
    {% assign adoptables = site.perritos | slice: 0, 3 %}
    {% for p in adoptables %}
    <div class="card">
      {% if p.foto %}
        <img src="{{ p.foto | prepend: site.baseurl }}" alt="Foto de {{ p.nombre }}">
      {% endif %}

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
      <h2>Historias</h2>
      <p class="small">Rescates, recuperaciones y finales felices.</p>
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

