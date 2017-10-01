<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/v/stable.svg" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://poser.pugx.org/laravel/framework/license.svg" alt="License"></a>
</p>

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
body form-data 

name "asdf"

email "asdf@asdf.asdf"

password asdfasdf

c_password asdfasdf

####response 
{
    "success": {
        "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImJkMGUzM2JmYWRhYTgyMzNhODk2ZWU3ZTBmNzQ1NDk3ZDM4ZTEzZDUyZjgzYmEyOGFhNmJmYjExZTMwZmViYTI5YTU1ZjljOWUxY2JjNmE3In0.eyJhdWQiOiIxIiwianRpIjoiYmQwZTMzYmZhZGFhODIzM2E4OTZlZTdlMGY3NDU0OTdkMzhlMTNkNTJmODNiYTI4YWE2YmZiMTFlMzBmZWJhMjlhNTVmOWM5ZTFjYmM2YTciLCJpYXQiOjE1MDY4OTgzMzcsIm5iZiI6MTUwNjg5ODMzNywiZXhwIjoxNTM4NDM0MzM3LCJzdWIiOiI1Iiwic2NvcGVzIjpbXX0.RoYwSyDjlKDUJzQZp7AL8cm3FA2dy_6sO_5lHaBWpgbF7lqyfzYQo4BfmorYupfpcnYdxwkaGh7u03BBVAWl8ZQJF07ABOTqv-96oY87nRnRJeWxkLHWsWVqm3Z9Rbnt0yxNFsF02apbZuD8UfeOGjX-p3K-qANzT0TWGtVJFm69tx7z6PSwrG2s4QiNrQumaQFkZMRogrLdEi8J7n2NYg4YVMmvI1GDBi2ETQMoJbBSQdyAKlVJ5-Yw9CmYAKUfROdEv1IvTv3Vn46D-j0UnCjUQ8HAizq8inIsfW50lx5uTaXaaOufG20SJZ_kh_80PHSbqHjm5eWFbVYD1yrmglI0X8JoI0pm8WUKY697D2icqhnZedFV1_NqklyPfYSMgNjFJEyj-SEPIwQA7qSyONpoFaOHzq3dZEfHJIFP91VewQ1PPYsinS3LvLxl237pEV5xn2CzMhADVCaLoF1OcZI_wnh7vHQj85KgR6p7clfaud9-IzbI6qOoQuf2cDgazTmLmScnPYW7WjLsoRR9bczJwgxHwzd0Eemhl9NsZfv8iLD4RL9RXDkqRN0JC45w0fOSjmuRtND9rbiqRfGB7faarEcfLJfGaAt0O6I5Mbn21kyTED7ViqwCnUYCNG7gGx_ye49k1Zfyxz0A-ysPQ4Y2MRo6iX1eUxxnJ9IPadk",
        "name": "asdfasdf"
    }
}

