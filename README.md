Paytm Payments Gateway 

Paytm
Paytm payments Gateway example.

Forked from here: paytm-django
Quick Start

    First open your terminal and clone the project

git clone https://github.com/Nayan-Code/paytm_django.git

    Open Project directory
    Now install the requirements

pip install -r requirements.txt

    Now go to payments ->settings.py and enter your credentials

PAYTM_MERCHANT_KEY = '' # < your production KEY >
PAYTM_MERCHANT_ID = '' # < your production ID >
PAYTM_WEBSITE = 'DEFAULT'
PAYTM_URL = 'https://securegw.paytm.in/theia/processTransaction'

    Staging Credentials

PAYTM_MERCHANT_KEY = 'GvYRwo%@Vl2Ml19y' # < your staging key >
PAYTM_MERCHANT_ID = 'BiDzIl44175596745392' # < your staging ID >
PAYTM_WEBSITE = 'WEBSTAGING'
PAYTM_URL = 'https://securegw-stage.paytm.in/theia/processTransaction'

    Make Migrations

python manage.py makemigrations

    Migrate paytm app for transactions details

python manage.py migrate

    Create Super user

python manage.py createsuperuser

    Now in terminal run the server and go to http://localhost:8000/

python manange.py runserver

    Go to

    http://localhost:8000/admin
        Log in using superuser credentials
    http://localhost:8000/
        Click Paytm Pay button to start payment

This should redirect you to Paytm Page. Test Credentials to use for login:

    Card:
    Card Number : Any Visa or Master Card
    Expiration Month & Year : Any Future month and Year
    CVV : 123
    OTP : 123123

    Wallet:
    Mobile Number : 7777777777
    Password : Paytm12345
    OTP: 489871

    Net Banking:
    Bank : Andhra Bank
    User : test
    Password : test

Paytm reference Documentation:

    Paytm Gateway Api Documentation
    Paytm Documentation

