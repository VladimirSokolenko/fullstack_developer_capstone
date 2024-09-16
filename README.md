# coding-project-template
Setup:
Environment
cd .\server\
virtualenv djangoenv
.\djangoenv\Scripts\Activate 
pip install -U -r requirements.txt 

Initial migrations
python3 manage.py makemigrations
python3 manage.py migrate

Create superuser
python3 manage.py createsuperuser

Run server
python3 manage.py runserver


Django application
cd .\frontend\
npm install
npm run build

Docker
cd .\database\
docker build . -t nodeapp
docker-compose up