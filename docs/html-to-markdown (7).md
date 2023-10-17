{% extends 'base.html' %} {% load static %} {% block titulo %} Logout {% endblock %} {% block content %}

Você saiu da sua conta
----------------------

[Fazer Login]({% url 'filme:login' %}) [Criar uma Conta]({% url 'filme:criarconta' %})

*   © 2021
*   Feito com Python (Django)
*   Hashtag

{% endblock %}