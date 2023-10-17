{% load static %}

[![]({% static 'images/Logonetflix.png' %})](/)

{% if user.is\_authenticated %}

 

{% endif %}

{% if user.is\_authenticated %} [Sair]({% url 'filme:logout' %}) {% else %} [Login]({% url 'filme:login' %}) {% endif %}

{% if user.is\_authenticated %}

[Editar Perfil]({% url 'filme:editarperfil' %})

{% endif %}