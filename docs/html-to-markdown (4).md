{% extends 'base.html' %} {% load static %} {% block titulo %} HomeFilmes Hashflix {% endblock %} {% block head %} $itemGrow: 1.2; $duration: 250ms; html { scroll-behavior: smooth; } body { margin: 0; background-color: #000; } h1 { font-family: Arial; color: red; text-align: center; } .wrapper { display: grid; grid-template-columns: repeat(3,100%); overflow:hidden; scroll-behavior: smooth; section { width: 100%; position: relative; display: grid; grid-template-columns: repeat(5, auto); margin: 20px 0; .item { padding: 0 2px; transition: $duration all; &:hover { margin: 0 40px; transform: scale(1.2); } } a { position: absolute; color: #fff; text-decoration: none; font-size: 6em; background:rgb(0,0,0); width: 80px; padding: 20px; text-align: center; z-index: 1; &:nth-of-type(1) { top:0; bottom:0; left:0; background: linear-gradient(-90deg, rgba(0,0,0,0) 0%, rgba(0,0,0,1) 100%); } &:nth-of-type(2) { top:0; bottom:0; right: 0; background: linear-gradient(90deg, rgba(0,0,0,0) 0%, rgba(0,0,0,1) 100%); } } } } // Remove the arrow for Mobile @media only screen and (max-width: 600px) { a.arrow\_\_btn { display:none; } } {% endblock %} {% block content %}

{{ filme\_destaque.titulo }}
----------------------------

{{ filme\_destaque.descricao }}

[Play]({% url 'filme:detalhesfilme' filme_destaque.pk %})

Novo
----

[‹](#section2) {% for filme in lista\_filmes\_recentes %} {% if forloop.counter < 5 %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endif %} {% endfor %} [›](#section2)

{% if lista\_filmes\_recentes|length > 4 %}

[‹](#section1) {% for filme in lista\_filmes\_recentes %} {% if forloop.counter > 4 %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endif %} {% endfor %} [›](#section1)

{% endif %}

Em Alta
-------

[‹](#section2emalta) {% for filme in lista\_filmes\_emalta %} {% if forloop.counter < 5 %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endif %} {% endfor %} [›](#section2emalta)

{% if lista\_filmes\_emalta|length > 4 %}

[‹](#section1emalta) {% for filme in lista\_filmes\_emalta %} {% if forloop.counter > 4 %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endif %} {% endfor %} [›](#section1emalta)

{% endif %}

Continuar Assistindo
--------------------

[‹](#section2vistos) {% for filme in request.user.filmes\_vistos.all %} {% if forloop.counter < 5 %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endif %} {% endfor %} [›](#section2vistos)

{% if request.user.filmes\_vistos.all|length > 4 %}

[‹](#section1vistos) {% for filme in request.user.filmes\_vistos.all %} {% if forloop.counter > 4 %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endif %} {% endfor %} [›](#section1vistos)

{% endif %}

{% endblock %}