# API REST DJANGO REST FRAMEWORK 3 #

### Tecnologias Utilizadas: ###

- ``Python 3.7``
- ``Django Rest Framework 3``

### O que existe nesse projeto? ###

* uma API representando um CRUD de escola
* utilização Modelos, Admin e Serializers
* Viewset, Urls e requisições GET e POST
* integração do django admin
* ListAPIView e Autenticação

### Instalação ###

* baixar o projeto utilizando o git clone https://github.com/jobrasil/escola-django-rest-api.git
* criando ambiente virtual no python <code>python3 -m venv ./venv</code>
* ativando ambiente no windows <code>venv\Scripts\activate.bat (windows)</code>
* ativando ambiente no windows <code>source venv/bin/activate (linux)</code>  
* instalando django <code>pip install Django==3.0.7</code>
* instalando o rest framework <code>pip install djangorestframework</code> recomendado rodar em seguida: <code>pip install --upgrade pip</code> 
* instalando o markdown <code>pip install markdown</code>
* instalando cors headers <code>pip install django-cors-headers</code>
* instalando o drive p/ mysql <code>pip install pymysql</code>


### Configurações adicionais (caso não existam ou sejam necessárias) ###

* criar o projeto
- ``django-admin startproject DjangoAPI``

* criando o nome da aplicacao
- ``python manage.py startapp EscolaApp``

* altere no arquivo settings.py o idioma e o horário que usaremos na aplicação
- ``LANGUAGE_CODE = 'pt-br'``
- ``TIME_ZONE = 'America/Sao_Paulo'``

* adicionar os modulos em INSTALLED_APPS settings.py
- ``'rest_framework',``
- ``'corsheaders',``
- ``'Employeeapp.apps.EmployeeappConfig'``

* adicionar ainda em settings.py
- ``CORS_ORIGIN_ALLOW_ALL = True #recommended in production  ``
- ``corsheaders.middleware.CorsMiddleware',``

* adicionando configurações no settings.py p/ acesso ao banco de dados

- ``import pymysql``
- ``pymysql.install_as_MySQLdb()``

- ``DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'escola',
        'USER': 'usuario',
        'PASSWORD' : 'senha_banco',
        'HOST':'localhost',
        'PORT':'3306'
    }
}``

* sempre que houver qualquer alteração de modelo rodar o comando:
- ``python manage.py makemigrations``

* aplicando alterações na banco:
- ``python manage.py migrate``


### Rodando o projeto ###

* utilize o comando para subir o serviço: <code>python manage.py runserver</code>
* para realizar o teste utilize  : karma start
