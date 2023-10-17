{% extends 'base.html' %} {% block titulo %} HomeFilmes Hashflix {% endblock %} {% block content %}

{{ object.titulo }}
-------------------

{{ object.descricao|slice:":100" }}...

[Play]({{ object.episodios.first.video }})

Descrição
---------

{{ object.descricao }}  
Visualizações: {{ object.visualizacoes }}

Episódios
---------

{% for episodio in object.episodios.all %}

### [

Episódio {{ forloop.counter }}: {{ episodio.titulo }}

]({{ episodio.video }})

{% endfor %}

Relacionados
------------

{% for filme in filmes\_relacionados %}

[![]({{ filme.thumb.url }})]({% url 'filme:detalhesfilme' filme.pk %})

{% endfor %}

{% endblock %}