This token we will must attach to each of your requests.
![alt text](http://joxi.ru/1A5XPazfnWjyg2)


###Login user
####request post http://localhost:8000/api/login
headers:
"key":"Content-Type", "value":"application/x-www-form-urlencoded"

body x-www-form-urlencoded
"key":"email",  "value":"asdf@asdf.asdf"
"key":"password",  "value":"asdfasdf"
 

####response 
{
    "success": {
        "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImY1OGQyODM4MTI2YjkzMDEyYWY3M2Q1YTgyMjBiNDI0NzRkYzg4YjdiMjYwYmRlMmE1OGEzMTRiNTJiMzkwOWQyNDRjYzk3Njk3ODJjNWI2In0.eyJhdWQiOiIxIiwianRpIjoiZjU4ZDI4MzgxMjZiOTMwMTJhZjczZDVhODIyMGI0MjQ3NGRjODhiN2IyNjBiZGUyYTU4YTMxNGI1MmIzOTA5ZDI0NGNjOTc2OTc4MmM1YjYiLCJpYXQiOjE1MDY4OTg2OTgsIm5iZiI6MTUwNjg5ODY5OCwiZXhwIjoxNTM4NDM0Njk4LCJzdWIiOiI1Iiwic2NvcGVzIjpbXX0.AeVI3Zc0F-nXnVehlKv5GdCnQooitawVvMNmjjKXhijkcdDeNgvDbRYMy4FPhA2DfcAB8uc2ntrsOA_d1EOO6fHwmM5G-HHyZO5DLm6kzVfvhcHAwzlPWTDikY60Buosf32yDwKd-JA6o301MuIwJ-SmN14D6aHqn0iHJqe_YTXHgM5enwiGy3n5l4375A4OrYiZSbKVwpxiDsx9HM9tXY2E7pFQ3smHTydyeLm6L5il-hBD5o4vi0SXL_OMuBjqQJmu4qHTn4alc5fsnTcOqLe1M2tjR1-CHkYGLec9K8syV7akiI722Anmi8EOTFDXuTEDHUsPbnCPd3JtTeY5taLX38Z6pzD1TYwI-dAxOTpKT1dMPlDPwL5VEu5VKXadsUy8hph9972YDm9JAPgfyH3kc0xo3y7F6WDkVaXUQtAjPVf9eNKoseTWyLa9lPo3tcGW_onDnoqK8YYFxykpuq6vpgkUJeXM6HlBfOL6xHEEWZ--z3q0GDSvp3N2Ckhoi5bCX1v3MkxopYFxmkZlz0ZEdMsCefbAmPNFjzItcDH-g4cNH5VDAMtbu7i0iHathXY6yLBcWhOhfyaupMtNUV8UfqgXY8e_UEudumrle_3FT-oxw_XTOHeotPTxMUS6apW9NVaq-zK0DgbDw3eOmivaTIUe-kJkuQlJsdZ7KIc"
    }
}

This token we will must attach to each of your requests.

###Details of user  (test for is user logged)
####request post http://localhost:8000/api/details
headers:
"key":"Accept", "value":"application/json"
"key":"Authorization", "value":"Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImZhZmM0ODcwODgwNjA4YTM2YzExOTczOWM1YTdiMjYzZWIyZTgyZGNhOTk4ZmYwNTA4OWM5ZmU2M2VlZGViNWIyMjU1ZmJiZjcxMjA1NzE5In0.eyJhdWQiOiIxIiwianRpIjoiZmFmYzQ4NzA4ODA2MDhhMzZjMTE5NzM5YzVhN2IyNjNlYjJlODJkY2E5OThmZjA1MDg5YzlmZTYzZWVkZWI1YjIyNTVmYmJmNzEyMDU3MTkiLCJpYXQiOjE1MDY4MTA5NjksIm5iZiI6MTUwNjgxMDk2OSwiZXhwIjoxNTM4MzQ2OTY5LCJzdWIiOiIzIiwic2NvcGVzIjpbXX0.sYtW97LZPTBd5MmO1exUAvbOUzgosEeskTYbp8yoaL7UBepBziT1LS-cayYQFUuYmkXmuviBK39qPUqB3-lLTq02YBFa7KA235LPpteObd6SpowbIw7Iq_m0SRGA0tzGJqCPMWpC-Hc0w5tYA6Chc9ka7fJoE1y0SdIP5f5Z5CRCHUIJ0686bpQPk5iWqpm-USh24zw5SNM-yswZLUxrjML10t9q2039pTNkd4A9HAg6Dp-ItU8pRydTZAHgDmoB7bpMo8L0b_IWWSFjzC9Aa6BYECuPxxRdXMK6x9YPp5luM-Uu7aEKx1jBvH9g1l_MXC2JY82dyC9C4rRPUbQzBSaRAZTNGi4hJwUSGgp4WEcsyrRyl5AShQnzz1JxBQd5vvurwhKQCx4pLFmSEv0qHGNt3MjCrLSDWtQouEZwYgTIoe6CPHUjLdM-s6CLfipfsKrjPmqZFRGReCO7v3Ag4U7DqN5GvRc8ruWg3HOgXWvsv2TvD04gYPPvjnMaOfCs-IReCdNbPMXqs-BnhnfkXELXuOv-4T6n6yi3_xEL-VcqsR_K2F-DwUiTb8tLf9lZB5lujOPctvRBRIe_d8ptKDODfwgIdLmdHVFuHkcCXbos1Vng4kN1OftmzNhwYIwPDuBGFI9H8k07_ZpSCAG0rDBBRX-g8XykmeaZmzuAINU"
"key":"Content-Type", "value":"application/x-www-form-urlencoded"

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


###Logout user
####request post http://localhost:8000/api/logout
headers:
"key":"Accept", "value":"application/json"
"key":"Authorization", "value":"Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiIsImp0aSI6ImZhZmM0ODcwODgwNjA4YTM2YzExOTczOWM1YTdiMjYzZWIyZTgyZGNhOTk4ZmYwNTA4OWM5ZmU2M2VlZGViNWIyMjU1ZmJiZjcxMjA1NzE5In0.eyJhdWQiOiIxIiwianRpIjoiZmFmYzQ4NzA4ODA2MDhhMzZjMTE5NzM5YzVhN2IyNjNlYjJlODJkY2E5OThmZjA1MDg5YzlmZTYzZWVkZWI1YjIyNTVmYmJmNzEyMDU3MTkiLCJpYXQiOjE1MDY4MTA5NjksIm5iZiI6MTUwNjgxMDk2OSwiZXhwIjoxNTM4MzQ2OTY5LCJzdWIiOiIzIiwic2NvcGVzIjpbXX0.sYtW97LZPTBd5MmO1exUAvbOUzgosEeskTYbp8yoaL7UBepBziT1LS-cayYQFUuYmkXmuviBK39qPUqB3-lLTq02YBFa7KA235LPpteObd6SpowbIw7Iq_m0SRGA0tzGJqCPMWpC-Hc0w5tYA6Chc9ka7fJoE1y0SdIP5f5Z5CRCHUIJ0686bpQPk5iWqpm-USh24zw5SNM-yswZLUxrjML10t9q2039pTNkd4A9HAg6Dp-ItU8pRydTZAHgDmoB7bpMo8L0b_IWWSFjzC9Aa6BYECuPxxRdXMK6x9YPp5luM-Uu7aEKx1jBvH9g1l_MXC2JY82dyC9C4rRPUbQzBSaRAZTNGi4hJwUSGgp4WEcsyrRyl5AShQnzz1JxBQd5vvurwhKQCx4pLFmSEv0qHGNt3MjCrLSDWtQouEZwYgTIoe6CPHUjLdM-s6CLfipfsKrjPmqZFRGReCO7v3Ag4U7DqN5GvRc8ruWg3HOgXWvsv2TvD04gYPPvjnMaOfCs-IReCdNbPMXqs-BnhnfkXELXuOv-4T6n6yi3_xEL-VcqsR_K2F-DwUiTb8tLf9lZB5lujOPctvRBRIe_d8ptKDODfwgIdLmdHVFuHkcCXbos1Vng4kN1OftmzNhwYIwPDuBGFI9H8k07_ZpSCAG0rDBBRX-g8XykmeaZmzuAINU"
"key":"Content-Type", "value":"application/x-www-form-urlencoded"

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

