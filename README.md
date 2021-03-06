# Eventex

Sistema de Eventos

[![Build Status](https://travis-ci.org/rodrigoSyscop/eventex.svg?branch=master)](https://travis-ci.org/rodrigoSyscop/eventex)
[![Code Health](https://landscape.io/github/rodrigoSyscop/eventex/master/landscape.svg?style=flat)](https://landscape.io/github/rodrigoSyscop/eventex/master)

## Como desenvolver?

1. Clone o repositório?
2. Crie um virtualenv com Python 3.6
3. Ative o virtualenv
4. Instale as dependências
5. Configure a instância com .env
6. Execute os testes

```console
git clone git@github.com:rodrigoSyscop:/eventex.git wttd
cd wttd
python -m venv .wttd
source .wttd/bin/activate
pip install -r requirements-dev.txt
cp contrib/env-sample .env
python manage.py test
```
## Como fazer deploy?

1. Crie uma instância no heroku.
2. Envie as configurações para o heroku.
3. Defina uma SECRET_KEY segura para a instância.
4. Defina DEBUG=False
5. Configure o serviço de email.
6. Envie seu código para o heroku.

```console
heroku create minhainstancia
heroku config:push
heroku config:set SECRET_KEY=`python contrib/secret_gen.py`
heroku config:set DEBUG=False
# configure o email
git push heroku master --force  #!/usr/bin/env python
"""
Django SECRET_KEY generator.
"""
from django.utils.crypto import get_random_string


chars = 'abcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*(-_=+)'
print(get_random_string(50, chars))
```
