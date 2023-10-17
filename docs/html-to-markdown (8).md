{% extends 'base.html' %} {% block titulo %} Pesquisa de Filmes {% endblock %} {% block content %}

Resultados da Busca
-------------------

{% for filme in object\_list %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endfor %}

{% endblock %}