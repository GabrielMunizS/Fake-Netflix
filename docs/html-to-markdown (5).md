{% extends 'base.html' %} {% load static %} {% block titulo %} HomePage Hashflix {% endblock %} {% block head %} #id\_email{ width: 100%; color: #000000; padding: 5px 5px; } {% endblock %} {% block content %}

Filmes e séries da Hashtag, tudo em um só lugar.
================================================

### Assista onde quiser. Cancele quando quiser.

#### Quer começar? Coloque seu e-mail abaixo para acessar.

{% csrf\_token %}

{{ form }} Acessar

Enjoy on your TV.
-----------------

##### Watch on Smart TVs, Playstation, Xbox, Chromecast, Apple TV, Blu-ray players, and more.

![]({% static 'images/tv.png' %})

![]({% static 'images/mobile-0819.jpg' %})

Download your shows to watch offline.
-------------------------------------

##### Save your favorites easily and always have something to watch.

Create profiles for kids.
-------------------------

##### Send kids on adventures with their favorite characters in a space made just for them—free with your membership.

![]({% static 'images/netflix_kid.png' %})

*   © 2021
*   Feito com Python (Django)
*   Hashtag

{% endblock %}