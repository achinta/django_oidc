### Purpose
Template django project with oidc authentication. Tested with keycloak 26.2.4


### How to run
 - Install uv
 - git clone this repo
 - cd into the repo
 - run `uv sync` to install the dependencies
 - Add the following to your .env file:
 ```
OIDC_RP_CLIENT_ID='<your_client_id>'
OIDC_RP_CLIENT_SECRET='<your_client_secret>'
OIDC_OP_AUTHORIZATION_ENDPOINT='<your_authorization_endpoint>'
OIDC_OP_TOKEN_ENDPOINT='<your_token_endpoint>'
OIDC_OP_USER_ENDPOINT='<your_user_endpoint>'
OIDC_OP_JWKS_ENDPOINT='<your_jwks_endpoint>'
 ```
 - run `python manage.py migrate` to create the database
 - run `python manage.py createsuperuser` to create a superuser
 - python manage.py runserver
 - Go to `http://localhost:8000/` to test the authentication.


### Initial Generation

This django project is generated with
```shell
mkdir mydjango
cd mydjango
uv init --python 3.11
uv add django
django-admin startproject base .
```