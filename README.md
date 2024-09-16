# coding-project-template
## Setup
Environment
cd .\server\
virtualenv djangoenv
.\djangoenv\Scripts\Activate 
pip install -U -r requirements.txt 

## Static pages server start
Initial migrations
python3 manage.py makemigrations
python3 manage.py migrate

Create superuser
python3 manage.py createsuperuser

Run server
python3 manage.py runserver


## Django application start
cd .\frontend\
npm install
npm run build

## Docker build and start containers (app and DB)
cd .\database\
docker build . -t nodeapp
docker-compose up