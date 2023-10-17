{% extends 'base.html' %} {% load static %} {% load crispy\_forms\_tags %} {% block titulo %} Criar Conta {% endblock %} {% block content %}

{% csrf\_token %}

Crie uma conta para continuar {{ form|crispy }}

Criar Conta

*   © 2021
*   Feito com Python (Django)
*   Hashtag

{% endblock %}