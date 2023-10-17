{% extends 'base.html' %} {% load static %} {% load crispy\_forms\_tags %} {% block titulo %} Fazer Login {% endblock %} {% block content %}

{% csrf\_token %}

Faça Login para continuar {{ form|crispy }}

Fazer Login

Não tem uma conta ainda?

[Clique aqui para criar uma conta]({% url 'filme:criarconta' %})

*   © 2021
*   Feito com Python (Django)
*   Hashtag

{% endblock %}