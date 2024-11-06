---
layout: default
title: "Ferretería La Cadena | Ferretería en Guatemala"
description: Encuentra las mejores herramientas eléctricas en Ferretería La Cadena. Ofrecemos una amplia selección de soldadoras, compresores y maquinarias para carpintería a precios competitivos en Guatemala.
og_description: Encuentra las mejores herramientas eléctricas en Ferretería La Cadena. Ofrecemos una amplia selección de soldadoras, compresores y maquinarias para carpintería a precios competitivos en Guatemala.
---
<style>
    .post-title a {
        text-decoration: none;
    }
    .tituloH3Skills{
      font-size:18px;
    }
</style>
<div class="container" style="margin-top:10%;margin-bottom:10%">
<h2 style="text-align:center" title="Proyectos">Proyectos</h2>
Tengo una gran variedad de proyectos, algunos son de código abierto y pueden verlo en mi perfil de [GitHub](https://github.com/santoslopez)
{% for post in site.posts limit:5 %}
<div class="card mb-3" style="max-width:100%;">
  <div class="row g-0">
    <!--div class="col-md-4">
      <a href="{{ post.url }}" title="Visita el enlace {{ post.title }} para más información.">
        <img src="{{ post.imagenPrincipal }}" class="img-fluid rounded-start" alt="Imagen de proyecto: {{ post.url }}">
      </a>
    </div-->
    <div class="col-md-8">
      <div class="card-body">
        <a href="{{ post.url }}" title="Más información de {{ post.title }} visita el enlace.">
            <h3 class="card-title tituloH3Skills">{{ post.title }}</h3>
        </a>
        <p class="card-text">{{ post.description }}</p>
        {{ post.enlaces }}
        <!--p class="card-text"><small class="text-body-secondary">{{ post.date | date: "%A %B %-d, %Y" }}</small></p-->
      </div>
    </div>
  </div>
</div>
{% endfor %}

{% if site.posts.size > 5 %}
## Post antiguos
<ul>
    {% for post in site.posts %}
        {% if forloop.index > 5 %}
            <li><a class="post-title" href="{{ post.url }}" title="{{ post.title }}">{{ post.title }}</a></li>
        {% endif %}
    {% endfor %}
</ul>
{% endif %}
</div>