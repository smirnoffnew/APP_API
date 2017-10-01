## API_APP

needs:
- php 7.1
- composer

## Install
- git clone https://github.com/smirnoffnew/APP_API.git
- cd API_APP
- composer install
- php artisan passport:install

## Serve
- php artisan serve

## Urls:

###Register user
####request post http://localhost:8000/api/register
- body form-data 
- name "asdf"
- email "asdf@asdf.asdf"
- password asdfasdf
- c_password asdfasdf
####response 
{
    "success": {
        "token": "eyJ0eXAiOiJKV1QiLCJhbGciOPQ4Y2MRo6iX1eUxxnJ9IPadk",
        "name": "asdfasdf"
    }
}
- This token we will must attach to each of your requests.
example http://joxi.ru/1A5XPazfnWjyg2


###Login user
####request post http://localhost:8000/api/login
#####headers:
- "key":"Content-Type", "value":"application/x-www-form-urlencoded"
#####body x-www-form-urlencoded:
- "key":"email",  "value":"asdf@asdf.asdf"
- "key":"password",  "value":"asdfasdf"
####response 
{
    "success": {
        "token": "eyJ0eXAiOiJKV1QiDw3eOmivaTIUe-kJkuQlJsdZ7KIc"
    }
}
- This token we will must attach to each of your requests.
example http://joxi.ru/Vm69PRQIDkp80r


###Details of user  (test for is user logged)
####request post http://localhost:8000/api/details
#####headers:
- "key":"Accept", "value":"application/json"
- "key":"Authorization", "value":"Bearer eyJ0eXAiOiJKV1QiLCJhbmeaZmzuAINU"
- "key":"Content-Type", "value":"application/x-www-form-urlencoded"
####response 
{
    "success": {
        "id": 3,
        "name": "asdfasdf",
        "email": "asdf@asdf.asdf",
        "created_at": "2017-09-30 19:15:19",
        "updated_at": "2017-09-30 19:15:19"
    }
}
####bad response 
{
    "error": "Unauthenticated."
}
example http://joxi.ru/5mdvJ37fk5zL0A


###Logout user
####request post http://localhost:8000/api/logout
#####headers:
- "key":"Accept", "value":"application/json"
- "key":"Authorization", "value":"Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSU"
- "key":"Content-Type", "value":"application/x-www-form-urlencoded"
####success response 
{
    "success": {
        "id": "f58d2838126b93012af73d5a8220b42474dc88b7b260bde2a58a314b52b3909d244cc9769782c5b6",
        "user_id": 5,
        "client_id": 1,
        "name": "MyApp",
        "scopes": [],
        "revoked": true,
        "created_at": "2017-10-01 22:58:18",
        "updated_at": "2017-10-01 22:58:18",
        "expires_at": "2018-10-01 22:58:18"
    }
}
####bad response 
{
    "error": "Unauthenticated."
}
example http://joxi.ru/Q2KLNBpI4RlEWA
